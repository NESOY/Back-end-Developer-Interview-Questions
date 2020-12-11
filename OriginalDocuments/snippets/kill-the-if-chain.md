# if-chain 제거

중첩된 구조는 [Vahid Najafi](https://github.com/vahidvdn)가 제안한대로 펼쳐질 수 있습니다.

```js
function()
{
    HRESULT error = S_OK;

    if( !SUCCEEDED(Operation1() ) return OPERATION1FAILED;
    if( !SUCCEEDED(Operation2() ) return OPERATION2FAILED;
    if( !SUCCEEDED(Operation3() ) return OPERATION3FAILED;
    if( !SUCCEEDED(Operation3() ) return OPERATION3FAILED;
    if( !SUCCEEDED(Operation4() ) return OPERATION4FAILED;

}
```

사실, 리팩토링할 공간이 더 많다고 생각하지만, 모두 프로젝트의 경제성에 달려있습니다.

리팩토링 목표를 설정하기 위해서는 코드의 냄새와 디자인 결함을 논의하는 것이 좋습니다.

## 냄새
다음과 같은 문제가 있습니다.

* 이 코드는 [SOLID 원칙][2]의 일부분을 위반합니다. 코드의 변경 없이는 확장을 할 수 없기 때문에 [Open Closed Principle][3]에 위배됩니다. 예를 들어 새로운 연산을 추가하려면 새로운 `if`/`else` 구문을 추가해야합니다.
* 이것은 또한 [Single Responsibility Principle][4]도 위반합니다. 너무 많은 일을 합니다. 오류 검사를 수행하고 4개의 작업을 모두 실행하고, 그것들의 구현도 포함하고 결과를 확인하고 올바른 순서로 실행을 연결해야합니다.
* 이것은 [Dependency Inversion Principle][5]를 위반합니다. 높은 수준과 낮은 수준의 구성 요소간에 종속성이 있기 때문입니다.
* 또한 끔찍한 [Cyclomatic complexity][6]를 가집니다.
* 높은 결합과 낮은 응집력을 가지며 [권장 사항][7]과 정반대입니다.
* 이것은 많은 코드 중복을 포함합니다; 함수 `Succeeded()`는 각 구문에 반복됩니다; `if`/`else`의 구조가 겹쳐있습니다; `error`의 할당이 중복되었습니다. 
* 순수한 기능적 특성을 가질 수 있지만 대신 상태 변이에 의존하므로 추론이 쉽지 않습니다.
* 혼란을 일으키는 비어있는 `if` 문이 있습니다.

## 리팩토링
무엇을 할 수 있을지 살펴봅시다.<br/>
여기서는 C#으로 구현했지만 어떤 언어로든 유사한 단계를 수행할 수 있습니다.<br/>
명명 규칙을 준수하는 것이 리팩토링의 일부라고 믿기 때문에 일부 요소의 이름을 변경했습니다.

```csharp
  internal class TestClass
    {
        HResult SomeFunction()
        {
            var error = HResult.Ok;

            if(Succeeded(Operation1()))
v            {
                if(Succeeded(Operation2()))
                {
                    if(Succeeded(Operation3()))
                    {
                        if(Succeeded(Operation4()))
                        {
                        }
                        else
                        {
                            error = HResult.Operation4Failed;
                        }
                    }
                    else
                    {
                        error = HResult.Operation3Failed;
                    }
                }
                else
                {
                    error = HResult.Operation2Failed;
                }
            }
            else
            {
                error = HResult.Operation1Failed;
            }

            return error;
        }

        private string Operation1()
        {
            // some operations
            return "operation1 result";
        }
        private string Operation2()
        {
            // some operations
            return "operation2 result";
        }
        private string Operation3()
        {
            // some operations
            return "operation3 result";
        }
        private string Operation4()
        {
            // some operations
            return "operation4 result";
        }

        private bool Succeeded(string operationResult) =>
            operationResult == "some condition";
    }

    internal enum HResult
    {
        Ok,
        Operation1Failed,
        Operation2Failed,
        Operation3Failed,
        Operation4Failed,
    }
}
```

단순성을 위해 각 작업이 문자열을 반환하고 성공 또는 실패는 문자열에 대한 동등성 검사를 기반으로한다고 가정했습니다.( 물론 그럴 수도 있습니다) 다음 단계에서 코드가 결과 유효성 검사 논리와 독립적이면 좋을 것입니다.

### 1 단계
일부 테스트 장치를 사용해서 리팩토링을 시작하는 것이 좋습니다.

```csharp
public class TestCase
{
    [Theory]
    [InlineData("operation1 result", HResult.Operation1Failed)]
    [InlineData("operation2 result", HResult.Operation2Failed)]
    [InlineData("operation3 result", HResult.Operation3Failed)]
    [InlineData("operation4 result", HResult.Operation4Failed)]
    [InlineData("never", HResult.Ok)]
    void acceptance_test(string failWhen, HResult expectedResult)
    {
        var sut = new SomeClass {FailWhen = failWhen};

        var result = sut.SomeFunction();

        result.Should().Be(expectedResult);
    }
}
```

우리의 경우는 사소한 문제이지만 면접 질문이어야하는 퀴즈이므로 무시하지 않을 것입니다.


### 2 단계
첫 번째 리팩토링은 변경 가능한 상태를 제거하는 것입니다. 각 if 분기는 변수 'error'를 변경하는 대신 값을 반환 할 수 있습니다. 또한 'error' 라는 이름은 성공 사례를 포함하므로 오해의 소지가 있습니다. 그냥 제거합시다.

```csharp
HResult SomeFunction()
{
    if(Succeeded(Operation1()))
    {
        if(Succeeded(Operation2()))
        {
            if(Succeeded(Operation3()))
            {
                if(Succeeded(Operation4()))
                    return HResult.Ok;
                else
                    return HResult.Operation4Failed;
            }
            else
                return HResult.Operation3Failed;
        }
        else
            return HResult.Operation2Failed;
    }
    else
        return HResult.Operation1Failed;
}
```

비어있는 `if` 문을 제거하여 코드를 추론하기가 약간 더 쉬워졌습니다.

### 3 단계
이제 각 `if` 문을 뒤집습니다. (Sergio가 제안한 단계)

```csharp
internal HResult SomeFunction()
{
    if (!Succeeded(Operation1()))
        return HResult.Operation1Failed;

    if (!Succeeded(Operation2()))
        return HResult.Operation2Failed;

    if (!Succeeded(Operation3()))
        return HResult.Operation3Failed;

    if (!Succeeded(Operation4()))
        return HResult.Operation4Failed;

    return HResult.Ok;
}
```

코드가 일련의 실행을 수행함을 명백하게 합니다. 작업이 성공하면 다음 작업이 호출됩니다. 그렇지 않다면 체인은 중단되고 오류가 발생합니다. GOF [Chain of Responsibility Pattern][8]가 떠오릅니다.

### 4 단계
각 작업을 별도의 클래스로 이동하고 함수가 일련의 작업을 수신하여 한 번에 실행할 수 있습니다. 각 클래스는 특정 작업 로직을 다룹니다 (the Single Responsibility Principle 준수).

```csharp
internal HResult SomeFunction()
{
    var operations = new List<IOperation>
    {
        new Operation1(),
        new Operation2(),
        new Operation3(),
        new Operation4()
    };

    foreach (var operation in operations)
    {
        if (!_check.Succeeded(operation.DoJob()))
            return operation.ErrorCode;
    }

    return HResult.Ok;
}
```

우리는 'if'를 모두 제거했습니다.

Notice how:

* 인터페이스 `IOperation`이 도입되었습니다. 이는 Dependency Inversion 원칙을 준수하여 작업에서 함수를 분리하기위한 예비 조치입니다.
* 오퍼레이션 목록은 [Dependency Injection] [9]을 사용하여 클래스에 쉽게 삽입 할 수 있습니다.
* 결과 검증 로직은 별도의 클래스 `Check`로 이동하여 메인 클래스에 삽입되었습니다 (Dependency Inversion and Single Responsibility 충족).

```csharp
internal class SimpleStringCheck : IResultCheck
{
    private readonly string _failWhen;

    public Check(string failWhen)
    {
        _failWhen = failWhen;
    }

    internal bool Succeeded(string operationResult) =>
        operationResult != _failWhen;
}

```

우리는 메인 클래스를 수정하지 않고 체크 로직을 전환 할 수있는 능력을 얻었습니다 (Open-Closed Principle).

각 작업은 다음과 같은 별도의 클래스로 이동되었습니다.

```csharp
internal class Operation1 : IOperation {
    public string DoJob()
    {
        return "operation1 result";
    }

    public HResult ErrorCode => HResult.Operation1Failed;
}
```

각 작업은 자체 오류 코드를 알고 있습니다. 기능 자체는 그것으로부터 독립되었습니다.

### 5 단계
코드를 리팩토링해야 할 것이 더 있습니다.

```csharp
foreach (var operation in operations)
{
    if (!_check.Succeeded(operation.DoJob()))
        return operation.ErrorCode;
    }

    return HResult.Ok;
}
```

* 첫째, `return HResult.Ok;`케이스가 특수한 경우로 처리되는 이유가 명확하지 않습니다. 체인에는 실패하지 않고 해당 값을 반환하는 종료 작업이 포함될 수 있습니다. 이렇게하면 마지막 `if`를 제거 할 수 있습니다.

* 둘째, 우리의 기능에는 여전히 두 가지 책임이 있습니다. 체인을 방문하고 결과를 확인하는 것입니다.

작업을 실제 체인으로 캡슐화하여 함수를 다음과 같이 줄일 수 있습니다.

```
return operations.ChainTogether(_check).Execute();
```

2 가지 옵션이 있습니다.

* 각 작업은 다음 작업을 알고 있으므로 operation1부터 시작하여 단일 호출로 전체 체인을 실행할 수 있습니다.
* 운영은 체인의 일부임을 인식하지 못합니다. 별도의 캡슐화 구조는 작업에 순서대로 실행되는 기능을 추가합니다.

나는 후자에 대해 계속하고 있지만 그것은 절대적으로 논쟁의 여지가 있습니다. 체인에서 링을 모델링하는 클래스를 소개하고 코드를 클래스에서 멀리 이동합니다.

```csharp
internal class OperationRing : IRing
{
    private readonly Check _check;
    private readonly IOperation _operation;
    internal IRing Next { private get; set; }

    public OperationRing(Check check, IOperation operation)
    {
        _check = check;
        _operation = operation;
    }

    public HResult Execute()
    {
        var operationResult = _operation.DoJob();

        if (_check.Succeeded(operationResult))
            return Next.Execute();

        return _operation.ErrorCode;
    }
}
```

이 클래스는 작업을 실행하고 성공한 경우 다음 링으로의 실행을 처리하거나 올바른 오류 코드를 반환하는 체인을 중단합니다.

체인은 실패하지 않는 요소에 의해 종료됩니다.

```csharp
internal class AlwaysSucceeds : IRing
{
    public HResult Execute() => HResult.Ok;
}
```

원본 클래스는 다음과 같이 줄었습니다.

```csharp
internal class SomeClass
{
    private readonly Check _check;
    private readonly List<IOperation> _operations;

    public SomeClass(Check check, List<IOperation> operations)
    {
        _check = check;
        _operations = operations;
    }

    internal HResult SomeFunction()
    {
        return _operations.ChainTogether(_check).Execute();
    }
}
```

이 경우`ChainTogether ()`는`List <IOperation>`의 확장으로 구현 된 함수입니다. 체인 로직이 우리 클래스의 책임이라고 생각하지 않기 때문입니다.


## 이것은 *정답*이 아닙니다

책임이 가장 적절한 클래스로 분리되었다는 것은 절대적으로 논쟁의 여지가 있습니다. 예로,

* 체인 작업이 우리 기능의 작업입니까? 아니면 체인 구조를 직접 받아야합니까?
* 왜 열거형을 사용합니까? Robert Martin이 "Refactoring : Improving the Design of Existing Code"에서 썼듯이 : 열거 형은 코드의 냄새이며 다형성 클래스로 리팩토링되어야합니다.
* 너무 많지 않나요? 결과 디자인이 왜 이리 복잡합니까? 전체 애플리케이션의 복잡성에 이러한 수준의 모듈화가 필요합니까?

따라서 원래 함수를 리팩토링하는 다른 여러 방법이 있다고 확신합니다.


  [1]: https://stackoverflow.com/users/125816
  [2]: https://en.wikipedia.org/wiki/SOLID
  [3]: https://en.wikipedia.org/wiki/Open%E2%80%93closed_principle
  [4]: https://en.wikipedia.org/wiki/Single_responsibility_principle
  [5]: https://en.wikipedia.org/wiki/Dependency_inversion_principle
  [6]: https://en.wikipedia.org/wiki/Cyclomatic_complexity
  [7]: https://en.wikipedia.org/wiki/Cohesion_(computer_science)
  [8]: https://en.wikipedia.org/wiki/Chain-of-responsibility_pattern
  [9]: https://en.wikipedia.org/wiki/Dependency_injection
  [10]: https://refactoring.guru/smells/primitive-obsession

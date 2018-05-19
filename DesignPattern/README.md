### [[↑]](#toc) <a name='patterns'>디자인 패턴:</a>

* 왜 global 객체와 static 객체는 나쁜 것일까요? code를 통한 예시로 설명할 수 있나요?
* 제어의 역전(Inversion of Control)에 대한 개념과 IoC가 코드의 디자인을 어떻게 향상시키는지 설명해 주세요.
* 디미터의 법칙(Law of Demeter)을 어기는 코드를 작성해주실 수 있나요? 그리고 이 코드가 왜 나쁜 디자인인지 그리고 어떻게 고쳐야 하는지 보여주세요.
* Active-Record는 CRUD기능을 포함하고 데이터베이스 테이블의 기초 컬럼들을 포함하고 있는 디자인 패턴입니다. 이러한 패턴의 한계점과 단점을 이야기해주세요.
* Data Mapper는 객체와 데이터베이스 사이에 데이터를 독립적으로 유지하면서 객체와 데이터베이스 사이에 데이터를 Mapping하는 Mapper Layer를 사용한 설계 패턴입니다. 반면 Active-Recorde객체에는 데이터베이스에 유지하기 위한 작업과 기본 데이터베이스 테이블에 해당하는 속성이 직접 통합되어 있습니다. 위 패턴에 대해 어떻게 생각하세요? 어떤 상황에서 어떤 패턴을 사용하는게 적절할까요?
* `null`은 왜 10억 달러의 실수라고 말할까요? Null Object Pattern이나 Option 타입과 같은 `null`을 피할 수 있는 기술들에 대해 설명해주세요.
* 많은 사람들이 객체지향프로그래밍에서 상속보다는 구성(Composition)이 더 나은 선택이라고 말합니다. 당신의 의견은 어떤가요?
* 손상 방지 레이어(Anti-corruption Layer) 패턴이란 무엇일까요?
* 싱글톤은 클래스에 대해 하나의 인스턴스만 생성해서 사용하도록 제한하는 패턴입니다. Thread-Safe한 싱글톤 Singleton기법은 명확하지 않습니다. 한번 시도해보세요.
* 클라이언트에게 영향을 미치지 않고 바꾸는 기능을 데이터 추상화(Data Abstraction)라고 합니다. 이 속성을 위반하는 것으로 나타나는 제품과 예를 들고 고쳐보세요.
* DRY원칙(Don't Repeat Yourself)을 깨는 작은 코드를 작성해보세요. 그리고 고쳐보세요.
* 의존성 지옥(Dependency Hell)을 어떻게 해결하실건가요?
* Is goto evil? You may have heard of the famous paper "Go To Statement Considered Harmful" by Edsger Dijkstra, in which he criticized the use of the `goto` statement and advocated structured programming instead. The use of `goto` has always been controversial, so much that even Dijkstra's letter was criticized with articles such as "'GOTO Considered Harmful' Considered Harmful". What's your opinion on the use of `goto`?
* The robustness principle is a general design guideline for software that recommends "*Be conservative in what you send, be liberal in what you accept*". It is often reworded as "*Be a tolerant reader and a careful writer*". Would you like to discuss the rationale of this principle?
* Separation of Concerns is a design principle for separating a computer program into distinct areas, each of ones addressing a separate concern. There are a lot of different mechanisms for achieving Separation of Concerns (use of objects, functions, modules, or patterns such as MVC and the like). Would you discuss this topic?


### [[↑]](#toc) <a name='design'>코드 디자인:</a>

* 우리가 평소에 자주 듣던 객체지향 디자인(Object-Oriented Design)은 높은 응집도와 낮은 결합도를 가장 중요한 목표로 가지고 있습니다. 이 목표가 무엇을 의미하는지? 왜 그렇게 중요한지? 무엇을 얻을 수 있는지 설명해주세요.
* 대부분의 언어에서 배열의 시작은 왜 0부터 일까요?
* 테스트와 TDD는 코드 디자인에 어떤 영향을 주나요?
* DRY원칙(Don't Repeat Yourself)을 깨는 작은 코드를 작성해보세요. 그리고 왜 나쁜 디자인인지 설명하고 고쳐보세요.
* 응집도와 결합도의 차이점은 뭘까요?
* 리팩토링(refactoring)은 언제 유용한가요?
* 코드에서 주석은 의미가 있을까요? 몇몇 사람들은 되도록이면 피하라고 이야기합니다. 또한 주석이 필요없기를 희망하고 있습니다. 의견에 동의하십니까?
* 디자인과 아키텍처의 차이점은 무엇일까요?
* 왜 TDD에서는 코드를 작성하기 전에 테스트 코드를 작성할까요?
* C++은 다중 상속을 제공합니다. 또한 자바도 다중 인터페이스를 허용합니다. 이러한 기능들을 사용함으로써 개발의 직교성(orthogonality)에 대해 어떤 영향을 줄까요? 다중 상속과 다중 인터페이스의 차이점이 있을까요? 위임과 상속에 대해 차이점이 있을까요?
* 저장하는 절차를 도메인 로직에 유지하는 것에 대해 장단점을 설명해주세요.
* 왜 객체 지향 디자인(Object-Oriented Design)은 오랜 기간동안 시장을 지배할 수 있었을까요?
* 당신의 코드에 나쁜 디자인이 있다면 당신은 어떻게 해결하실 건가요?

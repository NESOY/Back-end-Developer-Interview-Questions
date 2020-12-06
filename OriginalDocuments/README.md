백엔드 개발자 면접 질문
==================

중국어 번역본 [클릭](https://github.com/monklof/Back-End-Developer-Interview-Questions) by [monklof](https://github.com/monklof).

처음에는 친구나 동료들과 기술토론을 하기 위한 질문 목록을 만들기 위해 이 프로젝트를 시작했습니다. 하지만 그보다 뭔가 더 해보고 싶어졌습니다.

저는 사실 면접장에서 기술적인 질문을 하기 보다는, 후보자와 실제 코드를 앞에 두고 같이 앉아서 키보드 위에 손을 올리고 실질적인 문제들로 하루 종일 짝코딩 하는 편을 선호합니다. 가능하다면 회사 동료들과 돌아가면서요. 하지만 이런 기술적인 질문으로 멋진 토론을 유도할 수도 있고, 서로의 지식을 공유하는 좋은 방법이기도 한 것 같습니다.

이 백엔드 개발자용 질문 목록 프로젝트는 후보자에 대해 면밀히 알고자 할 때 쓸만한 질문을 모았습니다. 단, 한 후보에게 모든 질문을 다 하지는 마세요. 몇 시간이 걸릴지도 모르고, 의미도 없습니다. 그리고 한 사람이 알기에는 너무 광범위한 지식을 다루고 있습니다. JD와 유관한 질문을 추려서 기술적인 토론이 더 의미있도록 해 보세요.

### 알림
모든 질문은 기본적으로 열린 질문이고, 정답이 없는 질문도 있습니다. 모든 질문은 대화의 물꼬를 트는 용도로 작성하였습니다. 아마 정답이 정해진 질문보다 후보자의 역량을 확인하기에 더 적합할 겁니다. 개인적으로는 제가 아직 제대로 알지 못하는 분야의 질문을 선택하기도 합니다.

다시 한번 강조하지만, 이 질문만으로는 충분하지 않습니다. 후보자와 오랫동안 짝코딩을 해 보세요. 후보자의 개발 스타일, 문제 접근 방식을 알 수 있고, 후보자 편에서는 지원 회사의 업무 방식에 대해 구체적으로 알 수 있는 기회가 됩니다.

이 프로젝트는 [Front-end Job Interview Questions](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions) by [@darcyclarke](https://github.com/darcyclarke) 의 영향으로 시작되었습니다.



### 정답은 어디있나요?

조만간 완성할 것 같습니다. Contribute해 주신다면 대단히 감사하겠습니다!


## <a name='toc'>목차</a>

  * [디자인 패턴](#patterns)
  * [코드 설계](#design)
  * [언어](#languages)
  * [Web](#web)
  * [DB](#databases)
  * [NoSQL](#nosql)
  * [버전관리](#codeversioning)
  * [동시성(Concurrency)](#concurrency)
  * [분산 시스템](#distributed)
  * [소프트웨어 생명주기와 팀 관리](#management)
  * [알고리즘](#algorithms)
  * [소프트웨어 아키텍처](#architecture)
  * [SOA & MSA](#soa)
  * [보안](#security)
  * [일반](#general)
  * [열린 질문](#open)
  * [코드 제시형](#snippets)
  * [빌게이츠 스타일](#billgates)



### [[↑]](#toc) <a name='patterns'>디자인 패턴:</a>

#### 전역객체는 나쁘다
전역 static 객체가 나쁜 이유는 무엇인가요? 코딩으로 예를 들어 설명해 주세요.

#### 역제어 패턴 (IoC)
역제어 패턴(IoC)에 대해, 특히 설계 측면에서 설명해 주세요.

#### 데메테르 법칙
데메테르 법칙LoD(최소한의 지식 규칙)에 의하면 객체간의 정보가 제한되어야 하며 오직 직접 호출한 객체와 통신해야 한다고 합니다(낯선 객체와 통신하지 말라고 하기도 함). 이 원칙을 위반하는 코드를 작성해 보세요. 그리고 왜 나쁜 디자인인지 설명하고 수정해 보세요.

#### Active-Record
ActiveRecord 는 insert, update, delete 등의 함수와 DB table의 열을 속성으로 갖는 객체를 생성하는 디자인 패턴입니다. 이 패턴의 한계와 함정이 무엇인지 귀하의 경험에 비추어 의견을 이야기 해주세요.

#### Data-Mapper
Data-Mapper 는 객체와 DB 간 데이터 이동 중에 각각을 독립적으로 유지하기 위해 mapper를 사용하는 디자인 패턴입니다. 반면에, ActiveRecode 객체는 객체와 DB 간의 연결을 지속하기 위한 작업과 기본 DB 속성값을 직접 통합합니다. 이런 패턴에 대한 의견이 있으신가요? 각각 언제 사용하는게 좋을까요?

#### 억만금짜리 실수
Null의 도입이 억만금짜리 실수로 불리우는 이유는 무엇일까요? 또, Null문제를 해결하기 위한 Null 객체 패턴(GOF)이나 옵션 자료형에 대해 이야기해 봅시다.

#### 상속 vs 컴포지션
많은 사람들이 OOP에서 상속보다 컴포지션이 낫다고들 합니다. 당신의 의견은 어떻습니까?

#### 손상 방지 레이어(Anti-corruption Layer)
손상 방지 레이어(Anti-corruption Layer) 패턴이 무엇입니까?

#### 싱글톤 (Singleton)
싱글톤(Singleton) 디자인 패턴은 객체의 생성자를 하나로 제한합니다. 하지만 쓰레드에 안전한 싱클톤 클래스를 작성하기는 단순하지 않은데요, 한번 작성해 주시겠습니까?

#### 데이터 추상화
클라이언트에 영향 없이 구현부를 변경하는 기능을 데이터 추상화라고 합니다. 이 속성에 반하는 예제를 작성해 주시고, 수정하는 과정을 보여주세요.

#### DRY (Don't Repeat Yourself)
DRY(Don't Repeat Yourself) 원칙을 위반하는 코드를 작성하시고, 수정하는 과정을 보여주세요.

#### 의존성 지옥 (Dependency Hell)
의존성 지옥(Dependency Hell)은 어떻게 해결하는게 좋을까요?

#### Goto는 나쁘다
`goto` 문에 대해 어떻게 생각하시나요? `goto` 문의 사용을 비판하고 대신 구조화된 프로그래밍을 주창한 Edsger Dijkstra의 유명한 논문 "Go To Statement Considered Harmful"에 대해 들어보셨을 겁니다. `goto` 문은 항상 논란거리었는데요, 심지어 Dijkstra가 'goto가 유해한 것 같다'고 한 말조차 비판받기도 했습니다. 이 `goto` 문에 대해 어떻게 생각하시나요?

#### 견고함의 원칙 (Robustness principle)
견고함의 원칙(The robustness principle)은 "*보내기는 더디하고 받기는 쉬이하라*"는 일반적인 소프트웨어 설계의 가이드라인입니다. 때때로 "*관용적인 독자와 신중한 작가가 되라*"로 불리기도 합니다. 이 원칙에 대해 이론적인 해석을 해 봅시다.

#### 관심사 분리 (Seperation of Concerns)
관심사 분리(Separation of Concerns)는 프로그램을 각각의 구역으로 격리하는 설계 원칙으로, 각 구역은 관심사가 분리된 것으로 간주됩니다. 객체, 함수, 모듈, MVC 같은 패턴 등 관심사 분리를 달성하기 위한 수많은 메커니즘이 있습니다. 이 주제에 대해 토론해 봅시다.


### [[↑]](#toc) <a name='design'>코드 설계:</a>

* 보통 객체 지향 설계의 가장 중요한 목적으로 높은 응집도, 낮은 결합도를 꼽는데요, 각각 어떤 의미이고 왜 중요한지, 또 어떻게 달성할 수 있는지 설명해 주세요.
* 많은 언어에서 배열의 인덱스 시작이 0인 이유가 무엇인가요?
* 평소에 테스트를 어떤식으로 수행하시고, TDD가 코드 설계에 어떤 영향을 주는지 설명해 주세요.
* DRY(Don’t Repeat Yourself) 원칙을 위반하는 사례로서의 코드를 작성하세요. 그리고 왜 나쁜 설계인지 설명하고 수정해 보세요.
* 결합도와 응집도의 차이점은 무엇인가요?
* 리팩토링이 어디에 유용한가요?
* 주석이 필요하다고 생각하나요? 가능한 주석을 쓰지 말고, 주석이 필요 없도록 코딩하라는 사람도 있는데요, 그런 방식에 동의하시나요?
* 소프트웨어 디자인과 소프트웨어 아키텍처의 차이는 무엇인가요?
* TDD 에서 왜 실제 코드보다 테스트 코드를 먼저 작성하나요?
* C++는 다중 상속을 지원하고, 자바는 하나의 클래스가 여러 인터페이스를 구현할 수 있습니다. 이는 직교성에 어떤 영향을 주나요? 다중 상속과 다중 인터페이스 구현이 주는 영향이 서로 다른가요? 위임과 상속이 어떻게 다른가요? (이 문제는 책 ‘실용주의 프로그래머’에서 발췌했습니다.)
* Stored Procedure에 비즈니스 로직을 구현했을 때의 장단점을 설명해 주세요.
* 수 년간 객체 지향 설계가 시장을 지배한 이유에 대해 당신의 의견을 말해주세요.
* 당신의 코드 설계에서 악취가 나는지 알려면 어떻게 해야 할까요?


### [[↑]](#toc) <a name='languages'>언어:</a>

* 당신의 주력 언어가 왜 나쁜지 세 가지만 말해보세요.
* 근래 함수형 언어가 각광받는 이유가 무엇일까요?
* 클로저가 무엇이고, 어디에 쓰이나요? 클로저와 클래스의 공통점은 무엇인가요?
* 제너릭이 어떨 때 쓰이나요?
* 고차 함수란 무엇인가요? 고차 함수는 어떤 상황에서 쓰나요? 귀하의 주력 언어로 작성해 보세요.
* 반복문을 작성한 다음, 변수를 쓰지 말고 재귀 함수로 바꿔보세요. (토론)
* 어떤 언어가 함수를 일등 시민으로 간주한다는 것이 무엇을 의미하나요?
* 익명함수의 유용성을 예를 들어 설명해 주세요.
* 수 많은 타입 시스템이 있는데요, 정적/동적 타입 시스템에 대해서, 그리고 그 장단점에 대해서 이야기 해 봅시다. 아마 이 주제에 대한 의견이나 선호하는 방식이 있을 것입니다. 엔터프라이즈 급 소프트웨어를 개발하기 위해 특정 타입 시스템이 왜, 그리고 언제 쓰여야 하는지 의견을 말해주시고 토론해 봅시다.
* 네임스페이스는 어떨 때 유용한가요? 네임스페이스의 대안을 말해보세요.
* 자바와 C#의 상호운용성에 대해 이야기 해 봅시다. (다른 임의의 2개의 언어도 가능)
* 많은 개발자가 자바를 좋아하지 않는 이유는 무엇인가요?
* 무엇이 좋은 언어와 나쁜 언어를 만드나요?
* 참조(Referentially) 투명 함수(순수 함수)와 참조 불투명 함수를 각각 하나씩 작성하세요. (토론)
* Stack과 Heap은 무엇인가요? Stack Overflow는 무엇인가요?
* 언어에서 함수가 일등시민인지 여부가 왜 중요한가요?
* 일부 언어, 특히 함수형 언어는 패턴 매칭을 허용합니다. 이 사실을 알고 있나요? 그리고 패턴 매칭과 Switch 절이 어떻게 다른가요?
* 어떤 언어는 설계상 예외를 허용하지 않는데요, 그 이유와 장단점은 무엇일까요?
* `Cat` is a `Animal` 이면, `TakeCare<Cat>` is a `TakeCare<Animal>` 인가요?
* Java나 C# 등 많은 언어에서 인터페이스에 생성자가 없는 이유가 무엇인가요?
* 최근 몇 년간 Node가 많이 과장된 것 같습니다. 브라우저에서 실행되도록 고안된 언어를 백엔드에서 사용하는 부분에 대해 어떻게 생각하시나요?
* 만약 과거로 돌아가서 Java(C#, Python, Go 등 주력언어) 설계자와 대화할 수 있다면 어떤 부분을 바꿔야 한다고 설득하겠습니까? 명시적인 예외(checked exception)를 없애달라고 할까요? 부호 없는 기본 자료형을 추가해달라고 할까요? 다중 상속을 추가해 달라고 할까요?


### [[↑]](#toc) <a name='web'>Web:</a>
* first-party(도메인 귀속) 쿠키와 third-party(도메인 독립) 쿠키를 다르게 취급하는 이유는 무엇인가요?
* 웹 API의 버전관리는 어떻게 하시나요?
* 백엔드 관점에서 SPA는 어떤 단점이나 문제점이 있을까요?
* 상태 정보가 없는(stateless) 서비스를 만들기 위해 노력하는 일반적인 이유는 무엇인가요? 상태 정보가 없는 코드가 왜 좋으며 상태정보를 보관하는 방식(stateful)이 왜 나쁜가요?
* REST 와 SOAP: 각각 어떤 상황에서 선택해야 하나요?
* 웹개발에서 백엔드나 프론트엔드 모두 MVC나 MVVM 패턴이 매우 일반적입니다. 각각이 어떤 의미이고, 적합한 이유는 무엇인가요?


### [[↑]](#toc) <a name='databases'>DB:</a>

* 서로 다른 DB간 마이그레이션을 어떻게 진행하시나요?(예: MySQL에서 PostgreSQL로) 마이그레이션 프로젝트의 관리자라면 어떤 이슈가 예상되나요?
* DB가 null을 특수 케이스로 보는 이유가 무엇인가요? 예를 들면, 다음 SQL문 ```SELECT * FROM table WHERE field = null```이 널을 포함하는 ``field``를 가져오지 못하는 이유가 무엇인가요?
* ACID는 대부분의 DB가 지원하는 트랜잭션이 보장하는 원자성(Atomicity), 일관성(Consistency), 고립성(Isolation), 지속성(Durability)의 네 가지 속성을 말하는 약자입니다. 이 ACID에 대해 알고 계시나요? 구체적으로 얘기해 봅시다.
* DB 스키마를 어떻게 마이그레이션 하시나요? 다시말해, 응용프로그램의 버전이 올라감에 따라 변경된 DB 스키마를 자동화하여 적용하는 방법은 무엇인가요?
* Lazy Loading을 어떻게 만들어 낼까요? 언제 유용하고, 이 설계방식의 함정은 무엇인가요?
* "N + 1 문제"는 lazy-loading이 활성화된 부모-자식 관계로 설정된 ORM객체가 하나의 쿼리로 각각의 자식을 읽어올 때 발생하는 문제입니다. 이 문제를 어떻게 수정하시겠습니까?
* 프로그램에서 가장 비싼 쿼리를 어떻게 찾으시겠습니까?
* 항상 DB를 정규화해야 한다고 생각하시나요? 언제 DB를 정규화하지 않고 쓸 수 있나요?
* Blue-Green Deployment라 불리우는 CI 기술은 동일한 두 개의 프로덕션 환경에서 한 쪽이 작동중일 때 다른 쪽에 배포하고 간단한 테스트 후 다른 쪽 환경으로 안전하게 트래픽을 전환하는 기술입니다. 이 기술은 배포시 DB 구조나 내용이 변경될 때 더욱 복잡해집니다. 이 주제에 대해 토론해 봅시다.


### [[↑]](#toc) <a name='nosql'>NoSQL:</a>

* 최종 일관성(Eventual Consistency)은 무엇인가요?
* 보통 CAP 정리라고 알려져 있는 브루어(Brewer)의 정리는 시스템 설계자가 네트워크 파티션(Partition, P)에서 일관성(Consistency, C)과 가용성(Availability, A) 사이에서 하나를 선택해야 한다는 정리입니다. CP, AP, CA 시스템을 각각 예를 들어 설명해 주세요.
* 최근 NoSQL에 대한 관심이 부상하는 현상을 어떻게 설명하시겠습니까?
* NoSQL은 확장성 문제를 어떻게 해소하나요?
* 어떤 경우에 MySQL이나 PostgreSQL 같은 RDB 대신 MongoDB 같은 document DB를 사용하시겠습니까?


### [[↑]](#toc) <a name='codeversioning'>버전관리:</a>

* Mercurial이나 git이 SVN 보다 branch 따기 쉬운 이유가 무엇인가요?
* SVN 같은 중앙 집중형 버전 관리 시스템과 비교하여 Git 같은 분산형 버전 관리 시스템이 갖는 장단점은 무엇인가요?
* GitHub Flow와 GitFlow의 업무 흐름을 설명해주세요.
* Rebase란 무엇인가요?
* Mercurial과 git이 SVN이나 CVS보다 merge가 쉬운 이유는 무엇인가요?


### [[↑]](#toc) <a name='concurrency'>동시성(Concurrency):</a>

* 동시성(Concurrency)이 필요한 이유를 설명해 주세요.
* 멀티쓰레딩 / 동시 코드의 테스트가 어려운 이유는 무엇인가요?
* 경쟁 상태(Race Condition)란 무엇인가요? 선호하는 언어로 예제 코드를 작성해 주세요.
* Deadlock이 무엇인가요? Deadlock이 걸리는 코드를 작성해 보시겠습니까?
* 프로세스 기아상태(Starvation)-livelock, 역자주-란 무엇인가요? 정의를 확인하고 이야기 하셔도 좋습니다.
* Wait Free 알고리즘이 무엇인가요?


### [[↑]](#toc) <a name='distributed'>분산 시스템:</a>

* 분산 시스템은 어떻게 테스트 하나요?
* 어떤 경우에 두 시스템 간 비동기 통신을 허용하나요?
* 원격 프로시저 호출에서 일반적으로 예상되는 함정이 있다면 무엇일까요?
* 확장성과 견고성이 보장된 분산시스템을 구축한다면, 폐쇄망 환경에서 작업할 때와 지리적으로 분산된 공용 시스템에서 작업할 때 어떤 부분이 다를까요?
* 장애 허용(Fault Tolerance) 웹 애플리케이션을 어떻게 관리하시겠습니까? 데스크탑 애플리케이션은요?
* 분산 시스템의 장애를 어떻게 다루어야 할까요?
* 네트워크 재설정 이후 후처리 방법에 대해 이야기해 봅시다.
* 분산 시스템의 맹점은 무엇인가요?
* Request/Reply와 Publish/Subscribe를 각각 언제 사용하시겠습니까?
* 트랜잭션을 지원하지 않는 시스템에서 작업한다고 가정해 봅시다. 어떤식으로 접근해야 할까요?


### [[↑]](#toc) <a name='management'>소프트웨어 생명주기와 팀 관리:</a>

* Agility란 무엇인가요?
* 레거시 코드를 어떻게 처리하시나요?
* 제가 비 전문가인 PM이라고 가정하고, 레거시 코드가 무엇인지, 코드 품질을 왜 신경써야 하는지 설명해 주세요.
* 제가 CEO라고 가정하고, 칸반에 대해 설명하시고 투자하도록 설득해 보세요.
* 애자일과 폭포수 방법론의 가장 큰 차이는 무엇인가요?
* 회의가 너무 많은 문제를 관리자로서 어떻게 해결하시겠습니까?
* 너무 늦어버린 프로젝트를 어떻게 관리하시겠습니까?
* "*프로세스와 도구의 사유화 및 상호작용*"과 "*지속적 협상을 통한 고객 협업*"은 애자일 선언문의 절반을 차지합니다. 이에 대해 이야기 해 봅시다.
* CTO가 된다면 어떤식으로 회사를 꾸리시겠습니까?
* 프로그램 매니저(역자주: 사실상 프로젝트의 슈퍼맨)가 필요하다고 생각하나요?
* 휴가를 마음대로 쓸 수 있는 완전한 탄력적 근무 상황에서 개발팀을 조직해 보세요.
* 이직이 잦은 팀을 어떻게 관리하고 임금인상 말고 어떤 방법으로 개발자가 떠나지 않도록 설득하시겠습니까? 회사 차원에서는 개발자가 떠나지 않도록 어떻게 해야 할까요?
* 동료에게 바라는 가장 중요한 세 가지는 무엇인가요? 코드는 빼고요.
* 비개발자가 코딩에 대해 알았으면 하는 점 세 가지는 무엇인가요?
* 회사에서 당신과 동료들의 삶의 질을 높히기 위해 한 달의 시간과 예산을 줬다면 무엇을 하시겠습니까?


### [[↑]](#toc) <a name='algorithms'>알고리즘:</a>

* LIFO 스택만 써서 FIFO 큐를 작성하세요. 다음으로 FIFO 큐만 써서 LIFO 스택을 만드세요.
* Stack Overflow를 유발하는 코드를 작성하세요.
* 재귀를 사용하여 팩토리얼 함수를 작성하세요.
* 원하시는 언어로 입력값을 그대로 출력하는 REPL을 작성하세요. 그리고 후위표기법(RPN)에 의한 계산기능을 추가하세요.
* 조각모음 프로그램을 설계해보세요.
* 미로를 랜덤으로 생성하는 프로그램을 작성하세요.
* 메모리 누수를 유발하는 예제코드를 작성해 보세요.
* 유니크한 난수열을 발생시키세요.
* 간단한 GC(Garbage Collection) 시스템을 작성하세요.
* 원하는 언어로 기본 메시지 브로커를 작성하세요.
* 아주 기본적인 웹서버를 작성해 보세요. 그리고 추후 구현할 기능들에 대해 방향성을 제시해 보세요.
* 10GB 짜리 파일을 어떻게 정렬하시겠습니까? 10TB 짜리는 어떻게 접근방식을 바꿔야 할까요?
* 중복된 파일을 프로그램적으로 어떻게 감지해 날까요?


### [[↑]](#toc) <a name='architecture'>소프트웨어 아키텍처:</a>

* 언제 캐시가 필요 없거나 심지어 위험한가요?
* Event-Driven 아키텍처가 왜 확장성을 높히나요?
* 코드를 읽을 수 있게 만드는 것은 무엇입니까?
* 즉각적인 설계 수정과 진화형 아키텍처의 차이점은 무엇인가요?
* Scale out과 scale up의 차이점은 무엇이고 각각 어떤 경우에 적용하나요?
* Failover(대체 시스템, 부하분산 등)와 사용자 세션은 어떻게 다루나요?
* CQRS(Command Query Responsibility Segregation, 도메인 모델 설계시 CUD와 R을 분리)란 무엇이고, CQS 원칙과 어떻게 다른가요?
* 소위 말하는 "다중 계층 아키텍처"는 클라이언트-서버 시스템을 물리적/논리적인 구분, 애플리케이션 처리, 데이터 관리와 기타 다른 기능으로 각각 유지할 수 있도록 설계하는 접근방법입니다. 그중 3계층 아키텍처가 가장 널리 알려져 있습니다. 이러한 접근방식의 장단점에 대해 토론해 봅시다.
* 소프트웨어 시스템이 확장성을 갖기 위해 어떻게 설계하시겠습니까?
* 누군가 한번에 만 개가 넘는 동시 접속을 처리하기 위한 네트워크 소켓의 최적화 문제에 "The "C10k problem"이라는 이름을 붙였습니다. 만 개의 동시접속을 처리하는 문제와 만 개의 클라이언트를 처리하는 문제는 같지는 않지만 문맥상 비슷합니다. 어쨌든 대단한 도전인데, 아무도 이 문제를 풀기 위한 모든 세부 사항을 알지 못합니다. 이 문제를 해결하기 위한 귀하의 전략이 궁금한데요, 한번 도전해 보시겠습니까?
* 어떻게 분산형(중앙 서버가 없는) P2P 시스템을 설계하시겠습니까?
* CGI(Common Gateway Interface)란 서버에서 CLI 프로그램으로 실행하고, HTTP 요청에 의해 동적으로 HTML 페이지를 생성하는 웹서버를 위한 표준 프로토콜(CGI scripts)입니다. Perl이나 PHP가 이에 해당하는 대표적인 script 언어입니다. CGI에서는 일반적으로 HTTP 요청에 의해 서버에서 새로운 프로세스가 생성되지만, FastCGI, SCGI 등에서는 사전 프로세스 로딩(preforking process) 같은 기술로 메커니즘을 개선하여 퍼포먼스를 향상시킵니다. 결국 CGI가 왜 성공하지 못하고 이런 다른 아키텍처로 대체되었을까요?
* Vendor Lock-in 문제(플랫폼에 종속되어 발생하는 호환성 문제)에 대응하기 위해서 어떻게 설계해야 할까요?
* 대형화된 발행-구독(Publish-Subscribe) 모델의 단점은 무엇인가요?
* 80년대 이후 CPU의 새로운 기능은 무엇이며 프로그래밍에 어떤 영향을 주나요?
* 소프트웨어 성능의 생명주기에서 어느 부분을 고려하는 것이 좋을까요? 그리고 어떻게 하나요?
* 누군가의 악의가 아니라 설계나 아키텍처의 문제에 의한 서비스 거부 현상이 어떻게 일어날 수 있을까요?
* 성능과 확장성의 관계에 대해 이야기해 보세요.
* 강한 결합도(tight coupling)를 언제까지 쓸 수 있을까요?
* 시스템을 클라우드에 올리려면 어떤 특성을 갖춰야 하나요?
* 설계 통합이 최고의 아키텍트일까요? 간단히 말해서, 모든 개발자의 공동 노력으로 좋은 설계를 만들어낼 수 있을까요?
* 설계와 아키텍처, 기능성, 미학의 차이점은 무엇일까요? 토론해 봅시다.


### [[↑]](#toc) <a name='soa'>SOA & MSA:</a>
* SOA에서 긴 트랜잭션보다 saga 패턴이 권장되는 이유는 무엇인가요?
* SOA와 MSA 간의 차이는 무엇인가요?
* 웹 서비스의 버전 관리, 버전간 호환성, 변경에 의한 잠재적 오류에 대해 이야기 해 봅시다.
* SOA에서 트랜잭션과 saga 내의 보정 작업 간의 차이는 무엇인가요?
* 언제 MSA가 너무 작은가요?
* MSA의 장단점은 무엇인가요?


### [[↑]](#toc) <a name='security'>보안:</a>
* 어떻게 secure code를 작성하시겠습니까? 개발자의 임무인가요, 보안 전문가의 역할인가요? 그리고 왜 그렇게 생각하나요?
* 왜 암호화 자체를 개발하거나 설계할 필요가 없다고 하나요?
* 인증의 두 요소는 무엇인가요? 이미 서비스중인 웹앱에서 어떤 방식으로 구현하시겠습니까?
* 조심하지 않으면 언제든지 비밀번호 같은 민감정보가 로그에 기록될 수 있습니다. 이런 문제를 어떻게 하시겠습니까?
* SQL Injection에 취약한 코드를 작성하고 수정하세요.
* 정적 코드 분석기로 어떻게 SQL Injection을 탐지할 수 있나요? 이에 대한 알고리즘 작성까지 바라는 건 아니지만, 좀 거대한 주제이긴 해도 일반적인 접근방식에 대해 토론해 봅시다.
* Cross-Site Scripting에 대해 알고 있나요? 모른다면 인터넷에서 정의를 확인해 보고 이에 대해 토론해 봅시다.
* 사이트 위조 공격(Cross-Site Forgery Attack)에 대해 알고 있나요? 모른다면 인터넷에서 정의를 확인해 보고 이에 대해 토론해 봅시다.
* HTTPS는 어떤 방식으로 작동하나요?
* 중간자 공격(Man-in-the-middle Attack, MITM)이 무엇이고, HTTPS가 어떻게 중간자 공격을 막나요?
* 사용자 세션의 도난은 어떻게 막아야 하나요? 세션/쿠키 도용에 대해 기억나지 않는다면 위키 페이지를 읽어봅시다.


### [[↑]](#toc) <a name='general'>일반:</a>

* 함수형 프로그래밍이 왜 중요한가요? 언제 함수형 프로그래밍 언어를 써야 할까요?
* Microsoft, Google, Opera, Mozilla 같은 회사는 어떻게 브라우저로 수익을 낼까요?
* TCP 소켓을 열 때 오버헤드가 발생하는 이유는 무엇인가요?
* 캡슐화는 어디에 중요한가요?
* 실시간 시스템은 무엇이며, 일반적인 시스템과 어떻게 다른가요?
* 실시간 언어와 힙 메모리 할당 간의 관계에 대해 이야기 해 주세요.
* 불가역성(Immutability)이란 생성시점에 값을 한 번 할당한 후 이후로는 값을 변경하지 않는다는 뜻입니다. 더 안전한 코드를 작성하는데 불가역성이 어떻게 도움을 줄 수 있나요?
* 가변 변수와 불변 변수의 장단점에 대해 이야기 해 보세요.
* 객체-관계의 임피던스 부정합(Object-Relational impedance mismatch)은 무엇인가요?
* 캐시의 크기를 정의할 때 어떤 원칙을 적용해야 할까요?
* TCP와 HTTP의 차이점은 무엇인가요?
* 클라이언트 사이드 랜더링과 서버 사이드 랜더링의 절충안은 무엇인가요?
* 연속성을 보장할 수 없는 통신 프로토콜로 어떻게 연속적인 통신 프로토콜을 개발할 수 있을까요?
* Null 참조를 개발한 [Tony Hoare](https://en.m.wikipedia.org/wiki/Tony_Hoare) 는 "*셀 수 없는 수많은 에러, 취약성, 시스템 충돌을 초래하는 지난 40년 간의 백만불짜리 고통과 상처*"라며 "*저는 null 참조를 백만불짜리 실수라고 부릅니다*"라고 말했습니다. 귀하의 주 언어에서 null 참조를 없앤다면, 어떻게 해야 할까요? 또 그 결과는 어떨까요?


### [[↑]](#toc) <a name='open'>열린 질문:</a>
* 사람들이 변화에 저항하는 이유가 뭘까요?
* 조부모님께 쓰레드에 대해 설명해 보세요.
* 소프트웨어 엔지니어는 혁신적이면서 예측가능해야 합니다. 동일한 전략에서 어떻게 이 두 목표가 공존할 수 있나요?
* 좋은 코드를 좋은 코드답게 만드는 건 무엇일까요?
* 스트리밍이 무엇인지와 스트리밍을 어떻게 구현할지에 대해 설명해 보세요.
* 회사에서 당신과 동료들의 삶의 질을 높히기 위해 일주일을 줬다면 어떻게 하시겠습니까?
* 이번 주에 뭘 배우셨나요?
* 모든 설계에는 미적 요소가 있습니다. 질문 드리자면, 이 미적 요소가 당신의 친구입니까, 적입니까?
* 최근 읽은 5 권의 책을 말해주세요.
* 비즈니스의 규모와 복잡성 때문에 폭포수 방법론에서 지속적 배포(Continuous Delivery) 방식으로 변경하기 어려운 성공적인 대형 회사에서 지속적 배포에 대해 어떻게 소개하시겠습니까?
* 언제 바퀴를 다시 발명해도 말이 되나요?
* "*바퀴 다시 발명하기(Reinventing the wheel)*", "*여기서 발명 안했음 신드롬(Not Invented Here Syndrome)*", "*니꺼 먹어라(Eating Your Own Food)*" 연습에 대해 이야기 해 봅시다.
* 현재 당신의 업무에서 다음 자동화 대상은 무엇인가요?
* 소프트웨어 개발이 어려운 이유는 무엇인가요? 소프트웨어 유지보수가 어려운 이유는 무엇인가요?
* 신규 도메인 개발과 구현된 적이 있는 도메인 중 어느 쪽을 선호하나요? 이유는 무엇인가요?
* [브라우저에 google.com이라고 입력하고 엔터를 누르면 무슨 일이 일어나나요?(What happens when you type google.com into your browser and press enter?)](https://github.com/alex/what-happens-when)
* 실행할 사용자 지정 코드가 없어서 idle 상태처럼 보일 때 OS는 무엇을 하나요? 인터럽트, 데몬, 백그라운드 서비스, 폴링, 이벤트 핸들링 등에 대해 이야기해 봅시다.
* 유니코드/DB 트랜잭션을 5살 짜리 아이에게 설명해 보세요.
* Monolithic architecture를 변호해 보세요.
* 프로패셔널 개발자가 되는 것은 무슨 의미입니까?
* 소프트웨어 개발이 예술이나 장인정신, 혹은 공학적인 무언가일까요? 당신의 의견을 말해보세요.
* 쇼핑몰에서 연관상품 광고를 어떻게 구현하시겠습니까?
* 일반 기업이 스타트업보다 혁신이 느린 이유는 무엇인가요?
* 최근에 달성한 자랑거리 하나 소개해 주세요.



### [[↑]](#toc) <a name='snippets'>코드 제시형:</a>
* 이 자바스크립트 함수의 출력 결과는?
```javascript
function hookupevents() {
  for (var i = 0; i < 3; i++) {
    document.getElementById("button" + i)
      .addEventListener("click", function() {
        alert(i);
      });
  }
}
```

* 자바 제너릭의 타입 Erasure와 관련해서, 다음 자바 코드의 출력 결과는 무엇이고 그렇게 출력되는 이유는 무엇인가요?
```java
ArrayList<Integer> li = new ArrayList<Integer>();
ArrayList<Float> lf = new ArrayList<Float>();
if (li.getClass() == lf.getClass()) // evaluates to true
  System.out.println("Equal");
```


* 메모리 누수가 일어나는 지점을 짚어보세요.
```java
public class Stack {
    private Object[] elements;
    private int size = 0;
    private static final int DEFAULT_INITIAL_CAPACITY = 16;

    public Stack() {
        elements = new Object[DEFAULT_INITIAL_CAPACITY];
    }

    public void push(Object e) {
        ensureCapacity();
        elements[size++] = e;
    }

    public Object pop() {
        if (size == 0)
            throw new EmptyStackException();
        return elements[--size];
    }

    /**
     * 최소 하나 이상의 element를 위한 공간을 확보하세요.
     * 배열이 커지면 용량이 거의 두 배가 됩니다.
     */
    private void ensureCapacity() {
        if (elements.length == size)
            elements = Arrays.copyOf(elements, 2 * size + 1);
    }
}
```

* `if`문이나 일반적인 조건문은 프로그램을 절차지향적으로 만듭니다. 다음 코드에서 `switch`문을 제거하고 코드를 좀 더 객체지향적으로 만들어 주시겠어요?

```java
public class Formatter {

    private Service service;

    public Formatter(Service service) {
        this.service = service;
    }

    public String doTheJob(String theInput) {
        String response = service.askForPermission();
        switch (response) {
        case "FAIL":
            return "error";
        case "OK":
            return String.format("%s%s", theInput, theInput);
        default:
            return null;
        }
    }
}
```


* 다음 코드에서 `if`문을 제거하고 코드를 좀 더 객체지향적으로 만들어 주시겠어요?

```java
public class TheService {
    private final FileHandler fileHandler;
    private final FooRepository fooRepository;

    public TheService(FileHandler fileHandler, FooRepository fooRepository) {
        this.fileHandler = fileHandler;
        this.fooRepository = fooRepository;
    }

    public String Execute(final String file) {

        final String rewrittenUrl = fileHandler.getXmlFileFromFileName(file);
        final String executionId = fileHandler.getExecutionIdFromFileName(file);

        if (executionId.equals("") || rewrittenUrl.equals("")) {
            return "";
        }

        Foo knownFoo = fooRepository.getFooByXmlFileName(rewrittenUrl);

        if (knownFoo == null) {
            return "";
        }

        return knownFoo.DoThat(file);
    }
}
```

* 이 코드를 어떻게 리팩토링 할까요?

```js
function()
{
    HRESULT error = S_OK;

    if(SUCCEEDED(Operation1()))
    {
        if(SUCCEEDED(Operation2()))
        {
            if(SUCCEEDED(Operation3()))
            {
                if(SUCCEEDED(Operation4()))
                {
                }
                else
                {
                    error = OPERATION4FAILED;
                }
            }
            else
            {
                error = OPERATION3FAILED;
            }
        }
        else
        {
            error = OPERATION2FAILED;
        }
    }
    else
    {
        error = OPERATION1FAILED;
    }

    return error;
}
```

### [[↑]](#toc) <a name='billgates'>빌게이츠 스타일:</a>
이 섹션은 [맨홀 뚜껑 질문, Manhole Cover Question](https://en.wikipedia.org/wiki/Microsoft_interview#Manhole_cover_question)에서 좀 이상한 질문들을 모은 것입니다.

* 스캐너에 거울을 넣으면 무슨 일이 일어나나요?
* 귀하의 복제인간이 귀하의 상사라면 그 사람을 위해 즐겁게 일할 수 있나요?
* 저를 인터뷰 해보세요.
* 네이버 지식인이 다음 팁의 답변보다 나은 이유는 무엇인가요?(원문은 quora vs yahoo)
* 현대 언어로 부터 Cobol을 변호해 보세요. 그리고 가능한 많은 합리적인 논쟁거리를 찾아보세요.
* 10년 후 어디에 있을 것 같나요?
* 당신이 내 상사이고 난 해고되었습니다. 그 사실을 전해주세요.
* 저는 레거시 시스템을 리팩토링 하고 싶습니다. 당신은 처음부터 재작성 하고 싶구요. 논쟁해 봅시다. 역할을 바꿔서도 해 봅시다.
* 당신의 상사가 회사에 거짓말 할 것을 요구했습니다. 어떻게 대응하시겠습니까?
* 과거로 여행할 수 있다면 젊은 귀하에게 무슨 조언을 해 주시겠습니까?
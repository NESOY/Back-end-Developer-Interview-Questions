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

  1. [디자인 패턴](#patterns)
  1. [코드 설계](#design)
  1. [언어](#languages)
  1. [Web](#web)
  1. [DB](#databases)
  1. [NoSQL](#nosql)
  1. [버전관리](#codeversioning)
  1. [동시성(Concurrency)](#concurrency)
  1. [분산 시스템](#distributed)
  1. [소프트웨어 생명주기와 팀 관리](#management)
  1. [알고리즘](#algorithms)
  1. [소프트웨어 아키텍처](#architecture)
  1. [SOA & MSA](#soa)
  1. [보안](#security)
  1. [일반](#general)
  1. [열린 질문](#open)
  1. [코드 제시형](#snippets)
  1. [빌게이츠 스타일](#billgates)



### [[↑]](#toc) <a name='patterns'>디자인 패턴:</a>

* 전역 static 객체가 나쁜 이유는 무엇인가요? 코딩으로 예를 들어 설명해 주세요.
* 역제어 패턴(IoC)에 대해, 특히 설계 측면에서 설명해 주세요.
* 데메테르 법칙LoD(최소한의 지식 규칙)에 의하면 객체간의 정보가 제한되어야 하며 오직 직접 호출한 객체와 통신해야 한다고 합니다(낯선 객체와 통신하지 말라고 하기도 함). 이 원칙을 위반하는 코드를 작성해 보세요. 그리고 왜 나쁜 디자인인지 설명하고 수정해 보세요.
* ActiveRecode 는 insert, update, delete 등의 함수와 DB table의 열을 속성으로 갖는 객체를 생성하는 디자인 패턴입니다. 이 패턴의 한계와 함정이 무엇인지 귀하의 경험에 비추어 의견을 이야기 해주세요.
* Data-Mapper 는 객체와 DB 간 데이터 이동 중에 각각을 독립적으로 유지하기 위해 mapper를 사용하는 디자인 패턴입니다. 반면에, ActiveRecode 객체는 객체와 DB 간의 연결을 지속하기 위한 작업과 기본 DB 속성값을 직접 통합합니다. 이런 패턴에 대한 의견이 있으신가요? 각각 언제 사용하는게 좋을까요?
* Null의 도입이 억만금짜리 실수로 불리우는 이유는 무엇일까요? 또, Null문제를 해결하기 위한 Null 객체 패턴(GOF)이나 옵션 자료형에 대해 이야기해 봅시다.
* 많은 사람들이 OOP에서 상속보다 컴포지션이 낫다고들 합니다. 당신의 의견은 어떻습니까?
* 손상 방지 레이어(Anti-corruption Layer) 패턴이 무엇입니까?
* 싱글톤(Singleton) 디자인 패턴은 객체의 생성자를 하나로 제한합니다. 하지만 쓰레드에 안전한 싱클톤 클래스를 작성하기는 단순하지 않은데요, 한번 작성해 주시겠습니까?
* 클라이언트에 영향 없이 구현부를 변경하는 기능을 데이터 추상화라고 합니다. 이 속성에 반하는 예제를 작성해 주시고, 수정하는 과정을 보여주세요.
* DRY(Don't Repeat Yourself) 원칙을 위반하는 코드를 작성하시고, 수정하는 과정을 보여주세요.
* 의존성 지옥(Dependency Hell)은 어떻게 해결하는게 좋을까요?
* `goto` 문에 대해 어떻게 생각하시나요? `goto` 문의 사용을 비판하고 대신 구조화된 프로그래밍을 주창한 Edsger Dijkstra의 유명한 논문 "Go To Statement Considered Harmful"에 대해 들어보셨을 겁니다. `goto` 문은 항상 논란거리었는데요, 심지어 Dijkstra가 'goto가 유해한 것 같다'고 한 말조차 비판받기도 했습니다. 이 `goto` 문에 대해 어떻게 생각하시나요?
* 견고함의 원칙(The robustness principle)은 "*보내기는 더디하고 받기는 쉬이하라*"는 일반적인 소프트웨어 설계의 가이드라인입니다. 때때로 "*관용적인 독자와 신중한 작가가 되라*"로 불리기도 합니다. 이 원칙에 대해 이론적인 해석을 해 봅시다.
* 관심사 분리(Separation of Concerns)는 프로그램을 각각의 구역으로 격리하는 설계 원칙으로, 각 구역은 관심사가 분리된 것으로 간주됩니다. 객체, 함수, 모듈, MVC 같은 패턴 등 관심사 분리를 달성하기 위한 수많은 메커니즘이 있습니다. 이 주제에 대해 토론해 봅시다.


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
* How would you manage a very high turn over and convince developers not to leave the team, without increasing compensation? What could a Company improve to make them stay?
* What are the top 3 qualities you look for in colleagues, beyond their code?
* What are the top 3 things you wish non-technical people knew about code?
* Imagine your company gives you 1 month and some budget to improve your and your colleagues' daily life. What would you do?


### [[↑]](#toc) <a name='algorithms'>알고리즘:</a>

* Make a FIFO Queue using only LIFO Stacks. Then build a LIFO Stack using only FIFO Queues.
* Write a snippet of code affected by a Stack Overflow
* Write a tail-recursive version of the factorial function
* Using your preferred language, write a REPL that echoes your inputs. Evolve it to make it an RPN calculator.
* How would you design a "defragger" utility?
* Write a program that builds random mazes.
* Write a sample code that produces a memory leak
* Generate a sequence of unique random numbers
* Write a simple Garbage collection system
* Write a basic message broker, using whatever language you like.
* Write a very basic web server. Draw a road map for features to be implemented in the future.
* How would you sort a 10GB file? How would your approach change with a 10TB one?
* How would you programmatically detect file duplicates?


### [[↑]](#toc) <a name='architecture'>소프트웨어 아키텍처:</a>

* When is a cache not useful or even dangerous?
* Why does Event-Driven Architecture improve scalability?
* What makes code readable?
* What is the difference between emergent design and evolutionary architecture?
* Scale out vs scale up: how are they different? When to apply one, when the other?
* How to deal with failover and user sessions?
* What is CQRS (Command Query Responsibility Segregation)? How is it different from the oldest Command-Query Separation Principle?
* The so called "multitier architecture" is an approach to design a client–server system aimed to keep physically and logically separated presentation, application processing, data management and other functions. The most widespread of the multitier architectures is the three-tier architecture. Would you discuss the pros and cons of such approach?
* How would you design a software system for scalability?
* Someone gave the name "The "C10k problem" to the problem of optimising network sockets to handle over 10.000 open connections at once. While handling 10.000 concurrent clients is not the same as handling 10.000 open connection, the context is similar. It's a tough challenge anyway, and no one is expected to know every single detail to solve it. It may be interesting to discuss the strategies you know to deal with that problem. Would you like to try?
* How would you design a decentralized (that is, with no central server) P2P system?
* You may recall that Common Gateway Interface (CGI) is a standard protocol for web servers to execute programs (CGI scripts) that execute as Command-line programs on a server, and that dynamically generate HTML pages when invoked by a HTTP request. Perl and PHP used to be common languages for such scripts. In CGI, a HTTP request generally causes the invocation of a new process on the server, but FastCGI, SCGI and other approaches improved the mechanism, raising the performance, with techniques such as preforking processes. Can you imagine why has't CGI eventually win, and was instead replaced with other architectural approaches?
* How would you defend the design of your systems against Vendor Lock-in?
* What are the disadvantages of the Publish-Subscribe pattern at scale?
* What's new in CPUs since the 80s, and how does it affect programming?
* In which part of the lifecycle of a software performance should be taken in consideration, and how?
* How could a Denial of Service arise not maliciously but for a design or architectural problem?
* What’s the relationship between Performance and Scalability?
* When is it OK (if ever) to use tight coupling?
* What characteristic should a system have to be Cloud Ready?
* Does unity of design imply an aristocracy of architects? Putting it simple: can good design emerge from a collective effort of all developers?
* What's the difference between design, architecture, functionality and aesthetic? Discuss.



### [[↑]](#toc) <a name='soa'>SOA & MSA:</a>
* Why, in a SOA, long-lived transactions are discouraged and Sagas are suggested instead?
* What are the differences between Soa and Microservices?
* Let's talk about web services versioning, version compatibility and breaking changes.
* What's the difference between a transaction and a compensation operation in a saga, in SOA?
* When is a Microservice too micro?
* What are the pros and cons of MicroService architecture?


### [[↑]](#toc) <a name='security'>보안:</a>
* How do you write secure code? In your opinion, is it one of the developer's duties, or does it require a specialized role in the company? And why?
* Why is it said that cryptography is not something you should try to invent or design yourself?
* What is two factor authentication? How would you implement it in an existing web application?
* If not carefully handled, there is always a risk of logs containing sensitive information, such as passwords. How would you deal with this?
* Write down a snippet of code affected by SQL Injection and fix it.
* How would it be possible to detect SQL Injection via static code analysis? I don't expect you to write an algorithm capable of doing this, as it is probably a huge topic, but let's discuss a general approach.
* What do you know about Cross-Site Scripting? If you don't remember it, let's review online its definition and let's discuss about it.
* What do you know about Cross-Site Forgery Attack? If you don't remember it, let's review online its definition and let's discuss about it.
* How does HTTPS work?
* What's a Man-in-the-middle Attack, and why does HTTPS help protect against it?
* How can you prevent the user's session from being stolen? Chances are you remember what Session or Cookie Hijacking is, otherwise let's read its Wikipedia page together.


### [[↑]](#toc) <a name='general'>일반:</a>

* Why does Functional Programming matter? When should a functional programming language be used?
* How do companies like Microsoft, Google, Opera and Mozilla profit from their browsers?
* Why does opening a TCP socket have a large overhead?
* What is Encapsulation important for?
* What is a real-time system and how is it different from an ordinary system?
* What's the relationship between real-time languages and heap memory allocation?
* Immutability is the practice of setting values once, at the moment of their creation, and never changing them. How can immutability help write safer code?
* What are the pros and cons of mutable and immutable values.
* What's the Object-Relational impedance mismatch?
* Which principles would you apply to define the size of a cache?
* What's the difference between TCP and HTTP?
* What are the tradeoffs of client-side rendering vs. server-side rendering?
* How could you develop a reliable communication protocol based on a non-reliable one?
* [Tony Hoare](https://en.m.wikipedia.org/wiki/Tony_Hoare) who invented the null reference once said "*I call it my billion-dollar mistake*" since it lead to "*innumerable errors, vulnerabilities, and system crashes, which have probably caused a billion dollars of pain and damage in the last forty years*". Imagine you want to remove the possibility to have null references in your preferred language: how would you achieve this goal? What consequences could this have?


### [[↑]](#toc) <a name='open'>열린 질문:</a>
* Why do people resist change?
* Explain threads to your grandparents
* As a software engineer you want both to innovate and to be predictable. How those 2 goals can coexist in the same strategy?
* What makes good code good?
* Explain streaming and how you would implement it.
* Say your Company gives you one week you can use to improve your and your colleagues' lifes: how would you use that week?
* What did you learn this week?
* There is an aesthetic element to all design. The question is, is this aesthetic element your friend or your enemy?
* List the last 5 books you read.
* How would you introduce Continuous Delivery in a successful, huge company for which the change from Waterfall to Continuous Delivery would be not trivial, because of the size and complexity of the business?
* When does it make sense to reinvent the wheel?
* Let's have a conversation about "*Reinventing the wheel*", the "*Not Invented Here Syndrome*" and the "*Eating Your Own Food*" practice
* What's the next thing you would automate in your current workflow?
* Why is writing software difficult? What makes maintaining software hard?
* Would you prefer working on Green Field or Brown Field projects? Why?
* [What happens when you type google.com into your browser and press enter?](https://github.com/alex/what-happens-when)
* What does an Operating System do when it has got no custom code to run, and therefore it looks idle? I would like to start a discussions about interrupts, daemons, background services, polling, event handling and so on.
* Explain Unicode/Database Transactions to a 5 year old child.
* Defend the monolithic architecture.
* What does it mean to be a "Professional Developer"?
* Is developing software an art, a craftsmanship or an engineering endeavour? Your opinion.
* "People who like this also like... ". How would you implement this feature in an e-commerce shop?
* Why are corporations slower than startups in innovating?
* What have you achieved recently that you are proud of?



### [[↑]](#toc) <a name='snippets'>코드 제시형:</a>
* What's the output of this Javascript function?
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

* About Type Erasure, what's the output of this Java snippet, and why?
```java
ArrayList<Integer> li = new ArrayList<Integer>();
ArrayList<Float> lf = new ArrayList<Float>();
if (li.getClass() == lf.getClass()) // evaluates to true
  System.out.println("Equal");
```


* Can you spot the memory leak?
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
     * Ensure space for at least one more element, roughly
     * doubling the capacity each time the array needs to grow.
     */
    private void ensureCapacity() {
        if (elements.length == size)
            elements = Arrays.copyOf(elements, 2 * size + 1);
    }
}
```

* `if`s and in general conditional statements lead to procedural and imperative programming. Can you get rid of this `switch` and make this snippet more object oriented?

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


* Can you get rid of these `if`s and make this snippet of code more object oriented?

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

* How to refactor this code?

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
This section collects some weird questions along the lines of the [Manhole Cover Question](https://en.wikipedia.org/wiki/Microsoft_interview#Manhole_cover_question).

* What would happen if you put a mirror in a scanner?
* Imagine there's a perfect clone of yourself. Imagine that that clone is your boss. Would you like to work for him/her?
* Interview me
* Why are Quora's answers better than Yahoo Answers' ones?
* Let's play a game: defend Cobol against modern languages, and try to find as many reasonable arguments as you can.
* Where will you be in 10 years?
* You are my boss and I'm fired. Inform me.
* I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles.
* Your boss asks you to lie to the Company. What's your reaction?
* If you could travel back in time, which advice would you give to your younger self?
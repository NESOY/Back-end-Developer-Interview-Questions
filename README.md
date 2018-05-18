Back-End 개발자 인터뷰 질문
======================================
## 인터뷰 관련 정보
#### Back-End 인터뷰
- [영어](https://github.com/arialdomartini/Back-End-Developer-Interview-Questions) by [@arialdomartini](https://github.com/arialdomartini).
- [중국어](https://github.com/monklof/Back-End-Developer-Interview-Questions) by [@monklof](https://github.com/monklof).

#### Front-end 인터뷰
- [영어](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions) by [@darcyclarke](https://github.com/darcyclarke)
- [한국어](https://github.com/h5bp/Front-end-Developer-Interview-Questions/tree/master/Translations/Korean)🇰🇷

#### 한국🇰🇷 취업 정보.
- [Interview_Question_for_Beginner](https://github.com/JaeYeopHan/Interview_Question_for_Beginner) by [@JBee](https://github.com/JaeYeopHan)
- [junior-recruit-scheduler](https://github.com/jojoldu/junior-recruit-scheduler) by [@jojoldu](https://github.com/jojoldu)

#### Developer 로드 맵
- [developer-roadmap](https://github.com/kamranahmedse/developer-roadmap) by [@kamranahmedse](https://github.com/kamranahmedse/)


## 공지
[![HitCount](http://hits.dwyl.io/nesoy/Back-end-Developer-Interview-Questions.svg)](http://hits.dwyl.io/nesoy/Back-end-Developer-Interview-Questions)

대부분의 질문은 자유롭게 답할 수 있으며 그 중에는 *옳은 답*과 *틀린 답*이 없는 질문들이 있습니다. 반대로, 그들은 올바른 정답보단 지원자의 능력에 대해 더 많이 말해 줄 수 있기를 바라면서 대화의 시작점으로 출발하기를 바라고 있습니다. 개인적으로, 나는 명확한 답이 없는 질문들을 선택할 것입니다.

다시 한번 말하지만, 저는 단지 질문들을 물어보는 것만으로 충분하지 않다는 것을 강조합니다. 지원자와 짝 프로그래밍을 진행하면서 인터뷰를 본다면 완벽할 것입니다: 이런 인터뷰 방식은 서로의 스타일을 알 수 있는 최고의 방법이고 지원자는 미래에 자신의 작업에 대해 더 잘 알 수 있을 것입니다.

이 프로젝트는 [@darcyclarke](https://github.com/darcyclarke)님이 작성하신 [Front-end Job Interview Questions](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions)에 영감을 받았습니다.

🙏 Help Me With the Translation

## <a name='toc'>목차 </a>

  1. [디자인 패턴](#patterns)
  1. [코드 디자인](#design)
  1. [프로그래밍 언어](#languages)
  1. [Web](#web)
  1. [데이터베이스](#databases)
  1. [NoSQL](#nosql)
  1. [Code Versioning](#codeversioning)
  1. [동시성](#concurrency)
  1. [분산 시스템](#distributed)
  1. [Software Lifecycle and Team Management](#management)
  1. [알고리즘](#algorithms)
  1. [소프트웨어 아키텍처](#architecture)
  1. [Service Oriented Architecture and Microservices](#soa)
  1. [보안](#security)
  1. [일반적인 질문](#general)
  1. [Open Questions](#open)
  1. [작은 코드 질문](#snippets)
  1. [빌 게이츠 스타일의 질문](#billgates)



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
* `goto`는 나쁜가요? 아마 당신은 `goto`를 비판하고, 구조적인 프로그래밍을 옹호하는, Edsger Dijkstra의 유명한 논문인 "Go To Statement Considered Harmful"에 대해서 들어봤을 것입니다. `goto`에 대한 사용은 항상 논란이 되어왔습니다. 심지어, Dijkstra의 의견을 비판한 "'GOTO Considered Harmful' Considered Harmful"이라는 글까지 있으니까요. `goto`에 대한 당신의 생각은 어떤가요?
* 견고함의 원칙(The robustness principle)은 "*당신이 하는 일은 엄하게, 남의 것을 받아들일 때는 너그럽게*"라고 일컬어지는 일반적인 소프트웨어 설계 가이드라인입니다. 이는, "*관대한 독자, 신중한 작가가 되어라*"라는 말로써 표현되기도 하죠. 이런 법칙이 합리적인지에 대해서 얘기를 나누어볼 수 있을까요?
* 관심의 분리(Separation of Concerns)는 컴퓨터 프로그램을 각자의 관심사에 따라 나누어 구분지어 개발한다는 설계 원칙입니다. 관심의 분리를 달성하기 위해서는 다양한 메커니즘을 활용할 수 있죠(MVC와 같은 설계에 기반한 객체, 함수, 모듈, 패턴 등을 사용하는 것). 이 주제에 대하여 얘기를 나누어 볼까요?


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


### [[↑]](#toc) <a name='languages'>프로그래밍 언어:</a>

* 선호하는 언어의 단점 3가지만 말해주세요.
* 왜 함수 프로그래밍(Functional Programming)이 떠오르고 있는지 설명할 수 있나요?
* 클로져란 무엇일까요? 그리고 어떤 상황에서 유용할까요? 클로져와 클래스간의 공통점은 무엇이 있을까요?
* 어떤 상황에서 Generics이 유용할까요?
* 고차 함수(High-order functions)란 무엇일까요? 어떤 상황에 유용할까요? 당신의 선호하는 언어로 예를 들어주세요.
* Write a loop, then transform it into a recursive function, using only immutable structures (i.e. avoid using variables). Discuss.
* 언어에서 함수(Function)을 일급 시민(First-Class citizens)으로 다룬다는 것은 무슨 의미일까요?
* 익명 함수(Anonymous Function) 장점이 나타나는 예제를 보여주세요.
* There are a lot of different type systems: let's talk about static and dynamic type systems, and about strong and weak ones. You surely have an opinion and a preference about this topic. Would you like to share them, and discuss why and when would you promote one particular type system for developing an enterprise software?
* NameSpace는 어떤 상황에 유용할까요? 대안은 없을까요?
* Talk about Interoperability between Java and C# (in alternative, choose 2 other arbitrary languages)
* 왜 많은 소프트웨어 개발자들은 자바를 좋아하지 않을까요?
* 어떠한 점이 좋은 언어와 나쁜 언어를 만들까요?
* Write two functions, one Referentially Transparent and the other one Referentially Opaque. Discuss.
* 스택(Stack)과 힙(Heap)은 무엇일까요? 스택 오버플로우(Stack Overflow)는 무엇일까요?
* 프로그래밍 언어에서 왜 first class citizens은 함수에서 중요할까요?
* Some languages, especially the ones that promote a Functional approach, allow a technique called Pattern Matching. Do you know it? How is Pattern Matching different from Switch clauses?
* 일부 언어에서는 예외처리가 없게 디자인이 되었을까요? 이런 디자인에 대해 장단점을 설명해주세요.
* If `Cat` is an `Animal`, is `TakeCare<Cat>` a `TakeCare<Animal>`?
* Why in Java, C# and many other languages constructors are not part of the interface?
* 지난 몇년 동안 Node에 대한 광고가 많았습니다. 처음에 브라우저에서 실행되도록 고안된 언어 사용에 대해 어떻게 생각하시나요?
* Pretend you have a time machine and pretend that you have the opportunity to go to a particular point in time during Java's (or C#, Python, Go or whatever) history, and talk with some of the JDK architects. What would you try to convince them of? Removing checked exceptions? Adding unsigned primitives? Adding multiple-inheritance?



### [[↑]](#toc) <a name='web'>Web:</a>
* 왜 first-party 쿠키들과 third-party 쿠키들을 다르게 다룰까요?
* 웹 서비스 API(Web Services API) 버젼을 어떻게 관리하실 건가요?
* Back-End 관점에서, Single Page Application의 단점은 무엇이 있을까요?
* 왜 우리는 stateless service를 사용하기 위해 많은 노력을 할까요? stateless code가 가져다 주는 장점들과 statefullness code가 가져다 주는 단점들에 대해 설명해 주세요.
* REST 그리고 SOAP: 어떤 상황에서 두가지 방법 중 하나를 선택해서 사용하실 건가요?
* Model-View-Controller 그리고 Model-View-ViewModel은 웹 개발의 백엔드와 프론트엔드 관점에서 매우 일반적입니다. 그들이 무엇인지? 그리고 그들이 왜 권장되고있는지 설명하실수 있나요?


### [[↑]](#toc) <a name='databases'>데이터 베이스:</a>

* 예를 들어 MySQL에서 PostgreSQL로 어떻게 다른 Database로 Migrate 할까요? 또한 만약에 당신이 해당 프로젝트를 관리하고 있다면 어떤 문제를 직면하게 될까요?
* 왜 데이터 베이스는 null을 특별한 Case로 관리할까요? 예를 들어 ```SELECT * FROM table WHERE field = null```은 ``field``가 null과 Matching이 되지 않을까요?
* ACID는 대표적으로 Atomicity, Consistency, Isolation 그리고 Durability가 있습니다. 데이터베이스의 트랜잭션은 앞서 언급한 4가지 특성을 보장합니다. 위 주제에 얼마나 알고 계신가요? 조금 더 자세히 설명해주실 수 있나요?
* Version차이와 Application발전으로 인해 데이터 베이스 스키마 변화가 생깁니다. 그러면 데이터 베이스 스키마 Migration 자동화 방법에 대해 어떻게 관리할까요?
* 어떻게 구현하면 Lazy Loading을 얻을 수 있을까요? 언제 유용할까요? Lazy Loading에 대해 함정은 없을까요?
* The so called "N + 1 problem" is an issue that occurs when the code needs to load the children of a parent-child relationship with a ORMs that have lazy-loading enabled, and that therefore issue a query for the parent record, and then one query for each child record. How to fix it?
* 어플리케이션에서 가장 비싼 비용의 Query를 어떻게 찾을까요?
* 데이터베이스의 정규화가 항상 필요할까요? 언제 데이터베이스의 비정규화가 바람직할까요? 당신의 의견을 들려주세요.
* Of of the Continuous Integration's techniques is called Blue-Green Deployment: it consists in having two production environments, as identical as possible, and in performing the deployment in one of them while the other one is still operating, and than in safely switching the traffic to the second one after some convenient testing. This technique becomes more complicated when the deployment includes changes to the database structure or content. I'd like to discuss this topic with you.


### [[↑]](#toc) <a name='nosql'>NoSQL:</a>

* Eventual Consistency이란 무엇일까요?
* The Brewer's Theorem, most commonly known as the CAP theorem, states that in the presence of a Network Partition (the P in CAP), a system's designer has to choose between Consistency (the C in CAP) and Availability (the A in CAP). Can you think about examples of CP, AP and CA systems?
* 최근에 NoSQL의 인기가 상승하고 있는 이유에 대해 설명할 수 있나요?
* NoSQL은 확장 문제를 어떻게 해결할까요?
* 어떤 상황에서 MySQL이나 PostgreSQL와 같은 Relational Database보다 MongoDB와 CouchBase와 같은 Document Database를 사용하는게 좋을까요?

### [[↑]](#toc) <a name='codeversioning'>Code versioning:</a>

* Mercurial과 git에서의 branching이 SVN과 CVS에서의 branching보다 쉬운 이유는 무엇일까요
* SVN과 같은 중앙 집중형 시스템과 비교하여 Git과 같은 분산 버전 관리 시스템(Distributed Version Control Systems)의 장점과 단점은 무엇인가요?
* GitHub Flow와 GitFlow workflows에 대해 설명해주세요.
* 리베이스(rebase)가 무엇일까요?
* Mercurial과 git에서의 merge가 SVN과 CVS에서의 merge보다 쉬운 이유는 무엇일까요?


### [[↑]](#toc) <a name='concurrency'>동시성:</a>

* 왜 우리는 동시성(Concurrency)이 필요할까요? 항상 그럴까요? 설명해보세요.
* Multithreading / concurrent code를 테스트한다는 건 왜 어려울까요?
* Race Condition이란 무엇일까요? 잘하는 언어를 사용하여 코드로 예제를 보여주세요.
* Deadlock이란 무엇일까요? Deadlock에 영향을 받는 코드를 작성해 주실 수 있나요?
* Process Starvation이란 무엇일까요? 필요하다면 정의에 대해 리뷰해주세요.
* Wait Free algorithm이란 무엇일까요?


### [[↑]](#toc) <a name='distributed'>분산 시스템:</a>

* 분산 시스템은 어떻게 테스트를 진행할까요?
* 어떤 상황에서 두 시스템 간의 비동기 커뮤니케이션(asynchronously communication)을 적용할 것인가요?
* 원격 프로시저 호출(Remote Procedure Call)의 일반적인 문제점은 무엇일까요?
* If you are building a distributed system for scalability and robustness, what are the different things you'd think of in the case you are working in a closed and secure network environment or in geographically distributed and public system?
* How to manage Fault Tolerance in a Web application? And in a Desktop one?
* 분산시스템의 장애는 어떻게 해결하실 건가요?
* Let's talk about the several approaches to Reconciliation after network partitions
* 분산 컴퓨팅의 단점은 무엇일까요?
* 당신은 언제 Request/Reply를 사용할 것이며 또한 어떤 상황에서 Publish/Subscribe를 사용할 것인가요?
* Suppose the system you are working on does not support transactionality. How would you implement it from scratch?


### [[↑]](#toc) <a name='management'>Software Lifecycle and Team Management:</a>

* agility란 무엇일까요?
* 당신은 레거시 코드(Legacy Code)를 어떻게 다루실 건가요?
* Say I'm your Project Manager, and I'm no expert in programming. Would you try explaining me what Legacy Code is and why should I care about code quality?
* 저는 당신 회사의 CEO라고 가정합시다. Kanban을 설명해 주시고 그 부분을 투자하도록 설득해주세요. 
* 애자일(Agile)과 폭포수(Waterfall)의 가장 큰 차이점은 무엇일까요?
* 팀 매니저로서 너무 많은 미팅을 하는 문제점에 대해 당신은 어떻게 해결 할 건가요?
* 당신은 가장 최근의 프로젝트를 어떻게 관리하셨나요?
* "*Individuals and interactions over processes and tools*" and "*Customer collaboration over contract negotiation*" comprise half of the values of the Agile Manifesto. Discuss
* Tell me what decisions would you take if you could be the CTO of your Company.
* 프로그램 매니저(Program Managers)는 유용한가요?
* Organize a development team using flexible schedules (that is, no imposed working hours) and "Take as you need" vacation policy
* How would you manage a very high turn over and convince developers not to leave the team, without increasing compensation? What could a Company improve to make them stay?
* What are the top 3 qualities you look for in colleagues, beyond their code?
* What are the top 3 things you wish non-technical people knew about code?
* Imagine your company gives you 1 month and some budget to improve your and your colleagues' daily life. What would you do?


### [[↑]](#toc) <a name='algorithms'>알고리즘:</a>

* 스택(LIFO Stacks)들로 큐(FIFO Queue)를 구성해보세요. 그리고 큐(FIFO Queue)들을 사용해서 스택(LIFO Stacks)을 구성해보세요.
* Stack Overflow의 영향을 받는 코드를 작성해보세요.
* Write a tail-recursive version of the factorial function
* Using your preferred language, write a REPL that echoes your inputs. Evolve it to make it an RPN calculator.
* How would you design a "defragger" utility?
* Write a program that builds random mazes.
* 메모리 누수를 발생시키는 예제코드를 작성해 보세요.
* Generate a sequence of unique random numbers
* 간단한 Garbage collection system을 작성해보세요.
* 당신이 좋아하는 언어를 사용해서 기초적인 메세지 브로커를 작성해보세요.
* 기초적인 Web Server를 작성해주세요. 그리고 앞으로의 Web Server가 필요한 기능들에 대한 Road Map을 그려주세요.
* 10GB 크기의 파일을 어떻게 정렬 하실 건가요? 10TB의 크기로 변경된다면 당신은 문제 해결 방법을 어떻게 접근하실건가요?
* How would you programmatically detect file duplicates?


### [[↑]](#toc) <a name='architecture'>소프트웨어 아키텍처:</a>

* 언제 캐시전략이 유용하지 않고 심지어 위험스러운 상황까지 오게 될까요?
* 이벤트 기반 아키텍쳐(Event-Driven Architecture)를 통해 확장성이 향상되는 이유는 무엇일까요?
* 어떻게 하면 코드를 읽기 쉽게 만들 수 있을까요?
* What is the difference between emergent design and evolutionary architecture?
* Scale out과 scale up의 차이점을 알고 계신가요? 어떤 상황에 적용해야할까요?
* user 세션(sessions)의 장애를 어떻게 처리하실건가요?
* CQRS (Command Query Responsibility Segregation)이란 무엇일까요? 기존의 Command-Query Separation 원리랑 어떤 차이를 가질까요?
* The so called "multitier architecture" is an approach to design a client–server system aimed to keep physically and logically separated presentation, application processing, data management and other functions. The most widespread of the multitier architectures is the three-tier architecture. Would you discuss the pros and cons of such approach?
* 당신은 소프트웨어 시스템의 확장성(scalability)을 어떻게 고려해서 디자인 하나요?
* Someone gave the name "The "C10k problem" to the problem of optimising network sockets to handle over 10.000 open connections at once. While handling 10.000 concurrent clients is not the same as handling 10.000 open connection, the context is similar. It's a tough challenge anyway, and no one is expected to know every single detail to solve it. It may be interesting to discuss the strategies you know to deal with that problem. Would you like to try?
* How would you design a decentralized (that is, with no central server) P2P system?
* You may recall that Common Gateway Interface (CGI) is a standard protocol for web servers to execute programs (CGI scripts) that execute as Command-line programs on a server, and that dynamically generate HTML pages when invoked by a HTTP request. Perl and PHP used to be common languages for such scripts. In CGI, a HTTP request generally causes the invocation of a new process on the server, but FastCGI, SCGI and other approaches improved the mechanism, raising the performance, with techniques such as preforking processes. Can you imagine why has't CGI eventually win, and was instead replaced with other architectural approaches?
* How would you defend the design of your systems against Vendor Lock-in?
* 규모에 따른 Publish-Subscribe 패턴의 단점들은 무엇일까요?
* 80년대 이후 CPU에 나타난 새로운 특징은 무엇이며, 이는 프로그래밍에 어떠한 영향을 줬나요?
* In which part of the lifecycle of a software performance should be taken in consideration, and how?
* How could a Denial of Service arise not maliciously but for a design or architectural problem?
* 성능(Performance)과 확장성(Scalability)의 관계는 어떠할까요?
* 어떤 상황에 높은 결합도가 괜찮을까요?
* What characteristic should a system have to be Cloud Ready?
* Does unity of design imply an aristocracy of architects? Putting it simple: can good design emerge from a collective effort of all developers?
* What's the difference between design, architecture, functionality and aesthetic? Discuss.



### [[↑]](#toc) <a name='soa'>Service Oriented Architecture and Microservices:</a>
* Why, in a SOA, long-lived transactions are discouraged and Sagas are suggested instead?
* Soa와 Microservices는 어떤 차이점을 가지고 있나요?
* Let's talk about web services versioning, version compatibility and breaking changes.
* What's the difference between a transaction and a compensation operation in a saga, in SOA?
* 언제 Microservice는 지나치게 작다고 느껴질까요?
* MicroService architecture의 장단점에 대해 설명해주세요.


### [[↑]](#toc) <a name='security'>보안:</a>
* How do you write secure code? In your opinion, is it one of the developer's duties, or does it require a specialized role in the company? And why?
* Why is it said that cryptography is not something you should try to invent or design yourself?
* What is two factor authentication? How would you implement it in an existing web application?
* If not carefully handled, there is always a risk of logs containing sensitive information, such as passwords. How would you deal with this?
* Write down a snippet of code affected by SQL Injection and fix it.
* How would it be possible to detect SQL Injection via static code analysis? I don't expect you to write an algorithm capable of doing this, as it is probably a huge topic, but let's discuss a general approach.
* 크로스 사이트 스크립팅 공격법에 대해서 무엇을 알고 있나요? 기억이 나지 않는다면 온라인으로 정의를 확인하고 얘기해보도록 하죠.
* What do you know about Cross-Site Forgery Attack? If you don't remember it, let's review online its definition and let's discuss about it.
* HTTPS는 어떻게 동작하는지 아시나요?
* 중간자 공격(Man-in-the-middle attack)이 무엇이며, 왜 HTTPS가 이를 막아주는지 설명해줄 수 있나요?
* How can you prevent the user's session from being stolen? Chances are you remember what Session or Cookie Hijacking is, otherwise let's read its Wikipedia page together.


### [[↑]](#toc) <a name='general'>일반적인 질문:</a>

* 왜 함수형 프로그래밍(Functional programming)이 중요해졌을까요? 언제 함수형 프로그래밍을 사용하는게 좋을까요?
* Microsoft, Google, Opera 그리고 Mozilla와 같은 회사들은 무엇을 얻기 위해 그들의 브라우저를 만들었을까요?
* 왜 TCP 소켓을 여는데 많은 Overhead가 필요할까요?
* 캡슐화는 무엇을 얻기 위해 중요할까요?
* Real-Time 시스템은 무엇이며 일반 시스템과 어떻게 다를까요?
* What's the relationship between real-time languages and heap memory allocation?
* Immutability is the practice of setting values once, at the moment of their creation, and never changing them. How can immutability help write safer code?
* Mutable 그리고 immutable value의 장단점들은 무엇일까요?
* What's the Object-Relational impedance mismatch?
* 캐시크기를 결정하기 위해 적용하는 원칙은 무엇일까요?
* TCP와 HTTP의 차이점은 무엇일까요?
* 클라이언트 기반 렌더링과 서버 기반 렌더링의 차이점은 무엇인가요?
* 비안정적인 커뮤니케이션 프로토콜에 기반한 안정적인 커뮤니케이션 프로토콜을 만들려면 어떻게 해야할까요?
* [Tony Hoare](https://en.m.wikipedia.org/wiki/Tony_Hoare) who invented the null reference once said "*I call it my billion-dollar mistake*" since it lead to "*innumerable errors, vulnerabilities, and system crashes, which have probably caused a billion dollars of pain and damage in the last forty years*". Imagine you want to remove the possibility to have null references in your preferred language: how would you achieve this goal? What consequences could this have?


### [[↑]](#toc) <a name='open'>Open Questions:</a>
* 왜 사람들은 변화하는 것을 주저할까요?
* 할아버지 할머니에게 설명하는 것처럼 Thread를 설명해 보세요.
* 당신은 소프트웨어 공학자로서 변화와 예측 가능성을 동시에 얻고자 합니다. 어떻게 하나의 전략으로 이 두 가지 토끼를 모두 잡을 수 있을까요?
* 어떠한 것이 좋은 코드를 만들까요?
* 스트리밍에 대해서 설명하고, 어떻게 구현하는지에 대해서 말해보세요.
* Say your Company gives you one week you can use to improve your and your colleagues' lifes: how would you use that week?
* 당신은 이번 주에는 어떤 것을 배웠나요?
* 모든 디자인에 어울리는 미적으로 아름다운 요소가 있다고 생각해보세요. 이 요소는 당신에게 득이될까요 해가될까요?(is this aesthetic element your friend or your enemy?)
* 최근 읽었던 5권을 설명해주세요.
* How would you introduce Continuous Delivery in a successful, huge company for which the change from Waterfall to Continuous Delivery would be not trivial, because of the size and complexity of the business?
* When does it make sense to reinvent the wheel?
* Let's have a conversation about "*Reinventing the wheel*", the "*Not Invented Here Syndrome*" and the "*Eating Your Own Food*" practice
* What's the next thing you would automate in your current workflow?
* 왜 소프트웨어를 작성(개발)하는 것은 어려울까요? 무엇이 소프트웨어의 유지보수를 어렵게 만들까요?
* Would you prefer working on Green Field or Brown Field projects? Why?
* [브라우저에 google.com을 입력하면 어떤 일이 벌어질까요?](https://github.com/alex/what-happens-when)
* What does an Operating System do when it has got no custom code to run, and therefore it looks idle? I would like to start a discussions about interrupts, daemons, background services, polling, event handling and so on.
* Explain Unicode/Database Transactions to a 5 year old child.
* 모노리틱 아키텍쳐(Monolithic architecture)을 설명해주세요.
* 전문적인 개발자라는 사람은 어떤 의미일까요?
* Is developing software an art, a craftsmanship or an engineering endeavour? Your opinion.
* "이 상품을 좋아하는 사람들은 이런 상품도 좋아했습니다"와 같은 기능을 소셜 커머스 샵에서 어떻게 구현할 수 있을까요?
* 왜 대기업들은 스타트업보다 혁신하는 속도가 느릴까요?
* 최근에 이룬 일 중 가장 자랑스러웠던 일이 무엇인가요?



### [[↑]](#toc) <a name='snippets'>Questions about snippets of code:</a>
* 이 Javascript의 함수의 출력값은 무엇일까요?
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

* 타입을 지우게 되면 Java코드의 결과물은 어떻게 나올까요? 왜 그럴까요?
```java
ArrayList<Integer> li = new ArrayList<Integer>();
ArrayList<Float> lf = new ArrayList<Float>();
if (li.getClass() == lf.getClass()) // evaluates to true
  System.out.println("Equal");
```


* 메모리 누수가 발생하는 부분을 찾을 수 있으신가요?
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

* `if`문은 일반적으로 절차적이고 명령적인 프로그래밍으로 진행되게 만듭니다. `switch`를 제거하고 보다 객체지향적인 코드로 만들 수 있나요?

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


* `if`문을 제거하고 보다 아래의 코드를 보다 더 객체지향적으로 바꿀 수 있나요?

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

        if ((executionId.equals("")) || (rewrittenUrl.equals(""))) {
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

* 아래의 코드를 리팩토링 해보세요.

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

### [[↑]](#toc) <a name='billgates'>빌 게이츠 스타일의 질문:</a>
This section collects some weird questions along the lines of the [Manhole Cover Question](https://en.wikipedia.org/wiki/Microsoft_interview#Manhole_cover_question).

* What would happen if you put a mirror in a scanner?
* Imagine there's a perfect clone of yourself. Imagine that that clone is your boss. Would you like to work for him/her?
* 저를 인터뷰 해주세요.
* Why are Quora's answers better than Yahoo Answers' ones?
* Let's play a game: defend Cobol against modern languages, and try to find as many reasonable arguments as you can.
* 당신은 10년 후에 어떤 모습이 되어있을까요?
* 당신이 나의 보스이며, 나를 해고했다고 가정해봅시다. 나에게 해고 통지를 해보세요.
* I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles.
* Your boss asks you to lie to the Company. What's your reaction?
* If you could travel back in time, which advice would you give to your younger self?

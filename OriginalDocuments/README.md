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
* The Law of Demeter (the Principle of Least Knowledge) states that each unit should have only limited knowledge about other units and it should only talk to its immediate friends (sometimes stated as "Don't talk to strangers"). Would you write code violating this principle, show why it is a bad design and then fix it?
* Active-Record is the design pattern that promotes objects to include functions such as Insert, Update, and Delete, and properties that correspond to the columns in some underlying database table. In your opinion and experience, which are the limits and pitfalls of the this pattern?
* Data-Mapper is a design pattern that promotes the use of a layer of Mappers that moves data between objects and a database while keeping them independent of each other and the mapper itself. On the contrary, in Active-Record objects directly incorporate operations for persisting themselves to a database, and properties corresponding to the underlying database tables. Do you have an opinion on those patterns? When would you use one against the other?
* Why it is often said that the introduction of `null` is a "Billion dollar mistake"? Would you discuss the techniques to avoid it, such as the Null Object Pattern introduced by the GOF book, or Option types?
* Many state that, in Object-Oriented Programming, Composition is often a better option than Inheritance. What's you opinion?
* What is an Anti-corruption Layer?
* Singleton is a design pattern that restricts the instantiation of a class to one single object. Writing a Thread-Safe Singleton class is not so obvious. Would you try?
* The ability to change implementation without affecting clients is called Data Abstraction. Produce and example violating this property, then fix it.
* Write a snippet of code violating the Don't Repeat Yourself (DRY) principle. Then, fix it.
* How would you deal with Dependency Hell?
* Is goto evil? You may have heard of the famous paper "Go To Statement Considered Harmful" by Edsger Dijkstra, in which he criticized the use of the `goto` statement and advocated structured programming instead. The use of `goto` has always been controversial, so much that even Dijkstra's letter was criticized with articles such as "'GOTO Considered Harmful' Considered Harmful". What's your opinion on the use of `goto`?
* The robustness principle is a general design guideline for software that recommends "*Be conservative in what you send, be liberal in what you accept*". It is often reworded as "*Be a tolerant reader and a careful writer*". Would you like to discuss the rationale of this principle?
* Separation of Concerns is a design principle for separating a computer program into distinct areas, each of ones addressing a separate concern. There are a lot of different mechanisms for achieving Separation of Concerns (use of objects, functions, modules, or patterns such as MVC and the like). Would you discuss this topic?


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

* How would you migrate an application from a database to another, for example from MySQL to PostgreSQL? If you had to manage that project, which issues would you expect to face?
* Why databases treat null as a so special case? For example, why in SQL ```SELECT * FROM table WHERE field = null``` does not match records with null ``field``?
* ACID is an acronym that refers to Atomicity, Consistency, Isolation and Durability, 4 properties guaranteed by a database transaction in most of the database engines. What do you know about this topic? Would you like to elaborate?
* How would you manage database schema migrations, that is, how would you automate the changes a database schema is affected to, as the application evolve, version after version?
* How is Lazy Loading achieved? When is it useful? What are its pitfalls?
* The so called "N + 1 problem" is an issue that occurs when the code needs to load the children of a parent-child relationship with a ORMs that have lazy-loading enabled, and that therefore issue a query for the parent record, and then one query for each child record. How to fix it?
* How would you find the most expensive queries in an application?
* In your opinion, is it always needed to use database normalization? When is it advisable to use denormalized databases?
* Of of the Continuous Integration's techniques is called Blue-Green Deployment: it consists in having two production environments, as identical as possible, and in performing the deployment in one of them while the other one is still operating, and than in safely switching the traffic to the second one after some convenient testing. This technique becomes more complicated when the deployment includes changes to the database structure or content. I'd like to discuss this topic with you.


### [[↑]](#toc) <a name='nosql'>NoSQL:</a>

* What is Eventual Consistency?
* The Brewer's Theorem, most commonly known as the CAP theorem, states that in the presence of a Network Partition (the P in CAP), a system's designer has to choose between Consistency (the C in CAP) and Availability (the A in CAP). Can you think about examples of CP, AP and CA systems?
* How would you explain the recent rise in interest for NoSQL?
* How does NoSQL tackle scalability challenges?
* In which case would you use a document database like MongoDB instead of a relational database like MySQL or PostgreSQL?


### [[↑]](#toc) <a name='codeversioning'>버전관리:</a>

* Why is branching with Mercurial or git easier than with SVN?
* What are the pros and cons of Distributed Version Control Systems like Git over Centralized ones like SVN?
* Could you describe GitHub Flow and GitFlow workflows?
* What's a rebase?
* Why merges are easier with Mercurial and git than with SVN and CVS?


### [[↑]](#toc) <a name='concurrency'>동시성(Concurrency):</a>

* Why do we need Concurrency, anyway? Explain.
* Why is testing multithreading / concurrent code so difficult?
* What is a Race Condition? Code an example, using whatever language you like.
* What is a Deadlock? Would you be able to write some code that is affected by deadlocks?
* What is Process Starvation? If you need, let's review its definition.
* What is a Wait Free algorithm?


### [[↑]](#toc) <a name='distributed'>분산 시스템:</a>

* How to test a distributed system?
* In which case would you apply asynchronously communication between two systems?
* What are the general pitfalls of Remote Procedure Call?
* If you are building a distributed system for scalability and robustness, what are the different things you'd think of in the case you are working in a closed and secure network environment or in geographically distributed and public system?
* How to manage Fault Tolerance in a Web application? And in a Desktop one?
* How to deal with failures in Distributed Systems?
* Let's talk about the several approaches to Reconciliation after network partitions
* What are the Fallacies of Distributed Computing?
* When would you use Request/Reply and when Publish/Subscribe?
* Suppose the system you are working on does not support transactionality. How would you implement it from scratch?


### [[↑]](#toc) <a name='management'>소프트웨어 생명주기와 팀 관리:</a>

* What is agility?
* How would you deal with Legacy Code?
* Say I'm your Project Manager, and I'm no expert in programming. Would you try explaining me what Legacy Code is and why should I care about code quality?
* I'm the CEO of your company. Explain to me Kanban and convince me to invest in it.
* What is the biggest difference between Agile and Waterfall?
* Being a team manager, how would you deal with the problem of having too many meetings?
* How would you manage a very late project?
* "*Individuals and interactions over processes and tools*" and "*Customer collaboration over contract negotiation*" comprise half of the values of the Agile Manifesto. Discuss
* Tell me what decisions would you take if you could be the CTO of your Company.
* Are Program Managers useful?
* Organize a development team using flexible schedules (that is, no imposed working hours) and "Take as you need" vacation policy
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

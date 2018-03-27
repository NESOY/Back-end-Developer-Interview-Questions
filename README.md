Back-End 개발자 인터뷰 질문
======================================
## 인터뷰 관련 정보
#### Back-End 인터뷰
- [영어](https://github.com/arialdomartini/Back-End-Developer-Interview-Questions) by [@arialdomartini](https://github.com/arialdomartini).
- [중국어](https://github.com/monklof/Back-End-Developer-Interview-Questions) by [@monklof](https://github.com/monklof).

#### Front-end 인터뷰
- [영어](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions) by [@darcyclarke](https://github.com/darcyclarke)
- [한국어](https://github.com/h5bp/Front-end-Developer-Interview-Questions/tree/master/Translations/Korean)

#### 한국 취업 정보.
- [Interview_Question_for_Beginner](https://github.com/JaeYeopHan/Interview_Question_for_Beginner) by [@JBee](https://github.com/JaeYeopHan)
- [junior-recruit-scheduler](https://github.com/jojoldu/junior-recruit-scheduler) by [@jojoldu](https://github.com/jojoldu)
- [developer-roadmap](https://github.com/kamranahmedse/developer-roadmap) by [@kamranahmedse](https://github.com/kamranahmedse/)

## 공지
대부분의 질문은 자유롭게 답할 수 있으며 그 중에는 *옳은 답*과 *틀린 답*이 없는 질문들이 있습니다. 반대로, 그들은 올바른 정답보단 지원자의 능력에 대해 더 많이 말해 줄 수 있기를 바라면서 대화의 시작점으로 출발하기를 바라고 있습니다. 개인적으로, 나는 명확한 답이 없는 질문들을 선택할 것입니다.

다시 한번 말하지만, 나는 단지 질문들을 물어보는 것만으로 충분하지 않다는 것을 강조합니다. 지원자와 짝 프로그래밍을 진행하면서 인터뷰를 본다면 완벽할 것입니다: 이런 인터뷰 방식은 서로의 스타일을 알 수 있는 최고의 방법이고 지원자는 미래에 자신의 작업에 대해 더 잘 알 수 있을 것입니다.

이 프로젝트는 [@darcyclarke](https://github.com/darcyclarke)님이 작성하신 [Front-end Job Interview Questions](https://github.com/darcyclarke/Front-end-Developer-Interview-Questions)에 영감을 받았습니다.

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
  1. [Questions based on snippets of code](#snippets)
  1. [빌 게이츠 스타일의 질문](#billgates)



### [[↑]](#toc) <a name='patterns'>디자인 패턴:</a>

* 왜 global 객체와 static 객체는 나쁜 것일까요? code를 통한 예시로 설명할 수 있나요?
* 제어의 역전(Inversion of Control)에 대한 개념과 IoC가 코드의 디자인을 어떻게 향상시키는지 설명해 주세요.
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


### [[↑]](#toc) <a name='design'>코드 디자인:</a>

* It is often heard that one of the most important goals in Object-Oriented Design (and code design in general) is to have High Cohesion and Loose Coupling. What does it mean? Why is it that important and how is it achieved?
* 대부분의 언어에서 배열의 시작은 왜 0부터 일까요?
* How do tests and TDD influence code design?
* Write a snippet of code violating the Don't Repeat Yourself (DRY) principle. Then, explain why is it a bad design, and fix it.
* 응집도와 결합도의 차이점은 뭘까요?
* 리팩토링(refactoring)은 언제 유용한가요?
* Are comments in code useful? Some say they should be avoided as much as possible, and hopefully made unnecessary. Do you agree?
* 디자인과 아키텍처의 차이점은 무엇일까요?
* 왜 TDD에서는 코드를 작성하기 전에 테스트 코드를 작성할까요?
* C++ supports multiple inheritance, and Java allows a class to implement multiple interfaces. What impact does using these facilities have on orthogonality? Is there a difference in impact between using multiple inheritance and multiple interfaces? Is there a difference between using delegation and using inheritance? [This question is from The Pragmatic Programmer, by Andrew Hunt and David Thomas]
* Pros and cons of holding domain logic in Stored Procedures.
* In your opinion, why have Object-Oriented Design dominated the market for so many years?
* What would you do to understand if your code has a bad design?


### [[↑]](#toc) <a name='languages'>프로그래밍 언어:</a>

* Tell me the 3 worse defects of your preferred language
* 왜 함수 프로그래밍(Functional Programming)이 떠오르고 있는지 설명할 수 있나요?
* 클로져란 무엇일까요? 그리고 어떤 상황에서 유용할까요? 클로져와 클래스간의 공통점은 무엇이 있을까요?
* What are generics useful for?
* What are high-order functions? What are they useful for? Write one, in your preferred language.
* Write a loop, then transform it into a recursive function, using only immutable structures (i.e. avoid using variables). Discuss.
* What does it mean when a language treats functions as first-class citizens?
* 익명 함수(Anonymous Function) 장점이 나타나는 예제를 보여주세요.
* There are a lot of different type systems: let's talk about static and dynamic type systems, and about strong and weak ones. You surely have an opinion and a preference about this topic. Would you like to share them, and discuss why and when would you promote one particular type system for developing an enterprise software?
* What are namespaces useful for? Invent an alternative.
* Talk about Interoperability between Java and C# (in alternative, choose 2 other arbitrary languages)
* Why do many software engineers not like Java?
* What makes a good language good and a bad language bad?
* Write two functions, one Referentially Transparent and the other one Referentially Opaque. Discuss.
* Whats the Stack and what's the Heap? What's a Stack Overflow?
* Why is it important that in a language functions are first class citizens?
* Some languages, especially the ones that promote a Functional approach, allow a technique called Pattern Matching. Do you know it? How is Pattern Matching different from Switch clauses?
* Why do some languages have no exceptions by design? What are the pros and cons?
* If `Cat` is an `Animal`, is `TakeCare<Cat>` a `TakeCare<Animal>`?
* Why in Java, C# and many other languages constructors are not part of the interface?
* In the last years there has been a lot of hype on Node. What's your opinion on the use in the back end of a language that was initially conceived to run in the browser?
* Pretend you have a time machine and pretend that you have the opportunity to go to a particular point in time during Java's (or C#, Python, Go or whatever) history, and talk with some of the JDK architects. What would you try to convince them of? Removing checked exceptions? Adding unsigned primitives? Adding multiple-inheritance?



### [[↑]](#toc) <a name='web'>Web:</a>
* 왜 first-party 쿠키들과 third-party 쿠키들을 다르게 다룰까요?
* 웹 서비스 API(Web Services API) 버젼을 어떻게 관리하실 건가요?
* Back-End 관점에서, Single Page Application의 단점은 무엇이 있을까요?
* 왜 우리는 stateless service를 사용하기 위해 많은 노력을 할까요? stateless code가 가져다 주는 장점들과 statefullness code가 가져다 주는 단점들에 대해 설명해 주세요.
* REST and SOAP: when would you choose one, and when the other?
* In Web development, Model-View Controller and Model-View-View-Model approaches are very common, both in the Back End and in the Front End. What are they, and why are they advisable?


### [[↑]](#toc) <a name='databases'>데이터 베이스:</a>

* How would you migrate an application from a database to another, for example from MySQL to PostgreSQL? If you had to manage that project, which issues would you expect to face?
* Why databases treat null as a so special case? For example, why in SQL ```SELECT * FROM table WHERE field = null``` does not match records with null ``field``?
* ACID is an acronym that refers to Atomicity, Consistency, Isolation and Durability, 4 properties guaranteed by a database transaction in most of the database engines. What do you know about this topic? Would you like to elaborate?
* How would you manage database schema migrations, that is, how would you automate the changes a database schema is affected to, as the application evolve, version after version?
* 어떻게 구현하면 Lazy Loading을 얻을 수 있을까요? 언제 유용할까요? Lazy Loading에 대해 함정은 없을까요?
* The so called "N + 1 problem" is an issue that occurs when the code needs to load the children of a parent-child relationship with a ORMs that have lazy-loading enabled, and that therefore issue a query for the parent record, and then one query for each child record. How to fix it?
* How would you find the most expensive queries in an application?
* In your opinion, is it always needed to use database normalization? When is it advisable to use denormalized databases?
* Of of the Continuous Integration's techniques is called Blue-Green Deployment: it consists in having two production environments, as identical as possible, and in performing the deployment in one of them while the other one is still operating, and than in safely switching the traffic to the second one after some convenient testing. This technique becomes more complicated when the deployment includes changes to the database structure or content. I'd like to discuss this topic with you.


### [[↑]](#toc) <a name='nosql'>NoSQL:</a>

* What is Eventual Consistency?
* The Brewer's Theorem, most commonly known as the CAP theorem, states that in the presence of a Network Partition (the P in CAP), a system's designer has to choose between Consistency (the C in CAP) and Availability (the A in CAP). Can you think about examples of CP, AP and CA systems?
* 최근에 NoSQL의 인기가 상승하고 있는 이유에 대해 설명할 수 있나요?
* How does NoSQL tackle scalability challenges?
* In which case would you use a document database like MongoDB instead of a relational database like MySQL or PostgreSQL?


### [[↑]](#toc) <a name='codeversioning'>Code versioning:</a>

* Why is branching with Mercurial or git easier than with SVN?
* What are the pros and cons of Distributed Version Control Systems like Git over Centralized ones like SVN?
* Could you describe GitHub Flow and GitFlow workflows?
* 리베이스(rebase)가 무엇일까요?
* Why merges are easier with Mercurial and git than with SVN and CVS?


### [[↑]](#toc) <a name='concurrency'>Questions about Concurrency:</a>

* 왜 우리는 병행성(Concurrency)이 필요할까요? 항상 그럴까요? 설명해보세요.
* Multithreading / concurrent code를 테스트한다는 건 왜 어려울까요?
* Race Condition이란 무엇일까요? 잘하는 언어를 사용하여 코드로 예제를 보여주세요.
* What is a Deadlock? Would you be able to write some code that is affected by deadlocks?
* What is Process Starvation? If you need, let's review its definition.
* What is a Wait Free algorithm?


### [[↑]](#toc) <a name='distributed'>분산 시스템:</a>

* 분산 시스템은 어떻게 테스트를 진행할까요?
* In which case would you apply asynchronously communication between two systems?
* What are the general pitfalls of Remote Procedure Call?
* If you are building a distributed system for scalability and robustness, what are the different things you'd think of in the case you are working in a closed and secure network environment or in geographically distributed and public system?
* How to manage Fault Tolerance in a Web application? And in a Desktop one?
* How to deal with failures in Distributed Systems?
* Let's talk about the several approaches to Reconciliation after network partitions
* What are the Fallacies of Distributed Computing?
* When would you use Request/Reply and when Publish/Subscribe?
* Suppose the system you are working on does not support transactionality. How would you implement it from scratch?


### [[↑]](#toc) <a name='management'>Software Lifecycle and Team Management:</a>

* agility란 무엇일까요?
* 당신은 레거시 코드(Legacy Code)를 어떻게 다루실 건가요?
* Say I'm your Project Manager, and I'm no expert in programming. Would you try explaining me what Legacy Code is and why should I care about code quality?
* I'm the CEO of your company. Explain to me Kanban and convince me to invest in it.
* What is the biggest difference between Agile and Waterfall?
* Being a team manager, how would you deal with the problem of having too many meetings?
* How would you manage a very late project?
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
* Write a snippet of code affected by a Stack Overflow
* Write a tail-recursive version of the factorial function
* Using your preferred language, write a REPL that echoes your inputs. Evolve it to make it an RPN calculator.
* How would you design a "defragger" utility?
* Write a program that builds random mazes.
* 메모리 누수를 발생시키는 예제코드를 작성해 보세요.
* Generate a sequence of unique random numbers
* 간단한 Garbage collection system을 작성해보세요.
* 당신이 좋아하는 언어를 사용해서 기초적인 메세지 브로커를 작성해보세요.
* Write a very basic web server. Draw a road map for features to be implemented in the future.
* 10GB 크기의 파일을 어떻게 정렬 하실 건가요? 10TB의 크기로 변경된다면 당신은 문제 해결 방법을 어떻게 접근하실건가요?
* How would you programmatically detect file duplicates?


### [[↑]](#toc) <a name='architecture'>소프트웨어 아키텍처:</a>

* 언제 캐시전략이 유용하지 않고 심지어 위험스러운 상황까지 오게 될까요?
* Why does Event-Driven Architecture improve scalability?
* 어떻게 하면 코드를 읽기 쉽게 만들 수 있을까요?
* What is the difference between emergent design and evolutionary architecture?
* Scale out vs scale up: how are they different? When to apply one, when the other?
* How to deal with failover and user sessions?
* What is CQRS (Command Query Responsibility Segregation)? How is it different from the oldest Command-Query Separation Principle?
* The so called "multitier architecture" is an approach to design a client–server system aimed to keep physically and logically separated presentation, application processing, data management and other functions. The most widespread of the multitier architectures is the three-tier architecture. Would you discuss the pros and cons of such approach?
* 당신은 소프트웨어 시스템의 확장성(scalability)을 어떻게 고려해서 디자인 하나요?
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



### [[↑]](#toc) <a name='soa'>Service Oriented Architecture and Microservices:</a>
* Why, in a SOA, long-lived transactions are discouraged and Sagas are suggested instead?
* What are the differences between Soa and Microservices?
* Let's talk about web services versioning, version compatibility and breaking changes.
* What's the difference between a transaction and a compensation operation in a saga, in SOA?
* 언제 Microservice는 지나치게 작다고 느껴질까요?
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
* HTTPS는 어떻게 동작하는지 아시나요?
* What's a Man-in-the-middle Attack, and why does HTTPS help protect against it?
* How can you prevent the user's session from being stolen? Chances are you remember what Session or Cookie Hijacking is, otherwise let's read its Wikipedia page together.


### [[↑]](#toc) <a name='general'>일반적인 질문:</a>

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
* TCP와 HTTP의 차이점은 무엇일까요?
* What are the tradeoffs of client-side rendering vs. server-side rendering?
* How could you develop a reliable communication protocol based on a non-reliable one?
* [Tony Hoare](https://en.m.wikipedia.org/wiki/Tony_Hoare) who invented the null reference once said "*I call it my billion-dollar mistake*" since it lead to "*innumerable errors, vulnerabilities, and system crashes, which have probably caused a billion dollars of pain and damage in the last forty years*". Imagine you want to remove the possibility to have null references in your preferred language: how would you achieve this goal? What consequences could this have?


### [[↑]](#toc) <a name='open'>Open Questions:</a>
* 왜 사람들은 변화하는 것을 주저할까요?
* 할아버지 할머니에게 설명하는 것처럼 Thread를 설명해 보세요.
* As a software engineer you want both to innovate and to be predictable. How those 2 goals can coexist in the same strategy?
* What makes good code good?
* Explain streaming and how you would implement it.
* Say your Company gives you one week you can use to improve your and your colleagues' lifes: how would you use that week?
* 당신은 이번 주에는 어떤 것을 배웠나요?
* There is an aesthetic element to all design. The question is, is this aesthetic element your friend or your enemy?
* 최근 읽었던 5권을 설명해주세요.
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

        if ((executionId == "") || (rewrittenUrl == "")) {
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
* You are my boss and I'm fired. Inform me.
* I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles.
* Your boss asks you to lie to the Company. What's your reaction?
* If you could travel back in time, which advice would you give to your younger self?

### [[↑]](#toc) <a name='architecture'>소프트웨어 아키텍처:</a>

* 언제 캐시전략이 유용하지 않고 심지어 위험스러운 상황까지 오게 될까요?
* ~~이벤트 기반 아키텍쳐(Event-Driven Architecture)를 통해 확장성이 향상되는 이유는 무엇일까요?~~
* 어떻게 하면 코드를 읽기 쉽게 만들 수 있을까요?
* emergent design과 evolutionary architecture의 차이점은 무엇일까요?
* Scale out과 scale up의 차이점을 알고 계신가요? 어떤 상황에 적용해야할까요?
* user 세션(sessions)의 장애를 어떻게 처리하실건가요?
* CQRS (Command Query Responsibility Segregation)이란 무엇일까요? 기존의 Command-Query Separation 원리랑 어떤 차이를 가질까요?
* The so called "multitier architecture" is an approach to design a client–server system aimed to keep physically and logically separated presentation, application processing, data management and other functions. The most widespread of the multitier architectures is the three-tier architecture. Would you discuss the pros and cons of such approach?
* 당신은 소프트웨어 시스템의 확장성(scalability)을 어떻게 고려해서 디자인 하나요?
* Someone gave the name "The "C10k problem" to the problem of optimising network sockets to handle over 10.000 open connections at once. While handling 10.000 concurrent clients is not the same as handling 10.000 open connection, the context is similar. It's a tough challenge anyway, and no one is expected to know every single detail to solve it. It may be interesting to discuss the strategies you know to deal with that problem. Would you like to try?
* 분산화된 P2P System을 어떻게 디자인 하실 건가요?
* You may recall that Common Gateway Interface (CGI) is a standard protocol for web servers to execute programs (CGI scripts) that execute as Command-line programs on a server, and that dynamically generate HTML pages when invoked by a HTTP request. Perl and PHP used to be common languages for such scripts. In CGI, a HTTP request generally causes the invocation of a new process on the server, but FastCGI, SCGI and other approaches improved the mechanism, raising the performance, with techniques such as preforking processes. Can you imagine why has't CGI eventually win, and was instead replaced with other architectural approaches?
* How would you defend the design of your systems against Vendor Lock-in?
* 규모에 따른 Publish-Subscribe 패턴의 단점들은 무엇일까요?
* What's new in CPUs since the 80s, and how does it affect programming?
* In which part of the lifecycle of a software performance should be taken in consideration, and how?
* How could a Denial of Service arise not maliciously but for a design or architectural problem?
* 성능(Performance)과 확장성(Scalability)의 관계는 어떠할까요?
* 어떤 상황에 높은 결합도가 괜찮을까요?
* What characteristic should a system have to be Cloud Ready?
* Does unity of design imply an aristocracy of architects? Putting it simple: can good design emerge from a collective effort of all developers?
* What's the difference between design, architecture, functionality and aesthetic? Discuss.

### [[↑]](#toc) <a name='microservice'>Microservices:</a>

* SOA 관점에서 Long-Lived 트랜잭션은 되도록 사용하지 않고. 대신하여 Saga 패턴이 제안될까요?
* Soa와 Microservices는 어떤 차이점을 가지고 있나요?
* 웹 서비스 버젼 관리, 버젼 호환성 및 변경 사항을 어떻게 관리할까요?
* SOA에서 transaction과 compensation operation의 차이점이 무엇일까요?
* 언제 Microservice는 지나치게 작다고 느껴질까요?
* MicroService architecture의 장단점에 대해 설명해주세요.
* ~~모노리틱 아키텍쳐(Monolithic architecture)을 설명해주세요.~~
* Circuit Breaker Pattern이란 무엇일까요? 이 패턴이 왜 필요할까요?


### [[↑]](#toc) <a name='distributed'>분산 시스템:</a>

* 분산 시스템은 어떻게 테스트를 진행할까요?
* 어떤 상황에서 두 시스템 간의 비동기 커뮤니케이션(asynchronously communication)을 적용할 것인가요?
* 원격 프로시저 호출(Remote Procedure Call)의 일반적인 문제점은 무엇일까요?
* If you are building a distributed system for scalability and robustness, what are the different things you'd think of in the case you are working in a closed and secure network environment or in geographically distributed and public system?
* 웹 어플리케이션은 장애를 어떻게 관리하고 견뎌낼까요?
* 분산시스템의 장애는 어떻게 해결하실 건가요?
* Let's talk about the several approaches to Reconciliation after network partitions
* 분산 컴퓨팅의 단점은 무엇일까요?
* 당신은 언제 Request/Reply를 사용할 것이며 또한 어떤 상황에서 Publish/Subscribe를 사용할 것인가요?
* Suppose the system you are working on does not support transactionality. How would you implement it from scratch?



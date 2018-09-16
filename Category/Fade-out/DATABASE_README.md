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

* ~~Eventual Consistency이란 무엇일까요?~~
* The Brewer's Theorem, most commonly known as the CAP theorem, states that in the presence of a Network Partition (the P in CAP), a system's designer has to choose between Consistency (the C in CAP) and Availability (the A in CAP). Can you think about examples of CP, AP and CA systems?
* 최근에 NoSQL의 인기가 상승하고 있는 이유에 대해 설명할 수 있나요?
* NoSQL은 확장 문제를 어떻게 해결할까요?
* 어떤 상황에서 MySQL이나 PostgreSQL와 같은 Relational Database보다 MongoDB와 CouchBase와 같은 Document Database를 사용하는게 좋을까요?
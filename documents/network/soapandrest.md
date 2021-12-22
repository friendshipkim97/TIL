# Network

### **SOAP(Simple Object Access Protocol)**

SOAP란 Simple Object Access Protocol의 약자로, 그 자체로 프로토콜이며, 보안이나 메세지 전송등에 있어서 REST보다 더 많은 표준들이 정해져있기 때문에 조금 더 복잡하다. 오버헤드가 심하고 개발하기 어렵고 무겁다는 단점이 있다.

### **REST(Representational State Transfer)**

REST란 Representational State Transfer의 약자로, 네트워크를 통해서 컴퓨터들끼리 통신할 수 있게 해주는 아키텍쳐 스타일이다. REST는 Resource의 Representation에 의한 상태 전달을 하고, HTTP Method를 통해 Resource를 처리하기 위한 아키텍쳐이다. 그렇다면 REST API는 무엇일까? REST API는 URI와 HTTP 프로토콜을 기반으로 한다. API는 Application Programming Interface의 약자로, 어떤 서버의 특정한 부분에 접속해서 그 안에 있는 데이터와 서비스를 이용할 수 있게 해주는 도구이다. Restful이란 REST API를 제공하는 웹 서비스를 의미한다.

-> 정리하자면, **REST란 자원(Resource)의 대표(Representation)에 의한 상태전달**이다.

-> 일반적으로, **REST라고 하면 HTTP를 통해 CRUD를 실행하는 API이다**

### **자원(Resource)의 대표란?**

자원이란 소프트웨어가 관리하는 모든 것이다, 예를 들어, 학생데이터를 대표하기 위한 이름은 students가 될 수 있다. students는 복수형을 사용한다.

### **상태 전달이란?**

상태 전달이란 데이터가 요청되어지는 시점에서 자원의 상태를 전달하는 것이다. 예를 들어 프로그램이 학생 전체 리스트를 요청받으면 요청받은 시점의 상태를 전달하는 것이다.

### **RESTful이란?**

RESTful은 REST를 REST답게 쓰기 위한 방법이다. "REST API를 RESTful하게 작성하는 것"이라고 많이들 사용하는데, 이는 이해하기 쉽게 사용하기 쉬운 REST API를 만드는 것을 의미한다. 

 **REST API 작성 가이드**
|CRUD|HTTP verbs|Route|
|------|---|---|
|resource들의 목록을 표시|GET|/resource|
|resource 하나의 내용을 표시|GET|/resource/:id|
|resource를 생성|POST|/resource|
|resource를 수정|PUT|/resource/:id|
|resource를 삭제 |	DELETE|/resource/:id|

* resource는 영어 복수형으로 작성한다.
* :id는 하나의 특정한 resource를 나타낼 수 있는 고유의 값이다. 

### **URI(Uniform Resource Identifier)란?**

인터넷 자원을 나타내는 유일한 주소이다. 

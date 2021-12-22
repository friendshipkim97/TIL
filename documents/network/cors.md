# Network

### **Origin이란?**

Origin이란 프로토콜, 도메인, 포트를 말한다. **Same-Origin이란 프로토콜, 도메인, 포트가 같다는 말이며**, **Cross-Origin이란 이 3가지 중 하나라도 다른 것**을 의미한다.

### **Origin과 Domain의 차이?**

Origin과 Domain의 차이는 프로토콜과 포트번호의 포함 여부가 다르다. Origin은 프로토콜, 도메인, 포트를 포함하며, Domain은 도메인만 포함한다.

### **CORS란?**

CORS란 Cross Origin Resource Sharing의 약자로 W3C에서 내놓은 정책이다. Cross Origin을 허용하는 메커니즘을 의미한다. 즉, CORS는 특정 헤더를 통해서 브라우저에게 Origin에서 실행되고 있는 웹 애플리케이션이 다른 출처에 원하는 리소스에 접근 할 수 있는 권한이 있는지 없는지를 알려주는 메커니즘이다.

* W3C는 월드 와이드 웹을 위한 표준을 개발하고 장려하는 조직이다.

-> HTML은 기본적으로 Cross-Origin 요청이 가능하다. HTML 요청은 기본적으로 Same-Origin 정책을 따르기 때문이다. ex) HTML의 link태그를 이용해 다른 ORIGIN의 CSS의 리소스에 접근하는 것이 가능하다.

-> script 태그 내에 있는 HTTP 요청은 기본적으로 Same-Origin 정책을 따르기 때문에 Cross-Origin 요청이 불가능하다. 보안상의 이슈때문에 Cross-Origin 요청을 불가능하게 한다.

### **CORS가 나오게 된 배경?**

초기에는 보안을 위해 Cross-Origin을 허용하지 않는 것이 좋은 방법이라고 생각했지만, 최근 대규모 웹 서비스가 늘어나며, 외부 호출에 대한 필요성이 많아지고 W3C는 안전하게 브라우저와 서버간에 교차 통신을 할 수 있도록 CORS 정책을 내놓은 것이다. 
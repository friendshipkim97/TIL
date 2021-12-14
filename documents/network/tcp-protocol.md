# Network

### **전송 계층의 기능**

전송 계층에서는 네트워크 끝단에 위치하는 통신 주체가 중간의 논리적인 선로를 통해 데이터를 주고받는다. 이 과정에서 흐름 제어, 오류 제어, 패킷의 분할과 병합 등의 기능을 수행한다. 이를 지원하기 위하여 주소 표현, 멀티 플렉싱, 연결 관리 등에 대한 고려가 이루어져야 한다.

### **연결 설정**

연결 설정은 연결을 요청하는 프로세스의 연결 설정 요구인 **Conn_Req**와 상대편 프로세스에서 연결 수락을 의미하는 **Conn_Ack**의 회신으로 완료된다. 이와 같은 2단계 설정 과정은 통신 양단의 연결 설정을 위한 최소한의 단계이다. **실제 통신 환경에서는 오류 가능성 때문에 3단계 설정**이 이루어지는데, 3번째 단계에서 전송할 데이터가 있으면 바로 데이터를 전송하고, 그렇지 않으면 2번째 단계에 대한 응답을 전송해야 한다. 

### **TCP 프로토콜**

TCP는 IP 프로토콜 위에서 연결형 서비스를 지원하는 전송 계층 프로토콜로, 인터넷 환경에서 기본으로 사용한다. TCP는 **전이중 방식의 양방향 가상 회선**을 제공하기 때문에 신뢰성 있는 데이터 전송을 보장한다. 전송 계층 프로토콜은 운영체제의 내부 기능으로 구현되기 때문에 TCP 서비스를 사용하려면 상위 계층에서 시스템 콜이라는 프로그램 호출 방식을 이용해야 한다.

### **혼잡 제어**

TCP 프로토콜의 **ECN 기능**은 혼잡을 인지한 라우터가 송신 프로세스에 명시적으로 혼잡 발생을 알려주어 송신 프로세스 스스로 트래픽을 완화하는 기술이다. 이를 위하여 TCP 헤더에 CWR 필드와 ECE 필드를 정의한다. **ECE 비트는 네트워크 트래픽이 많아질 때 라우터가 송신 프로세스에 명시적으로 혼잡을 알리려고 사용하며**, ECE 비트를 수신한 송신 프로세스가 전송 윈도우 크기를 줄였음을 통지하기 위한 목적으로 CWR비트가 사용된다. 

### **포트 번호**

포트 번호는 TCP와 UDP가 상위 계층에 제공하는 주소 표현 방식이다. 소켓 시스템 콜을 이용해 TCP 연결 설정이 되면 통신 양단의 프로세스가 사용하는 고유 주소는 해당 호스트의 IP 주소와 호스트 내부의 포트 번호가 조합된 형태이다. 클라이언트-서버의 연동은 서버가 먼저 실행되고, 클라이언트가 서버와 연결을 시도하는 방식으로 이루어진다. 이때 연결을 원하는 서버와 접속하려면 서버의 IP주소와 포트 번호를 알아야 한다. 인터넷 환경에서 많이 사용하는 네트워크 응용 서비스의 서버 프로세스에 할당된 포트 번호를 Well-Known포트라 한다.

### **데이터 전송**

TCP는 전이중 방식의 양방향 통신을 지원하므로 가상 회선으로 연결된 두 프로세스가 동시에 데이터를 전송할 수 있다. 연결형 서비스를 제공하는 TCP에서 데이터를 전송하려면 연결 설정, 데이터 전송, 연결 해제라는 3단계를 순차적으로 진행해야 한다. 연결 설정은 3단계 설정 방식을 사용하며, 연결 해제는 양자의 합의 아래 이루어진다. 

### **ECN의 동작 원리**

ECN기능은 TCP의 혼잡 제어 기능을 지원한다. 이를 위해 TCP 헤더의 ECE, CWR 플래그와 IP 헤더의 ECN필드가 정의되었다. ECN 기능을 사용하기 위해서는 TCP 연결 설정 단계에서 ECN 기능의 사용 여부를 협상해야 한다. 데이터 전송 단계에서는 혼잡을 인지한 라우터가 수신 프로세스에 혼잡을 통지한다. 그러면 수신 프로세스는 다시 송신 프로세스에 혼잡을 통지함으로써 송신 프로세스가 전송하는 데이터의 양을 줄이는 방식으로 혼잡 제어가 이루어진다. 
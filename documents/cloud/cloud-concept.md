# CLOUD

## CLOUD란?
초기 투자나 장기 계약 없이 인터넷을 통해 IT 리소스와 애플리케이션을 원할 때 언제든지 사용한 만큼만 요금을 내는 서비스이다.

## ON-PREMISE란?
CLOUD와 반대되는 개념으로, 자체적으로 보유한 전산실 서버에 소프트웨어를 직접 설치하는 방식이다.

## 클라우드가 되기 위한 5가지 조건은?

* 첫째로, 사용자 개별 관리 화면을 통해 서비스가 이용 가능해야 한다는 주문형 셀프 서비스이다. 

* 둘째로, 모바일, PC 등 다양한 디바이스를 통한 서비스 이용이 가능해야 한다는 광범위한 네트워크 접속이다.

* 셋째로, 사업자의 컴퓨팅 리소스를 여러 사용자가 공유하며, 사용자는 본인이 이용하는 리소스의 정확한 위치를 알 수 없는 특성을 가진다는 리소스의 공유이다. 

* 넷째로, 필요시 필요한 만큼 처리 능력을 높이거나 낮추는게 가능해야 한다는 빠른 탄력성이다. 

* 다섯번째로, 서비스를 이용한 만큼 요금이 부과되는 종량제 특성인 측정 가능한 서비스이다. 


## 클라우드의 장점은?

* 첫째로, 많은 초기 자본 투자 비용이 발생하는 On-premise에 비해 Cloud는 사용한 만큼만 지불하기 때문에 초기 선투자 비용이 없다.


* 둘째로, 전력 비용, 향온 향습, 상면 비용, 운영 관리 비용, 라이센스 비용, 향후 증설 비용이 발생하는 On-premise에 비해 Cloud는 운영 비용을 절감할 수 있다.

* 셋째로, Cloud는 필요한 자원을 탄력적으로 증설 및 감소를 할 수 있어 비용 효율적이다.

* 넷째로, 혁신을 위한 시도가 자주 일어나지 않고 실패의 비용이 높으며, 혁신 속도가 느려지는 On-premise에 비해 Cloud는 혁신을 위한 시도를 많이 할 수 있고, 실패의 비용이 낮아 속도 및 민첩성에서 우위에 있다.

* 다섯번째로, Cloud는 비즈니스에만 집중할 수 있다. 데이터 센터 운영과 같은 영역은 AWS, Azure, GCP등에 맡긴다. 

* 여섯번째로, Cloud는 글로벌 확장이 가능하다. 전 세계 어디라도 수 분 내 확장하여 서비스를 구축할 수 있다. 

## SaaS, PaaS, IaaS란?

다음으로, 3개의 클라우드 서비스 모델에 대해 알아본다. 
* 첫번째로 Infrastructure as a Service의 약자인 **IaaS**이다. 서버, 스토리지, 네트워크를 가상화 환경으로 만들어, 필요에 따라 인프라 자원을 사용할 수 있게 서비스를 제공하는 형태이다. 예를 들어 **AWS EC2**가 있다. 장점으로는, 필요에 따라 빠르게 확장 가능하다는 점, 다양한 사용자가 하나의 물리 서버를 이용해, 유지보수 비용을 감소한다는 점, 서버가 다운되었을때, 다른 서버로 즉시 이전되어 다운 타임을 최소화 한다는 점이 있다. 단점으로는 운영체제와 미들웨어 보안 유지는 소비자가 해결해야 한다는 점, 의존성이 높아진다는 점, IaaS의 인프라 유지 보수팀을 운영하거나 훈련을 시킬 필요가 있을 수 있다는 점이다. 

* 두번째로 Platform as a Service의 약자인 **PaaS**가 있다. 일반적으로 개발 및 시작과 관련된 인프라를 만들고 유지보수 하는 복잡함 없이 고객이 어플리케이션을 개발, 실행, 관리할 수 있게 하는 플랫폼 제공 형태이다. 예를 들어 **구글 앱 엔진**이 있다. 장점으로는, 미리 코딩된 애플리케이션이 구성요소로 제공되기 때문에 코딩 시간을 단축할 수 있다는 점, 인터넷을 통해 개발 환경에 엑세스하므로 개발 팀은 팀 멤버가 원격 위치에 있는 경우에도 프로젝트를 함께 작업할 수 있다는 점이다. 또한, PaaS는 같은 통합 환경 내에서 빌드, 테스트, 배포, 관리, 업데이트의 완전한 애플리케이션 수명 주기를 지원하는 데 필요한 모든 기능을 제공한다는 점이다. 

* 세번째로, Software as a Service의 약자인 **SaaS**이다. 소프트웨어 및 관련 데이터는 중앙에 호스팅되고 사용자는 웹 브라우저등의 클라이언트를 통해 접속하는 형태의 소프트웨어 전달 형태이다. 예를 들어 **구글클라우드**, **드롭박스**등이 있다. 장점으로는 리소스가 부족한 조직에서도 경제적 부담 없이 정교한 엔터프라이즈 응용 프로그램을 사용가능하다는 점, 사용한 양만큼 요금을 지불하면 된다는 점, 사용자가 인터넷에 연결된 컴퓨터 또는 모바일 장치에서 SaaS 앱 및 데이터에 엑세스 할 수 있으므로 리소스에 “이동성”을 손쉽게 적용할 수 있다는 점, 데이터가 클라우드에 저장되어 있으면 사용자는 인터넷에 연결된 컴퓨터 또는 모바일 장치에서 정보에 엑세스가 가능하다는 점이다. 

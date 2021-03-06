# MSA

## DevOps란?
Development(개발)과 Operations(운영)이 합쳐진 합성어로, 개발과 운영이 분리되지 않은, 개발과 동시에 운영을 할 수 있는 조직, 그 문화를 의미한다. 

## CI란?
Continuous Integration의 약자로, 지속적 통합이다. 자동으로 통합하고 테스트하고 레포트로 남기는 활동을 의미한다.

## CD란?
Continuous Development or Continuous Delivery의 약자로, 지속적 배포이다. 실행 환경에 자동으로 배포하는 것인데, Continuous Development과 Continuous Delivery의 차이점은 다음과 같다. 
* Continuous Development는 담당자의 승인 절차가 필요 없는, 배포까지도 실시간으로 진행하는 것이다. 
* Continuous Delivery은 통제를 하나 더 둔 것으로, 중간에 담당자의 컨펌을 받아야 한다. 

## CI/CD 파이프라인이란?
통합 및 배포까지 일련의 프로세스를 하나로 연계하여 자동화하고, 시각화된 프로세스를 구축하는 것이다.

## 넷플릭스 OSS란? 
넷플릭스 OSS(Open Source Software)는 넷플릭스가 마이크로서비스를 개발, 운영해 보면서 생긴 노하우를 다른 사람들도 쉽게 사용할 수 있도록 공유한 것이다. 

마이크로서비스 운영 중 생긴 어려움을 해결할 전형적인 마이크로서비스 애플리케이션 패턴들이 되었다.

## Transaction Script Pattern이란?
Transaction Script Pattern이란 서비스 계층에서 대부분의 비즈니스 로직을 처리하는 패턴이다. 단순한 입출력 구조의 쉬운 업무 처리를 하고자 할 때 사용한다. 또한, 엔티티에는 비즈니스 로직이 거의 없고 서비스 클래스를 처리하기 위한 데이터 역할만 수행한다. 이 경우에는 SQL Mapping 방식의 MyBatis가 적합하다.

## Domain Model Pattern이란?
Domain Model Pattern에서 서비스는 모든 비즈니스 로직을 처리하지 않고 엔티티에 비즈니스 로직 처리를 위임한다. 복잡한 비즈니스 로직을 사용하고자 할 때 효율적이다. 또한 엔티티는 비즈니스 로직을 가지고 객체 지향의 특성을 활용한다. 이 경우에는 OR Mapping 방식의 JPA가 적합하다. 


## 전략적 설계와 전술적 설계
* 전략적 설계
    
    마이크로서비스를 식별하는 역할로, 비즈니스에서 전략적으로 중요한 것을 찾아 중요도에 따라 일을 나누는 방법이다. 
    도메인의 주요 개념들을 정의하고 도메인 간의 경계를 식별하는 **바운디드 컨텍스트** 식별, 프로젝트팀원이 공통으로 사용하는 언어로 정의하는 **유비쿼터스**언어 정의, 경계 간 관계를 분석하여 매핑을 정의하는 **컨텍스트 매핑**을 진행한다. 

* 전술적 설계

    식별된 마이크로서비스의 내부 구조를 상세하게 정의하고, 비즈니스의 고유한 활동을 모델링한다. 즉, **마이크로서비스 내부 구조 설계**, **도메인 모델 및 모듈 등 정의**, **서비스 인터페이스, API 정의**를 진행한다. 

## 서브도메인이란?

전체 비즈니스 도메인의 하위영역으로 하나의 논리적 도메인 모델

## 서브도메인의 유형

* 핵심 서브 도메인
    
    * 다른 경쟁자와 차별화를 만들 수 있는 비즈니스 영역이다.
    * 높은 우선순위를 갖는 전략적 투자 영역이다.
    * 가장 큰 투자가 필요한 곳이다.

</br>

* 지원 서브 도메인

    * 맞춤 개발이 필요한 영역이다.
    * 핵심 서브도메인의 성공을 위한 중요한 영역이다.
    
</br>

* 일반 서브 도메인

    * 기존 제품 구매를 통해 바로 충족시킬 수 있는 영역이다.
    * 핵심/지원 서브도메인이 할당된 팀에서 직접 구현가능하다. 
# Native application (desk-top)<br> 
- **특정 Platform이나 Device에서 사용되도록 개발된 Application**
- 해당 플랫폼에 일반적으로 설치된 기타 소프트웨어 및 운영 체제와 상호 작용하고 이를 활용할 수 있음
- 특정 장비를 위한 하드웨어 및 소프트웨어를 사용할 수 있으며, 이는 네이티브 어플리케이션이 GPS나 카메라같은 최신 기술을 모바일 디바이스에서 이용할 수 있다는 것을 의미함
- 이는 native apps의 장점이 Web apps나 mobile cloud apps 보다 우위에 있다고 해석할 수 있음

# Web application <br> 
- **표준 Web 기술을 사용하여 Platform이나 Device에 상관 없이 사용되도록 개발된  Application, 요즘 많이 씀**
- Client-server 소프트웨어 어플리케이션
- 프로그램은 원격 서버에 저장되고 인터넷을 통해 웹 브라우저에서 실행
- 예) webmail, online retail sales, online auctions, wikis, instant messaging services 등

# Cloud Native Application
개념 : Cloud 환경에 최적화 되어 서비스 되도록 개발된 어플리케이션
- **Desktop application + Web application으로 클라우드 환경에서 실행되는 어플리케이션 프로그램, 오프&온&웹에서 가능**
- 최소의 상태(stateful) 컴포넌트들이 격리된 상태의 (마이크로)서비스로 구성되며, 각각의 서비스는 분산되고, 탄력적이며 수평적 확장성 있는 시스템으로 구성
- 어플리케이션과 각각의 독립적인 배포 단위는 클라우드 중심의 디자인 패턴들과 셀프서비스 가능한 탄력적인 플랫폼에서 운영되도록 설계되어 있음

### Cloud Native Application의 핵심은 **'서비스'**
- 어플리케이션을 여러 개의 서로 독립적인 기능을 하는 서비스로 구분
- 서비스들을 어떻게 구성하고 어떻게 연결하고 어떻게 관리하느냐가 관건
- ‘서비스’들을 묶어서 하나의 통합된 ‘(비즈니스) 서비스’를 할 수 있도록 하기 위한 다양한 기능과 기술 필요
- desktop app과 같이 응답 속도가 빠르고 오프라인에서도 작업 가능
- web apps처럼 특정 기기(device)에 종속될 필요가 없고 온라인으로 쉽게 업데이트 가능
- 사용자가 통제 가능하지만, 사용자 컴퓨터나 저장장치의 저장공간을 사용할 수 없음
- 잘 작성된 cloud apps은 desktop apps의 호환성과 Web apps의 휴대성을 모두 제공함


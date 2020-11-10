# 클라우드 모델
![image](https://github.com/Jiyooung/Computer_Science/blob/main/Cloud/Image/CloudModel.png)

## IaaS - Infrastructure as a Service<br>
정의 : CPU나 하드웨어 등의 컴퓨팅 리소스(자원)를 네트워크를 통해 서비스로 제공하는 모델<br>
- 물리적 리소스를 가상화 하여 유연한 Infrastructure을 제공<br>

### 가상화 유형
![image](https://github.com/Jiyooung/Computer_Science/blob/main/Cloud/Image/Hypervisor_VS_Container.png)
### 1. Hypervisor
- OS 환경을 통째로 가상화 함

- **장점**
    - 가상 서버마다 OS를 선택할 수 있음
    - 가상 서버들이 완전히 분리되어 있음
    
- **단점**
    - 가상 서버마다 OS가 필요하므로 하드웨어 리소스의 소비량이 많음
    - 가상 서버의 부팅에 시간이 걸림

### 2. Container
- 하나의 호스트 OS에서 멀티 OS 환경을 구현함
    
- **장점**
    - 하나의 호스트OS에서 여러개의OS를 동시에 이용할 수 있음
    - 다른 컨테이너로의 복제성과 이식성이 뛰어남

- **단점**
    - 운영체제의 커널을 공유하므로, 각 운영체제의 이미지는 각 운영체제에서만 실행 가능함
    - 하나의 호스트 OS를 공유하기 때문에 컨테이너 하나가 사이버 공격을 받으면 다른 컨테이너가 위험에 노출될 가능성이 있음

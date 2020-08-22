# 도커

리눅스 컨테어너에 여러 기능을 추가함으로써 애플리케이션을 컨테이너로 쉽게 사용할 수 있게 만들어진 오픈소스 프로젝트

## 가상 머신과 도커 컨테이너

- 가상 머신

  - 한개의 HOST위에 여러개의 운영체제(가상 머신의 단위가 됨)를 설치하여 사용

  - 독립적인 GuestOS: 하이퍼바이저에 의해 생성, 관리되는 운영체제는 GuestOS라 불리며 각 GuestOS는 독립된 공간과 시스템 자원을 할당받아 사용함

  - 일반 HOST에 비해 성능 손실이 큼: 각종 시스템을 가상화하고 독립된 공간을 생성하는 작업은 하이퍼바이저를 거치기 때문

  - 배포를 위한 이미지 생성시 크기가 큼: 가상 머신은 게스트 운영체제를 사용하기 위한 라이브러리, 커널을 모두 포함

- 도커

  - 가상화 공간을 위해 리눅스 자체 기능을 사용: chroot, namespace ,cgroup 프로세스 단위의 격리 환경을 만들기 때문에 성능 손실이 거의 없음

  - 컨테이너를 이미지로 만들었을때 크기가 작고 빠름: 컨테이너에 필요한 커널은 HOST 커널을 고유하여 사용, 컨테이너에는 애플리케이션 구동을 위한 라이브러리 및 실행파일만 존재

## Docker Toolbox와 Docker for Windows/Mac의 차이점

- Docker Toolbox

  - 버추얼박스 사용으로 도커 사용에 최적화

  - 외부에서 컨테이너 접근시 2중 포트 포워딩 필요: Windows/Mac -> 버추얼박스 -> 가상 머신(ip: 192.168.x.x) -> 도커 컨테이너(ip: 172.17.0.x)

    - Windows/Mac -> 가상 머신 사이 포트 포워딩

    - 가상 머신 -> NAT IP를 할당받은 도커 컨터이너 사이 포트 포워딩 (컨테이너 생성시 쉽게 가능)

- Docker for Windows/Mac

  - 쉽게 외부에서 접근 가능: 가상 머신을 생성하지 않고 가체 가상화 기술로 리눅스 환경을 만들어 컨테이너를 생성. 포트 포워딩 설정하면 외부 접근 가능
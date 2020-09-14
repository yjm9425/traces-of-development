# 도커 엔진

핵심: 이미지와 컨테이너

## 도커 이미지

- 컨테이너 생성시 필요한 요소

- 이미지는 여러개의 계층으로 된 바이너리 파일로 존재, 컨테이너를 생성, 실행시 읽기 전용으로 사용

- 형태 [저장소 이름]/[이미지 이름]:[태그]

  - 저장소: 이미지가 저장된 장소를 의미. 명시되지 않으면 Docker Hub의 Official 이미지를 뜻함. 생략 가능

  - 이미지 이름: 이미지의 역할을 표시. 생략 불가

  - 태그: 버전 관리, 리비전 관리 사용. 생략시 이미지 태그를 latest로 인식

## 도커 컨테이너

- 이미지로 생성되는 컨테이너

  - 파일 시스템, 격리된 시스템 자원및 네트워크를 사용할 수 있는 독립된 공간 생성, 컨테이너별로 독립적임

  - 1개의 이미지에서 N개의 컨테이너 생성이 가능(1:N)

  - 이미지를 읽기 전용으로 사용, 이미지에서 변경된 사항만 컨테이너 계층에 저장. 이미지에 영향을 주지 않음.

### 컨테이너 다루기

**생성**

```bash
[run: 이미지 생성, 실행, 터미널 접속]
docker run -i -t unbuntu:14.04
```

run: pull(이미지 없을때) -> create -> start -> attach

옵션: -i(상호 입출력), -t(tty활성화 bash셀 사용), 두 옵션 설정 안할시 셸을 정상적으로 사용불가.

```bash
[create: 이미지 생성]
docker create -i -t --name userDefinedImageName centos:7
```

create: pull(이미지없을때)-> create

```bash
[컨테이너를 정지시킴]
exit
or
Ctrl + D

[컨테이너를 정지시키지 않음]
CTRL + P,Q
```

**조회**

```bash
docker ps
```

**삭제**

```bash
docker rm -f 컨테이너명
dokcer container prune
```

실행중인 컨테이너는 삭제불가. docker stop 컨테이너명 명령어 실행하거나 -f 옵션을 추가해야함.

prune은 모든 컨테이너를 삭제.

**외부로 노출**

```bash
docker run -i -t --name mywebserber -p 192.0.0.1:7777:80 ubuntu:14.04
```

호스트의 port(7777)를 컨테이너의 port(80)으로 연결

# 네트워크 기초 지식

## 서버와 클라이언트간의 통신을 지원하는 네트워크

### 서버와 클라이언트의 데이터 통신

![서버와 클라이언트의 데이터 통신](https://raw.githubusercontent.com/yjm9425/traces-of-development/master/img/network%20between%20server%20and%20client.png)

## OSI 7 Layer

네트워크 학습시 가장 먼저 이해해야할 개념으로 컴퓨터 통신 기능을 계층구조로 나누어 정리한 모델

| 계층                 |                                        의미                                        |
| -------------------- | :--------------------------------------------------------------------------------: |
| `Application Layer`  |                   애플리케이션별로 서비스를 제공하는 방법을 규정                   |
| `Presentation Layer` |          애플리케이션 데이터를 통신에 적합한 형태로 변환하는 방법을 규정           |
| `Session Layer`      |     데이터를 흘려보내는 논리적인 통신로(커넥션)의 확립과 연결 끊기에 대해 규정     |
| `Transport Layer`    |                데이터를 통신 상대에게 확실하게 전달하는 방법을 규정                |
| `Network Layer`      |    동일 또는 다른 네트워크의 기기와 연결하기 위한 주소와 경로의 선택방법을 규정    |
| `Datalink Layer`     |     직접 연결된 기기 사이에 논리적인 전송로(데이터링크)를 확린하는 방법을 규정     |
| `Physical Layer`     | 네트워크 케이블의 재질이나 커넥터 형식, 핀의 나열 방법등 물리적인 요소를 모두 규정 |

<br>
애플리케이션 프로토콜: Application Layer, Presentation Layer, Session Layer
<br>TCP,UDP: Transport Layer  
<br>IP,ICMP,ARP: Network Layer  
<br>Ethernet: Datalink Layer, Physical Layer

<hr>

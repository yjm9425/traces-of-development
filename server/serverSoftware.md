# 서버 소프트웨어

## 웹 서버

웹 서버는 주로 정적 데이터(그림, stylesheet, javascript, ...)처리를 한다.  
이외에도 인증, https, 가상 호스팅, 대역폭 스로틀링 등의 기능을 지원한다.

- Apache
- IIS(마이크로소프트)
- nginx(오픈소스)

## 웹 어플리케이션 서버

웹 어플리케이션 서버는 주로 동적 데이터를 처리한다.  
트랜잭션, 보안, 메시징, 쓰레드처리 등의 기능을 지원한다.

- Tomcat(오픈소스)
- WebLogic Server(오라클)
- WebSphere Application Server(IBM)
- IIS(마이크로소프트)

## SSL 서버

SSL: Secure Sockets Layer, 웹사이트와 브라우저 사이에 전송된 데이터를 암호화하여 인터넷 연결 보안을 유지하는 표준기술

- OpenSSL(오픈소스)
- IIS(마이크로소프트)

## DNS 서버

- BIND(오픈소스)
- Windows Server(마이크로소프트)

## 프록시 서버

- Squid(오픈소스)

## 메일(POP/SMTP) 서버

- sendmail(오픈소스)
- qmail(오픈소스)
- postfix(오픈소스)
- Exchange Server(마이크로 소프트)

## FTP 서버

- vs-ftpd(오라클)
- IIS(마이크로소프트)

## 데이터베이스 서버

- Oracle Database(오라클)
- MySQL(오라클, 오픈소스)
- SQL Server(마이크로소프트)
- PostgreSQL(오픈소스
- DB2(IBM)

## NTP

Network Time Protocol: Network 상에 연결된 장비와 장비간의 시간정보 동기화를 위한 프로토콜

- ntpd(오픈소스)
- Windows Server(마이크로소프트)

## Syslog 서버

Syslog: 로깅 메시지 프로그램의 표준. 다양한 프로그램들이 생성하는 메시지를 저장, 분석가능한 형태로 제공.

- syslog-ng(오픈소스)
- rsyslog(오픈소스)
- Kiwi Syslog Server(SolarWinds)

## SNMP 서버

Simple Network Management Protocol: IP 네트워크상의 장치로부터 정보를 수집 및 관리, 정보를 수정하여 장치의 동작을 변경하는 인터넷 표준 프로토콜

- net-snmp(오픈소스)
- TWSNMP 매니저(오픈소스)
- OpenView NNM(휴렛팩커드)
- Tivoli NetView(IBM)

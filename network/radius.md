# RADIUS (Remote Authentication Dial in User Service)

RADIUS는 네트워킹 프로토콜로 사용자가 서비스를 요청하면 인증, 인가, 회계관리에 대해 중앙집중화된 서비스를 제공

## RADIUS 서버

통상적으로 ISP(Internet Service Provider)에서 제공된 자원을 활용하여 원격 접속할때 인증을 수행하는 서버를 지칭

### 필요성

무선랜망을 권한을 가진사람만 접근할 수 있을때

### 구성요소

1. 사용자
2. RADIUS 클라이언트: 원격접속 터미널서버, NAS, 802.1x, 브리지 또는 AP
3. RADIUS 서버: 인증서버, 인증을 위한 주요자격 ID, PW 저장 관리

# 모든 개발자를 위한 HTTP 웹 기본지식 - 김영한

## 섹션 1. 인터넷 네트워크

인터넷 프로토콜 스택의 4계층
애플리케이션 계층 - HTTP,FTP
전송 계층 - TCP, UDP
인터넷 계층 - IP
네트워크 인터페이스 계층

### TCP 특징(Transmission Control Protocol 전송제어 프로토콜)

- 연결지향 - TCP 3way handshake
- 데이터 전달 보증
- 순서 보장
- 신뢰할 수 있는 프로토콜
- 현재는 대부분 TCP 사용

### UDP 특징(User Datagram Protocol 사용자 데이터그램 프로토콜)

- 하얀 도화지에 비유 (기능이 거의 없음)
- 연결지향 - TCP 3way handshake X
- 데이터 전달보증 X
- 순서 보장X
- 데이터 전달 및 순서가 보장되지 않지만, 단순하고 빠름
- 정리 : IP 와 거의 같음, PORT + 체크섬 추가 , 애플리케이션에서 추가작업 필요

### PORT

- 같은 IP 내에서 프로세스 구분 (IP가 아파트면 PORT는 몇동 몇호)
- 0 ~ 65535: 할당 가능
- 0 ~ 1023: 잘 알려진 포트, 사용하지 않는 것이 좋음

### DNS(Domain Name System)

- IP는 변경될 수 있기에 DNS 서버에 도메인을 등록하여 도메인 주소 검색시 IP주소를 변환해 준다.

### URI(Resource Identifier)

- URI 안에는 URL과 URN이 있다.

  - Uniform :리소스 식별하는 통일된 방식
  - Resource: 자원, URI로 식별할 수 있는 모든 것(제한 없음)
  - Identifier: 다른 항목과 구분하는데 필요한 정보

- URL(Resource Locator)

- URN(Resource Name)

### 웹브라우저 요청 흐름

ex: https://www.google.com:443/search?q=helo&hl=ko

1. 웹브라우저가 HTTP 요청 메시지 생성

- GET/search?q=hello&hl=ko HTTP/1.1 HOST:www.google.com

2. TCP/IP패킷이 생성되어 전송 데이터에 HTTP 요청메시지가 담김.

3. 구글 서버로 도착, 쿼리 스트링을 해석하여 HTTP 응답 메시지 생성,반환

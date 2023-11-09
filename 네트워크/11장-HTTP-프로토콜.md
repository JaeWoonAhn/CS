### [HTTP 프로토콜](https://youtu.be/TwsQX1AnWJU?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)
-  [[OSI 7 Application Layer]]로서 웹 서버스 통신에 사용
#### 1. HTTP/1.0
- 한 연결당 하나의 요청을 처리하도록 설계
	- RTT 증가 초래
		- `RTT : 패킷이 목적지에 도달하고 나서 다시 출발지로 돌아오기까지 걸리는 시간이며 패킷 왕복 시간`
		- 서버 부담 증가
		- 사용자 응답 시간 증가
		- 해결 방법
			- [[이미지 스플리팅]]
			- [[코드 압축]]
			- [[이미지 Base64 인코딩]]

#### 2. HTTP/1.1
 - 1.0에서 발전
 - 매번 TCP를 연결하는 방식 -> 한 번 TCP 초기화
	 - keep-alive라는 옵션으로 여러 개의 파일을 송수신 가능
![[ZZ_HTTP 1.0 VS 1.1.png]]
- keep-alive 표준화되어 기본 옵션으로 설정
- 단점
	- 문서 안에 포함된 다수의 리소스(이미지, css, script)를 처리하려면 요청할 리소스 개수에 비례해서 대기 시간이 길어짐
	- [[HOL Blocking]]
		- ==만약 TCP 핸드쉐이크를 각 리소스마다 하게되면 병렬로 전송이될까요??==
	- 무거운 헤더 구조
		- 쿠키
		- 메타 데이터
		- 등 다양한 데이터가 들어있음
		- 압축이 되지 않아 무거움

#### 3. HTTP/2
- 장점
	- HTTP/1.x 보다 지연 시간 줆
	- 응답 시간 빠름
	- [[멀티플렉싱]]
		- HOL Blocking 극복
	- 헤더 압축
		- [[허프만 코딩]]
	- 서버 푸시
		- HTTP/1.1 : 클라가 서버에 요청 해야 파일을 다운받을 수 있었음
		- HTTP/2 : 클라 요청 없이 서버가 바로 리소스 푸시 가능
	- 요청의 우선순위 처리

#### 4. HTTPS
- HTTP/2는 HTTPS 위에서 동작
- 정의
	- 애플리케이션 계층과 전송 계층 사이에 신뢰 계층인 [[SSL TLS]] 계층을 넣은 신뢰할 수 있는 HTTP 요청
- 통신 암호화 가능

### [HTTP 요청 프로토콜](https://youtu.be/rxaBwwI_JnI?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- HTTP Method 설명 중 GET, POST만 사용해야 한다고 하지만 개발자 입장에서 RESTful API 개발시 PUT, DELETE도 사용하는게 원칙임

### [URL, URI란?](https://youtu.be/2ikhZ_fNP5Y?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [HTTP 요청 프로토콜 작성 실습](https://youtu.be/XbGJYsxed2w?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [URI 이해를 위한 실습](https://youtu.be/HBojczyd1Ac?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [HTTP 응답 프로토콜](https://youtu.be/kuucNF4Zvbs?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [HTTP 헤더 포맷](https://youtu.be/mQTGmxendk8?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

- 

### [HTTP 프로토콜 분석 실습](https://youtu.be/dhMrKTwNI8U?list=PL0d8NnikouEWcF1jJueLdjRIC4HsUlULi)

-
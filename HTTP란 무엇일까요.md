# HTTP는 무엇일까요?
## HTTP란?
HTTP(Hypertext Transfer Protocol)는 인터넷상에서 웹 서버와 클라이언트 브라우저 간의 하이퍼텍스트 문서를 전송하기 위해 사용되는 통신 규약이다. 

## HTTP 특징
+ 클라이언트 서버 구조
: 클라이언트가 서버에 요청을 보내면 서버는 그에 대한 응답을 보낸다.
+ 무상태 프로토콜(Stateless)
: HTTP에서 서버가 클라이언트의 상태를 보존하지 않는다.
+ 비연결성 
: 비연결성을 가지는 HTTP에서는 실제로 요청을 주고 받을 때만 연결을 유지하고 응답을 주고나면 TCP/IP 연결을 끊는다.

## HTTP의 동작방식
클라이언트와 서버들은 개별적인 메시지 교환에 의해 통신한다. 
+ 요청(Request) : 보통 브라우저인 클라이언트에 의해 전송되는 메시지
+ 응답(Responses) : 요청에 대해 서버에서 응답으로 전송되는 메시지

## 요청(Request)
<pre>
<code>
GET https://www.zerocho.com HTTP/1.1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) ...
Upgrade-Insecure-Requests: 1
</code>
</pre>

### 1. Start line
+ HTTP Method + Request Target + HTTP Version
<pre>
<code>
GET https://www.zerocho.com HTTP/1.1
</code>
</pre>

+ HTTP Method
    - GET : 자료를 요청할 때 사용
    - POST : 자료의 생성을 요청할 때 사용
    - PUT : 자료의 수정을 요청할 때 사용
    - PATCH : 자료의 부분 수정을 요청할 때 사용
    - DELETE : 자료의 삭제를 요청할 때 사용

+ Request Target : 해당 Request가 전송되는 목표 URL
+ HTTP Version

### 2. Header
+ 요청에 대한 추가 정보를 담고 있다.
<pre>
<code>
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) ...
Upgrade-Insecure-Requests: 1
</code>
</pre>

+ Hearder의 정보 종류
    - Host : 요청이 전송되는 Target의 Host URL
    - User-Agent : 요청을 보낸 클라이언트의 정보
    - Accept : 해당 타입의 Response를 보내달라고 요청
    - Content-Type : Request의 body 타입

### 3. Body
+ 해당 Request의 실제 메시지
+ 없는 경우가 많음

## 응답(Response)
<pre>
<code>
HTTP/1.1 200 OK
Connection: keep-alive
Content-Encoding: gzip												 
Content-Length: 35653
Content-Type: text/html;

<!DOCTYPE html><html lang="ko" data-reactroot=""><head><title...>
</code>
</pre>

### 1. Ststus line
+ 버전 상태 코드 상태 메시지
<pre>
<code>
HTTP/1.1 200 OK //성곡적인 요청
</code>
</pre>

### 2. Header
+ 응답에 대한 정보
<pre>
<code>
Connection: keep-alive
Content-Encoding: gzip												 
Content-Length: 35653
Content-Type: text/html;
</code>
</pre>

### 3. Body
+ 요청에 대한 응답 값
<pre>
<code>
<!DOCTYPE html><html lang="ko" data-reactroot=""><head><title...>
</code>
</pre>
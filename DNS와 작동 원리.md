# DNS와 작동 원리
![DNS 작동 원리](https://media.vlpt.us/images/minj9_6/post/5b013d74-b681-42bc-aadf-ea883bbb6f59/image.png)
![DNS 작동 원리](https://d1.awsstatic.com/Route53/how-route-53-routes-traffic.8d313c7da075c3c7303aaef32e89b5d0b7885e7c.png)

1. 사용자가 웹 브라우저를 열어 주소 표시줄에 www.example.com을 입력하고 Enter 키를 누른다.
2. www.example.com에 대한 요청은 일반적으로 케이블 인터넷 공급업체, DSL 광대역 공급업체 또는 기업 네트워크 같은 인터넷 서비스 제공업체(ISP)가 관리하는 DNS resolver로 라우팅한다.
3. ISP의 DNS resolver는 www.example.com에 대한 요청을 DNS Root Name Server에 전달한다.
4. ISP의 DNS resolver는 www.example.com에 대한 요청을 이번에는 .com 도메인의 TLD(Top-Level Domain) Name Server 중 하나에 다시 전달한다. 
5. ISP의 DNS resolver는 Amazon Route 53 Name Sever 하나를 선택해 www.example.com에 대한 요청을 해당 이름 서버에 전달한다.
6. Amazon Route 53 Name Server는 example.com 호스팅 영역에서 www.example.com 레코드를 찾아 웹 서버의 IP 주소 192.0.2.44 등 연관된 값을 받고 이 IP 주소를 DNS 해석기로 반환한다.
7. ISP의 DNS resolver는 사용자에게 필요한 IP 주소를 확보 했다. 해석기는 이 값을 웹 브라우저로 반환한다. DNS 해석기는 다음에 누군가가 example.com 을 탐색할 때 좀 더 빠르게 응답할 수 있도록 사용자가 지정하는 일정기간 example.com의 IP 주소를 캐싱(저장)합니다. 
8. 웹 브라우저는 DNS resolver로부터 얻은 IP 주소로 www.example.com에 대한 요청을 전송한다. 
9. 192.0.2.44에 있는 웹 서버 또는 그 밖의 리소스는 www.example.com의 웹 페이지를 웹 브라우저로 반환하고, 웹 브라우저는 이 페이지를 표시한다.

![DNS 작동 원리](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FH79v0%2Fbtq1b9Rmezu%2F5diSMKPSB7ksFMdgrmEvDk%2Fimg.png)

1. DNS Query (Web Browser -> Local DNS) : beta.example.com의 IP주소를 알고 계신가요?
2. DNS Query (Local DNS -> Root DNS) : beta.example.com의 IP주소를 알고 계신가요?
3. DNS Response (Root DNS -> Local DNS)) : .com 도메인을 관리하는 서버에 물어보세요
4. DNS Query (Local DNS -> .com TLD NS) : beta.example.com의 IP주소를 알고 계신가요?
5. DNS Response (.com TLD NS -> Local DNS) : .com 도메인을 관리하는 서버에 물어보세요.
6. DNS Query (Local DNS -> naver.com NS) : beta.example.com의 IP 주소를 알고계신가요?
7. DNS Response (naver.com NS -> Local DNS) : 해당 웹은 beta.g.example.com이라는 이름으로 통해요. g.example.com 도메인을 관리하는 네임 서버에 물어보세요.
8. DNS Query (Local DNS -> g.example.com NS) : beta.g.example의 IP주소를 알고 계신가요?
9. DNS Response (g.example.com NS -> Local DNS) : beta.g.naver.com의 IP주소는 123.456.789 입니다.
10. DNS Response (Local DNS -> Web Browser) : www.naver.com의 IP주소는 123.456.789 입니다.
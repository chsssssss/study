# HTML 기초배우기
## HTML이란
HTML(Hypertext Markup Language)이란 우리가 보는 웹페이지가 어떻게 구조화되어 있는지 브라우저로 하여금 알 수 있도록 하는 마크업 언어
태그는 웹 상의 다른 페이지로 이동하게 하는 하이퍼링크 내용들을 생성하거나, 단어를 강조한느 등의 역할, <>로 둘러싸인 키워드

## HTML의 구조
<pre>
<code>
<p>moms spaghetti<p>
</pre>
</code>
1. 시작태그
2. 종료태그
3. 요소 : 시작태그, 종료태그, 내용을 모두 포함

## HTML 문서의 구조
<pre>
<code>
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p>mom's spaghetti</p>
</body>
</html>
```
</pre>
</code>
1. <pre><code><!DOCTYPE html></pre></code>
- 웹 문서가 어떤 버전의 HTML 언어로 작성되었는지 결정하는 기능
2.<pre><code><html></html></pre></code>
- HTML 문서의 루트요소를 정의
3. <pre><code><head></head></pre></code>
- 웹페이지의 정보, 문서에 사용할 외부 파일들을 링크할 때 사용
4. <pre><code><meta charset="UTF-8"></pre></code>
웹 페이지의 문자 인코딩 방식을 utf-8로 지정
5. <pre><code><title></title></pre></code>
- 브라우저 탭에 표시되는 제목을 설정
6. <pre><code><body></body></pre></code>
- 브라우저에 실제 표시되는 내용
- 텍스트, 이미지 등 페이지에 표시되는 모든 콘텐츠
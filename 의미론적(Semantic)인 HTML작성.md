# 의미론적(Simantic)인 HTML 작성
## Simantic HTML?
div, span처럼 이름만 보고 어떤 내용인지 유추할 수 없는 태그가 아닌 **form, table,article** 등 의미가 있는 태그는 내용을 명확하게 정의
![simantic](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile30.uf.tistory.com%2Fimage%2F99C1E2495C61C8A3092560)

## Semantic HTML을 짜야하는 이유
+ 시각장애가 있는 사용자가 스크린 리더를 사용하여 페이지를 탐색할 때 도움이 된다.
+ 검색엔진은 태그를 기반으로 페이지 내 검색 키워드의 우선순위를 판단하기 때문에 SEO(Search Engine Optimization)을 향상시켜 웹 페이지의 방문자를 늘릴 수 있으며 SEO가 높을수록 웹사이트를 빠르게 식별할 수 있고, 중요한 정보에 적절한 가중치를 부여할 수 있다.
+ 코드의 가독성을 향상시켜준다.

## header
+ 페이지의 제목, 로고, 검색 폼과 같은 내용을 포함
```
<header>
<nav>
    <a href="#">야구<a>
    <a href="#">축구<a>
    <a href="#">e스포츠<a>
</nav>
</header>
```

## nav
+ 메뉴, 목차에 사용
```
<nav>
    <a href="#">야구<a>
    <a href="#">축구<a>
    <a href="#">e스포츠<a>
</nav>
```

## main
+ 가장 핵심적인 내용
```
<main>
    <section>
        <h1>Baseball</h1>
        <article>
            <p>baseball</p>
        </article>
    </section>
</main>
```

## section
+ 문서의 섹션을 알려줌
+ article 안이나 main 안에서 연관된 내용을 묶을 때 사용
```
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
</section>
```

## article
+ 독립적으로 배포, 재사용되도록 의도 된 문서
+ 독립적으로 읽을 수 있어야함
ex) 게시물, 신문 기사, 블로그 포스트
```
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
</section>
```

## aside 
+ 꼭 필요하진 않지만 부가적인 정보를 전달할 때 사용
```
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
    <aside>
        <p>sports</p>
    </aside>
</section>
```

## footer
+ 작성자에 대한 정보, 저작권 등을 포함
```
<footer>
    <p>Copyright KaKao Corp. All rights reserved.</p>
</footer> 
```
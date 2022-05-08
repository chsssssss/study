# 의미론적(Simantic)인 HTML 작성
## Simantic HTML?
div, span처럼 이름만 보고 어떤 내용인지 유추할 수 없는 태그가 아닌 **form, table,article** 등 의미가 있는 태그는 내용을 명확하게 정의
![simantic](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile30.uf.tistory.com%2Fimage%2F99C1E2495C61C8A3092560)
## Semantic HTML을 짜야하는 이유

## header
+ 페이지의 제목, 로고, 검색 폼과 같은 내용을 포함
<pre>
<code>
<header>
<nav>
    <a href="#">야구<a>
    <a href="#">축구<a>
    <a href="#">e스포츠<a>
</nav>
</header>
</code>
</pre>

## nav
+ 메뉴, 목차에 사용
<pre>
<code>
<nav>
    <a href="#">야구<a>
    <a href="#">축구<a>
    <a href="#">e스포츠<a>
</nav>
</code>
</pre>

## main
+ 가장 핵심적인 내용
<pre>
<code>
<main>
    <section>
        <h1>Baseball</h1>
        <article>
            <p>baseball</p>
        </article>
    </section>
</main>
</code>
</pre>

## section
+ 문서의 섹션을 알려줌
+ article 안이나 main 안에서 연관된 내용을 묶을 때 사용
<pre>
<code>
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
</section>
</code>
</pre>

## article
+ 독립적으로 배포, 재사용되도록 의도 된 문서
+ 독립적으로 읽을 수 있어야함
ex) 게시물, 신문 기사, 블로그 포스트
<pre>
<code>
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
</section>
</code>
</pre>

## aside 
+ 꼭 필요하진 않지만 부가적인 정보를 전달할 때 사용
<pre>
<code>
<section>
    <h1>Baseball</h1>
    <article>
    <p>baseball</p>
    </article>
    <aside>
        <p>sports</p>
    </aside>
</section>
</code>
</pre>

## footer
+ 작성자에 대한 정보, 저작권 등을 포함
<pre>
<code>
<footer>
    <p>Copyright KaKao Corp. All rights reserved.</p>
</footer>
</code>
</pre>
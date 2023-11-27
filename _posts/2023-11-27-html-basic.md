---
layout: post
title:  "HTML 구조와 기본 명령어"
date:   2023-11-27 09:57:13 +0800
categories: Web
tags: web html
---
**HTML (Hypertext Markup Language)**이란 웹 페이지 표시를 위해 개발된 지배적인 마크업 언어다. 
또한, HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공한다.

**마크업 언어**는 태그 등을 이용하여 문서나 데이터의 구조를 명기하는 언어의 한 가지이다. 

<h4>HTML의 기본 구조</h4>

Basic HTML Structure:
{% highlight python linenos %}
<!doctype html>
<html>
    <head>
    <meta charset="utf-8">
    <title>내가 처음 만드는 html 문서</title>
    </head>
    <body>
    <h1> 시간이란..</h1>
    <p>내일 죽을것처럼 오늘을 살고 영원히 살 것처럼 내일을 꿈꾸어라.</p>
    <img src="file_path", alt='test'>
    </body>
</html>
{% endhighlight %}

!doctype, html, head, body의 네 가지 태그를 이용해 문서의 시작과 끝을 표기한다.

+ <code><html></code> 태그: 웹 문서의 시작을 알리는 태그. 안에 사용할 언어도 표기 가능. <code><html lang="ko"></code>처럼
+ <code><head> 태그</code>: 웹 브라우저가 알아야할 정보 그리고 문서에서 사용할 외부 파일들의 링크
+ <code><meta> </code>태그: 문자 인코딩 및 문서 키워드, 요약 정보
+ <code><body> </code>태그: 실제 브라우저에 표시될 내용



<h4>주의 사항</h4>
+ 태그 내용은 소문자를 권장한다.
+ 여는 태그와 닫는 태그를 명확하게 표기한다.
+ 들여쓰기를 수행하여 가독성을 높인다.
+ 태그의 포함 관계를 명확하게 한다.

<h4>텍스트 관련 태그</h4>

Text 관련 태그:
{% highlight python linenos %}
<!doctype html>
<html>
    <head>
    <meta charset="utf-8">
    <title>텍스트 관련</title>
    </head>
    <body>
    <h1> 제목 1</h1>
    <h6> 제목 6</h6>
    <p>단락 변경</p>
    <br>줄 바꾸기. 닫는 태그가 없다.
    <blockquote cite="https://www.huxley.net/bnw/four.html">
        <p>Words can be like X-rays, if you use them properly—they’ll go through anything. You read and you’re pierced.</p>
        <footer>—Aldous Huxley, <cite>Brave New World</cite></footer>
    </blockquote>
    <strong>강조 한 번</strong>
    <strong><strong>강조 두 번</strong></strong>
    <b>굵은 글씨</b>
    <p>특정 글자를 <em>이탤릭</em>으로 표시한다.</p>
    <p>특정 글자를 <i>이탤릭</i>으로 표시한다.</p>
    <q> 짧은 인용 </q>
    <p>특정 글자를 <span><mark>하이라이트</mark></span> 표시한다.</p>
    <p><cite>www.google.com</cite></p>
    <p><small>글씨를 작게 표시</small></p>
    <p>텍스트<sub>아랫 첨자</sub></p>
    <p>텍스트<sup>윗 첨자</sup></p>
    <p><s>취소선 표시</s></p>
    <p><u>밑줄 표시</u></p>
    </body>
</html>
{% endhighlight %}







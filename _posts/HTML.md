---
layout: post
title: HTML 내용 정리
color: rgb(242,85,44)
tags: [websolute,html]
---

## HTML
HTML= Hyper Text Markup Language의 약자
웹 페이지를 만드는데 사용하는 아주 쉽고 중요한 언어이다.



## HTML의 기본 문법 - 태그(tag)
HTML에서는 "태그"라는 것을 이용한다.

기본 형태는 <태그> 내용 </태그> 형태이다.

추가로, 태그의 관계를 표현하기 위해 부모 자식이라는 표현을 사용한다.
태그 안에 태그가 있는 그림일 때 사용하는 표현.


+태그는 중첩해서 사용할 수 있다.
+태그는 내용을 설명하는 역할을 한다.

## HTML의 기본 문법 - 속성(attribute)
태그만으로는 우리가 원하는 모든 정보를 웹상에 담을 수 없다. 태그에 속성이라는 것을 더해 정보를 표현한다.

기본 형태는 src="정보"(소스) width="정보"(크기) 이다ㅏ.

## 웹 페이지의 기본 구조
<pre>
&lt;!doctype html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;title&gt;웹 페이지&lt;/title&gt;
  &lt;meta charset="utf-8"&gt;
&lt;/head&gt;
&lt;body&gt;
 본문 내용 ----
&lt;/body&gt;
&lt;/html&gt;
</pre>

## 배운 태그 정리
<pre>
&lt;u&gt; underline의 약자로 밑줄을 긋는다.

&lt;h1&gt;, &lt;h2&gt;, ..., &lt;h6&gt; heading의 약자로, 제목을 만들 때 주로 사용한다. 

&lt;strong&gt; 글씨를 굵은 글씨체로 바꿔준다.

&lt;ul&gt; unordered list 순서가 없는 리스트(목록)을 만든다.

&lt;li&gt; 리스트 만들기 

&lt;ol&gt; ordered list 순서대로 번호를 부여하는 리스트 만들기

&lt;br&gt; 줄바꿈 태그이다. *이 태그는 닫지 않는다. HTML에서 무엇인가를 설명하지 않는 태그들은 감쌀 필요가 없는 경우가 있다. ex)img, input,br, hr, meta등등

&lt;img&gt; 이미지를 추가하기 위해 사용하는 태그, 송

&lt;head&gt; 본문을 설명하기 위한 정보라는 것을 나타내는 태그. 머릿말이라고 생각하자
&lt;body&gt; 본문이라는 정보를 주기 위한 태그.
&lt;html&gt; head, body 태그를 감싸는 태그이다.

&lt;title&gt; 웹 페이지의 제목을 설정할 때 사용하는 태그이다. (검색엔진이 웹 페이지를 분석 할 때 가장 많은 비중을 가짐)

&lt;meta&gt; 웹 페이지를 작성할 때 코드의 작성 방식과 표현 방식을 맞춰주기 위한 태그. 
닫는 태그는 없다.

*&lt;a&gt; anchor의 첫글자이다. 링크를 나타냄. 
형태:&lt;a href="링크 주소" target="blank"&gt;

&lt;p&gt; 문단을 나누는 태그
&lt;script&gt; 자바 스크립트 언어를 사용하기 위해 사용하는 태그
</pre>

## 인깊문
적게 공부하고 많이 활용하기(통계에 기반한 학습)

검색과정도 프로그래밍이다 (검색 지향 프로그래밍)

가치있는 코드를 작성하자. 줄바꿈 태그와 단락 태그를 사용할 때 보기에는 같지만 코드가 가지고 있는 정보로써의 가치가 달라진다.

unslpash.com - 저작권 상관없이 자유롭게 이미지를 사용할 수 있는 사이트

웹 페이지를 작성할 때 한글이 써지지 않으면 작성 방식을 같게 해주어야 한다(UTF-8 기억)
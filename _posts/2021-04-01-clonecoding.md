---
layout: post
title: clone coding 1
color: rgb(242,85,44)
tags: [websolute,team]
---

노마드 코더 트위터 클론 코딩


## 시작
firebase 의 강력함!
백엔드 코드를 작성하지 않고 할거야

HTML CSS Github react , hooks 등등 을 배우고 오면 좋대

firebase란?
app을 만들 수 있어 
클라우드 저장공간, hosting = 배포할때 쓰는거 , authentication -> 이게 app 만드는걸 빠르고 쉽게 도와줌

경쟁사로 amplify 라는 것도 있는데 데이터가 부족해서 아직 좋지 않다는 듯

언제 사용하나?? -> 아이디어를 빠르고 값싸게 테스트해보고 싶을때 
데이터관리 권한이 절로 간다는듯

## 셋업

어떤 형태로 만들지 선택 가능

* create react app 사용할 때 REACT_APP 으로 시작하는 이름의 환경변수를 지정해 줘야함(.env 파일)

코드 안에 url이나 key 값들을 넣을 필요는 없다. (보안의 이유지만 완벽한 보안은 아님)

<>fragment 여러 요소를 넣고 싶은데 다른거 쓰기 싫을 때 사용


2. 
<footer></footer>? 이 뭐고 approuter쓰고 나서 다른걸 쓸수 있게 하는거

authService에 여러가지 있음 (여기선 currentUser 사용함)

firebase의 authentication에서 app 사용 설정을 수작업으로 할 수 있음.

깃험 개발 설정에서 새로운 github app 만들 수 있음

* onchange를 사용할 때마다 event가 사용됨 -> event로부터 target:{}을 받아와서 사용!! 하는거 이해하기

email auth provider (firebase) 이메일과 패스워드로 사용자를 만들고 로그인 시키는거!!

local 탭이 꺼져도 유저 정보 기억  ( 기본값이래 )
session 탭이 꺼지면 유저 정보 사라짐
none 기억 멈춰!

이대로 했는데도 로그인이 안된거 같다?? 
useEffect (시작할때 하는거!) , onAuthStateChanged(유저 상태에 변화가 있을 때  발생) 이용해서 수정 

signinWithpopup provider 만들고 , 로그인하기.
-> 이걸 이용해서 구글, 깃헙 계정이랑 연동해서 (social login) 로그인 가능!
쑤ㅖ에에에에엣


로그아웃하기 만들기
navigation만들기 (홈 가기, 프로필 가기 등)



redirect 새로고침 하면 어떤 경로로 보내 버리는거
useHistory = 기록 보고 홈으로 보내 버릴 수 있는거!




ES6??
async??
.



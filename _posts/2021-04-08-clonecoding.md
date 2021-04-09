---
layout: post
title: clone coding 2
color: rgb(242,85,44)
tags: [websolute,team]
---

## 3
같은 방식으로 home 에서 정보를 받아오는 툴을 만들자 
firebase에서 database를 테스트 모드로 생성 가능
(NOSQL database)
1. collection(폴더)
2. document (문서)
간단하게 어드민 상에서 이 두가지 요소를 만들고 설정가능

우리는 코드로 만들거임
export const dbService = firebase.firestore();
export이름.collection("경로").add(원하는 데이터) 
이러고 home에 작성해주면 
-> 귀신같이 클라우드에 정보가 가

다음은 트윗을 가져오는거
state 만들기. async써서 함수 만들기(dbservice의 collection, get을 써서 정보 가져오기) useEffect로 함수 부르기

* forEach 모든 데이터를 각각 처리함

트윗을 보이게 만들자
새 div를 만들어 map 함수 사용

이렇게만 하면 우린 새로고침을 해야 트윗이 갱신된다.


누가 로그인했는지 알아보자
어플리케이션은 모든 요소들의 위에 있음. 
uststate와 실행하면 시작되는 authservice를 이용해서 유저 정보를 받는다.
approuter로 보내고  home에 공유를 해주면 (props전달)  
이를 onsubmit에 넣어주면 nweet을 누가 썼는지 알려준다.



##
데이터베이스의 변화를 알 수 있는 방법
onSnapshot() 실시간으로 정보를 줌 -> 정보를 받아서 배열을 만들고 state에 배열을 집어 넣는다
->
doc 의 full map으로 Nweet component 만들어서 (snapshot.docs.map) 변수에 지정하면 원하는 rerender하지 않고 원소를 쉽게 가져올 수 있음
 그래서 새로고침을 안해도 트윗이 갱신됨
fire베이스 어드민에서도 바로 올릴 수 있음

--> 너무 실시간으로 볼수있음 채팅어플의 채팅을 수정하고 지우는것도 볼수 있대

## 트윗 수정하고 지우기
creater id가 있고, home이 userobj을 가지고 있으니까 home에 있다.
nweet에 isOwner prop을 추가하면 주인일때만 뜨는 내용을 만들 수 있음.


ok = confirm??물어보고 bool값 받아옴

이제 함수를 스슥 작성하고 id를 받아와서 .delete() 하면 사라짐. ㄷㄷ

수정하기
state 만들기  함수 만들기( 이전값을 받아오는데 그 이전값과는 반대 이건 무슨소린지 다시 봐)

3.6강에 복습있음!



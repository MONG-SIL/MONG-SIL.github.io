---
layout: post
title: local state
color: rgb(242,85,44)
tags: [websolute,team]
---

## LOCAL STATE
내가 직접 api에서 넘어온 데이터를 바꿀 수 있는거!
클라이언트에서 데이터를 받을 수 있음
예시 좋아요 표시!

resolvers 기본적으로 백엔드나 api에서  resolve하는 역할
client에서 필드를 resolve하는데 사용할거임
예를 들어 movie를 치려면 (api에 있는 타입 이름)에서 와야함

* 만들었으면 요청을 해야한다. gql이용해서 (이때 @client해서 클라이언트(프론트엔드)에 있다고 입력해야 오류 안뜸) !! 

cache를 잡아서 이용할 수도 있음


## local state 바꾸는 방법
client에 mutation을 생성해 바꿀 수 있다.
mutation(경로무시, parameter)-- grapgql resolver과 같이 동작
작성할 때 mutation도 @client에 있다고 알려줘야함

## 디테일 페이지 홈 페이지 연결
아폴로는 멍청해서 id가 없으면 작동을 안해
그래서 연결을 해야해
무비 리스트와 무비 디테일을 연동해야함 id로
같은 id를 요청하면 아폴로가 그제서야 알아들어


## 지식
Int Int! 다른점?
_ == whatever?



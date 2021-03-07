---
layout: post
title: React Hooks 3
color: rgb(242,85,44)
tags: [websolute,team]
---

- 2.5~

## useFadein ( hook + animation )
useRef, useEffect 사용 
fadein 함수에 delay 옵션을 주어 순서대로 나타나게 할 수 있음. 
property,duration,timing 등 설정 가능함
current.style.transition=opacity
current.style.opacity =

## useNetwork 
네트워크 변경시마다 창 띄워주기
useState, useEffect 사용
navigator.online 의 bool값을 이용

## useScroll
스크롤을 내리는 (y축)것에 따라 특수 효과
useState, useEffect사용
window. 중에 scrollY,scrollX가 화면상의 좌표를 뜻함

## useFullscreen
이미지를 전체화면으로 만들 수 있음
useRef 사용해 이미지의 ref를 받아 requestFullscreen 한다.

## useNotification
알림 실행 hook은 아님
Notification()

## useAxios (react4)
새로 import 해줘야함
axios는 약간의 변경을 허락한다는듯
axios는 url을 받아야함 
refetch : dependency에 trigger를 주어 재실행 가능

## 잡지식
opacity : 나타나는데 걸리는 시간을 뜻하는 것 같다.
window. document. 차이?
useNetwork에서 useEffect 안의 내용을 작성할 때 removeEvent~할때는 왜 앞에 return 작성 x인지
axios에서 optinon은 opts
${}는 대체 뭘까 , .then
date.now = 랜덤숫자 발생
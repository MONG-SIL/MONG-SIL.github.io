---
layout: post
title: React Hooks 3
color: rgb(242,85,44)
tags: [websolute,team]
---

## useEffect(중요)
* componentDidMount, componentDidUpdate 역할을 동시에 함.
* function형태의 effect, dependency 두 인자를 가지며 dependency는 그 인자가 바뀔 때만 실행되어 componentDidupdate 역할을 해준다는 것이다.
-

## useTitle
helmet을 사용한대 보통 
useEffect를 이용한다.

## useClick
references 에 대한 이해 : component를 찾기위한 주소 같은 느낌 (태그에 주소를 주면 접근 가능함) (useREf 추가)
.focus =get elementBYID랑 같다
* 정리: ref를 사용한 뒤 addEventListener를 이용해 이벤트를 추가한다. 하지만 이 event를 정리해줘야한다. dependency 에 []를 주어 함수가 한 번만 실행되게 한 뒤 return을 이용해 정리

## usePreventLeave, useConfirm
둘 다 useEffect, useState를 이용 x
- useconFirm : 사용자가 어떤 행동을 하기 전에 계속 할지 물어보는거
- usePreventLeave : 페이지를 떠나기 전 저장했는지 물어보는거 
* "beforeunload"는 window가 닫히기 전 함수 실행을 허락함
window.addEventListener
window.removeEventListener
* event.returnValue= ""; 라는 선언을 해줘야 크롬에서 정상적으로 작동.

## useBeforeleave
useEffect사용! dependency = []
document.addEventListner에 mouseleave 이용해 작성
검사의 속성에서 clinetY는 Y축인듯 하다 

## 잡지식
setTimeout 시간지연 함수
.js를 해서 저장하는 이유?
window. ??
* if(typeof 함수 !=="function"){
    return;
}을 통해 함수인지 확인하는 습관
addEventListener,removeEventListener 두 개의 인자를 받으며 하나는 조건, 하나는 함수로 보인다.

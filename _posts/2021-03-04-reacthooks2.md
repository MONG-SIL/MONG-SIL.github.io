---
layout: post
title: React Hooks -useState
color: rgb(242,85,44)
tags: [websolute,team]
---

## hooks
리액트의 기능중 하나이다.
functional component에서 state를 가질 수 있게 해줌
class component did mounmt render 등등을 사용하지 않아도 App을 만들 수 있게 해주는 것이라고 생각
* 필수는 아님

함수형 프로그래밍의 길-- 조금 더 효율적인 코드를 만드는 길

## useState
array(value ,setvalue)를 return하는 useState()를 사용해서 hooks사용 
- useState(1)[0]을 이용해서 item값만 사용 가능

## useInput
input을 update함
사용자가 실행한 event를 받아 사용할 수 있게 한다.
유효성을 검증하는 함수 validator 해서 글자수를 제한한다거나 할 수 있음

## useTabs
useState와 버튼을 사용해 원하는 content를 노출시킬 수 있는 행위, setstate공부 1-3 다시 보기 (난이도 겁나 높음)
## 공부
* arrow function 같은 역할인듯?
function App() {  }   /   const App = () => { }
input 태그 안의 {...name} 은 name안에 있는 모든 것을 풀어준다. 즉 name 안에 있는 모든 값을 풀어준다
! 반대라는 뜻 !value는 value 제외임
array.isarray()는 해당 인자가 array인지 구분
* setState는  새로고침을 해준다 (re render해준다)


* arrow function 질문
질문
I have a question.

button onClick={() => changeValue(index)}
it does work

button onClick={changeValue(index)}
it does not work

what's different?

답
serranoarevalo1 month ago
@gwcattower button onClick={changeValue(index)} is calling the function automatically.

button onClick={() => changeValue(index)}

is a function that calls a function.

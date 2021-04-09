---
layout: post
title: clone coding 3
color: rgb(242,85,44)
tags: [websolute,team]
---

4번
fire base storage 에서 bucket(파일을 넣는 곳) 생성 되어 있음

<input type="file" accept="image/*"> 이미지 파일을 선택해 입력 가능
+
 onChange={onFileChange} /> 속성을 넣어서 
 event.target.file 로 접근해 파일로 접근!

 fileReader API (파일 읽는 api)
 변수에 api 주고 .readAsDataURL(ES6 형식으로 만든 파일)

 이렇게 되면 result값으로 사진의 텍스트를 얻는다.

 이제 얻은 텍스트를 img태그로 살짝 미리 보기 시킬 수도 있음!

clear도 너무 간단하게 구현가능임

이제 이걸 bucket에 업로드
사진 업로드 -> url -> nweet에 추가
 
 storageService.ref().child(`이미지의 path를 넣어, ${uuid4()}`) 
 == collection이랑 비슷하게 이해 ,사진에 이름을 줄 수 있음 

putstring() 이미지텍스트를 아니까 이걸 쓸거야
put == 파일의 ref를 만들고, 업데이트 해서 사용 

일케 하면 유저 아이디로 구분해서 폴더를 만들고 거기에 이미지 파일이 storage로 업데이트 됨


w버그 걸려서 작업한게 다 날아갔다.
화가난다.

## nweet을 지울 때
reference에서 옵션이 있음
url만 알면 삭제 가능

storage에서도 refFromURL에 접근해서 삭제 가능이다.

## 5. 프로필을 가져오는거 
지금은 home 에서 스냅샷을 가져오는거
router은 userObj를 줌. 프로필에 prop으로 주자
이제 dbService를 호출해서 collection을 이용해 내 userObh를 받을 수 있음

* where()= 필터링 할거 알려줌 
* orderby 를 이용해 정렬가능임(오름차순, 내림차순 선택 가능)
-> firebase는 항상이런식으로 움직일 수 없음 -> 쿼리를 만들거라고 알려줘야한대 -> 오류의 링크타고 누르면 됨 그냥

## displayname
router에 있는 navigation을 이용해 userOBJ를 보내서 displayname을 전달할 수 있음(이러면 충분함)

filebase.user에서 유저 계정을 줌.
updateProfile. 을 이용하면 접근 가능 
즉 이렇게 유저 이름을 바꿀 수 있는데 새로고침을 해야만 이름이 보이는 걸 개선하고 싶어!

* userobj를 공유해서 사용하는 이유는 그게 정보를 다시 렌더링하는 것도 그렇고 하나가 바뀌면 전체가 바뀌어서 편하기 때문이야

## 이거 어려움
새로고침을 해야만 바뀌는걸 바꾸자
-> 변화를 줬는데 rerender안되는 이유?? 
-> rerender은 되는데 안바뀌는 이유??
-> currentuser 전체를 보면 react가 결정장애가 온다..?
->object 크기를 줄여주면 돼
-> setUserObj 에서 필요한것만 적어주고, 함수를 설정해줄거야(중간 함수래)
-> setUserObj 를 설정한걸 refresh한데 붙여주면 끝!






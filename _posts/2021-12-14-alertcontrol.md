---
layout: post
title: "Alertcontrol" 
subtitle:  "UIAlertController"
cover-img: /assets/img/c1.jpeg
thumbnail-img: /assets/img/d1.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

창작자가 앱사용자에게 무언가를 메세지를 주고 싶거나 이야기를 하고 싶을때 알림메소드인 UIAlertController를 사용합니다.
두가지 형태입니다. 하나는 알림창 (.alert)이고 하나는 액션시트(actionsheet)입니다.

알림창은 화면 중앙에 표시되고 액션시트는 하단에 표시됩니다. 또한 알림창은 모달방식이고 액션시트는 아닙니다.

알림창은 3가지로 구분되어 있습니다.
 객체 생성 -> 컨트롤러 등록  -> 메세지창 실행
 
 만약 사용자에게 입력 필드를 주고 싶으면 addTextfield함수를 추가하여 원하는 인스턴스 구문에 있는 클로저블록안에 추가합니다.
 
 첫번째버튼 함수를 보면 UIAertController를 선언하고 UIAlertAction 선언후 addaction으로 컨트롤러에 등록해 present메소드로 알림창을 실행합니다
 
 <img width="1050" alt="Screen Shot 2021-12-14 at 15 30 37" src="https://user-images.githubusercontent.com/40172001/145947315-afc52c9a-7540-4caf-91cf-6f73f718cfa9.png">

두번쨰는 addtextfield함수를 인용해 메세지 창에서 텍스트 필드를 추가합니다. 또하 isSecureTextEnrty는 입력된값을 별로 사용자에게 안보이게 처리하는 속성입니다.

<img width="1063" alt="Screen Shot 2021-12-14 at 15 30 49" src="https://user-images.githubusercontent.com/40172001/145947689-ed6e9876-edda-411d-ab95-da890c2dc911.png">

세번째는 간단한 로그인과정으로써 아이디와 패스워드가 맞으면 success 아니면 fail을 선언하는 구문입니다. 

<img width="1088" alt="Screen Shot 2021-12-14 at 15 32 15" src="https://user-images.githubusercontent.com/40172001/145947960-5055e3f4-e75f-4715-8b05-594043945664.png">




 초기화면 
 
 
 <img width="310" alt="Screen Shot 2021-12-14 at 15 56 49" src="https://user-images.githubusercontent.com/40172001/145948301-651d8715-b384-4bf2-9655-7e0eb47ff42f.png">

 
 첫번째 알림을 누르면
 
 <img width="318" alt="Screen Shot 2021-12-14 at 15 32 54" src="https://user-images.githubusercontent.com/40172001/145947163-23dbc4a3-4966-4dd7-8506-f85bd877c30e.png">

 
 
 두번째 알림을 누르면
 
 
<img width="314" alt="Screen Shot 2021-12-14 at 15 33 03" src="https://user-images.githubusercontent.com/40172001/145948457-3844a297-31ac-46e4-b604-7b297994704b.png">

 
 세번째 알림을 누르면
 
 
 <img width="316" alt="Screen Shot 2021-12-14 at 15 33 14" src="https://user-images.githubusercontent.com/40172001/145948095-ef53c379-12bd-4f11-a9cd-c0882e91b83e.png">

 
 세번째 알림에서 내가 지정한 iD와 password가 일치하면 success로 바뀌는 것을 볼 수 있습니다.
 
 <img width="329" alt="Screen Shot 2021-12-14 at 15 32 46" src="https://user-images.githubusercontent.com/40172001/145947036-8c11c44f-f6b1-44bf-b8f0-82123e8ad083.png">

 
 이로써 사용자에게 제작자가 알림을 줄 수 있다는 것과 간단한 로그인 방식에 관해서도 공부를 해보았습니다. 끝!

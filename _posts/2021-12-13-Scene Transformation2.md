---
layout: post
title: "scene Transformation2" 
subtitle:  "NaviGationController"
cover-img: /assets/img/castle3.jpeg
thumbnail-img: /assets/img/castle2.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


Navigation Controller

UINavigationController

네비게이션 컨트롤러는 뷰 컨트롤러를 직접 관리하고 뷰와 뷰사이의 구조를 관리하는 컨트롤러입니다.
계층적 구조르 가지고 있으며 루트뷰 -> 리스트뷰 -> 디테일 뷰로 이루어져 있습니다.

화면전환할떄에는 pushViewController(_:animated:)을 사용하고
반대로 돌아오려면 popViewController(animated:)을 사용합니다.

네비게이션 컨트롤러를 기본 컨트롤러인 뷰컨틀롤러에게 임베이드 인 시켜줍니다.

<img width="668" alt="Screen Shot 2021-12-13 at 23 23 13" src="https://user-images.githubusercontent.com/40172001/145830558-971f3eeb-50a5-45bf-823a-61000ada580a.png">


화면전환이 필요한 뷰 컨트롤러를 생성하고 화면전환을 하였는 지 확인 하기 위해 라벨링을 추가해줍니다

<img width="591" alt="Screen Shot 2021-12-13 at 23 23 30" src="https://user-images.githubusercontent.com/40172001/145830741-103fb939-91e2-4db7-8c44-d6108860143a.png">


뷰컨트롤러는 기본적으로 스토리보드와 짝궁입니다. 스토리보드아이디를 확인해주는것이 먼저이고
그 후 pushviewcontroller를 사용하여 화면을 전환합니다

<img width="1066" alt="Screen Shot 2021-12-13 at 23 22 03" src="https://user-images.githubusercontent.com/40172001/145830791-543723fd-4361-40e3-815a-e30ec79b4975.png">

세컨드 컨트롤러에서 다시 화면전환을 하려면
Popviewcontroller를 사용해야 다시 돌아갈수 있고
위에보이는 기본적으로 네비게이션 컨트롤러에서 제공하는 뒤로가기 버튼을 이용하여 전환할수도 있습니다

<img width="1018" alt="Screen Shot 2021-12-13 at 23 22 14" src="https://user-images.githubusercontent.com/40172001/145831507-dd269f22-35e2-4193-a49d-c73de993fc9e.png">

첫번쨰 화면
<img width="344" alt="Screen Shot 2021-12-13 at 23 23 47" src="https://user-images.githubusercontent.com/40172001/145831710-6c132ad7-69b5-49ff-8e55-7e1836b754f4.png">

두번째 화면

<img width="334" alt="Screen Shot 2021-12-13 at 23 23 56" src="https://user-images.githubusercontent.com/40172001/145831829-f875bb3f-6f55-40e9-9ed2-01277096b634.png">

다시  back이나 뒤로가기버튼을 누르면 초기화면으로 돌아갑니다

<img width="344" alt="Screen Shot 2021-12-13 at 23 23 47" src="https://user-images.githubusercontent.com/40172001/145832077-852bfa71-b81f-40d2-b2b1-dc66bf426704.png">

네비게이션 컨트롤러 

Finish!



---
layout: post
title: "generic"
subtitle:  "제너릭"
cover-img: /assets/img/b60.jpeg
thumbnail-img: /assets/img/b57.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


Generic


제너릭은 모드 타입에 유연하게 나타낼 수 있는 함수입니다.

예를 들어 코드를 보면 어떤 두가지 value를 바꾸는 함수를 만들면 int로 함수르 선언하여 만듭니다. 

int형으로 만든 함수가 돌아가게 됩니다.

<img width="724" alt="Screen Shot 2022-02-09 at 16 29 14" src="https://user-images.githubusercontent.com/40172001/153144840-a91760dc-12be-447e-b2d5-ca1a178adde0.png">


만약 double형의 함수를 구현하고자 하면 구현타입에 double을 명시합니다. 

그 후 함수를 실행하면 double 형으로 돌아가게 만들 수 있습니다.

<img width="750" alt="Screen Shot 2022-02-09 at 16 29 40" src="https://user-images.githubusercontent.com/40172001/153144864-bd5ee778-1278-488b-859e-1d4a261ef6a8.png">


하지만 모든 것을 아우르는? 제너릭함수는  보통 타입파라미터는 T를 씁니다
  
<img width="661" alt="Screen Shot 2022-02-09 at 16 29 54" src="https://user-images.githubusercontent.com/40172001/153144900-10c35063-2598-4361-9d03-8f885061ac22.png">

  
코드애 나와있는 것처럼 당연히 string 타입도 함수가 스스로 해내는 것을 볼 수 있습니다.

<img width="591" alt="Screen Shot 2022-02-09 at 16 30 06" src="https://user-images.githubusercontent.com/40172001/153144926-bce4a2d2-d719-409d-bd01-438bb34436fa.png">


 

---
layout: post
title: "Multi touch event"
subtitle:  "멀티 터치 이벤트 핸들링"
cover-img: /assets/img/e88.jpeg
thumbnail-img: /assets/img/e90.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Implementing a muiti-Touch

Photo1

<img width="322" alt="Screen Shot 2022-02-12 at 14 47 50" src="https://user-images.githubusercontent.com/40172001/153699359-6ce92daf-27f2-4bb0-ad6b-e8a8ae223e96.png">

Single main view가 각각 touch 장소에 회색 원으로 그려져
있고 터치가 끝나면 각 원은 사라지는 앱이다

-------------------------------

Photo2

<img width="754" alt="Screen Shot 2022-02-12 at 14 48 07" src="https://user-images.githubusercontent.com/40172001/153699364-384c5d3d-c724-418c-aebe-d27458c91012.png">

커스텀 서브클래스로 toruchableview를 설정하고 라벨도 넣어준다

Touchableview class  3가지 method

TouchesBegan(_: with :) - 각 이벤트 장소에 새로운 서브뷰를 만듬
TouchesMoved(_: with :) - 각 이벤트 장소에 새로운 장소를 업데이트
TouchesEnded_: with :) - 각 이벤트 장소에  관련된 서브뷰를 제거


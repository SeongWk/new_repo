---
layout: post
title: "초기화,상속,접근제어" 
subtitle:  "기본,멤버즈,등등"
cover-img: /assets/img/l877.jpeg
thumbnail-img: /assets/img/l878.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


initializer

이니셜라이저는 인스턴스 사용을 위해 초기화하는 것입니다.
init 키워드를 사용합니다.

![Screen Shot 2022-01-06 at 19 52 03](https://user-images.githubusercontent.com/40172001/148376726-659ae195-47ec-4101-b7e3-ae96916bbde1.png)


이니셜라이져를 통해 프로퍼티의 초깃값으 설정해 줄 수 있습니다. 
또한 이니셜라이져로 매개변수도 가질수 있습니다

![Screen Shot 2022-01-06 at 19 52 18](https://user-images.githubusercontent.com/40172001/148377213-6733832e-1e04-494a-82f0-8cb53c88418d.png)


이니셜라이저중  구조체는 기본 이니셜라이저와 멤버와이즈 이니셜라이즈가 있습니다
기본 이니셜라이저는 저장프로퍼티의 기본값으로 저장되어 있습니다.
멤버와이즈 이니셜라이저는 프로퍼티의 이름을 매개변수로 갖는 이니셜라이져 입니다.

<img width="819" alt="Screen Shot 2022-01-06 at 20 17 53" src="https://user-images.githubusercontent.com/40172001/148377154-8860736d-326f-479b-953b-22c7b5702c98.png">

반대로 클래스는 지정 이니셜라이저와 편의이니셜라이저가 주요 라이저입니다.
지정이니셜라이저는 모든 클래스가 하나의 지정이니셜라이즈를 가지고 있듯이 기본 라이저입니다
편의이니셜라이저는 지정이니셜라이저를 내부에서 호출하는 라이저입니다
편의 이니셜라이저는 앞에 convenience를 붙여줍니다.


<img width="779" alt="Screen Shot 2022-01-06 at 20 47 40" src="https://user-images.githubusercontent.com/40172001/148378800-4491980e-45fe-43a1-9152-66ec870faac0.png">

초기화 위임을 하기 위해서는 init앞에 self를 붙여주면 됩니다.


상속
inheritence

상속은 부모클래스로부터 자식클래스가 매서드나 프로퍼티를 받는 다는 것입니다.
상속받은 클래스를 자식클래스라고 이야기하고 상속하는 클래스를 부모클래스라고 합니다.

class 자식클래스:부모클래스
{
  코드
}

![Screen Shot 2022-01-06 at 15 59 17](https://user-images.githubusercontent.com/40172001/148377003-da698fd3-7f36-4c90-bd44-1fd4c8f519d2.png)




재정의
override

자식클래스는 부모클래스로부터 받은 특성들을 그대로 사용하지 아니하고 자신의 기능으로 변경하여 재정의할 수 있습니다.
만약 자식클래스가 부모클래스를 재정의한것을 부모클래스 그대로 사용하고 싶으면 super를 사용합니다

![Screen Shot 2022-01-06 at 16 14 30](https://user-images.githubusercontent.com/40172001/148377046-82114d53-0201-4b98-acb1-1229d98c96ca.png)
![Screen Shot 2022-01-06 at 16 15 04](https://user-images.githubusercontent.com/40172001/148377070-8a8ce621-dce5-4eb6-8e29-752794ac0107.png)

![Screen Shot 2022-01-06 at 16 15 10](https://user-images.githubusercontent.com/40172001/148377085-20ba663d-9997-4f82-9f06-b927af6d2bcc.png)

접근제어

access control

접근제어란 코드의 불필요한 접근을 막고 벽을 세우기위해서 만들어졌습니다.
다른 언어와 마찬가지로 외부에서 쓸 수 있는 것, 내부에서 쓸 수 있는 것, 내 자신홀로 쓸수 있는 것등
다양하게 구성되어 있습니다.

Private < internal < public < open

차례대로 비공개, 내부수준, 외부수준, 개방적 수준으로 이어집니다. 

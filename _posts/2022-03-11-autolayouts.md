---
layout: post
title: "autolayout" 
subtitle:  "apple developer document"
cover-img: /assets/img/q245.jpeg
thumbnail-img: /assets/img/q246.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

AutoLayout

자동레이아웃 = 오토레이아웃

오토레이아웃은 뷰를 계층적으로 사이즈에 맞게 계산하는 것

예를 들어 아이폰 8, 아이폰 11, 아이폰 13 pro or max에서 어떤 객체가 각각 크기가 다르게 변하지 않고  아이폰 크기에 
일정한 비율로 나오게 하는 것

만약 오토레이아웃을 하지 않는 다면 크기가 달라지고 위치가 바뀌고 나오지 않을 수 있다. 그런것으 위해 방지하려고 만든 그것

외부변화
- 사용자 윈도우 재조정
- 상용자 아이패드 스플릿 뷰 실행 전후 조정
- 기기 기울기 
- 엑티브된 통화 오디오를 recording bar에서 appear or disappear

내부변화
- 앱변화에 따른 컨텐츠 디스플레이 변화
- 앱 내부화 지원
- 앱 dynaminc type 지원


오토레이아웃은 사용자 인터페이스에 사용되는 제약을 정의시키고 계산한다.
제약은 보통 두가지 뷰 사이에서 관계를 나타낸다.

<img width="425" alt="Screen Shot 2022-03-11 at 23 15 44" src="https://user-images.githubusercontent.com/40172001/157884679-1a89b5a8-f9a7-4e07-a52a-b3f87177fa4e.png">

제약에 기반하여 각각의 뷰의 위치와 크기를 계산한다.


-------

제약없는 오토레이아웃

스택뷰를 통해 레이아웃을 조절

스택뷰는 UIStackview와 NSStackView가 있다.

스택뷰의 중요한 프로퍼티들

<img width="729" alt="Screen Shot 2022-03-11 at 15 45 33" src="https://user-images.githubusercontent.com/40172001/157884767-af2d9a69-9ff0-467e-801d-33d920454f13.png">


- axis:스택뷰의 방향성을 수직적으로, 수평적으로 정의(UIStackview에서만)
- orientation: axis와 같다(NSStackView에서만)
- distribution: axis에 따라 뷰를 정의
- allignment: 스택뷰 axis에따라 뷰를 정의
- spacing: 인접한 뷰 사이 공간을 정의

--------

레이아웃 계산법


<img width="632" alt="Screen Shot 2022-03-11 at 15 46 38" src="https://user-images.githubusercontent.com/40172001/157884810-a94fc230-41e8-4912-9b06-fd964f3269ab.png">

실제 계산식을 통해 어느정도 두 객체간 레이아웃을 표현가능

-------

레이아웃 속성

레이아웃에서 속성은 각 제약의 특징을 나타낸다. 

<img width="591" alt="Screen Shot 2022-03-11 at 15 47 07" src="https://user-images.githubusercontent.com/40172001/157884847-ee278743-cc56-4487-81fc-56555b1f3a34.png">


예를 들면 left,right, top, bottom,leading,trailing 등등


-------

인터페이스 빌더를 사용한 오토레이아웃


컨트롤 디버깅 제약

<img width="284" alt="Screen Shot 2022-03-11 at 23 11 12" src="https://user-images.githubusercontent.com/40172001/157884945-6b7c707c-d466-443c-9974-cfb84e788631.png">



스택,을, 핀, 리졸브 도구

<img width="186" alt="Screen Shot 2022-03-11 at 23 11 19" src="https://user-images.githubusercontent.com/40172001/157884969-af8e01a1-471d-4fce-9c3b-5c6307b42897.png">

스택:스택뷰를 생성


정렬: 레이아웃에 있는 아이템들을 정렬

<img width="426" alt="Screen Shot 2022-03-11 at 23 18 23" src="https://user-images.githubusercontent.com/40172001/157885107-284b2776-03c0-459b-becd-362f4b078397.png">

핀: 새로운 제약을 주고 싶거나 사이즈르 재정의할떄 사용,

<img width="372" alt="Screen Shot 2022-03-11 at 23 18 30" src="https://user-images.githubusercontent.com/40172001/157885139-63e85fa6-0820-4d1e-aede-d4e16f0a3768.png">

리졸브: 레이아웃 이슈들을 정리 및 fix

<img width="467" alt="Screen Shot 2022-03-11 at 23 19 23" src="https://user-images.githubusercontent.com/40172001/157885235-a1e4cf92-f4cd-4edb-b1b4-6cbd8c168100.png">


에디터디스플레이를 통해 제약을 볼 수 있다

<img width="513" alt="Screen Shot 2022-03-11 at 23 21 21" src="https://user-images.githubusercontent.com/40172001/157885550-d16ab1d0-11a7-486b-9b23-87906031d47a.png">


인터페이스 빌더에서 리스트로된 제약을 파일로 볼 수 있다.

<img width="439" alt="Screen Shot 2022-03-11 at 23 19 59" src="https://user-images.githubusercontent.com/40172001/157885388-329c5d84-3aef-42be-8519-0bbdad64c459.png">


사이즈인스펙터를 통해 제약을 확인가능하다

<img width="338" alt="Screen Shot 2022-03-11 at 23 20 08" src="https://user-images.githubusercontent.com/40172001/157885364-2fe24bad-9d24-4266-94c9-c6af46af0354.png">



오토레이아웃 간단정리

오토레이아웃은 레이아웃을 자동으로 계산하는 것

핵심

- 해당 뷰의 x,y, 위치
- 해당 뷰의 가로, 세로 크기

두가지를 지정해주거나 알려주면 컴퓨터가 알아서 레이아웃을 조정

Constraint 우선순위

- 각 constraint를 우선순위를 매길 수 있다.
- 1000이 가장 높고 낮은 거는 무시된다.

Hugging(허깅)

안으로 끌어안기는 것
- 공간이 낮아서 당겨지는 상황

Compression Resistance(컴프레션 레지스턴스)

밖으로 밀어내는 것
- 공간이 없어서 쪼그라드는 상황


이정도만 공부하였고 더 추가해야할 오토레이아웃 속성들이 넘쳐난다.

레이아웃 마진, 디버깅, 스크롤뷰, 제약 변경 등등 추가로 할 예정이다.

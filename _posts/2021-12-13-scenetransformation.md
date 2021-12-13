---
layout: post
title: "sceme Transformation" 
subtitle:  "view to view, Navigation, Segue"
cover-img: /assets/img/p1.jpg
thumbnail-img: /assets/img/effel.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


화면 전환은 3가지로 나눌수가 있습니다.

1. 뷰와 뷰사이 화면 전환
2. 네비게이션 컨트롤러를 사용한 화면 전환
3. 객체 세그웨이를 통한 화면전환


--뷰와 뷰사이 화면전환

-하나의 뷰 컨트롤러에서 이동할 뷰 컨트롤러를 호출해서 화면으 전환하는 방식으로 프레젠테이션이라고 합니다.

프레젠트 메소드라고 불리오는 present(_:animated:completion) 사용합니다.

<img width="1040" alt="Screen Shot 2021-12-13 at 21 55 42" src="https://user-images.githubusercontent.com/40172001/145817215-550da566-386f-483e-819f-e023d9162bab.png">

인스탠드뷰컨트롤러메소드는 스토리보드에서 뷰 컨트롤러와 연결된 클래스를 이어주는 메소드입니다.


<img width="1047" alt="Screen Shot 2021-12-13 at 21 55 53" src="https://user-images.githubusercontent.com/40172001/145817138-1d9632f5-784c-4219-8938-ffbfadf11c44.png">

만약 이전 화면으로 돌아가려면 dismiss(animated)을 사용합니다. 짝궁이라고 볼수?도 있습니다 :)


<img width="754" alt="Screen Shot 2021-12-13 at 21 56 57" src="https://user-images.githubusercontent.com/40172001/145817372-50fdde69-1215-4519-acb2-3f325e4a0f38.png">


뷰컨트롤러 객체를 사용할떄는 스토리보드아이디를 참조하여 갈지 안갈지 확인합니다.


<img width="320" alt="Screen Shot 2021-12-13 at 21 57 39" src="https://user-images.githubusercontent.com/40172001/145816766-d0686e9f-82b9-4be8-a325-ffb81f2c6804.png">

시작화면

next을 누르고 

<img width="319" alt="Screen Shot 2021-12-13 at 21 57 50" src="https://user-images.githubusercontent.com/40172001/145816983-1492b5ca-4217-4a99-aaed-4a336c7f1937.png">

다시 back 누르면

<img width="320" alt="Screen Shot 2021-12-13 at 21 57 39" src="https://user-images.githubusercontent.com/40172001/145817029-d96d0eae-26d5-4398-aadd-eccc0cc26bc8.png">




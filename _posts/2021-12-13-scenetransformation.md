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


뷰와 뷰사이 화면전환
-하나의 뷰 컨트롤러에서 이동할 뷰 컨트롤러를 호출해서 화면으 전환하는 방식으로 프레젠테이션이라고 합니다.

프레젠트 메소드라고 불리오는 present(_:animated:completion) 사용합니다.

만약 이전 화면으로 돌아가려면 dismiss(animated)을 사용합니다. 짝궁이라고 볼수?도 있습니다 :)

뷰컨트롤러 객체를 사용할떄는 스토리보드아이디를 참조하여 갈지 안갈지 확인합니다.

인스탠드뷰컨트롤ㄹ러메소드는 스토리보드에서 뷰 컨트롤러와 연결된 클래스를 이어주는 메소드입니다.


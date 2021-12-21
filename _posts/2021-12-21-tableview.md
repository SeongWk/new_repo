---
layout: post
title: "Table_view" 
subtitle:  "movie chart"
cover-img: /assets/img/p1.jpg
thumbnail-img: /assets/img/effel.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Talbe View

테이블 뷰 컨트롤러는 어떠한 목록에 관해 관리하기 좋으 컨트롤러입니다.
예를 들면 imusic이나 itunes같은 음악 목록이 좋은 예로 볼 수 있습니다.
테이블 뷰 컨트롤러는 테이블 뷰 컨트롤러, 테이블 뷰, 테이블 뷰 셀, 컨텐츠 뷰로 4가지로 구성되어 있습니다.

프로토타입 셀은 테이블 뷰에 있는 셀을 디자인 할 수 있는 객체입니다. 컨텐츠 영역과 악세서리 뷰로 이루어져있는데 
보통 컨텐츠뷰는 설명이 써있고 악세사리는 부가정보를 표시합니다

프로토타입셀을 설정할 수 있습니다.  basic은 조직은 갖추어져 있지만 자신이 원하는 모양이 나오지 않고 커스텀은 자신이 원하는 모양이 나오지만 하나씩
다 설정하고 연결해야하는 단점?이 있습니다. 

테이터 소스를 만들기 위해서 movie info swift파일을 생성합니다. 
왜냐하면 정보는 항상 갱신되거나 업데이트 되기떄문에 따로 소스가 필요하기 떄문입니다

기존컨트롤러 대신 listviewcontroller swift파일을 생성 한 후 UITableviewcontroller로 연결 시킵니다. 
테이블 뷰컨트롤러를 사용하기 위해서느 UITableviewController가 선언되어야만 합니다.

func tableview(numberofRowsInsection)은 테이블 뷰 내에서 몇번째 해당하는 뷰인지를 알려주는 함수입니다.
func tableview(cellForRowat)은 데이터 소스를 읽어오는 함수입니다.
dequeueReusablecell(identifier:)는 스토리보드에 정의된 셀을 찾고 인스턴스를 제공해줍니다.

movie2라는 스위프트 파일으 선언하여 라벨에 해당하는 아울렛함수를 선언해줍니다.
마지막으로는 추가로 썸네일 사진을 넣고 싶다라고 하면 imgaeview함수를 라벨링 옆에 넣어두고 UIimage함수로 자신이 원하는 테이블 뷰에 맞는 사진을 선언해 주면 완성됩니다.


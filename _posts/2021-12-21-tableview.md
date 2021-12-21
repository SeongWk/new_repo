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

저는 이번에 실습으로 커스텀으로 해보았습니다. 제가 볼 영화들 스파이더맨 매트릭스 킹스맨 영화포스터르 가지고 영화차트를 임의로 만들어 보았습니다.
영화사진은 썸네일 사진으로만 사용했습니다.

테이터 소스를 만들기 위해서 movie info swift파일을 생성합니다. 
이유는 정보는 항상 갱신되거나 업데이트 되기떄문에 따로 소스가 필요하기 떄문입니다

![Screen Shot 2021-12-21 at 17 05 21](https://user-images.githubusercontent.com/40172001/146894459-f3767e67-cd17-461a-8f08-9c0dfe93c5a4.png)



기존컨트롤러 대신 listviewcontroller swift파일을 생성 한 후 UITableviewcontroller로 연결 시킵니다. 
테이블 뷰컨트롤러를 사용하기 위해서느 UITableviewController가 선언되어야만 합니다.

![Screen Shot 2021-12-21 at 17 04 57](https://user-images.githubusercontent.com/40172001/146894493-d46af32d-9055-4878-8cba-69de3fb900ab.png)


func tableview(numberofRowsInsection)은 테이블 뷰 내에서 몇번째 해당하는 뷰인지를 알려주는 함수입니다.
func tableview(cellForRowat)은 데이터 소스를 읽어오는 함수입니다.

![Screen Shot 2021-12-21 at 17 05 07](https://user-images.githubusercontent.com/40172001/146894540-565cf741-8519-4650-bf7d-d71bd711d066.png)

dequeueReusablecell(identifier:)는 스토리보드에 정의된 셀을 찾고 인스턴스를 제공해줍니다.
사진에 나와있듯이 listcell로 설정해 두었습니다

![Screen Shot 2021-12-21 at 17 05 46](https://user-images.githubusercontent.com/40172001/146894691-514ed9d2-1976-46a9-82ef-16394220c217.png)


movie2라는 스위프트 파일으 선언하여 라벨에 해당하는 아울렛함수를 선언해줍니다.

![Screen Shot 2021-12-21 at 17 05 15](https://user-images.githubusercontent.com/40172001/146894575-cd93aa03-ea34-4eef-bbf1-774efab17197.png)


마지막으로는 추가로 썸네일 사진을 넣고 싶다라고 하면 imgaeview함수를 라벨링 옆에 넣어두고 UIimage함수로 자신이 원하는 테이블 뷰에 맞는 사진을 선언해 주면 완성됩니다.
또한 이미지를 넣고 싶으면 이미지 사진을 끌어와 참조해주는 방식으로 설정하면 됩니다.
![Screen Shot 2021-12-21 at 17 14 11](https://user-images.githubusercontent.com/40172001/146894856-773ef945-8439-4f00-a6e1-1d3bf8089b75.png)
![Screen Shot 2021-12-21 at 17 14 23](https://user-images.githubusercontent.com/40172001/146894875-4890bec1-91b6-4d12-916a-6656d2d66f82.png)

초기화면

![Screen Shot 2021-12-21 at 17 05 55](https://user-images.githubusercontent.com/40172001/146894990-001cbf19-257e-4e0a-a3fd-43c0670b5fc7.png)

사진에 나와있듯이 썸네일 ㅅ

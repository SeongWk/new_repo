---
layout: post
title: "Tabbaritem,navi cusom" 
subtitle:  "no storyboard"
cover-img: /assets/img/l23.jpeg
thumbnail-img: /assets/img/l22.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

tabbar를 커스터마이징과 navigation 커스터마이징

보통 탭바컨틀롤러 실행시킬 떄 스토리보드를 통해 라벨, 버튼, 텍스트필드등으 입력시켜 각 뷰컨트롤러에 해당하는 객체를 생성합니다.

그 후 객체에 맞는 액션함수를 실행시키거나 보여주기하여 탭바에 이로운점을 이야기합니다.

이것도 마찬가지로 스토리보드없이 해보겠습니다.

여기서는 Delegate부문입니다 ios는 앱 라이프사이클을 두개로 나뉘었는데 app delegat와 scene delegat입니다.

app delegate는 말 그대로 앱이 켜있을때부터 꺼질떄까지의 라이프사이클을 관리하고 scene delegate는 씬 말 그대로 뷰 ui lifecycle을 관리하는 delegate로 나뉘었습니다.

저는 여기서 기존의 delegate보다 커스텀 delegate를 선언하였습니다.

탭바컨트롤러 선언후 view 컬러와 루트뷰를 설정하여 줍니다. 스토리보드에서 했던거와 같이..

씬으 관리하고 있기 떄문에 탭바아이템을 선언하는 곳도 이곳입니다. 

![Screen Shot 2022-01-17 at 20 58 32](https://user-images.githubusercontent.com/40172001/149768029-b43a8f4b-58ec-4f6a-98f1-43dccc2d8729.png)

그리고 혹시나 잘못 설정하였을 수 있기에 각 뷰는 뷰컨트롤러파일으 가집니다. 당연히 3개를 더 만들어줍니다.
또한 뷰상태변경으 표시하기 위해 라벨링을 추가하고 addsubview로 타이틀을 표시홰줍니다.

![Screen Shot 2022-01-17 at 20 58 49](https://user-images.githubusercontent.com/40172001/149768051-70a3d2d9-bc96-42df-bcd8-aa7c6eb61dc3.png)

![Screen Shot 2022-01-17 at 20 59 00](https://user-images.githubusercontent.com/40172001/149768102-08269239-4d51-4807-9c7d-e0fa76bd0b68.png)

![Screen Shot 2022-01-17 at 20 59 06](https://user-images.githubusercontent.com/40172001/149768122-0e5d9b03-6631-44bb-b870-249551115036.png)

첫번쨰화면 

![Screen Shot 2022-01-17 at 20 59 41](https://user-images.githubusercontent.com/40172001/149768294-11a6bee8-d202-423f-8ec6-3f1a71938e6b.png)

두번쨰화면 

![Screen Shot 2022-01-17 at 20 59 48](https://user-images.githubusercontent.com/40172001/149768303-6dde2712-ac8e-481b-9991-97305a7fca26.png)

세번쨰화면

![Screen Shot 2022-01-17 at 20 59 55](https://user-images.githubusercontent.com/40172001/149768312-e6b92d8c-408f-42dd-87bc-674e00d85695.png)

스토리보드없이 탭바컨트롤러도 커스텀마이징을 할 수 있습니다.!!



두번쨰로는 네비게이션입니다.

스토리보드해서 만들어지는 기존 컨트롤러는 재미가 없습니다.


구글에 있는 알림창을 비슷하게 만들어보았습니다.
구조를 보면 뒤로가기 텍스트창 더보기창이 있습니다. 
또한 인터넷주소를 쓸 수 있는 텍스트필드와 라벨링을 추가하면 됩니다.


텍스트필드 추가 ->  뒤로가기 추가 ->  라벨링 추가 -> 더보기 추가로 이루어져 있습니다.
커스텀마이징을 할때 navigationitem에 구조를 찾을 수 있는데
가운데가 title view,  왼쪽이 leftitem, 오른쪽이 rightitem 분리해져 있습니다.
부분에 맞게 라벨링과 버튼 혹은 이미지를 커스텀마이징을 해야합니다.
 
![Screen Shot 2022-01-17 at 21 01 22](https://user-images.githubusercontent.com/40172001/149769432-c468d951-0cf4-422f-ab0c-354edbe8365e.png)


결과화면

![Screen Shot 2022-01-17 at 21 01 52](https://user-images.githubusercontent.com/40172001/149769449-e9bd76af-e59d-4299-805a-54c6c45b151e.png)

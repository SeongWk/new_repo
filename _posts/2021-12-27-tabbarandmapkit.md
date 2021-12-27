---
layout: post
title: "Tab Bar and Mapkit" 
subtitle:  "inappframework"
cover-img: /assets/img/c1.jpeg
thumbnail-img: /assets/img/d1.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Tab Bar controller는 수평적 관계로 각 화면의 접근할 수 있느 컨트롤러입니다.
다른 컨트롤러를 방해하지 않고 각각 움직일 수 있는 형태입니다.

스토리보드에서 보통 맨앞에 위치하며 모든 것을? 지휘하는 지휘자 역할이기도 해요

tabbar는 navigation컨트롤러와 유사하지만 바(bar)로 나타낸다는 것이 특징이고 
다른 탭으로 화면을 전환할 수 있습니다.
UITabBarcontroller에 정의되어 있습니다.

각각의 탭마다 루트뷰 컨틀롤러 직겆 연결되고 보통 네비게이션컨트롤러를 추가하면 
같이 뷰컨트롤러도 딸려?나오기 떄문에 굳이 뷰컨트롤러를 다시 로드할 필요가 없습니다.

연결하는 방법은  tabBarcontroller에서 드래그를 한뒤 viewcontrollers를 선택하면 됩니다.
추가하는 동시에 자동으로 탭바에는 새로운 탭(baby?)가 생겨납니다.

탭바는 순서를 변경할 수 있고 아이콘을 바꾸거나 원하는 이미지로 표시할 수 도 있습니다.
저는 영화관정보를 제공하는 목표로 탭바를 이용해 목록화면을 실행해보고자합니다.

![Screen Shot 2021-12-27 at 16 22 39](https://user-images.githubusercontent.com/40172001/147446308-228910a9-3f76-446b-a37b-18a45fefaca7.png)

탭바를 임베디드하여 각 뷰컨트롤러와 연결시킨후 segue를 형성합니다.

![Screen Shot 2021-12-27 at 16 24 00](https://user-images.githubusercontent.com/40172001/147446669-7e3ff48c-b863-4453-82ad-91d4d131c452.png)

네비게이션 컨트롤러를 하나 더 만들어 label를 설정해줍니다.

![Screen Shot 2021-12-27 at 16 23 16](https://user-images.githubusercontent.com/40172001/147446422-4f227a27-959e-4ed2-8d08-b3c0ad2252de.png)

영화 정보를 불러들어오는 것과 마찬가지로 api를 받고 json파일을 앱에서 읽어들일수 있게 데이터로 바꾸어 해당하는 정보에 일치시킵니다

![Screen Shot 2021-12-27 at 16 23 24](https://user-images.githubusercontent.com/40172001/147446621-d3c267c7-4346-49bc-b187-088c44bf28c9.png)

api에 담겨져있는 상영관명,주소,연락처가 개시된 data를 실제 뷰컨틀롤러와 연결시켜 사용자에게 보여주게 합니다.

![Screen Shot 2021-12-27 at 16 31 50](https://user-images.githubusercontent.com/40172001/147447062-4f0b84bd-17d0-46cf-bf0d-335e37ce12a7.png)

앱을 실행시킨 후 옆에 탭을 눌러보면 영화관정보가 나오는 것으 볼 수 있습니다.

mapkit

맵킷을 말 그대로 맵을 보여주는 프레임워크입니다,.
맵킷을 실행하고 싶을 떄는 import mapkit을 한 뒤 사용하는 것입니다.

자신이 원하는 장소의 지도를 보여주는 view로써 다양하게 쓰입니다.

저는 영화관 지도를 보여주는 것을 해보겠습니다.

![Screen Shot 2021-12-27 at 16 35 25](https://user-images.githubusercontent.com/40172001/147447565-7c7e6a3b-9255-4f38-afec-40c853d7de21.png)

뷰컨트롤러를 옆에 추가한후 mapkiit을 뷰컨틀롤러 안에다가 배치시킵니다.

![Screen Shot 2021-12-27 at 16 35 25](https://user-images.githubusercontent.com/40172001/147447862-41997c6f-9c67-42c6-8364-f198368f964a.png)


저번에 배웠던 peformsegue를 사용하기위해 identifier을 지정시킨뒤에 segue를 설정합니다.

![Screen Shot 2021-12-27 at 16 35 07](https://user-images.githubusercontent.com/40172001/147447852-e9c67e85-3d68-4dab-9441-f610757a1b4b.png)


위도와경도,지도데이터를 가져와 화면에 보여줍니다.

![Screen Shot 2021-12-27 at 16 34 52](https://user-images.githubusercontent.com/40172001/147447839-f4de27e9-8e5d-4e2f-8b35-86af5f17c933.png)


실행된 화면

![Screen Shot 2021-12-27 at 16 35 44](https://user-images.githubusercontent.com/40172001/147447815-75aae5bd-bb1a-410e-8ad6-08e3d965d3ab.png)

finish!

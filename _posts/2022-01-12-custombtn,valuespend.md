---
layout: post
title: "custombtn,valuespend" 
subtitle:  "No_storyboard"
cover-img: /assets/img/aa124.jpeg
thumbnail-img: /assets/img/aa123.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

스토리보드 없이 프로그래밍 방식으로 버튼과 valuespend만들어보기

1.버튼 만들어보기

![Screen Shot 2022-01-12 at 21 11 30](https://user-images.githubusercontent.com/40172001/149138572-fb49b595-75f5-4c05-bd29-5ff3195f9ae7.png)

스토리보드르 사용하지 않는 것으 기본으로 합니다.
그렇기에 모든 것을 다 스스로 채워넣어주어야합니다.
btn객체 생성 -> .frame(CGRect)으로 객체 특성 설정 -> settitle,center을 설정 -> view.addsubview로 화면에 나타내기를 설정합니다.

스토리보드와 마찬가치로 액션변수를 설정하기 위해 addtarget메소드를 설정하고
touchupinside로 터치 후 바로 보여줍니다
액션함수를 설정하기 위해 btnonclick함수를 생성하고 버튼을 누르고 난후 설정을 합니다
여기서는 클릭이라는 단어를 나타내개했습니다

![Screen Shot 2022-01-12 at 21 12 23](https://user-images.githubusercontent.com/40172001/149139189-acbf2cbb-06d4-465f-8927-1cb1136596a0.png)

![Screen Shot 2022-01-12 at 21 12 31](https://user-images.githubusercontent.com/40172001/149139195-ce97b002-6569-4943-a363-b7c74d6c92c6.png)

2. 값을 실제로 전달해보기

이메일과 업데이트 설정 갱신주기를 넘기는 예제를 만들어보았습니다.

![Screen Shot 2022-01-12 at 21 23 00](https://user-images.githubusercontent.com/40172001/149140143-896731cf-fb20-489c-bee4-f451e37e1f0c.png)

스위치, 스테퍼, 텍스트필드 변수를 선언하고 이메일라벨링과 인터벌 라벨링을 선언해줍니다
1번과 마찬가지로  라벨링 선언 -> 크기,이름,폰트를 설정 -> view,addsubview로 컨트롤러에 추가해줍니다.

![Screen Shot 2022-01-12 at 21 23 24](https://user-images.githubusercontent.com/40172001/149140800-c6bbf05d-ebac-4418-8b59-d02b9fea575b.png)

텍스트필트,스위치,스테퍼설정과  업데이트 와 인터벌 확인 라벨링을 해주어야 합니다. 
중요한건 스위치와 스테퍼는 액션함수를 추가해주어야 하기 떄문에 addtarget을 추가해줍니다.

![Screen Shot 2022-01-12 at 21 23 48](https://user-images.githubusercontent.com/40172001/149142038-b988380a-8703-4214-9925-9e4e5ab189e5.png)

각 변수에 맞는 액션함수 설정 후
 Value spend를 하기 위해  submit를 추가해줍니다.
여기서 가져갈 파라미터를 설정해주고 pushviewcontroller로 값을 readviewcontroller로 내보냅니다.

![Screen Shot 2022-01-12 at 21 23 58](https://user-images.githubusercontent.com/40172001/149142183-de7ff047-7014-4e82-866b-1ab212eadbd3.png)

모든 뷰컨트롤러는 하나의 스위프트 파일을 갖고 있기 때문에 새로운 파일을 추가해줍니다.
readviewcontroller에서는  좀전에 submit액션이 가져온 파라미터를 받기 위한 변수를 선언하고 마찬가지로 필요한 라벨링과 설정을 한뒤에
readviewcontroller에 있는 변수와 submit파라미터를 맞춘 후 addsubview로 화면에 나타내개 합니다

![Screen Shot 2022-01-12 at 21 22 21](https://user-images.githubusercontent.com/40172001/149142217-b898b42d-41ad-4de5-b4fa-7a45501aee67.png)

초기화면 

![Screen Shot 2022-01-12 at 21 24 08](https://user-images.githubusercontent.com/40172001/149142328-1b9c6e9e-da0b-4a7d-8023-f96dea0c0b85.png)


값을 설정한 후


![Screen Shot 2022-01-12 at 21 24 28](https://user-images.githubusercontent.com/40172001/149142349-9317f48c-1e57-4f8c-a70c-acde7b6d82b0.png)

결과화면

![Screen Shot 2022-01-12 at 21 24 37](https://user-images.githubusercontent.com/40172001/149142365-4d1f8460-66bc-49e8-a151-bc27737e3551.png)

버튼설정하는 것과 똑같이 스토리보드없이 커스터마이징 방식으로 설정해보았습니다.

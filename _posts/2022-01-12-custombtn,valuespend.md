---
layout: post
title: "custombtn,valuespend" 
subtitle:  "No_storyboard"
cover-img: /assets/img/l877.jpeg
thumbnail-img: /assets/img/l878.jpeg
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


---
layout: post
title: "ImagePicker" 
subtitle:  "Pick me Pick me Pick me One!"
cover-img: /assets/img/c12.jpeg
thumbnail-img: /assets/img/c13.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


이미지피커 컨트롤러는 말 그대로 카메라나 앨범에서 이미지를 선택하여 사용하는 컨트롤러입니다.

여기서 추가로 델리게이트 패턴을 사용합니다,
델리게이트패턴은 간단히 설명하자면 누군가가 무엇을 하기 전에 먼저 물어보거나 아님 관련된 메소드를 델리게이트를 통해서 전달하여 사용하는 패턴입니다.
주로 앞에 설명했던 텍스트필드도 사용하지만 이미지피커에서도 사용됩니다.


사용하려면 UIViewController옆에 UIImagePickerControllerdelegate와 UINavigationControllerdelegate를 추가합니다.


<img width="1143" alt="Screen Shot 2021-12-15 at 16 31 49" src="https://user-images.githubusercontent.com/40172001/146143651-52c3c1c2-d1b3-4eef-a281-d15fd2d06021.png">

그리고 보안문제로 인해 info 에서 Camera Usage Description과 photo library Usage Description도 허용이 필요해서 type을 yes로 바꿔줍니다.

<img width="692" alt="Screen Shot 2021-12-15 at 16 39 21" src="https://user-images.githubusercontent.com/40172001/146143768-0eefa2b9-6125-4df5-914d-f01c92b2f608.png">

self.delegate = self로 바꿔줘야 delegate를 거쳐갈 수 있습니다 중요한 구문입니다.

자신이 원하는 함수를 선언해줍니다 UIImagePickerDelegate에 나와있습니다.

<img width="1020" alt="Screen Shot 2021-12-15 at 16 32 32" src="https://user-images.githubusercontent.com/40172001/146143961-e20d0f16-8e55-46a8-a431-7ca6a1e46d9c.png">



초기화면
<img width="314" alt="Screen Shot 2021-12-15 at 16 33 19" src="https://user-images.githubusercontent.com/40172001/146143228-3b4f0e2c-d064-47f8-bd82-4d1fdb120ffd.png">


초기화면에서 버튼을 누르면 사진을 고를 수 있는 선택창으로 넘어갑니다

<img width="312" alt="Screen Shot 2021-12-15 at 16 33 35" src="https://user-images.githubusercontent.com/40172001/146143262-c2894aa3-50da-46c1-9aee-4c819f8e2088.png">

예를 들면 폭포사진을 선택합니다


<img width="315" alt="Screen Shot 2021-12-15 at 16 33 44" src="https://user-images.githubusercontent.com/40172001/146143386-18c74e3b-792e-4573-a194-770eb50eb4df.png">

초기화면에는 이미지뷰에 폭포사진이 나오게 되는 걸 볼 수 있습니다

<img width="315" alt="Screen Shot 2021-12-15 at 16 33 52" src="https://user-images.githubusercontent.com/40172001/146143463-4f8a848a-1a00-465f-99ba-c58f44b41f15.png">

다른 사진을 고르면 

<img width="318" alt="Screen Shot 2021-12-15 at 16 34 06" src="https://user-images.githubusercontent.com/40172001/146143489-0549b445-35dd-4d70-8958-46665cf36ee0.png">

다르게 나옵니다

이미지피커는 다양하게 사용됩니다




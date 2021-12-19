---
layout: post
title: "value spend" 
subtitle:  "view to view, navigation"
cover-img: /assets/img/castle3.jpeg
thumbnail-img: /assets/img/castle2.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


값을 전달해보는 실습을 해보겠습니다.

view to view

이메일입력과 자동갱신, 자동갱신 주기를 설정해보는 데모앱입니다.

처음 scene을 설정합니다.

![Screen Shot 2021-12-20 at 1 41 25](https://user-images.githubusercontent.com/40172001/146683688-722b7b7d-fd0d-44d3-99f6-6ef3e9a3e912.png)

스토리보드id를 설정합니다 저번에 이야기하였듯이 컨트롤러하나당 스토리보드 id를 하나 설정하는 것이 짝궁이라고 말했습니다.

![Screen Shot 2021-12-20 at 1 43 43](https://user-images.githubusercontent.com/40172001/146683706-e3e7fd8a-ed57-487d-a6f3-12f4886c7453.png)

각각의 버튼을 해당하는 값을 선언해줍니다 view to view이기 때문에 present함수를 사용합니다

![Screen Shot 2021-12-20 at 1 42 42](https://user-images.githubusercontent.com/40172001/146683766-3b191c1e-1579-4176-b9b9-f036041dd746.png)

go 버튼에서 받을 파라미터를 설정하고 videoload함수에 선언합니다 이유는 오버라이딩된 함수의 값을 다운캐스팅에서 바로 받아야되기 때문에 videoload에다가 선업합니다.
받을 값을 변수에 저장해두고 다시 반대로 돌아가기위한 버튼도 선언합니다.
back버튼은 dismiss를 사용합니다.

![Screen Shot 2021-12-20 at 1 42 50](https://user-images.githubusercontent.com/40172001/146683794-85f182c6-8f6f-4d85-b8c1-a0465adf5633.png)

처음화면입니다

![Screen Shot 2021-12-20 at 1 44 24](https://user-images.githubusercontent.com/40172001/146683896-91b4eb7e-ee64-4dc1-a51f-1b7b3cec1be5.png)

google.com과 갱신못함 갱신주기를 2분으로 설정합니다

![Screen Shot 2021-12-20 at 1 44 52](https://user-images.githubusercontent.com/40172001/146683936-83d8ac1f-473a-4c21-9629-96faf3e62c7d.png)

결과화면

![Screen Shot 2021-12-20 at 1 45 00](https://user-images.githubusercontent.com/40172001/146683951-f8bf775e-4255-4da8-b26b-a932885d744d.png)

다시 back버튼을 누르면

![Screen Shot 2021-12-20 at 1 44 52](https://user-images.githubusercontent.com/40172001/146683959-94259cce-d5e5-485f-a45b-906cc802714f.png)

다시 자신이 원하는 이메일을 설정할 수 있습니다.

Navigationcontroller로 값 전달해보기

바뀌는 값은 별로 없습니다 몇가지만 설정하면 다를께없습니다.
네비게이션 컨트롤러를 임베디드 하고 을 네비게이션 버튼으로 올려 설정합니다

![Screen Shot 2021-12-20 at 2 09 42](https://user-images.githubusercontent.com/40172001/146684034-44f56d7a-64ea-4afd-aa6f-f399a7c610c8.png)

present함수 대신 네비게이션 컨트롤러에서 사용하는 pushViewController함수를 사용합니다

![Screen Shot 2021-12-20 at 1 54 31](https://user-images.githubusercontent.com/40172001/146684048-d8c0c042-6c7c-41b6-93ef-6ed0f9f7bdc8.png)


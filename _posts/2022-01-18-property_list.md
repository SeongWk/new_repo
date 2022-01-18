---
layout: post
title: "Property_List" 
subtitle:  "UserDefaults,custompropertylist"
cover-img: /assets/img/y78.jpeg
thumbnail-img: /assets/img/b56.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

애플은 비교적 간단한 데이터를 xml에 맞추어 key-value로 저장하고 있습니다.

프로퍼티리스트는 xml형식의 데이터저장소?라고 부를 수 있습니다.

딕셔너리 방식이기도 한 프로퍼티 리스트의 데이터 타입은 두가지 입니다. 

원시타입(int,string,float...)과 레퍼런스 타입(NSString,NSData,CFArray..)-> 파운데이션, 코어파운데이션 이 있습니다.

또한 프로퍼티리스트는 앱의 공통 데이터나 정보를 저장하는데 쓰이고 있습니다.

보통 xml을 구상하려면 xml version utf-8을 선언...-> 전체적으로 xml을 선언해야하지만

애플은 쉽게 xcode에서 리스트를 편집할 수 있는 도구를 가지고 있습니다. 바로 info.list라는 파일입니다.

간단한 예제를 만들어보겠습니다.

new file로 list파일을 추가해줍니다. 
user라고 지칭한 후 노드라고 불리우는 데이터목록에 자신이 원하는 키와 값을 적어줍니다.

만약 타입을 array라고 선언해주면 그 array에 해당하는 키와 값을 입력할 수 있게 나와 있습니다.

모든것이 끝나면 user.list에서 오른쪽 버튼을 클릭하여 실제 소스코드를 보면 xml코드로 깔끔?하게 나오는 것을 볼 수 있습니다.

<img width="691" alt="Screen Shot 2022-01-18 at 22 24 56" src="https://user-images.githubusercontent.com/40172001/149945850-6938d895-945f-43c8-9717-65ff1eb1e176.png">

<img width="463" alt="Screen Shot 2022-01-18 at 22 25 13" src="https://user-images.githubusercontent.com/40172001/149945792-6dad9e21-2273-4c00-a498-0db0d08df0c7.png">

<img width="635" alt="Screen Shot 2022-01-18 at 22 24 44" src="https://user-images.githubusercontent.com/40172001/149945819-62c09762-edae-4006-b5c9-54ae360c4713.png">

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



두번째로는 userDefaults입니다

ios에서는 기본적으로 저장소를 다룰 수 있도록 userdefaults를 제공합니다.

userdefaults의 주요메소드는
set(_value, forKey:  _value )입니다.

사용자 정보를 저장하는 예제를 만들어보겠습니다.

레이블과 세그먼트, 스위치 컨트롤을 선언하고 액션메소드도 선언합니다

<img width="578" alt="Screen Shot 2022-01-18 at 22 40 57" src="https://user-images.githubusercontent.com/40172001/149949144-5414183b-094b-4cee-a4cf-31866a64a3cb.png">


<img width="903" alt="Screen Shot 2022-01-18 at 22 42 17" src="https://user-images.githubusercontent.com/40172001/149949189-62d7e35a-a112-4804-9d1a-017bf060d3d5.png">


UIAlertController로 첫번쨰 셀을 클릭할때만 글자를 바꿀 수 있는 메소드를 작성합니다. 

여기서 가장 중요한 저장 구문에서 보면
 Name , sex, marriage를 키로 하는 저장 구문을 구현하게 됩니다. 
 
.syhchronize() -> 동기화 처리 구문입니다.

<img width="943" alt="Screen Shot 2022-01-18 at 22 42 31" src="https://user-images.githubusercontent.com/40172001/149949269-2959550c-1300-4613-a255-da0db9d061bf.png">


마지막으로 수정된값을 실제레이블에 적용한다는 구문을 적고 바로 적용되는 현상을 볼 수 있고요

또한 다음에 열때 저장된데이터를 열기 위해 저장된 값을 꺼낼 수 있게 forkey값을 설정하게 되면!

<img width="855" alt="Screen Shot 2022-01-18 at 22 41 51" src="https://user-images.githubusercontent.com/40172001/149949328-1364a22b-fe73-4095-933a-f3dff12fe2e9.png">

계속 켤때마다 그 전에 저장된 값이 나오고 다시 바꾸게 되면 다시 킬떄  바꾸었던 값이 나오게 됩니다.

Jenny, female, marriage o 으로 설정한 초기화면

<img width="314" alt="Screen Shot 2022-01-18 at 22 44 00" src="https://user-images.githubusercontent.com/40172001/149950100-71230124-8de9-4a19-9218-a3577105e511.png">


첫번쨰 셀을 클릭한 후 Tom으로 바꿉니다.

<img width="309" alt="Screen Shot 2022-01-18 at 22 44 11" src="https://user-images.githubusercontent.com/40172001/149950125-b71710a5-9443-41fd-ad88-1a0b73f64758.png">


또한 male, marriage x 으로 바꿉니다.

<img width="321" alt="Screen Shot 2022-01-18 at 22 44 24" src="https://user-images.githubusercontent.com/40172001/149950141-0b3f3dd1-dc24-474e-8b55-73bd961c2333.png">


다시켜기 되면 바꾼화면이 나오게 되고 다시 첫번쨰 셀을 클릭하게되면 이름을 바꿀 수 있는 알림창이 뜨게 됩니다.

<img width="321" alt="Screen Shot 2022-01-18 at 22 45 40" src="https://user-images.githubusercontent.com/40172001/149950162-cdb3c24e-d535-4d30-b076-064a0f8d12b9.png">


이렇게 userdeaults는 기본적인 컨트롤러사이의 저장소 역할을 하는 것을 볼 수 있습니다.

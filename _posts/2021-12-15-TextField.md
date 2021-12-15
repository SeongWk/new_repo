---
layout: post
title: "TextField" 
subtitle:  "Text"
cover-img: /assets/img/a24.jpeg
thumbnail-img: /assets/img/a23.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

TextField

텍스트 필드란 사용자가 컴퓨터에게 값을 입력할 수 있도록 제공하는 컨트롤러입니다.

텍스트 필드는 여러 제어 속성을 가지고 있습니다.


화면에 나와있듯이 대문자처리,스펠링체크, 키보드타입정의, 리턴키 지정 등등 많은 것을 수정하고 삽입할 수 있습니다.


<img width="243" alt="Screen Shot 2021-12-15 at 15 58 27" src="https://user-images.githubusercontent.com/40172001/146139348-e60af5d5-f83f-4be8-9713-9a5f89c55520.png">



또한 최초 응답자라는 기능도 있습니다. 만약 앱에서 바로 사용자에게 바로 키보드를 치거나 응답할 객체가 필요하다면 becomefirstResponder라는 객체를 만들어 사용할 수 있습니다.
마찬가지로 해제하려면 resignFirstResponder를 선언한후 해제하면 됩니다

<img width="858" alt="Screen Shot 2021-12-15 at 16 03 44" src="https://user-images.githubusercontent.com/40172001/146139368-33301204-1810-4913-90e5-babc93594d00.png">


초기화면

<img width="327" alt="Screen Shot 2021-12-15 at 15 59 29" src="https://user-images.githubusercontent.com/40172001/146139400-d1003d38-eea5-443f-a967-7e0a2fd475b0.png">


초기화면에서 start를 누르면
end를 누르면 키보드가 해제 되고 종료됩니다.

<img width="325" alt="Screen Shot 2021-12-15 at 15 59 36" src="https://user-images.githubusercontent.com/40172001/146139443-4ca0876a-69eb-4c20-b7f4-bc687271b466.png">

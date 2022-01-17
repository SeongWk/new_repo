---
layout: post
title: "Tab bar, Alert"
subtitle:  "No storyboard"
cover-img: /assets/img/b56.jpeg
thumbnail-img: /assets/img/b57.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

이번에도 스토리보드없이 만들어보기 거의 3번째인가 합니다.
알림창과 탭바입니다.

알림창도 자신이 만들 수 있습니다. 이미지가 들어가는 경우가 있죠
알림창커스텀마이징을 해보았습니다.

버튼 생성시 addtarget을 해줍니다 왜냐하며 액션함수를 쓰기 위해서 항상 그래왔던것처럼!
UIalertController메소드를 활용하여 선언하고 Uialertaction 을 설정해줍니다.

addaction도 해줍니다. 여기서 중요한점이 일반적인 알림창은 그냥 글자가 나왔지만 뷰컨트롤러를 
생성하여 안에 집어넣어 줄 수 있습니다.
이미지를 첨부하여 넣을 수 있고 다양합니다.

그 후 present메소드로 함수를 실행합니다.
마지막에는 버튼생성을 할 수 있는 addsubview를 시작하면 됩니다.

![Screen Shot 2022-01-17 at 21 38 20](https://user-images.githubusercontent.com/40172001/149772192-22d51c2d-e75f-4bc6-9dc6-d1735455fa04.png)


초기화면

![Screen Shot 2022-01-17 at 21 38 29](https://user-images.githubusercontent.com/40172001/149772196-8d5a0909-3286-445f-bf2c-ed38ffda9e5b.png)

버튼을 누르면 빨강색 view가 나오게 됩니다.

![Screen Shot 2022-01-17 at 21 38 36](https://user-images.githubusercontent.com/40172001/149772208-bc38eb5e-28f8-4368-96cf-2bc3b9c0af85.png)

두번쨰로는 탭바인데 이것도 마찬가지입니다. 
탭바를 보면 버튼을 누르면 바뀌는 식으로 되어 있는 것을 볼 수 있습니다.

하지만 탭바도 굳이 기본적인 탭바컨트롤러를 사용해 가면서 디자인에 재미가 없는 것을 느낄 수가 있습니다.
그래서 이것도 알림창과 같이 커스텀마이징을 할 수 있습니다.

버튼과 뷰를 멤버함수로 설정합니다.
뷰와 버튼에 위치를 조정한 후 색을 설정해주고  버튼안에  쓰여질  title도 설정할 수 있습니다.

![Screen Shot 2022-01-17 at 21 41 13](https://user-images.githubusercontent.com/40172001/149773069-66644c71-5a70-49e5-818b-5619c40c4cda.png)


탭바를 터치하면 바뀌는 것을 보기위해 addtabbarbtn을 생성 후 터치하는 순간 색이 바뀔수 있게 설정해줍니다.
마지막으로 액션함수 click을 통해 터치하기전에를 false로 두고 touch하고 나면 함수가 실행되게 만들어주는 함수를 생성합니다.

![Screen Shot 2022-01-17 at 21 41 20](https://user-images.githubusercontent.com/40172001/149773075-6aaab384-6fcb-48db-afd5-7a9e1c864e16.png)


첫번쨰화면

![Screen Shot 2022-01-17 at 21 41 48](https://user-images.githubusercontent.com/40172001/149773092-934710d5-663b-443c-8d6e-e47f5488fb5d.png)


두번째화면

![Screen Shot 2022-01-17 at 21 41 55](https://user-images.githubusercontent.com/40172001/149773097-200134fa-8df8-4cdd-acdb-23fb6e95af7d.png)


세번째화면

![Screen Shot 2022-01-17 at 21 42 01](https://user-images.githubusercontent.com/40172001/149773106-3f30cb7f-d12b-4bb7-b8ac-d35993cd016c.png)


탭바사이즈를 늘리거나 줄이거나 커스텀마징을 하고 싶을 떄 프로그래밍 방식을 사용하면 간편하다는 것을 알게 되었습니다.!

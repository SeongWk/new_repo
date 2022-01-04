---
layout: post
title: "function,optional,class,struct"
subtitle:  "함수와 옵셔널 그리고 구조체와 클래스"
cover-img: /assets/img/k459.jpeg
thumbnail-img: /assets/img/p42.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

function

함수는 이름 매개변수 반환 타입, 실행문, 리턴문으로 이루어져 있습니다.

   func name(parameter)->return type
   
   {  
      code
      return 
 
   }
   
![Screen Shot 2021-12-31 at 14 19 25](https://user-images.githubusercontent.com/40172001/147804922-05f27493-a494-492f-a825-b832b88a3641.png)

   
매개변수에다가 이름을 넣어 매개변수끼리 분류해줄 수 있습니다.

![Screen Shot 2021-12-31 at 14 24 27](https://user-images.githubusercontent.com/40172001/147805057-5c3c0823-ca2c-4377-98bb-481c29d319ea.png)



전달인자도 지정해줄 수 있습니다. 전달인자는 매개변수 앞에 쓰게 됩니다. 만약 전달인자 레이블을 사용하고 싶지 않다면 와일드카드식별자 _ 를 사용합니다.

![Screen Shot 2021-12-31 at 14 24 17](https://user-images.githubusercontent.com/40172001/147805039-56b04ffb-b090-414a-b344-d4cfacbcc4ba.png)


![Screen Shot 2021-12-31 at 14 19 38](https://user-images.githubusercontent.com/40172001/147804993-db28d47d-3c34-412e-b40f-50a03ebfc83d.png)



만약 매개변수가 입력이 몇개가 들어오는지 모를떄 가변매개변수를 사용할수 있습니다

![Screen Shot 2021-12-31 at 14 20 10](https://user-images.githubusercontent.com/40172001/147804978-5e1506d1-e2b8-4371-996e-bd9d1082e2b7.png)


또한 함수를 데이터타입을 선언해주어서 사용할수도 있습니다.

![Screen Shot 2021-12-31 at 14 20 24](https://user-images.githubusercontent.com/40172001/147804983-f1c714b5-0c65-4204-b770-723627f899b7.png)


옵셔널

optional

옵셔널은 말 그래도 값이 있을 수도 아니면 없을 수도 있는 값입니다.
값이 있는 것을 사용자에게 컴퓨터가 보장할 수 없음을 이야기하고 있습니다.

또한 옵셔널은 nil이라는 명령어를 사용하게 되는데 값이 안전하지 않을수가 있음을 의미하기도 합니다

보통 ? 로 값을 물어봅니다 제대로 된 값이 맞는지 아닌지를요

![Screen Shot 2021-12-31 at 14 34 30](https://user-images.githubusercontent.com/40172001/147805421-119a8352-8160-4f51-87a3-ebe21a166aa3.png)

만약 옵셔널을 강제추출하고 싶으면 ! 를 사용하여 강제로 뺴내어 오게 하면 됩니다

![Screen Shot 2021-12-31 at 14 34 37](https://user-images.githubusercontent.com/40172001/147805424-9426dbc4-94e0-4811-a9a4-108e8571650e.png)


struct 

구조체 - 사용자가 원하는 묶음을 모음으로 만든 것입니다.

Strict  name
{
	code
}

![Screen Shot 2022-01-04 at 22 50 51](https://user-images.githubusercontent.com/40172001/148070583-73b3e18c-18a3-4291-ab50-f947b6c85ef0.png)


구조체는 인스터스를 생성할 떄 변수는 상관없지만 만약 상수로 선언이 되면 값을 변경할 수가 없습니다.

![Screen Shot 2022-01-04 at 22 50 36](https://user-images.githubusercontent.com/40172001/148070620-819009bd-2fb6-405c-8c37-72ecd9ef1e7a.png)



Class

클래스는 구조체와 마찬가지로 선언문입니다.

Class name
{
	code
}

![Screen Shot 2022-01-04 at 22 55 16](https://user-images.githubusercontent.com/40172001/148070647-06bbe706-2bef-4e49-818a-ec150adb84ad.png)

구조체와 다른 점은 클래스는 참조타입이므로 상수로 선언 된 값을 변경 할 수 있습니다
![Screen Shot 2022-01-04 at 22 54 50](https://user-images.githubusercontent.com/40172001/148070678-c11a660f-3dd0-4568-aba6-3517d1397f4b.png)

구조체와 클래스와 다른 점은 구조체는 값타입 클래스는 참조타입입니다.

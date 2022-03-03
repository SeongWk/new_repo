---
layout: post
title: "function,optional,class,struct,closure"
subtitle:  "함수와 옵셔널 그리고 구조체와 클래스,클로져까지"
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

옵셔널 바인딩

옵셔널 바인딩은 옵셔널에 값이 있는 지 확인이 필요할 때 사용합니다. 
만약 옵셔널에 값이 있으면 값을 반환하고 없으면은 확인만 합니다.
보통 조건문을 사용하여 바인딩으 시작합니다.

![Screen Shot 2022-01-06 at 15 00 32](https://user-images.githubusercontent.com/40172001/148347765-98cca175-7d5d-4c26-918c-b86f726d3af0.png)

![Screen Shot 2022-01-06 at 15 01 02](https://user-images.githubusercontent.com/40172001/148347797-2f2e26cf-9116-4357-ab7a-b80ab3c5583b.png)


옵셔널 체이닝 

옵셔널 체이닝은 옵셔널을 반복사용하여 마치 자전거 체인처럼 엮여 있는 형태르 말합니다.
옵셔널체이닝은 그림과같이 ?을 반복사용하여 값을 찾아냅니다. 
중요한점은 옵셔널체이닝이 ? 물어봐서 nil이라는 값을 찾아내면 그 다음 체이닝은 필요없이 바로 리턴합니다

![Screen Shot 2022-01-06 at 14 51 55](https://user-images.githubusercontent.com/40172001/148347879-54f60827-2adc-4bb6-a347-496361a64bd7.png)

![Screen Shot 2022-01-06 at 14 52 08](https://user-images.githubusercontent.com/40172001/148347920-f7f7545c-a483-4798-b739-713f4b81656d.png)


만약 값을 할당하고 싶으면 기존 체이닝문에서 하나씩 Nil 값에 값을 넣어 최종적으로 사용자가 원하는 값을 옵셔널로 값으 가져오게 할 수 있습니다.

![Screen Shot 2022-01-06 at 14 52 23](https://user-images.githubusercontent.com/40172001/148347951-68950318-4a1e-4712-809e-392a7166fc0e.png)


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


closure

클로져는 익명함수이면서 1급 함수이다.

클로져 표현식

	{ (Parameters)-> return type in
	   code
	}

Clousure head와 closure body를 구분하는 것이 in이다.

예를들어보면

ex1이라는 클로져 함수를 만들었을 때 값을 상수에다가 쓸수 있다.

<img width="476" alt="Screen Shot 2022-03-03 at 21 00 08" src="https://user-images.githubusercontent.com/40172001/156561973-64192c59-c657-4ab9-9f00-522b041e5b27.png">

<img width="394" alt="Screen Shot 2022-03-03 at 21 00 14" src="https://user-images.githubusercontent.com/40172001/156561935-89b2e9b0-dc64-486b-8d4a-5d25c9cf4cc7.png">

또한 클로져 안에 클로져를 써서 결과를 나타낼수도 있고

<img width="708" alt="Screen Shot 2022-03-03 at 21 00 42" src="https://user-images.githubusercontent.com/40172001/156562179-d6860d41-6d68-4c5c-9a4e-1e9594e06658.png">


Capture value 특징을 통해 해당 상수나 변수의 값을 참조할 수 있다.
또한 캡쳐도 가능하다

<img width="625" alt="Screen Shot 2022-03-03 at 21 11 29" src="https://user-images.githubusercontent.com/40172001/156562573-80b6337e-b509-492d-88e0-67010f64560b.png">

클로져의 대표적인 method로  sort(), filter(), map(), reduce()가 있습니다.

값을 정렬하거나

<img width="632" alt="Screen Shot 2022-03-03 at 21 21 15" src="https://user-images.githubusercontent.com/40172001/156564549-c7d77aff-833b-4ed5-9f5e-e260f470c6f3.png">


값을 필터링하거나

<img width="641" alt="Screen Shot 2022-03-03 at 21 22 21" src="https://user-images.githubusercontent.com/40172001/156564545-10ca59f6-18f8-4356-af22-546fb4014d5b.png">


값을 재가공하거나

<img width="606" alt="Screen Shot 2022-03-03 at 21 23 29" src="https://user-images.githubusercontent.com/40172001/156564526-56456006-1957-461f-8213-b0bb063a0dd6.png">


값을 지워버리게 만들거나 

<img width="655" alt="Screen Shot 2022-03-03 at 21 24 16" src="https://user-images.githubusercontent.com/40172001/156564493-fb67fcdc-a95c-495b-888c-b7d6f7bf46d4.png">

여러모로 자주 쓰인다.


또한 탈출클로져가 있는데 탈출한 클로져 앞에 
@escaping을 붙여주면 탈출을 허락하는 의미로 쓰일 수 있습니다.

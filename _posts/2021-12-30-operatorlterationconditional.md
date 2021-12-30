---
layout: post
title: "operator,lteration,conditional"
subtitle:  "blablabla"
cover-img: /assets/img/e88.jpeg
thumbnail-img: /assets/img/e90.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---
연산자

산술연산자 : +,-, *. %, / 
더하기 뺴기 곱하기 나누기 나머지 연산

비교연산자: ==,>=,<=,>,<,!=
두가지 값으 비교합니다 같다,다르다,이상,이하 ..

삼항연산자: value ? A : B
value상황일때 진실이면 a  거짓말이면 b

부울연산자 : !, &&, II
거짓을 반전, and 연산 or 연산

비트연산자: ~,&,^,>>,<<
바트 반전, 비트 and, 비트 or  비트 xor, 비트 shift 연산

복합연산자: +=,-=,*=,/=…

a+=b -> a=a+b
a-=b -> a=a-b
a*=b -> a=a*b
a/=b -> a=a/b


조건문

If

if는 대표적인 조건문 연산으로 조건이 해당하는 값이 맞으면 코드를 실행하고 아니면 else를 통해 값으 찾아나가는 조건문

	If  조건
	{
	code

	} else if 조건

	{
	code
	} else

	{	
	code
	}

![Screen Shot 2021-12-30 at 23 32 06](https://user-images.githubusercontent.com/40172001/147761196-332007c8-b7fa-4ad6-b321-780515f826d0.png)



switch

switch는 if문과 비슷한 조건문으로 해당하는 case를 열거형으로 나열시킨후 해당되는 값을 코드르 출력시키는 조건문

	Switch 이름
	{	

	case 값1:
		code
		
	case 값2:
		code
		
	case 값3:
		code
		
	default:
		code


	}
	
	
![Screen Shot 2021-12-30 at 23 21 35](https://user-images.githubusercontent.com/40172001/147760309-e04ff1e0-fdf9-47f7-8855-adf0dd3d2476.png)


반복문

for ..in구문은 for 문으로 특정 범위나 상수를 시퀀스를 시킬떄 반복 값에 해당하는 값들을 실행코드에 의해 출력시키는 반복문

	For 상수 in 반복 값
	{	
		code
	}
	
![Screen Shot 2021-12-30 at 23 32 55](https://user-images.githubusercontent.com/40172001/147761214-842b616a-bdc9-4f2d-81cd-349fd94ccda0.png)


while문은 while조건이 끝날때까지 구문을 시퀀스 시키느 반복문 , 해당하는 값이 나오면 while문을 빠져 나올 수 있다.

	While 조건
	{
		code
	}

![Screen Shot 2021-12-30 at 23 35 27](https://user-images.githubusercontent.com/40172001/147761233-3c84beaa-ed3d-4839-afda-5d5102abf7b0.png)


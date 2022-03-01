---
layout: post
title: "Dispatchqueue"
subtitle:  "GCD 간단 정리"
cover-img: /assets/img/e89.jpeg
thumbnail-img: /assets/img/z45.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Dispatchqueue


일명 GCD라고 불리우는 DispatchQueue는 FIFO작돈하는 큐이다.

앱의 main 과 background 스레드를 동시적으로 일을 관리해주는 역할이다.

Dispathqueue에는 Serial과 Concurrent 방식이 대표적으로 있고

queue는 main과 global로 되어 있다.

또한 queue는 동기적 혹은 비동기적으로 실행 가능하다.

swiftdoc에 나와 있듯 메인을 sync로 실행하면 데드락이 걸리므로 async로 해야한다.

Serial은 말그대로 순차적으로 직렬하는 작업 순서

Concurrent는 작업을 동시에 진행하지만 순서가 보장되지 않음

sync는 동기적 async는 비동기적 방식으로 뜻한다.

example을 만들어보면

1.Serial

main

<img width="842" alt="Screen Shot 2022-03-01 at 15 31 57" src="https://user-images.githubusercontent.com/40172001/156120438-665dd5e6-0f4f-4f17-8afd-df6bda61fe7f.png">

<img width="164" alt="Screen Shot 2022-03-01 at 15 32 26" src="https://user-images.githubusercontent.com/40172001/156120464-4bc2f1dc-b6ab-4a8f-807b-b2adb7992773.png">

mainqueue는 main 스레드에서 실행되기 때문에 다른 dispatchqueue가 다 실행된 다음에 실행된다

custom = 디폴트는 Serial이다

global queue은 Main queue와 다르게 독립적으로 실행된다
<img width="647" alt="Screen Shot 2022-03-01 at 15 49 07" src="https://user-images.githubusercontent.com/40172001/156120497-52809015-0eec-44ce-81b7-d8596b6d5eeb.png">

<img width="116" alt="Screen Shot 2022-03-01 at 15 49 18" src="https://user-images.githubusercontent.com/40172001/156120522-379c1ec8-21b9-4122-b506-e523cfa02a44.png">


반대로 sync는 순차적으로 실행 된다

<img width="669" alt="Screen Shot 2022-03-01 at 15 50 40" src="https://user-images.githubusercontent.com/40172001/156120550-396e8ae0-1c24-49b8-9455-b4c82074fdc4.png">

<img width="58" alt="Screen Shot 2022-03-01 at 15 51 01" src="https://user-images.githubusercontent.com/40172001/156120562-9cd1d2ad-f00e-4f5b-a0bb-bea3bcf65aad.png">

2. Concurrent

global queue는 qos를 통해  우선순위를 지정할 수 있다.

  DispatchQueue.global(qos: .userInteractive).async {
      // 가장 중요 우선순위
  }

  DispatchQueue.global(qos: .userInitiated).async {
    // 두번쨰 우선순위
  }

  DispatchQueue.global(qos: .default).async {
    // 그냥 기본
  }

  DispatchQueue.global(qos: .utility).async {
    // 기본보다 낮은 우선순위
  }

  DispatchQueue.global(qos: .background).async {
    // 가장 낮은 우선순위
  }

ex
default로 해서 예를 들면

<img width="627" alt="Screen Shot 2022-03-01 at 16 10 50" src="https://user-images.githubusercontent.com/40172001/156122221-a2f9c8a4-0d8d-4dee-b8e1-b4a788767017.png">

<img width="164" alt="Screen Shot 2022-03-01 at 16 10 58" src="https://user-images.githubusercontent.com/40172001/156122227-370dd02f-7d4a-4764-b371-d1fda1462698.png">


1,2이후에 B가 나오는 것이 맞고 3,4 이후에 D가 나오는 것을 무조건 볼 수 있지만
비동기인 A,C는 알 수 없느 것을 알 수 있다.



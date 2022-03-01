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

Serial은 말그대로 순차적으로 직렬하는 작업 순서
Concurrent는 작업을 동시에 진행하지만 순서가 보장되지 않음

sync는 동기적 async는 비동기적 방식으로 뜻한다.

만약 

---
layout: post
title: "Restfulapi" 
subtitle:  "간단정리"
cover-img: /assets/img/rr54.jpeg
thumbnail-img: /assets/img/rr55.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


HTTP

HTTP는 서버에서 클라이언트로 데이터를 전송하기 위해 사용하는 어플리케이션 프로토콜이다. 

HTTP는 사용자가 목적에 따라 메소드를 정의를 하고 있다
참고로 https: http에서 보안버전이다.

- GET: 웹 페이지 같은 데이터를 가져온다
- HEAD: GET과 동일하지만 실제 데이터가 아닌 header를 요청한다
- POST: 서버에 데이터를 내보낸다.
- PUT: 특정 위치에 데이터를 보내기 위해 사용한다
- DELETE: 데이터를 삭제하기 위해 사용한다.


------------------------


Rest

REST는 Representational State Transfer라는 용어의 약자

rest의 구성요소

- resource: 자원
- method: 방법
- representation of resources: 자원의 표현

HTTP의 URI(Uniform Resource Identifier)를 통해 자원(Resource)을 정하고, 

HTTP Method(POST, GET, PUT, DELETE)를 통해 해당 자원에 대한 CRUD을 적용하는 것이다

CRUD Operation

- Create : 생성(POST)
- Read : 조회(GET)
- Update : 수정(PUT)
- Delete : 삭제(DELETE)
- HEAD: header 정보 조회(HEAD)


---------------------------


Restful api

-> rest기반으로 만드는 애플리케이션 프로그래밍 인터페이스


-----------------------------

URLSession

URLSession은 http,https를 통한 데이터를 주고받기 위해서  api를 제공하는 class

URLSession 사용 순서

1.  URL 설정
2.  URLSession 생성
3.  Task 설정
4. Task 실행


URLSessionConfiguration

- Default: 기본
- Ephemeral: 쿠키를 저장하지 않는 것들
- Background: 백그라운드 앱이 있을 떄 업로드나 다운로드 할 떄

URLSession Task

- DataTask: data를 받는 작업
- UploadTask: 파일 업로드
- DownloadTask: 파일 다운로드


URLRequest: URL load 요청

- URLRequest객체 직접 create해서 옵션 및 설정 확인 후 통신

URLResponse: URL load 요청에 관한 data 응답


Response할 떄 받는 두가지 방법

Completion Handler로 결과 받는 법

URLSession -> URLSessionDataTask -> CompletionHandler

Delegate로 결과 받는 법

URLSession -> URLSessiondataTask(Create)
URLSession -> URLSessionDelegate(callback function)


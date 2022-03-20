---
layout: post
title: "Cocoapods" 
subtitle:  "패키지매니저"
cover-img: /assets/img/kk78.jpeg
thumbnail-img: /assets/img/kk77.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Cocoa pods

코코아팟
 
코코아팟은 오브젝트 c 와 스위프트를 위한 패키지 관리 매니저이다.

터미널에서 sudo gem install cocoapods을 하고

패스워드를 자신 맥북 패스워드 입력 후

코코아팟 설치 완료

내 파일에 Alarmfire을 넣어보자

자신이 원하는 장소에 들어가 Pod init을 해준다

<img width="456" alt="Screen Shot 2022-02-21 at 16 10 18" src="https://user-images.githubusercontent.com/40172001/154906912-93277790-dd7d-47c8-ab92-a48730da62db.png">

podfile을 열기 위해 open을 한다.

<img width="537" alt="Screen Shot 2022-02-21 at 16 10 24" src="https://user-images.githubusercontent.com/40172001/154906946-0e9b9fb1-e6f2-4b05-b617-93adfe187941.png">

Pod Alamofire을 입력한 후 Command s를 하고 저장을 한다

podfile을 다시 설치하기 위해 pod install을 한다.

<img width="645" alt="Screen Shot 2022-02-21 at 16 24 52" src="https://user-images.githubusercontent.com/40172001/154907937-7c916848-df57-4574-bc53-366e53d30fe8.png">

그러면 내가 입력한 Alamofire가 podfile로 인해 파일에 넣어졌다는 것을 볼 수 있다.

<img width="734" alt="Screen Shot 2022-02-21 at 16 09 39" src="https://user-images.githubusercontent.com/40172001/154906878-4b3a5a36-6e87-4a06-a06d-2315d0099c12.png">

다시 파일로 들어가 .xcworkspace에 들어가면

<img width="728" alt="Screen Shot 2022-02-21 at 16 10 35" src="https://user-images.githubusercontent.com/40172001/154907007-4ea6d551-4082-4856-815f-3afea9807954.png">

실제로 Alamofire 설치가 되어있다는 것을 볼 수 있다,

<img width="1231" alt="Screen Shot 2022-02-21 at 16 11 01" src="https://user-images.githubusercontent.com/40172001/154907027-608c53a7-4255-4d2d-9516-1035800fc1e0.png">

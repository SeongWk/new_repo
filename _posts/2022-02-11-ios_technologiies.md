---
layout: post
title: "ios technologies "
subtitle:  "앱 생명주기"
cover-img: /assets/img/lt1.jpeg
thumbnail-img: /assets/img/lt2.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


App life cycle



1. unattached - Scene에 연결이 되지 않는 상태

2. Foreground Inactive -app이 foreground이고 이벤트를 받지 않는 상태

3. Foreground Active - app이 foreground이고 이벤트를 받는 상태

4. Background - app이 background이고 실행된 코드가 있는 상태

5. SuSpended - app이 background이고 실행된 코드가 없는 상태


----------------------------------------------------


사용자의 앱을 상태를 변경하려면 사용자는 반드시 행동을 해주어야합니다


12 이전에는 use the UIapplicationDelegate

13 이후에는 use UISceneDelegate로 Lifecycle을 조정함


------------------------------------------------------

Scene-based Life cycle	



UIkit deliever는 각각 이벤트의 life-cycle을 분리할 수 있습니다.

scene은 너의 앱 ui 하나의 인스턴스를 표현합니다.
사용자들은  각 앱의 다양한 scene은 만들어 보여주고 분리할 수 있습니다.
왜냐하면 각각의 scene은 자기만의 생명주기가 있고 다른 상태에 있을 수 있습니다. 

사용자나 시스템이 너의 앱에서 새로운 scene을 요청하였을때 
uikit은 Unattached 상태로 나두어둡니다.
사용자가 요청한 scene은  onscreen으로 나타낼떄 foreground에서 빠르게 움직입니다. 
시스템이 요청한 scene은 background에서 움직입니다, 그래야 이벤트를 진행할 수 있습니다.

<img width="627" alt="Screen Shot 2022-02-11 at 15 21 28" src="https://user-images.githubusercontent.com/40172001/153546112-340f9f55-63c8-44c6-874e-531a383d5f80.png">



---
layout: post
title: "protcol and extension" 
subtitle:  "@IBOutlet and @IBAction"
cover-img: /assets/img/p1.jpg
thumbnail-img: /assets/img/effel.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---


프로토콜은 메서드나,프로퍼티를 기본적인 요구사항이나 희망사항을 말 그대로 건물을 짓기 전에 모델링 하듯이 청사진을 의미합니다.
추가로 익스텐션은 상속과 다르게 수평확장 되면 재정의 불가 기능입니다.

프로토콜 예시

<img width="806" alt="Screen Shot 2022-01-31 at 15 52 42" src="https://user-images.githubusercontent.com/40172001/151751428-64dc352f-1b1c-4fe1-8542-62dea18b7db3.png">

exampleprotcol이라는 프로토콜을 정의 한후 상속 받아 특별히 기능 없이 말 그대로 제시만 하고 있느 것을 볼수 있습니다.
제시만 하고 기능을 구현하지 않습니다.


익스텐션 예시

<img width="562" alt="Screen Shot 2022-01-31 at 15 54 10" src="https://user-images.githubusercontent.com/40172001/151751441-3bb6b7f2-cb67-413f-b85a-075f618395a3.png">

또하 extension은 기능을 확장시키기만 할 뿐 재정의를 할 수 없습니다.


스위프트는 에러를 처리할 수 있는 구문도 함꼐 있습니다.
에러처리는 컴퓨터에 있는 프로그램이 오류가 났을 떄 감지하고 처리하는 과정입니다.
error라는 타입 값으로 표현됩니다.

보통 3가지 처리 방법입니다
1. do catch
2. 옵셔널
3. 발생한 오류를 코드에 알림

1번부터 3번까지 차례대로 구문을 처리하느 것을 표현하면
do -catch구문은 do 내부코드에서 오류를 던지면 catch구문에서 전달받고 오루를 처리하는 것입니다.
옵셔널은 try?구문으 통해 오류를 던지면 오류인지 아닌지 확인하고 오류면 nil이 반환되게 처리합니다.
try -throws로 받아 오류를 처리합니다.

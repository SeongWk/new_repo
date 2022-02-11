---
layout: post
title: "ios technologies "
subtitle:  "앱 아키텍쳐"
cover-img: /assets/img/lt1.jpeg
thumbnail-img: /assets/img/lt2.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---



ios design theme
1. clarity
2. deference
3. depth


Interface essentials
1. Bars- 사용자들이 너의 앱에서 어떠한 기능들이 앱에서 사용될 수 있냐를 알려줍니다.
2. Views - 사용자들이 그래픽,애니메이션,다른 요소들을 통해 앱 화면에 어떻게 띄어야 사람들이 알 수 있는가를 알려줍니다.
3. Controls - 사용자들이 상호작용가능한 요소들로 앱이 어떻게 액션 할 수 있느냐를 보여줍니다.

App architecture

1. Launching -시작화면은  앱에 관련해서 어떠한 느낌을 주는지 중요한 효과를 가지게 한다. 적절한 오리엔테이션을 보여주기도하고  자신의 정보를 셋업할 떄 필요한 물음을 피할 수 있다. 사람들이 너의 앱에 관련해서 더 자주 ,혹은 빨리 물어보는 것을 피할 수 있다.


2. Onboarding - 온볼딩은 너의 새로운 유저들이 새로운 앱 환경에서 적응하는 과정이다.튜토리얼은 필요로 하다. 새로운 앱에서 사용자들이 새로운 것을 배워가고 모르는 것을 알아가는 단계이기 떄문에 중요하다.

<img width="296" alt="Screen Shot 2022-02-04 at 14 48 22" src="https://user-images.githubusercontent.com/40172001/152479317-59e3a6ce-5cd9-4964-9fcb-e209e79844db.png">


3. Loading - 컨텐츠가 로드될때  너의 앱은 잠시 얼어버리게 된다, 그것은 너의 앱이 사람들을 나가게 하는 하나의 원인이 될 수 있으므로 바꾸어야한다. 
방법은 로딩할때 로딩하는 중이라는것을 사용자에게 확실히 보여주어야하고 컨텐츠가 최대한 빨리 보여줄 수 있다는 과정 또한 스크린을 통해 볼 수 있어야 한다.

<img width="285" alt="Screen Shot 2022-02-04 at 14 48 29" src="https://user-images.githubusercontent.com/40172001/152479339-646ddc88-9e4a-43d3-a392-6c2626f9478d.png">


4. Modality - 모달리티는 액션을 통해 나갈수 있는 일시적모드입니다.  사람들을 그 상황에서 더욱 집중할 수 있게하고  관련된 옵션들을 자세히 볼수 있습니다.
 
<img width="262" alt="Screen Shot 2022-02-04 at 14 48 40" src="https://user-images.githubusercontent.com/40172001/152479352-95972c18-490f-4916-8606-de602bca5660.png">

5. Navigation - ios에서는 메인 네비게이션 스타일이 3가지가 있다. 
계층형 네비게이션, 플랫 네비게이션, 컨텐츠 경험 네비게이션 . 
네비게이션 특징은 터치제스쳐로 컨트롤해야한다. 자료제공을 빠르고 컨텐츠를 쉽게 줄 수 있게 디자인 해야한다.

6. Accessing user data -  
장소,건강,주식,연락처 기타 다른 컨텐츠 등 개인적인 정보는 개인적으로 정보를 구별해서 제공해야한다. 
또한 접근 제공에 관해서 요청해야한다
 
 <img width="306" alt="Screen Shot 2022-02-04 at 14 48 55" src="https://user-images.githubusercontent.com/40172001/152479367-6bf1a3ce-70fe-4791-8aad-30994a42e4a1.png">

 
7. Settings - 사용자가 시스템으로부터 원하는것을  자연스럽게 혹은 편하게 추론할 수 있어야 한다.
 딜레이되거나 피하게 된다면 사용자들은 그 앱을 성공적인 앱이 아니라 할 수 있다.
 
<img width="296" alt="Screen Shot 2022-02-04 at 14 49 04" src="https://user-images.githubusercontent.com/40172001/152479374-ef74ba98-d742-43fc-bc6b-1487cd57ae12.png">


apple mobile human interface를 참조

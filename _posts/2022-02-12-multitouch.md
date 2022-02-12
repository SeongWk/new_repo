---
layout: post
title: "Multi touch event"
subtitle:  "멀티 터치 이벤트 핸들링"
cover-img: /assets/img/e88.jpeg
thumbnail-img: /assets/img/e90.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---

Implementing a muiti-Touch

Photo1

<img width="322" alt="Screen Shot 2022-02-12 at 14 47 50" src="https://user-images.githubusercontent.com/40172001/153699359-6ce92daf-27f2-4bb0-ad6b-e8a8ae223e96.png">

Single main view가 각각 touch 장소에 회색 원으로 그려져
있고 터치가 끝나면 각 원은 사라지는 앱이다

-------------------------------

Photo2

<img width="754" alt="Screen Shot 2022-02-12 at 14 48 07" src="https://user-images.githubusercontent.com/40172001/153699364-384c5d3d-c724-418c-aebe-d27458c91012.png">

커스텀 서브클래스로 toruchableview를 설정하고 라벨도 넣어준다

Touchableview class  3가지 method

TouchesBegan(_: with :) - 각 이벤트 장소에 새로운 서브뷰를 만듬
TouchesMoved(_: with :) - 각 이벤트 장소에 새로운 장소를 업데이트
TouchesEnded_: with :) - 각 이벤트 장소에  관련된 서브뷰를 제거

class TouchableView: UIView {
   var touchViews = [UITouch:TouchSpotView]()  
 
   override init(frame: CGRect) {
      super.init(frame: frame)
      isMultipleTouchEnabled = true
   }
 
   required init?(coder aDecoder: NSCoder) {
      super.init(coder: aDecoder)
      isMultipleTouchEnabled = true
   }
 
   override func touchesBegan(_ touches: Set<UITouch>, with event: UIEvent?) {
      for touch in touches {
         createViewForTouch(touch: touch) // 새로우 터치뷰 생성
      }
   }
 
   override func touchesMoved(_ touches: Set<UITouch>, with event: UIEvent?) {
      for touch in touches {
         let view = viewForTouch(touch: touch) 
         // Move the view to the new location.
         let newLocation = touch.location(in: self)
         view?.center = newLocation. // 터치가 움직일떄마다 로케이션 조절
      }
   }
 
   override func touchesEnded(_ touches: Set<UITouch>, with event: UIEvent?) {
      for touch in touches {
         removeViewForTouch(touch: touch) // 터치가 끝나면 터치 뷰 제거
      }
   }
 
   override func touchesCancelled(_ touches: Set<UITouch>, with event: UIEvent?) {
      for touch in touches {
         removeViewForTouch(touch: touch) // 터치가 취소되면 터치 뷰 제거
      }
   }
  
   // Other methods. . . 
}

  
func createViewForTouch( touch : UITouch ) {
   let newView = TouchSpotView()
   newView.bounds = CGRect(x: 0, y: 0, width: 1, height: 1)
   newView.center = touch.location(in: self)
 
   // Add the view and animate it to a new size.
   addSubview(newView)
   UIView.animate(withDuration: 0.2) {
      newView.bounds.size = CGSize(width: 100, height: 100)
   } ->뷰안에 실제 애니메이션 생성
 
   // Save the views internally
   touchViews[touch] = newView
}
 
func viewForTouch (touch : UITouch) -> TouchSpotView? {
   return touchViews[touch]
}
 
func removeViewForTouch (touch : UITouch ) {
   if let view = touchViews[touch] {
      view.removeFromSuperview()
      touchViews.removeValue(forKey: touch)
   } -> 뷰안에서 터치제거
}
  
class TouchSpotView : UIView {
   override init(frame: CGRect) {
      super.init(frame: frame)
      backgroundColor = UIColor.lightGray
   }
 
   // Update the corner radius when the bounds change.
   override var bounds: CGRect {
      get { return super.bounds }
      set(newBounds) {
         super.bounds = newBounds
         layer.cornerRadius = newBounds.size.width / 2.0
      }
   }
}  
  

---
layout: post
title: "linkedlist & Tree" 
subtitle:  "연결리스트와 트리"
cover-img: /assets/img/vbc1.jpeg
thumbnail-img: /assets/img/vbc2.jpeg
share-img: /assets/img/path.jpg
gh-repo: Seongwk/testts
gh-badge: [star, fork, follow]
tags: [swift, ios, Xcode]
comments: true
---



링크드리스트

링크드리스트는 배열과 유사한 구조를 가진다.

하지만 배열은 연속된 값을 받지만 링크드리스트는 다르다.

첫번쨰에 노드를 삽입한다면 기존 헤드노드가 새로운노드에 포인터에 할당되는 형태로 이루어진다.

재미있게 말하자면 앞에 있는 사람의 꼬리에 잠시 매달리는 식의꼬리잡기?라고도 생각한다.


count() = 스택에 저장되어 있는 값 확인

isEmpty() = 스택이 비었을 경우 트루 반환

push() = 스택에 마지막 위치에 데이터 추가

pop() = 스택에 첫번쨰 데이터 제거 

peek() = 스택에 첫번쨰 요쇼 반환


public struct StackList<T>
{
    fileprivate var head: Node<T>?  =  nil
    private var _count: Int = 0
    public init(){}

    public mutating func push(element: T)
    {
        let node = Node<T>(data: element)
        node.next = head
        head = node
        _count += 1
    }
    public mutating func pop() ->T?
    {
        if isEmpty()
        {
            return nil
        }
        let item = head?.data
        head = head?.next
        _count  -= 1
        return item
    }
    public func peek() ->T?
    {
        return head?.data
    }
    public func isEmpty()->Bool{
        return count == 0
    }
    public var count: Int
    {
        return _count
    }
    private class Node<T>
    {
        fileprivate var next: Node<T>?
        fileprivate var data : T
        init(data: T)
        {
            next  = nil
            self.data = data
        }
    }
}
  

Tree

트리는 노드의 집합이다.

루트: 트리 최상위 노드
  
노드: 자식와 부모노드에 대한 데이터
  
모서리: 자식노드와 부모노드의 연결선
  
부모 : 노드 바로 위에 있는 노드
  
자식: 노드 바로 아래에 있는 노드
  
잎: 자식 노드를 지니지 않는 노드
  
<img width="560" alt="Screen Shot 2022-04-25 at 20 32 49" src="https://user-images.githubusercontent.com/40172001/165081014-209a5364-f8f0-47e6-9b13-9c0f36754f24.png">
  
<img width="494" alt="Screen Shot 2022-04-25 at 20 33 07" src="https://user-images.githubusercontent.com/40172001/165081032-352d9aa5-c1c7-40cb-872f-fd8b9a59d942.png">
  
<img width="424" alt="Screen Shot 2022-04-25 at 20 33 16" src="https://user-images.githubusercontent.com/40172001/165081049-2c3b4e29-dbe2-4924-a6b8-d26893584717.png">

루트는 커피라는 루트
    
노드는 핫,콜드, 아메리카노,아이스아메리카노…
    
잎: 아이스아메리카노,콜드브류,아메리키노,코코아
    
부모노드: 코코아의 부모노드는 핫
    
자식노드: 콜드노드의 자식노드는 콜드브류와 아이스아메리카노
    

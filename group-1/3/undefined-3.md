# 🐣 링크드 리스트 : 이론



* 연결리스트 : 차례로 연결된 노드를 표현해주는 자료구조
* 단방향 연결리스트 : 개별 노드 ➡️ 다음 노드
* 양방향 연결리스트 : 개별 노드 ➡️ 다음 노드 & 이전 노드



* ⭐️ 시작 지점에서의 아이템 추가 및 삭제 연산이 상수 시간 소요



### 1. Creating a Linked List

* 단방향 연결리스트 구현 코드

```java
class Node {
  Node next = null;
  int data;
  public Node(int d) {
    data = d;
  }
  void appendToTail(int d){
    Node end = new Node(d);
    Node n = this;
    while(n.next != null){
      n = n.next;
    }
    n.next = end;
  }
}
```

* 단방향 연결리스트에서의 고려사항 : `head` 가 바뀌면 어떻게 되는가?
  * 👉 _`head` 가 바뀌었음에도 어떤 객체는 `head`를 계속 가리키고 있을 수도 있다._
  * `Node` 클래스를 포함하는 `LinkedList` 클래스를 만든다.(`head Node` 변수에 head를 가리키는 값 저장)





### 2. Deleting a Node from a Singly Linked List

* 삭제 노드 : n
  1. `prev.next` 를 `n.next` 로 연결한다.
  2. (양방향 연결리스트일 경우) `n.next.prev` 를 `n.prev` 로 연결한다.



* ⚠️ 메모리 관리가 필요한 언어를 사용해 구현하는 경우에는 삭제한 노드에 할당되었던 메모리가 제대로 반환되었는지 확인 필요!



* 노드 삭제 코드

```java
Node deleteNode(Node head, int d) {
  Node n = head;
  if (n.data == d) {
    return head. Next;
  }
  
  while (n.next != null) {
    if (n.next.data == d) {
      n.next = n.next.next;
      return head;
    }
    n = n.next;
  }
  return head;
}
```

###

### 3. The "Runner" Technique

* Runner : 연결리스트를 순회할 때 두 개의 포인터를 동시에 사용한다.
* 한 포인터가 다른 포인터보다 앞서도록 하고 포인터를 움직일 때 지정된 개수 혹은 여러 노드를 한번에 움직일 수 있도록 설정한다.



### 4. Recursive Problems

* 연결리스트 문제 ≒ 재귀 호출
* ⚠️ 재귀(recursive) 알고리즘은 적어도 $O(n)$의 공간 복잡도를 갖는다!

\

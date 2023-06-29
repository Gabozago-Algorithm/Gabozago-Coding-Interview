# 🐢 링스크 리스트 : 이론

## <mark style="background-color:orange;">**🫧 연결 리스트**</mark>

: 차례로 연결된 노드를 표현해주는 자료구조

: 단) 배열과 달리 특정 인덱스를 상수 시간에 접근할 수 없다

(k번째 원소를 찾고싶다면 처음부터 k번 루프 돌아야함)

: 장) 리스트의 시작 지점에서 아이템을 추가하거나 삭제 연산을 상수 시간에 할 수 있다

*   단방향

    ![](<../../.gitbook/assets/image (6).png>)

    * 각 노드는 다음 노드 가리킴
*   양방향

    ![](<../../.gitbook/assets/image (2).png>)

    * 각 노드는 다음 노드와 이전 노드를 함께 가리킴



**💖 (단방향) 연결 리스트 만들기**

```java
class Node {
	Node next = null;
	int data;
	public Node(int d) {
		data = d;
	}

	void appendToTail(int d) {
		Node end = new Node(d);
		Node n = this;
		while (n.next != null) {
			n = n.next;
		{
		n.next = end;
	}
}
```



**💖 (단방향) 연결 리스트 삭제하기**

1. 노드 n 이 주어지면, 이전 노드 prev 를 찾아 [prev.next](http://prev.next) 와 [n.next](http://n.next) 가 같도록 설정한다

* 양방향 연결 리스트일 경우, n.next가 가리키는 노드를 갱신하여 n.next.prev 가 n.prev 가 같도록 설정

> **💥 주의**
>
> * 널 포인트 검사를 반드시 한다
> * head와 tail 포인터를 갱신한다

```java
Node deleteNode(Node head, int d) {
	Node n = head;
	if (n.data == d) {
		return head.next;    // head 움직이기
	}

	while (n.next != null) {
		if (n.next.data == d) {
			n.next = n.next.next;
			return head;     // head 움직이지 않음
		}
	}
	return head;
}
	
```



**💖 Runner (부가 포인터)**

: 연결리스트를 순회할 때 두 개의 포인터를 동시에 사용하는 것

: 한 포인터가 다른 포인터보다 앞서도록 한다

* 앞선 포인터는 뒤 포인터보다 항상 지정된 개수만큼은 앞설 수 있다
* 뒤 포인터를 여러 노드를 한번에 뛰어넘도록 설정할 수 있다



**💖 재귀 문제**

: 재귀 호출 깊이가 n일 경우, 해당 재귀 알고리즘이 적어도 O(n) 의 공간을 사용

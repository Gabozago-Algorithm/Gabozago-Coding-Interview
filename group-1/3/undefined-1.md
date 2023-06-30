# 🐢 링스크 리스트 : 구현

## <mark style="background-color:orange;">**🫧 링크드 리스트 구현하기**</mark>

**➡️** size() - 리스트 안의 데이터 개수를 반환한다.

```java
LinkedList<Integer> list = new LinkedList<Integer>(Arrays.asList(1,2,3));
System.out.println(list.size()); //list 크기 : 3
```

**➡️** empty() - 리스트가 비어있다면 true를 반환한다.

```java
// 리스트가 비었는가
template <typename E>
bool SLinkedList<E>::empty() const{
    return head == NULL;
}
```

**➡️** value\_at(index) - index번째 위치의 value을 반환한다. (가장 앞은 0부터 시작한다.)

```cpp
# declaring array
a = [18, 22, 33, nil, 5, 6]

puts "values_at() method form : #{a.values_at(2, 4)}\\n\\n"
// values_at() method form : [33, 5]
```

**➡️** push\_front(value) - 가장 앞에 value를 추가한다.

```cpp
int main(void) {
	list<int> L = { 3, 7 };
	L.push_front(1); // { 1, 3, 7 }
	return 0;
}
```

**➡️** pop\_front() - 가장 앞에 있는 것을 제거하고, 그 value를 반환한다.

```cpp
int main(void) {
	list<int> L = { 1, 5, 3, 7, 10 }   
	L.pop_front(); // { 5, 3, 7, 10 }
	return 0;
}
```

**➡️** push\_back(value) - 가장 끝에 value을 추가한다.

```cpp
int main(void) {
	list<int> L = { 3, 7 };
	L.push_back(10); // { 3, 7, 10 }
	return 0;
}
```

**➡️** pop\_back() - 가장 끝에 있는 것을 제거하고, 그 value를 반환한다.

```cpp
int main(void) {
	list<int> L = { 1, 5, 3, 7, 10 }   
	L.pop_back(); // { 5, 3, 7, 10}
	return 0;
}
```

**➡️** front() - 가장 앞에 있는 것의 value를 가져온다.

```cpp
class CircleList{
public:
    CircleList(); // 생성자
    ~CircleList(); // 소멸자

    const string& front() const; // 커서 다음의 원소
};
```

**➡️** back() - 가장 끝에 있는 것의 value를 가져온다.

```cpp
class CircleList{
public:
    CircleList(); // 생성자
    ~CircleList(); // 소멸자

    const string& back() const; // 커서의 원소

};
```

**➡️** insert(index, value) - index번째 위치에 value를 추가한다. 즉, index번째에 새로 추가된 것이 기존의 index번째에 있던 것을 가리킨다.

```cpp
list<int>::iterator iterInsertPos = list1.begin();
list1.insert(iterInsertsPos, 100);    // 첫 번째 위치에 100 넣기
```

**➡️** erase(index) - index번째에 있는 노드를 삭제한다.

```cpp
list1.erase(list1.begin());    // list1 첫 번 째 요소 삭제
```

**➡️** value\_n\_from\_end(n) - 뒤에서부터 n번째에 있는 노드의 value를 반환한다.

**➡️** reverse() - 리스트를 뒤집는다.

```cpp
public class UnitTest {
    public static void main(String[] args) {
        SinglyLinkedList list = new SinglyLinkedList();
        list.addLast(1);
        list.addLast(2);
        list.addLast(3);
        list.addLast(4);

        System.out.println(list);
        list.reverse();

        System.out.println(list);
    }
}

// 1 -> 2 -> 3 -> 4
// 4 -> 3 -> 2 -> 1
```

**➡️** remove\_value(value) - value와 같은 값을 가지는 첫 번째 노드를 제거한다.

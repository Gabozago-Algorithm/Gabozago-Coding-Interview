# 🐢 배열 : 이론

## <mark style="background-color:red;">**🫧 배열과 문자열**</mark>

**️‍💖 해시테이블 (hash table)**

: 효율적인 탐색을 위한 자료구조로서, key를 value 에 대응시킴

: 최악의 경우 O(n) // n은 키의 개수

: 최선의 경우 O(1)



**1) 키의 해시 코드 계산**

* 키의 자료형은 보통 int or long
* 키의 개수 무한 (int 는 유한)

**2) hash(key) % array\_length 방식으로 해시 코드 이용해 배열의 인덱스 구함**

* 서로 다른 두 개의 해시 코드가 같은 인덱스 가리킬 수 있음

**3) 배열의 각 인덱스에는 키와 값으로 이루어진 연결리스트 존재**

* 키와 값을 해당 인덱스에 저장 (반드시 연결리스트 이용!)
* **💥 충돌** : 서로 다른 두 개의 키가 같은 코드를 가리키거나, 서로 다른 두 개의 해시 코드가 같은 인덱스를 가리키는 경우

⇒ 키에 상응하기 위해서 위를 반복!

⇒ 주어진 키로부터 해시 코드를 계산, 해시 코드를 이용해 인덱스 계산, 해당 키에 상응하는 값을 연결 리스트에서 탐색



> **균형 이진 탐색 트리 (balanced binary search tree)**
>
> : 탐색 시간은 O(logN) : 크기가 큰 배열을 미리 할당해 놓지 않아도 되기 때문에 적은 공간 사용 가능
>
> : 키의 집합을 특정 순서대로 접근 가능



**💖 ArrayList 와 가변 크기 배열**

* **ArrayList**
  * 동적 가변 크기 기능 내재의 배열일 때 사용
  * 필요에 따라 크기를 변화 가능
  * O(1)의 접근 시간을 유지
  * 배열이 가득 차면, 배열의 크기를 두 배로 늘림
    * O(n)으로 늘려지지만, 상환 입력 시간으로 인해 O(1)
    * n개의 원소를 삽입할 때 소요 작업은 O(n)
    * 평균적으로 각 삽입은 O(1)



**💖 StringBuilder**

: 가변 크기 배열을 이용해서 필요한 경우에만 문자열 복사

```java
String joinWords(String[] words) {
	StringBuilder sentence = new StringBuilder();
	for (String w : words) {
		sentence.append(w);
	}
	return sentence.toString();
}
```

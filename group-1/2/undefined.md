# 🐣 배열 : 이론

### 1. Hash Tables

* 해시테이블 : 효율적인 탐색을 위한 자료구조
* 키(key)를 값(value)에 대응한다.



* 간단한 해시테이블 구현 방법
  * 연결리스트(linked list), 해시 코드 함수(hash code function)



* 해시테이블 데이터 삽입 과정
  * 키의 해시 코드를 계산한다.
    * _키의 자료형은 보통 `int` 혹은 `long` 이 된다._ **➡️ 이는 서로 다른 두 개의 키가 같은 해시 코드를 가리킬 수 있음을 나타냄!**
  * `hash(key) % array_length` 와 같은 방식으로 해시 코드를 이용해, 배열의 인덱스를 구한다.
  * 배열의 각 인덱스에는 키-값 으로 이루어진 연결리스트가 존재한다.
    * **충돌에 대비하여 반드시 연결리스트를 이용한다!**

####

#### 🤔 해시 충돌?

* 서로 다른 두 개의 키가 같은 해시 코드를 가리키거나
* 서로 다른 두 개의 해시 코드가 같은 인덱스를 가리키는 경우



#### 🕐 수행 시간

* 최악의 경우 : O(N)
* _But 일반적으로 해시에 대해 이야기할 때는 충돌을 최소화하도록 잘 구현된 경우를 가정한다._ \
  _➡️ 이 경우는 O(1)_





### 2. ArrayList & Resizable Arraya

* ArrayList : 동적 가변 크기 기능 내재 자료형
  * ArrayList는 필요에 따라 크기를 변화시킬 수 있으면서 $$O(1)$$의 접근 시간을 유지한다.
  * 배열이 가득 차는 순간, 배열의 크기를 **2배**로 늘린다.
* 크기를 2배 늘리는 연산은 $$O(N)$$ 이지만 자주 발생하지 않으므로, $$O(1)$$이 된다.
  * _⭐️상환 입력 시간 개념 도입!_





### 3. StringBuilder

* 문자열을 하나로 이어붙이는 방법



* ex1

```java
String joinWords(String[] words){
  String sentence = "";
  for (String w : words) {
    sentence = sentence + w;
  }
  return sentence;
}
```

* 문자열을 이어붙일 때마다 새로운 문자열에 복사하는 방법
  * 처음에는 x개, 두 번째는 2x개, 세 번째는 3x개, n번째는 nx개의 문자를 복사한다.
* 시간복잡도 :  $$O(xn^2)$$
* $$1 + 2 + ... + n = n(n + 1)/2$$



* ex2

```java
String joinWords(String[] words) {
  StringBuilder sentence = new StringBuilder();
  for (String w : words) {
    sentence.append(w);
  }
  return sentence.toString;
}
```

* `StringBuilder` 를 이용하여 가변 크기 배열을 사용하는 방법
  * 필요한 경우에만 문자열을 복사하게끔 한다.

\

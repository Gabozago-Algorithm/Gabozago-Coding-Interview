# 🐢 스택 : 구현

## <mark style="background-color:red;">**🫧 스택 구현하기**</mark>

```java
function Stack(arr = Array()) {
  this.arr = arr;
}

let stk = new Stack();
let stk2 = new Stack(['test', 'test2']);
```

➡️ isEmpty() : 비어있는지 확인(반환값 t/f)

```java
Stack.prototype.isEmpty = function(){
  return this.arr.length === 0;
}
```

➡️ push(data) : 스택에 데이터 추가하기

```java
Stack.prototype.push = function (data) {
  this.arr.push(data);
};
```

➡️ pop() : 스택 맨 위의 데이터 삭제하기

```java
Stack.prototype.pop = function () {
  return this.arr.pop();
};
```

➡️ top() : 스택 맨 위의 데이터 확인하기

```java
Stack.prototype.top = function () {
  return this.arr.slice(-1);
};
```

➡️ size() : 스택의 데이터 개수 출력

```java
Stack.prototype.size = function () {
  return this.arr.length;
};
```

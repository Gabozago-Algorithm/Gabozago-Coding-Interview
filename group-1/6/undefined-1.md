# 🐢 해시 테이블 : 구현

## <mark style="background-color:green;">**🫧 해시테이블 구현하기**</mark>

Linear probing을 사용하여 배열로 구현해보기

```java
class Node:
    def __init__(self, key, value, next):
        self.key = key
        self.value = value
        self.next = next
```

**➡️ hash(k, m) - m은 해시 테이블의 크기**

```jsx
// map의 크기: map.size()
map.size // 4
map.length // undefined
```

**➡️ add(key, value) - 키가 이미 존재한다면, 값을 갱신한다.**

```java
Hashtable ht = new Hashtable();
ht.Add("irina", "Irina SP");
ht.Add("tom", "Tom Cr");

if (ht.Contains("tom"))
{
    Console.WriteLine(ht["tom"]);
}
```

**➡️ exists(key)**

```jsx
map에 해당 key의 value 존재 여부: has(key)
map.has(str); // true
map.has(obj); // true
map.has('none'); // falsemap의 크기: map.size()
map.size // 4
map.length // undefinedmap의 크기: map.size()
map.size // 4
map.length // undefined
```

**➡️ get(key)**

*   Map 객체는 key-value로 이루어진 해시테이블

    * set(): key-value pair를 map에 삽입
    * get(): key값으로 value를 찾아 리턴
    * key에 들어갈 수 있는 자료형은 number, string, function, object, NaN 등이 가능

    ```jsx
    let number = 0;
    let str = 'string';
    let obj = { a: 1 };
    let func = () => {
        console.log('func');
    };

    map.set(number, 4); //key에 number 가능
    map.set(str, 1); // key에 string 가능
    map.set(obj, 2); //key에 object 가능
    map.set(func, 3); // key에 함수 가능
    map.set(number, 0); // 덮어쓰기 가능

    console.log(map); // Map(4) {0 => 0, "string" => 1, {…} => 2, ƒunc => 3}

    map.get(str); // 1
    map.get(obj); // 2
    map.get('none'); // undefined  
    map.get({ a: 1 }); // undefined, obj !== { a: 1 }
    ```

**➡️ remove(key)**

```csharp
using System;
using System.Collections;
public class SamplesHashtable
{

   public static void Main()
   {
      // Creates and initializes a new Hashtable.
      var myHT = new Hashtable();
      myHT.Add("1a", "The");
      myHT.Add("1b", "quick");

      // Removes the element with the key "3b".
      myHT.Remove("3b");

   }
}
```

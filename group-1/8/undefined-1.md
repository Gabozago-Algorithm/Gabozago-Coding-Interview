# 🐢 비트 연산 : 구현

## <mark style="background-color:purple;">**🫧 2의 보수, 음수**</mark>

: 컴퓨터가 정수를 저장할 때는 대부분 2의 보수 형태로 저장

![](<../../.gitbook/assets/image (13).png>)

: 음수를 나타내기 위해서는 기존의 수에서 비트를 뒤집은 다음(1의 보수) 1을 더해주면 되는데, 이는 기존의 수를 2의 보수 표현을 이용해서 음수로 나타낸 것

![](<../../.gitbook/assets/image (14).png>)



## <mark style="background-color:purple;">**🫧 산술 시프트, 논리 시프트**</mark>

: 비트를 1bit씩 밀면서 생긴 빈자리에 새로운 bit를 채워주는 연산

![](<../../.gitbook/assets/image (8).png>)

* 산술 시프트 연산
  * 부호비트를 그대로 채워준다
  * 기본적으로 2로 나누거나 곱한 결과와 같다
* 논리 시프트 연산
  * 부호비트에 0을 채워준다
  * 산술적으로는 거의 관계가 없는 것처럼 숫자가 변화



## <mark style="background-color:purple;">**🫧 기본 연산**</mark>

* NOT \[`~`] : 1이면 0, 0이면 1
*   OR \[`|`] : 두 값 중 1이 하나라도 있다면 1, 아니면 0

    합집합 개념과 유사하다.
*   XOR \[`^`] : 두 값이 다르면 1, 같으면 0

    실제로는 XOR에 들어가는 값 중 1의 갯수가 홀수개이면 1
*   AND \[`&`] : 두 값 모두 1이라면 1, 아니면 0

    교집합 개념과 유사하다.
* SHIFT \[`<<` `>>`] : 비트 단위로 한 칸씩 미는 연산

####

## <mark style="background-color:purple;">**🫧 함수 구현**</mark>

1. Get : 특정 위치의 비트 값을 가져온다.
2. Set : 특정 위치의 비트 값을 세팅한다.
3. Count : 세팅된 비트 값이 몇 개인지 반환한다.
4. Clear : 비트를 0으로 초기화 한다.
5. Toggle : 비트를 반전시킨다.
6. MSB : 최상위 비트를 찾는다.
7. LSB : 최하위 비트를 찾는다.



## <mark style="background-color:purple;">**🫧 비트마스크(BitMask)**</mark>

: 여러 표현 시 비트를 이용하여 메모리 사용을 줄이고 효율적으로 표현할 수 있다

ex) 집합 {1,2,3,5}가 있을 때 11101로 나타낼 수 있고 저장할 때는 10진수로 29를 저장하면 된다

: 배열을 이용할 필요없이 정수 하나만으로 저장이 가능하므로 메모리 사용을 줄일 수 있다
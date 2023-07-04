# 🐢 스택 : 이론

## <mark style="background-color:red;">**🫧 스택**</mark>

: 데이터를 쌓아 올린다

: **LIFO (Last In First Out)** 에 따라 자료를 배열한다

: 가장 최근에 스택에 추가한 항목이 가장 먼저 제거될 항목

: 배열과 달리 스택은 상수 시간에 i 번째 항목에 접근할 수 없음

: 스택에서 데이터를 추가하거나 삭제하는 연산은 상수 시간에 가능하다



## <mark style="background-color:red;">**🫧 스택이 유용할 경우**</mark>

: 재귀 알고리즘을 사용할 때 유용함

: 재귀적으로 함수를 호출해야 하는 경우에 임시 데이터를 스택에 넣어 주고, 재귀 함수를 빠져 나와 퇴각 검색(backtrack) 할 때는 스택에 넣어 주었던 임시 데이터를 빼 줘야 한다

: 일련의 행위를 직관적으로 가능하게 해 준다

: 재귀 알고리즘을 반복적 형태 (iterative) 를 통해서 구현할 수 있게 함
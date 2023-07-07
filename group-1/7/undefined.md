# 🐢 이진 탐색 : 이론

<본 블로그는 코딩인터뷰대학 님의 Git과 서적을 참고해서 공부하며 작성하였습니다 :-)>

## <mark style="background-color:orange;">🫧 트리</mark>

: 하나의 루트 코드를 가진다

: 루트 노드는 0개 이상의 자식 노드를 갖고 있다

: 트리에는 사이클 존재할 수 없다

: 노드들은 특정 순서로 나열될 수도 있고 그럴 수 없을 수도 있다

: 각 노드는 어떤 자료형으로도 표현이 가능하다



## <mark style="background-color:orange;">🫧 이진트리</mark>

: 각 노드가 최대 두 개의 자식을 갖는 트리



## <mark style="background-color:orange;">🫧 이진탐색트리</mark>

<figure><img src="https://blog.kakaocdn.net/dn/1gU1h/btsmGlbEPHl/bD1wy8rBZ3nIJg1UG3LyKk/img.png" alt="" height="195" width="513"><figcaption></figcaption></figure>

: “모든 왼쪽 자식들 ≤ n < 모든 오른쪽 자식들” 속성은 모든 노드 n에 대해서 반드시 참이어야 함

: 모든 노드에 대해서 왼쪽 자식들의 값이 현재 노드 값보다 작거나 같도록 하고, 오른쪽 자식들 값은 현재 노드의 값보다 반드시 커야함\


## <mark style="background-color:orange;">🫧 균형 vs 비균형</mark>

* 균형
  * 레드 블랙 트리
  * AVL 트리



## <mark style="background-color:orange;">🫧 완전이진트리</mark>

<figure><img src="https://blog.kakaocdn.net/dn/bqbV8J/btsmHa1zLhF/GrCMBVl98BwaoXK3sISZ5K/img.png" alt="" height="184" width="573"><figcaption></figcaption></figure>

: 트리의 모든 높이에서 노드가 꽉 차 있는 이진 트리

: 마지막 단계는 꽉 차 있지 않아도 되지만 노드가 왼쪽에서 오른쪽으로 채워져야 함



## <mark style="background-color:orange;">🫧 전이진트리</mark>

<figure><img src="https://blog.kakaocdn.net/dn/crbxbt/btsmGPQRQuY/Ye4dm1vO1bAp8aJcAZSFD1/img.png" alt="" height="197" width="526"><figcaption></figcaption></figure>

: 모든 노드의 자식이 없거나 정확히 두 개 있는 경우

: 자식이 하나만 있는 노드가 존재해서는 안됨



## <mark style="background-color:orange;">🫧 포화이진트리</mark>

<figure><img src="https://blog.kakaocdn.net/dn/nd3FP/btsmJherDXL/sYGtKV6Krw9Shiu0ZyZB7K/img.png" alt="" height="222" width="383"><figcaption></figcaption></figure>

: 전 이진 트리이면서 완전 이진 트리인 경우

: 모든 말단 노드는 같은 높이에 있어야 하며, 마지막 단계에서 노드의 개수가 최대가 되어야 한다

: 노드의 개수가 정확히 2^K-1 (K는 트리의 높이) 개

\

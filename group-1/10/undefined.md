# 🐢 이진 탐색 트리 : 이론

#### 🫧 이진탐색트리

<figure><img src="https://blog.kakaocdn.net/dn/bBMJbZ/btsngJbpyNQ/thXg5qZNJxydTYn77jjLZK/img.png" alt="" height="195" width="513"><figcaption></figcaption></figure>

: “모든 왼쪽 자식들 ≤ n < 모든 오른쪽 자식들” 속성은 모든 노드 n에 대해서 반드시 참이어야 함

: 모든 노드에 대해서 왼쪽 자식들의 값이 현재 노드 값보다 작거나 같도록 하고, 오른쪽 자식들 값은 현재 노드의 값보다 반드시 커야함

&#x20;

#### 🫧 균형 vs 비균형

* 균형
  * 레드 블랙 트리
  * AVL 트리

&#x20;

#### 🫧 완전이진트리

<figure><img src="https://blog.kakaocdn.net/dn/cT9nhY/btsngtGnxC2/ogpsIkSaL3YviKeDs5Nvb1/img.png" alt="" height="184" width="573"><figcaption></figcaption></figure>

: 트리의 모든 높이에서 노드가 꽉 차 있는 이진 트리

: 마지막 단계는 꽉 차 있지 않아도 되지만 노드가 왼쪽에서 오른쪽으로 채워져야 함

&#x20;

#### 🫧 전이진트리

<figure><img src="https://blog.kakaocdn.net/dn/NIbL9/btsngNxRGMM/HYoJp0a08HLf7PdiixQjM1/img.png" alt="" height="197" width="526"><figcaption></figcaption></figure>

: 모든 노드의 자식이 없거나 정확히 두 개 있는 경우

: 자식이 하나만 있는 노드가 존재해서는 안됨

&#x20;

#### 🫧 포화이진트리

<figure><img src="https://blog.kakaocdn.net/dn/ARqBo/btsnaM7PKsa/Mb8noMsBRlNPs0QyZnFOT1/img.png" alt="" height="222" width="383"><figcaption></figcaption></figure>

: 전 이진 트리이면서 완전 이진 트리인 경우

: 모든 말단 노드는 같은 높이에 있어야 하며, 마지막 단계에서 노드의 개수가 최대가 되어야 한다

: 노드의 개수가 정확히 2^K-1 (K는 트리의 높이) 개

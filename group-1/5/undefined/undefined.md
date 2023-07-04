# 🐢 큐 : 구현

## <mark style="background-color:red;">**🫧 큐 구현하기**</mark>

**💖 tail 포인터가 있는 연결 리스트를 사용하여 구현하기**

*   enqueue(value) - tail이 가리키는 곳에 value를 추가한다

    ```cpp
    int main()
    {
        int keys[] = { 1, 2, 3, 4, 5 };
        Queue q;
     
        // 위의 키 삽입
        for (int key: keys) {
            q.enqueue(key);
        }
        return 0;
    }
    ```
*   dequeue() - value를 반환하고 가장 최근에 추가된 원소(front)를 제거한다.

    ```cpp
    int main()
    {
        int keys[] = { 1, 2, 3, 4, 5 };
        Queue q;
     
        // 위의 키 삽입
        for (int key: keys) {
            q.enqueue(key);
        }
     
        cout << q.dequeue() << endl;    // 1을 출력
        cout << q.dequeue() << endl;    // 2를 출력
     
        return 0;
    }
    ```
*   empty()

    ```cpp
    #include <iostream>
    #include <stack>
    #include <cstdlib>
    using namespace std;
     
    // 두 개의 Stack을 사용하여 Queue 구현
    class Queue
    {
        stack<int> s1, s2;
     
    public:
        // Queue에 아이템 추가
        void enqueue(int data)
        {
            // 첫 번째 Stack의 모든 요소를 두 번째 Stack으로 이동
            while (!s1.empty())
            {
                s2.push(s1.top());
                s1.pop();
            }
     
            // 항목을 첫 번째 Stack에 푸시
            s1.push(data);
     
            // 모든 요소를 두 번째 Stack에서 첫 번째 Stack으로 다시 이동합니다.
            while (!s2.empty())
            {
                s1.push(s2.top());
                s2.pop();
            }
        }
     
        // Queue에서 아이템 제거
        int dequeue()
        {
            // 첫 번째 Stack이 비어 있는 경우
            if (s1.empty())
            {
                cout << "Underflow!!";
                exit(0);
            }
     
            // 첫 번째 Stack의 최상위 항목을 반환합니다.
            int top = s1.top();
            s1.pop();
            return top;
        }
    };
    ```



**🧡 고정 길이 배열을 사용하여 구현하기**

* enqueue(value) - 사용 가능한 저장 공간의 끝에 item을 추가한다.
* dequeue() - value를 반환하고 가장 최근에 추가된 원소를 제거한다.
* empty()
* full()



**💛 비용**

* a bad implementation using linked list where you enqueue at head and dequeue at tail would be O(n) because you'd need the next to last element, causing a full traversal each dequeue
* enqueue: O(1) (amortized, linked list and array \[probing])
* dequeue: O(1) (linked list and array)
* empty: O(1) (linked list and array)

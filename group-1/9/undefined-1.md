# 🐢 트리 : 구현

**🫧 노드의 선언**

```c
#define N 10

typedef struct tagNode {
	char data;
	int degree;
	struct tagNode child[N];
} Node;
```



**🫧 트리의 선언**

```c
typedef struct tagTree {
	Node *root;
}Tree;
```



**🫧 생성자**

```c
Node* newNode(char data) {
	Node* returnNode = (Node*)malloc(sizeof(Node));
	returnNode->data = data;
	returnNode->degree = 0;
	returnNode->child = NULL;
	return returnNode;
}

Tree* newTree() {
	Tree* returnTree = (Tree*)malloc(sizeof(Tree));
	returnTree->root = NULL;
	return returnTree;
}
```



**🫧 트리**

```c
#include <stdio.h>
#include <stdlib.h>

typedef struct node //구조체 정의
{
    int data;
    struct node *left;
    struct node *right;
}NODE;
  
/* newNode(): 노드에 메모리 할당하고 초기화*/
NODE* newNode(int data)
{
  //노드에 메모리 할당 
  NODE* node = (NODE*)malloc(sizeof(NODE));
  
  //데이터 넣음
  node->data = data;
  
  // 왼쪽, 오른쪽 노드를 NULL로 초기화
  node->left = NULL;
  node->right = NULL;
  return(node);
}
  
  
int main()
{
  /*루트 노드를 만든다*/
  NODE *root = newNode(1);  
  /* 루트 노드를 만든 상태
  
        1
      /   \\
     NULL  NULL  
  */
    
  
  root->left        = newNode(2);
  root->right       = newNode(3);
  /* 루트 노드1에 왼쪽, 오른쪽에 각각 2, 3이라는 자식 노드 추가한 상태
           1
         /   \\
        2      3
     /    \\    /  \\
    NULL NULL NULL NULL
  */
  
  
  root->left->left  = newNode(4);
  /* 2의 왼쪽 자식으로 4를 추가한 상태
           1
       /       \\
      2          3
    /   \\       /  \\
   4    NULL  NULL  NULL
  /  \\
NULL NULL
*/
  
  getchar();
  return 0;
}
```

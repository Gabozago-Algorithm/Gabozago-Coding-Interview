# 🐢 이진 탐색 : 구현

## <mark style="background-color:red;">**🫧 이진 탐색**</mark>

처음에 N개 크기의 배열에서 단계가 하나씩 지나감에 따라 탐색할 배열의 크기가 반씩 줄어들기 때문



## <mark style="background-color:red;">**🫧 (정수가 정렬된 배열에서) 이진 탐색**</mark>

```jsx
int BSearch(int arr[], int target) {
    int low = 0;
    int high = arr.length - 1;
    int mid;

    while(low <= high) {
        mid = (low + high) / 2;

        if (arr[mid] == target)
            return mid;
        else if (arr[mid] > target)
            high = mid - 1;
        else
            low = mid + 1;
    }
    return -1;
}
```



## <mark style="background-color:red;">🫧 재귀를 사용한 이진 탐색</mark>

```jsx
int BSearchRecursive(int arr[], int target, int low, int high) {
    if (low > high)
        return -1;

    int mid = (low + high) / 2;
    if (arr[mid] == target)
        return mid;
    else if (arr[mid] > target)
        return BSearchRecursive(arr, target, low, mid-1);
    else
        return BSearchRecursive(arr, target, mid+1, high);
}
```

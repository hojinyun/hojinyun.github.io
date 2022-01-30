---
title:  "Insertion Sort(삽입 정렬)"
categories: [Algorithm & Data Structure]
tags: [Sorting]
---
# 삽입 정렬

## 설명:

삽입 정렬은 다른 정렬과 달리 필요할 때만 위치를 바꾸는 정렬 기법이다. Array에 각 값을 한번 씩 확인하는데 그 특정 값 기준 왼쪽으로는 정렬이 돼 있다고 가정한다. 그 값과 왼쪽에 있는 값들을 왼쪽으로 가면서 그 숫자와 비교하고 맞는 자리에 넣어 준다.

## 예시:

1 5 10 8 7 6 4 같은 숫자가 있을 때 4번째 숫자 8은 들어 갈 수 있는 자리가

_ 1 _ 5 _ 10 _  이렇게 있다. 10과 처음에 비교를 하고 5와도 비교를 10보다 작으니 위치를 바꾸고 5와 비교를 하였지만 5보다 크므로 자리를 안바꾸고 다음 인덱스의 7로 넘어간다.

## 예시 코드:

```cpp
#include <iostream>
using namespace std;

int main(){
	int i, j, temp;
	int array[10]={10, 9, 8, 7, 6, 5, 4, 3, 2, 1};
	for(i=0;i<9;i++){
		j=i;
		while(array[j]>array[j+1]){
			temp = array[j];
			array[j] = array[j+1];
			array[j+1] = temp;
			j--;
		}
	}	
	for(i=0; i<10; i++){
		cout<<array[i]<<" ";
	}
	return 0;
}
```

## 시간 복잡도:

O(N^2)  🔎정렬이 어느정도 된 array면 더 빠르게 작동함 b/c 필요할 때만 위치를 바꾸기 때문
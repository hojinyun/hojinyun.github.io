---
title:  "Selection Sort(선택 정렬)"
categories: [Algorithm & Data Structure]
tags: [Sorting]
---
# 선택 정렬

## 설명:

선택 정렬은 제일 첫번 째 인덱스부터 마지막 인덱스까지 array 전체를 돌면서 최솟 값을 넣어 주는 정렬이다.

## 예시:

![https://miro.medium.com/max/1400/1*5WXRN62ddiM_Gcf4GDdCZg.gif](https://miro.medium.com/max/1400/1*5WXRN62ddiM_Gcf4GDdCZg.gif)

## 예시 코드:

```cpp
#include <iostream>
using namespace std;

int main(){
	int i, j, min, index, temp;
	int array[10]={1,10,5,8,7,6,4,3,2,9};
	for(i=0;i<10;i++){
		min = 9999;
		for (j=i;j<10;j++){
			if (array[j]<min){
				min=array[j];
				index = j;
			}
		}
		temp = array[i];
		array[i] = array[index];
		array[index] = temp;
	}
	for(i=0;i<10;i++){
		printf("%d ",array[i]);
	}
	return 0;
	
}
```

## 시간 복잡도:

O(N^2)
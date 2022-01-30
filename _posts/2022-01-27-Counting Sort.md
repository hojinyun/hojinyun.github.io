---
title:  "Counting Sort(계수 정렬)"
categories: [Algorithm & Data Structure]
tags: [Sorting]
---
# 계수 정렬

## 설명:

크기가 한정 되어 있는 데이터 한에서 사용 하는데 그 이유는 counting sort는 특정 데이터의 계수를 세어서 그 데이터의 개수 만큼 순서대로 다시 출력 하는 방식을 사용하기 때문이다.

## 예시:

1, 5, 4, 3, 2, 2, 3, 5, 1, 3, 1 의 데이터 셋이 있으면 크기 5의 array를 만든 다음 첫번 째 인덱스에는 1의 개수를 넣고 두번째는 2의 개수를 세어서 넣는 방식이다.

## 예시 코드:

```cpp
#include <stdio.h>

int main(void){
	int temp;
	int count[5];
	int array[30] = {
		1, 3, 2, 4, 3, 2, 5, 3, 1, 2,
		3, 4, 4, 3, 5, 1, 2, 3, 5, 2,
		3, 1, 4, 3, 5, 1, 2, 1, 1, 1 
	};
	
	for(int i = 0; i < 5; i++){
		count[i] = 0;
	}
	for(int i = 0; i < 30; i++){
		count[array[i]-1]++;
	}
	for (int i = 0; i < 5; i++){
		if(count[i] != 0){
			for(int j = 0; j < count[i]; j++){
				printf("%d ", i+1);
			}
		}
	}
	
	return 0;
}
```

## 시간 복잡도:

O(N)
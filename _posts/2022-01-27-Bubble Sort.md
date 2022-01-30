---
title:  "Bubble Sort(버블 정렬)"
categories: [Algorithm & Data Structure]
tags: [Sorting]
---
# 버블 정렬

## 설명:

구현이 쉽다는 장점이 있는 알고리즘 이지만 그만큼 제일 비효율적인 알고리즘이다. 붙어 있는 두 숫자를 비교해서 작은걸 앞으로 보내고 큰 것을 뒤로 보낸다. 이렇게 하면 제일 큰 수가 제일 뒤로 가기 때문에 loop을 한번 돌 때마다 마지막 자리에서 빼기 1을 한 인덱스까지만 정렬을 실행 해주면 된다. 제일 큰 수를 오른쪽에서 하나씩 비교하면서 끌어 올려 오른쪽부터 정렬 해준다고 생각하면 편하다.

## 예시:

![https://miro.medium.com/max/1102/1*OJuKXwBjg2JtgDDP9SI0qA.gif](https://miro.medium.com/max/1102/1*OJuKXwBjg2JtgDDP9SI0qA.gif)

## 예시 코드:

```cpp
#include <iostream>
using namespace std;

int main(){
	int i, j, temp;
	int array[10]={10, 9, 8, 7, 6, 5, 4, 3, 2, 1};
	
	for (i=0; i<10; i++){
		for(j = 0; j<9-i; j++){
			if(array[j]>array[j+1]){
				temp = array[j];
				array[j]=array[j+1];
				array[j+1]=temp;
			}
		}
	}
	
	for(i=0; i<10; i++){
		cout<<array[i]<<" ";
	}
}
```

## 시간 복잡도:

O(N^2)

## 문제 풀이:

[#2750 수 정렬하기](/algorithm%20&%20data%20structure/2750-수-정렬하기/)
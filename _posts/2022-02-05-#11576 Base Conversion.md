---
title:  "#11576: Base Conversion"
categories: [Algorithm & Data Structure]
tags: Math
---

[백준 11576번: Base Conversion](https://www.acmicpc.net/problem/11576)

## 문제:

타임머신을 개발하는 정이는 오랜 노력 끝에 타임머신을 개발하는데 성공하였다. 미래가 궁금한 정이는 자신이 개발한 타임머신을 이용하여 500년 후의 세계로 여행을 떠나게 되었다. 500년 후의 세계에서도 프로그래밍을 하고 싶었던 정이는 백준 사이트에 접속하여 문제를 풀기로 하였다. 그러나 미래세계는 A진법을 사용하고 있었고, B진법을 사용하던 정이는 문제를 풀 수가 없었다. 뛰어난 프로그래머였던 정이는 A진법으로 나타낸 숫자를 B진법으로 변환시켜주는 프로그램을 작성하기로 하였다.

N진법이란, 한 자리에서 숫자를 표현할 때 쓸 수 있는 숫자의 가짓수가 N이라는 뜻이다. 예를 들어 N은 17일 때 한 자릿수에서 사용할 수 있는 수는 0, 1, 2, ... , 16으로 총 17가지가 된다.

## 입력:

입력의 첫 줄에는 미래세계에서 사용하는 진법 A와 정이가 사용하는 진법 B가 공백을 구분으로 주어진다. A와 B는 모두 2이상 30이하의 자연수다.

입력의 두 번째 줄에는 A진법으로 나타낸 숫자의 자리수의 개수 m(1 ≤ m ≤ 25)이 주어진다. 세 번째 줄에는 A진법을 이루고 있는 숫자 m개가 공백을 구분으로 높은 자릿수부터 차례대로 주어진다. 각 숫자는 0이상 A미만임이 보장된다. 또한 수가 0으로 시작하는 경우는 존재하지 않는다.

A진법으로 나타낸 수를 10진법으로 변환하였을 때의 값은 양의 정수이며 220보다 작다.

## 풀이:

- 이 문제를 우선 풀기 위해서는 이해를 잘 해야 된다. 작성자는 문제 이해를 잘못 하여 삽질만 1시간 하였다. 처음에 문제에서 m이 자리 수라고 말해주었지만 무슨 말인지 이해가 안돼서 각 숫자를 A진수에서 B진수를 바꿔주면 되는 문제인줄 알았다. 하지만, 문제가 말하는 것은 3번째 줄의 입력값은 A진수로 나타낸 하나의 값이라는 것이다. 예를 들면, 11진수인 경우에 2 10입력이 세번째 줄에 들어오면 2A와 같은 값이라는 것이다.
- 따라서 오히려 풀기 쉬워졌다. 왜냐하면 알파벳인 경우를 구분 안해줘도 되기 때문이다. 이 문제를 풀기 전에 [#2745: 진법 변환](/algorithm%20&%20data%20structure/2745-진법-변환/)과 [#11005: 진법 변환 2](/algorithm%20&%20data%20structure/11005-진법-변환-2/)를 안풀어 봤으면 풀어보길 바란다. 왜냐하면, 이 문제를 풀기 위해서는 10진수를 한번 거쳐가야 되기 때문에 두가지 부분으로 나눌 수 있다. A진수에서 10진수로 바꿔주는 부분 10진수에서 B진수로 바꿔주는 부분이다. [#2745: 진법 변환](/algorithm%20&%20data%20structure/2745-진법-변환/)이 A진수에서 10진수로 바꿔주는 문제이고 [#11005: 진법 변환 2](/algorithm%20&%20data%20structure/11005-진법-변환-2/)가 10진수에서 A진수로 바꿔주는 문제이다.
- [#2745: 진법 변환](/algorithm%20&%20data%20structure/2745-진법-변환/)과 [#11005: 진법 변환 2](/algorithm%20&%20data%20structure/11005-진법-변환-2/)에서의 차이점은 11진수 이상일 때 알파벳 구분이기 때문에 각 문제에서 알파벳 예외 처리 해준 것을 지워주고 숫자들을 char 자료형으로 받아서 int로 바꿔주는 연산도 그냥 int 연산으로 바꿔주면 된다.

### 코드:

```cpp
#include <iostream>
#include <stack>

using namespace std;

int main(){
	int A, B, m, dec=0;
	stack<int> answer;
	//첫번째 줄과 두번째 줄 입력
	cin >> A >> B >> m;
	for(int i = 0; i < m; i++){
		int number;
		cin >> number;
		//A진법에서 10진법으로 변환 
		dec = dec*A+number;
	}
	//10진법에서 B진법으로 변환 
	while(dec > 0) {
		answer.push(dec%B);
		//숫자를 반내림으로 나누어 줌 
		dec /= B;
	}
	//출력
	while(!answer.empty()){
		cout<<answer.top()<<" ";
		answer.pop();
	}
}
```
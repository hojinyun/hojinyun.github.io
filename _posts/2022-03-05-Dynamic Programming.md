---
title:  "Dynamic Programming(동적 프로그래밍)"
categories: [Algorithm & Data Structure]
tags: [Dynamic Programming]
---
# 동적 프로그래밍

## 설명:

- 아래의 설명은 [유튜브 동빈나](https://www.youtube.com/watch?v=5Lu34WIx2Us&ab_channel=%EB%8F%99%EB%B9%88%EB%82%98)님의 다이나믹 프로그래밍 강의를 정리하였다. 정말 잘 설명 해주시니 다이나믹 프로그래밍이 무엇인지 잘 모른다면 꼭 확인 해보길 권한다.

다이나믹 프로그래밍(동적 프로그래밍은) 메모리를 적절히 사용하여 수행 시간의 효율성을 비약적으로 올리는 방법이다. 이미 계산 된 결과를 배열에 저장함으로 써 한번 더 수행하는 것을 방지하며 정답이 바로 나오도록 한다. 이렇게 한번 계산한 결과를 메모리 공간에 메모 하는 형식의 기법을 메모이제이션(memoization)/캐싱(caching)이라고 한다. 그렇다고 해서 메모이제이션은 다이나믹 프로그래밍에만 국한 된 것이 아닌 다른 기법에도 사용 될 수 있다는 것을 기억하자. 다이나믹 프로그래밍은 두 종류로 나뉜다:

1. 탑 다운(Top-down): 위에서 아래로 내려온다는 뜻으로 하향식이라고도 한다. 재귀 함수를 사용하여 구현한다.

2. 보텀 업(Bottom-up): 아래에서 위로 올라간다는 뜻으로 상향식이라고도 한다. for문을 사용하여 구현한다.

사용 조건:

1. 최적 부분 구조(Optimal Substructure) - 큰 문제를 작은 문제로 나눌 수 있으며 작은 문제의 답을 모아 큰 문제가 해결 가능할 때
2. 중복되는 부분 문제(Overlapping Subproblem) - 동일한 작은 문제를 반복적으로 해결 해야 될 시

## 예시:

다이나믹 프로그래밍을 설명할 때 제일 많이 드는 예시는 피보나치 수열이다. 피보나치 수열은 n번째 값이 n-1번째 값 더하기 n-2 번째 값인 수열을 뜻 한다. 다이나믹 프로그래밍이 피보나치 수열에서 사용 되는 방식은 n-1번째 값이나 n-2번째 값이 이미 계산이 한번 실행 되었을 경우 연산을 한번 더 하는 것이 아닌 배열에 저장 된 답을 불러오는 방식이다. 피보나치 수열은 보통 재귀함수를 사용하여 탑 다운 방식으로 풀지만 보텀 업 방식으로도 n번째까지 for문을 돌면서 활용 가능하다.

## 문제 풀이:

#### 🥉브론즈(Bronze):

#### 🥈실버(Silver):

[#1149: RGB거리](/algorithm%20&%20data%20structure/1149-RGB거리/)

[#1309번: 동물원](/algorithm%20&%20data%20structure/1309번-동물원/)

[#1463: 1로 만들기](/algorithm%20&%20data%20structure/1463-1로-만들기/)

[#1699: 제곱수의 합](/algorithm%20&%20data%20structure/1699-제곱수의-합/)

[#1912: 연속합](/algorithm%20&%20data%20structure/1912-연속합/)

[#1932: 정수 삼각형](/algorithm%20&%20data%20structure/1932-정수-삼각형/)

[#2156: 포도주 시식](/algorithm%20&%20data%20structure/2156-포도주-시식/)

[#2193: 이친수](/algorithm%20&%20data%20structure/2193-이친수/)

[#9095: 1, 2, 3 더하기](/algorithm%20&%20data%20structure/9095-1,-2,-3-더하기)

[#9465: 스티커](/algorithm%20&%20data%20structure/9465-스티커)

[#10844: 쉬운 계단 수](/algorithm%20&%20data%20structure/10844-쉬운-계단-수)

[#11052: 카드 구매하기](/algorithm%20&%20data%20structure/11052-카드-구매하기/)

[#11053: 가장 긴 증가하는 부분 수열](/algorithm%20&%20data%20structure/11053-가장-긴-증가하는-부분-수열/)

[#11055: 가장 큰 증가 부분 수열](/algorithm%20&%20data%20structure/11055-가장-큰-증가-부분-수열/)

[#11057: 오르막 수](/algorithm%20&%20data%20structure/11057-오르막-수/)

[#16194: 카드 구매하기 2](/algorithm%20&%20data%20structure/16194-카드-구매하기-2/)

[#11722: 가장 긴 감소하는 부분 수열](/algorithm%20&%20data%20structure/11722-가장-긴-감소하는-부분-수열/)

[#11726: 2×n 타일링](/algorithm%20&%20data%20structure/11726-2-n-타일링/)

[#11727: 2×n 타일링 2](/algorithm%20&%20data%20structure/11726-2-n-타일링-2/)

[#15988: 1, 2, 3 더하기 3](/algorithm%20&%20data%20structure/15988-1,-2,-3-더하기-3)

[#15990: 1, 2, 3 더하기 5](/algorithm%20&%20data%20structure/15990-1,-2,-3-더하기-5)


#### 🥇골드(Gold):

[#2133: 타일 채우기](/algorithm%20&%20data%20structure/2133-타일-채우기)

[#2225: 합분해](/algorithm%20&%20data%20structure/2225-합분해/)

[#11054: 가장 긴 바이토닉 부분 수열](/algorithm%20&%20data%20structure/11054-가장-긴-바이토닉-부분-수열/)

[#13398: 연속합 2](/algorithm%20&%20data%20structure/13398-연속합-2/)

[#14002: 가장 긴 증가하는 부분 수열 4](/algorithm%20&%20data%20structure/14002-가장-긴-증가하는-부분-수열-4/)

[#17404: RGB거리 2](/algorithm%20&%20data%20structure/17404-RGB거리-2/)

#### 👑플레티넘(Platinum):
---
layout: post 
tag: Advance
title: Knapsack
date: 2018.08.01
---

## Knapsack  

### 참고

- [http://huiyu.tistory.com/entry/DP-01-Knapsack배낭-문제](http://huiyu.tistory.com/entry/DP-01-Knapsack배낭-문제)  

<br>
### 특징  

Knapsack 문제는 **제한된 무게**에서 가치가 높은 물건들을 넣어 **전체적으로 가치를 최대화**하는 문제입니다.   
**DP 문제**의 일종입니다.   
종류는 여러 종류가 있는데 **0/1 Knapsack에 대해** 간략히 알아보겠습니다.  

<br>
### 알고리즘   
문제를 풀기위해 **2차원 배열**이 필요로 합니다.  
배열에서 **첫번째 인덱스**는 **물건의 종류**, **두번째 인덱스**는 현재까지 물건을 담은 **가방의 무게**입니다.   
<br>
2중 for문을 사용하며, **바깥쪽** for문의 경우 **물건의 종류**에 대한 반복을 수행하고, **안쪽** for문의 경우 **가방 무게**에 대한 반복을 수행합니다.  
```
for i = 1 to N:
	for j = 1 to W:
		if a[i].w <= j:	//새로운 물건을 넣을 수 있는 경우
			dp[i][j] = max(a[i].v + dp[i - 1][j - a[i].w], dp[i - 1][j])	//이득이 큰 쪽으로
		else:			//새로운 물건을 넣을 수 없는 경우
			dp[i][j] = dp[i - 1][j]	//이전 값을 가져옴
```

<br>
### 관련 문제  
- [https://www.acmicpc.net/problem/12865](https://www.acmicpc.net/problem/12865)  

<br>

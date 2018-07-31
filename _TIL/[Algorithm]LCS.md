---
layout: post 
tag: Advance
title: LCS
date: 2018.08.01
---

## LCS  

### 참고

- [http://mygumi.tistory.com/126](http://mygumi.tistory.com/126)  
- [http://알고리즘.com/boj/17](http://알고리즘.com/boj/17)  

<br>
### 특징  

LCS는 **두가지 뜻**이 있습니다.  
LCS(Longest Common **Substring**) 와 LCS(Longest Common **Subsequence**)입니다  
두개의 차이점은 **연속성**입니다.  
**전자**는 주어진 문자열 중 가장 긴 **스트링(이어진)**을 찾는 것이고, **후자**는 가장 긴 **수열(이어질 필요 없음)**을 찾는 것입니다.   
<br>
아래와 같이 두 문자열이 존재하면  
ABCDFG  
BCDEG  

|구분|결과|
|:---:|:---:|
|Longest Common Substring|**BCD**|
|Longest Common Subsequence|**BCG**|

가 됩니다.  
<br>
보통 LCS를 푸는 알고리즘이라고 하면 **후자**를 의미합니다.  
여기서도 **후자**를 다루겠습니다.  
<br>
### 알고리즘   
두 문자열 A, B에 대하여 다음 알고리즘이 성립합니다.  
```
if A[i] == B[j]:
	dp[i][j] = dp[i-1][j-1] + 1
else:
	dp[i][j] = max(dp[i-1][j], dp[i][j-1])
```

<br>
### 관련 문제  
- [https://www.acmicpc.net/problem/9251](https://www.acmicpc.net/problem/9251)  
- [https://www.acmicpc.net/problem/9252](https://www.acmicpc.net/problem/9252)  
- [https://www.acmicpc.net/problem/1958](https://www.acmicpc.net/problem/1958)  

<br>

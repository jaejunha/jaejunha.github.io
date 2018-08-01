---
layout: post 
tag: Library
title: 순열
date: 2018.08.01
---

## 순열  
### 특징  

C++에서 순열 함수를 **STL로 제공**합니다.   
반복문을 통해 총 **n!개의 경우의 수**를 만들 수 있니다.  

### 헤더   

```
#include <algorithm>
```

<br>
### 적용  

```
sort(a, a + n);	//순열 함수를 사용하기전 정렬을 해줍니다.
...
do{
    ...
}while(next_permutation(a, a + n));	//마지막 경우의 수가 나올 때까지 순열 생성
```

<br>

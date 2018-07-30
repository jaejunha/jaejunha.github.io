---
layout: post 
tag: Library
title: 우선 순위 큐
date: 2018.07.30
---

## 우선 순위 큐  
### 특징  

**큐**와 동일하지만 **정렬하면서 삽입**하는 것이 차이점입니다.   
**최대, 최소 힙**과 동일합니다.  
**다익스트라** 알고리즘에 주로 사용이됩니다.  

### 헤더   

```
#include <queue>
#include <functional>	//오름 차순 할 때 사용
```

<br>
### 선언  

```
priority_queue<int> q;	//일반적인 선언(내림 차순)
priority_queue<int, vector<int>, greater<int>> q;	//오름 차순 선언
```

<br>
### 연산  

```
q.push(1);			//큐에 1을 넣음
int v = q.top();	//큐에서 가장 앞에 있는 값을 읽어옴
q.pop();			//큐에서 가장 앞에 있는 놈을 뺌(읽어오지 않음!)
```

<br>

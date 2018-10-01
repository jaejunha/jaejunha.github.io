---
layout: post 
tag: PS
title: 등산로 조성
date: 2018.09.30
---

## 등산로 조성  

### 참고

- [https://www.swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PoOKKAPIDFAUq](https://www.swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV5PoOKKAPIDFAUq)  

<br>
### 유형  

`DFS`, `백트래킹`  

<br>

### 통과  

첫 시도 49/50 통과  
**원인**: 백트래킹을 사용하지 않고 배열을 매개변수로 넘겼는데 로직 오류 발생  

<br>

### 특징   

산을 한번 깍을 수 있다는 점  
<br>

### 알고리즘   
가장 높은 봉우리가 여러개 이므로 입력 받을 때 가장 높은 봉우리 파악  
**a\[i\]\[j\]**: 상태판  
**v\[i\]\[j\]**: 방문 여부 체크  
**m**: 가장 높은 봉우리의 높이  

```
for (int i = 1; i <= n; i++) {
	for (int j = 1; j <= n; j++) {
		cin >> a[i][j];
		v[i][j] = false;
		/* 최대 높이 측정 */
		m = max(m, a[i][j]);
	}
}
```
<br>

백트래킹 사용  
**x, y**: 기준 좌표  
**px, py**: 이동할 좌표  
**b**: 높이를 이미 깍았는 지  
**c**: 이동 거리  
**temp**: 백트래킹시 높이 복원 용도  

```
void dfs(int x, int y, int c, bool b) {
	v[x][y] = true;
	for (int i = 0; i < 4; i++) {
		int px = x + dx[i];
		int py = y + dy[i];
		
		/* 상태판 밖으로 나간 경우 */
		if (px<1 || py<1 || px>n || py>n)
			continue;
		/* 이미 방문 한 경우 */
		if (v[px][py])
			continue;
		
		/* 높이가 낮을 경우만 이동 */
		if (a[px][py] < a[x][y])
			dfs(px, py, c + 1, b);
			
		/* 높이가 높은 경우 한번 깍을 수 있을때 이동 */
		else if ((a[px][py] < a[x][y] + k) && !b) {
			/* 높이 복원 용도 */
			int temp = a[px][py];
			/* 가능성을 고려해 현재 높이기준으로 1만 더 깍음 */
			a[px][py] = a[x][y] - 1;
			dfs(px, py, c + 1, true);
			/* 높이 복원 */
			a[px][py] = temp;
		}
	}
	/* 방문 복원 */
	v[x][y] = false;
	/* 최대 거리 갱신 */
	s = max(s, c);
}
```

<br>
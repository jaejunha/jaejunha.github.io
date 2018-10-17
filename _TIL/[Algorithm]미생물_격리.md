---
layout: post 
tag: PS
title: 미생물 격리
date: 2018.10.1
---

## 등산로 조성  

### 참고

- [https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV597vbqAH0DFAVl&categoryId=AV597vbqAH0DFAVl&categoryType=CODE](https://swexpertacademy.com/main/code/problem/problemDetail.do?contestProbId=AV597vbqAH0DFAVl&categoryId=AV597vbqAH0DFAVl&categoryType=CODE)  

<br>
### 유형  

`시뮬레이션`  

<br>

### 통과  

첫 시도 50/50 통과  

<br>

### 특징   

**벽에 부딛히면** 미생물의 수가 반으로 감소  
합쳐지는 경우 **3방향 이상에서** 같은 곳으로 도착해 합쳐질 수 있음  

<br>

### 알고리즘   
미생물의 정보가 **3개 이상이기 때문에 구조체 사용**  
미생물의 군집을 **벡터**로 표기  
미생물이 특정 지점을 **방문한 것을 bool형 배열로 체크**(for문 돌 때마다 초기화)  
미생물 **합치는 과정을 자료구조 집합을 활용**하여 합침  

```
#include <iostream>
#include <algorithm>
#include <set>
#include <vector>
using namespace std;

/* 미생물 정보를 담을 구조체 */
typedef struct A{
    int x, y, c, d;
}A;
 
int n, m, k, t;
int dx[] = { -1,1,0,0 };
int dy[] = { 0,0,-1,1 };
bool b[100][100];
 
int main() {
    int m;
    cin >> t;
    for (int z = 1; z <= t; z++) {
        cin >> n >> m >> k;
        int x, y, c, d;
        vector<A> v;
        A a;
        for (int i = 1; i <= k; i++) {
            cin >> x >> y >> c >> d;
            a.x = x;
            a.y = y;
            a.c = c;
            a.d = d;
            v.push_back(a);
        }
        int l = v.size();
        for (int i = 1; i <= m; i++) {
            for (int j = 0; j < n; j++) {
                for (int k = 0; k < n; k++)
                    b[j][k] = false;
            }
             
            /* 세균들이 합치는 것 고려할 집합 */
            set<pair<int, int>> st;
 
            for (int j = 0; j < l; j++) {
            	/* 합쳐지고 버려진 미생물 군단은 건너뜀 */
                if (!v[j].c)
                    continue;
                    
                /* 이동할 위치 파악 */   
                int px = v[j].x + dx[v[j].d - 1];
                int py = v[j].y + dy[v[j].d - 1];
                v[j].x = px;
                v[j].y = py;
 
                /* 벽에 닿은 경우 */
                if (px == 0 || py == 0 || px == n - 1 || py == n - 1) {
                    v[j].c = v[j].c / 2;
                    if (!v[j].c)
                        continue;
                    if (v[j].d == 1)
                        v[j].d = 2;
                    else if (v[j].d == 2)
                        v[j].d = 1;
                    else if (v[j].d == 3)
                        v[j].d = 4;
                    else
                        v[j].d = 3;
                }
 
                /* 옮긴 자리에 이미 세균이 있는 경우 */
                if (b[px][py])
                    st.insert({ px,py });
                    
                /* 방문했다는 것을 체크 */
                b[px][py] = true;
            }
            
            /* 미생물 합치기 */
            for (pair<int, int> p : st) {
                int mx = -1;
                int s = 0;
                for (int k = 0; k < l; k++) {
                    if (v[k].x == p.first && v[k].y == p.second) {
                        if (mx == -1) {
                            mx = k;
                            s += v[k].c;
                        }
                        else {
                            if (v[mx].c < v[k].c) {
                                /* 합쳐지고 남은 군단은 제거 */
                                v[mx].c = 0;
                                mx = k;
                                /* 합쳐질 군단의 미생물 수 카운트 */
                                s += v[k].c;
                            }
                            else {
                                /* 합쳐질 군단의 미생물 수 카운트 */
                                s += v[k].c;
                                /* 합쳐지고 남은 군단은 제거 */
                                v[k].c = 0;
                            }
                        }
                    }
                }
                /* 합쳐진 미생물 수 재갱신 */
                v[mx].c = s;
            }
        }
        int s = 0;
        for (A a : v)
            s += a.c;
        cout << '#' << z << ' ' << s << endl;
    }
    return 0;
}
```
<br>
---
layout: post 
tag: Three.js
title: Animation
date: 2018.07.11
---

## Animation  
### AnimationAction  
액션 조작을 위한 클래스  

| 함수 | 역할 |
| :---: | :--- |
| .clampWhenFinished(true) | action이 끝나면 초기 프레임으로 돌아가지 않고 마지막 프레임에서 정지 |
| .timeScale(n) | action의 속도를 n배로 빠르게 재생 |
| .setLoop(THREE.LoopOnce, 0) | action 반복 안함(한번만 재생) |
| .play() | action을 시작함 |

<br>
---
layout: post 
tag: AI
title: VDBE-Softmax
date: 2018.04.25
---
참고 사이트
- [Value-Difference based Exploration: Adaptive Control between epsilon-Greedy and Softmax](http://www.tokic.com/www/tokicm/publikationen/papers/KI2011.pdf)
- [Multi-armed Bandit](http://sanghyukchun.github.io/96/)
- [소프트맥스함수](http://eehoeskrap.tistory.com/144)  
- [Simple Reinforcement Learning with Tensorflow Part 7: Action-Selection Strategies for Exploration (한국어 버젼)](http://ishuca.tistory.com/m/399)

<br>
## Epsilon-Greedy  
### Exploitation vs Exploration  
**Exploitation**: 기존 경험 혹은 관측값을 토대로 가장 좋은 action을 선택하는 것  
**Exploration**: 더 많은 정보를 위하여 새로운 action을 선택하는 것  
상식 적으로 생각하면 exploitation만 하는 것이 베스트겠지만, 만약 exploration을 하지 않을 경우, **적은 정보를 토대로** exploitation을 하여 최종 결과가 최적의 결과가 아닐 수 있음  
역으로 exploration만 너무 치중 할 경우, 충분히 정보를 가졌는데 더 정보를 가지기 위해 **불필요한 비용**이 소모됨  
Exploitation과 Exploration을 **어느 정도 비율로** 하느냐가 핵심 요소  
<br>
### Multi-armed Bandit Problem  
기존 Reinforcement Learning과 다른 점은  
**Reinforcement Learning**은 매 순간 reward를 **전부 정확하게** 알 수 있음  
하지만 **Multi -armed Bandit Problem**은 **선택한 action에 대한 보상만 알 수 있고** 다른 action에 대한 보상을 알 수 없음  
<br>
### Epsilon-Greedy Algorithm  
**exploitation exploration dilemma**를 해결 하기 위해 고안된 알고리즘  
<br>
<img src="{{site.url}}/images/AI_VDBE-Softmax2.JPG?raw=true">  
일정한 확률 **epsilon 만큼**은 **랜덤으로 action을 선택**하고(**exploration**)  
나머지 확률 **1-epsilon 만큼**은 **가장 최적의 action을 선택**(**exploitation**)  
<br>
**epsilon 값을 잘 조정해** exploitation exploration dilemma를 **해결** 할 수 있음  
하지만 epsilon **값 조정하는 것 자체가 어렵**고, 학습 후반 부에 **exploration가 충분히 많이 된 상태에서는 비효율적**   
<br>
### Softmax Algorithm  
Epsilon-Greedy algorithm과 유사하게 **exploitation exploration dilemma를 해결 하기 위해** 고안된 알고리즘  
Epsilon-Greedy의 경우 특정 확률 동안은 action을 랜덤으로 뽑지만, Softmax의 경우 **확률 분포에 따라 action을 선택**  
<br>
<img src="{{site.url}}/images/AI_VDBE-Softmax1.jpg?raw=true">  
**확률 분포는 Action Value Function에 따름**  
즉 Action Value Function의 **값이 클 수록 더 높은 확률**을 나타냄  
<br>
## VDBE Softmax  
### Concept  
이것은 **표준은 아님**  
Epsilon-Greedy의 **단점을 보완 하기 위해** 만듦  
**Michel Tokic**가 개발한 알고리즘  
<br>
<img src="{{site.url}}/images/AI_VDBE-Softmax3.JPG?raw=true">  
<img src="{{site.url}}/images/AI_VDBE-Softmax4.JPG?raw=true">  
**상태에 따른 확률**을 계산함: ε(s)  
(Epsilon-Greedy에서는 **상태와 무관하게 확률이 일정** )  
**ε(s) 확률** 만큼 **Softmax에 따라 action을 선택**  
**그 외의 확률**에서는 **가장 높은 Action Value Function 값을 갖는 action** 선택  

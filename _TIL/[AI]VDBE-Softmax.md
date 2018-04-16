---
layout: post 
tag: AI
title: VDBE-Softmax
date: 2018.04.16
---
참고 사이트
- [Multi-armed Bandit](http://sanghyukchun.github.io/96/)
- [Value-Difference based Exploration: Adaptive Control between epsilon-Greedy and Softmax](http://www.tokic.com/www/tokicm/publikationen/papers/KI2011.pdf)
- [소프트맥스함수](http://eehoeskrap.tistory.com/144)

## Softmax  
### Softmax function  
<img src="{{site.url}}/images/AI_VDBE-Softmax1.jpg?raw=true">  
소프트맥스 함수의 출력을 **확률로 해석**하여 **분류**함  
<br>
## Epsilon-Greedy  
### Exploitation vs Exploration  
**Exploitation**: 기존 경험 혹은 관측값을 토대로 가장 좋은 action을 선택하는 것  
**Exploration**: 더 많은 정보를 위하여 새로운 action을 선택하는 것  
상식 적으로 생각하면 exploitation하는 것이 베스트겠지만, 만약 exploration을 하지 않을 경우, **잘못된 정보를 토대로** exploitation을 하여 최종 결과가 좋지 않을 수 있음  
역으로 exploration만 너무 치중 할 경우, 충분히 정보를 가졌는데 더 정보를 가지기 위해 **불필요한 비용**이 소모됨  
<br>
### Multi-armed Bandit Problem  
기존 Reinforcement Learning과 다른 점은  
**Reinforcement Learning**은 매 순간 reward를 **전부 정확하게** 알 수 있음  
하지만 **Multi -armed Bandit Problem**은 **선택한 action에 대한 보상만 알 수 있고** 다른 action에 대한 보상을 알 수 없음  
<br>
### Epsilon-Greedy Algorithm  
<img src="{{site.url}}/images/AI_VDBE-Softmax2.JPG?raw=true">  
일정한 확률 **epsilon 만큼**은 **랜덤으로 action을 선택**하고(그 action에 따른 보상을 파악)  
나머지 확률 **1-epsilon 만큼**은 **가장 최적의 action을 선택**  
<br>
**epsilon 값을 정하는 것을 통해** exploitation과 exploration 선택 정도의 **문제를 해결** 할 수 있음  
<br>
## VDBE Softmax  
이것은 표준은 아님  
**Michel Tokic**가 개발한 알고리즘  
<img src="{{site.url}}/images/AI_VDBE-Softmax3.JPG?raw=true">  
<img src="{{site.url}}/images/AI_VDBE-Softmax4.JPG?raw=true">  
Epsilon-Greedy를 확장하여 **상태에 따른 확률**을 계산함: ε(s)  
**불확실한 상황**에서 사용됨  
특정 확률에서 Softmax에 따라 random action을 선택  
불확실한 상황의 예시: 학습 중 값이 오르락 내리락 할 때  
VDBE-Softmax는 값이 오르락 내리락 할 때 안정적임  

---
layout: post 
tag: AI
title: POMDP
date: 2018.04.16
---
참고 사이트
- [위키: POMDP](https://en.wikipedia.org/wiki/Partially_observable_Markov_decision_process)
- [인공지능에 의한 자율주행기술 현황과 과제](http://magazine.hellot.net/magz/article/articleDetail.do?flag=all&showType=showType1&articleId=ARTI_000000000041369&articleAllListSortType=sort_1&page=1&selectYearMonth=201605&subCtgId=)
- [고파스](https://www.koreapas.com/m/view.php?id=gofun&page=1&sn1=&divpage=27&select_arrange=headnum&desc=asc&no=142813&allc=1)
- [Lecture notes](https://www.cs.cmu.edu/~ggordon/780-fall07/lectures/POMDP_lecture.pdf)
- [Toturial](https://www.techfak.uni-bielefeld.de/~skopp/Lehre/STdKI_SS10/POMDP_tutorial.pdf)
- [OpenRL - 강화학습 그리고 OpenAI - 2: Intro to Reinforcement Learning (1) MDP &amp;Value Function](http://www.modulabs.co.kr/RL_library/2136)
- [Why do we use expectation in reinforcement learning?](https://stats.stackexchange.com/questions/225098/why-do-we-use-expectation-in-reinforcement-learning)

## MDP  
### Definition  
현재의 상태를 기준으로 미래의 상태를 결정  
<br>
### Action  
Environment에서 특정 state에서 **다른 state로 이동할 때** 이를 action 이라고 함  
<br>
### Reward  
Action을 취하면 **그에 따른 reward**를 얻음  
Agent는 즉각적으로 나오는 reward만 고려하는게 아니라 **이후 reward까지 고려**하여 계산  
<br>
### Discount Factor  
agent가 episode가 시작하자마자 1 받았을 경우와 끝났을 때 1을 받을 경우는 다름(시간을 고려한 가치)  
비유를 들자면 배고픈 사람은 **밥을 최대한 빨리 먹는 것**에 대해 가치를 부여  
<br>
### Policy  
특정 state에서 **어떤 action을 취할지 정하는 것**  
<br>
### Value function  
Value function에는 크게 2종류가 있음  
- **State-Value Function**  
<img src="{{site.url}}/images/AI_POMDP1.JPG?raw=true">  
**첫번째 식의 의미**는 t시간 이후 episode가 끝날 때까지 **정책에 따라 전체 얻을 수 있는 reward를 계산**  
두 번째 식의 의미는 **특정 state를 선택한 후** value function의 결과를 보고 **다음 state를 어디로 갈지 결정**함  
E는 평균을 의미하는데 들어가는 이유는 정책에서 특정 action을 선택할 때 **반드시 하나만 고려하는 것이 아니라 여러개를 고려**하기 때문  

<br>
- **Action-Value Function(= Q Function)**  
<img src="{{site.url}}/images/AI_POMDP2.JPG?raw=true">  
**위의 State-value function의 경우** 모든 state 정보를 알아야 할 필요가 있음, 예를들면 **state s로 가려면 어떤 action을 취해야하는지** 알아야 함
이 방법은 **state와 더불어 action에 따라** 어떤 받을 가치를 계산함을 통해 다음 **어떤 action을 취할지** 결정함  
보통 Q-learning에 적용  

<br>
## POMDP  
Partially Observable Markov Decision Process의 약어  
MDP의 한 종류  
상태들이 완전히 관측 가능해질 때 MDP, 완전히 관측 못할 때, 즉 **부분적으로 관측 가능**해질 때 **POMDP**라고 함  
환경이나 시스템 자체가 가지는 예측 불가능한 현상(불확실성)을 POMDP로 정의  
게임으로 비유를 하면 상대방의 환경을 모르고 **자신이 관찰한 환경만을 가지고 판단**하도록 하는 방법(즉 전체를 모름)  
<br>
**가능한 state들에 대한 확률 분포**, **observation**과 **그에 따른 확률 분포**를 포함   
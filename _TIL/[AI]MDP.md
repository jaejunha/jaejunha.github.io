---
layout: post 
tag: AI
title: MDP
date: 2018.04.19
---
참고 사이트
- [위키: POMDP](https://en.wikipedia.org/wiki/Partially_observable_Markov_decision_process)
- [인공지능에 의한 자율주행기술 현황과 과제](http://magazine.hellot.net/magz/article/articleDetail.do?flag=all&showType=showType1&articleId=ARTI_000000000041369&articleAllListSortType=sort_1&page=1&selectYearMonth=201605&subCtgId=)
- [Lecture notes](https://www.cs.cmu.edu/~ggordon/780-fall07/lectures/POMDP_lecture.pdf)
- [Toturial](https://www.techfak.uni-bielefeld.de/~skopp/Lehre/STdKI_SS10/POMDP_tutorial.pdf)
- [OpenRL - 강화학습 그리고 OpenAI - 2: Intro to Reinforcement Learning (1) MDP &amp;Value Function](http://www.modulabs.co.kr/RL_library/2136)
- [Why do we use expectation in reinforcement learning?](https://stats.stackexchange.com/questions/225098/why-do-we-use-expectation-in-reinforcement-learning)
- [모두를 위한 머신러닝/딥러닝 강의](https://hunkim.github.io/ml/)

## MDP  
### Definition  
현재의 상태를 기준으로 미래의 상태를 결정  
<br>
### Action  
Environment에서 특정 state에서 **다른 state로 이동하는 행동**을 **action** 이라고 함  
<br>
### Reward  
Action을 취해 **특정 state로 이동하면** **특정 reward**를 얻음  
<br>
### Discount Factor  
Agent가 특정 state에서 reward를 얻을 때 step을 많이 갈때와 적게 갈때 가치가 다름(시간을 고려)  
비유를 들자면 배고픈 사람은 **밥을 최대한 빨리 먹는 것**에 대해 가치를 부여  
<br>
### Policy  
특정 state에서 **어떤 action을 취할지 정하는 것**  
<br>
### Value function  
Value function에는 크게 2종류가 있음  
- **State-Value Function**  
<img src="{{site.url}}/images/AI_MDP1.JPG?raw=true">  
**첫번째 식의 의미**는 t시간 이후 episode가 끝날 때까지 **정책에 따라 전체 얻을 수 있는 reward를 계산(마지막 state까지 안다고 가정)**  
두 번째 식의 의미는 **특정 state를 선택한 후** value function의 결과를 보고 **다음 state를 어디로 갈지 결정**함  
E는 평균을 의미하는데 들어가는 이유는 **불확실성** 때문(위에서 마지막 state까지 안다고 **가정**함)  

<br>
- **Action-Value Function(= Q Function)**  
<img src="{{site.url}}/images/AI_MDP2.JPG?raw=true">  
이 방법은 **state와 더불어 action에 따라** 어떤 받을 가치를 계산함을 통해 다음 **어떤 action을 취할지** 결정함  
보통 **Q-learning**에 적용  

<br>
## Q-Learning  
### Concept  
Agent는 **현재 state만 볼 수 있음**  
Agent는 **Q table을 참고**해 **어떤 길로 갈지 알 수 있음**  
**높은 Q 값**을 갖는 action을 취함  
식은 아래와 같고(**'는 미래**를 의미)  
<img src="{{site.url}}/images/AI_MDP3.JPG?raw=true">  

식을 **전개하면** 아래 식이 나옴(위의 Action-Value Function과 동일한 형태)  
<img src="{{site.url}}/images/AI_MDP2.JPG?raw=true">  

<br>
초기 모든 Q값은 **모두 0**으로 셋팅  
기본적으로 action을 선택을 할 때 Q table을 참고해 **Q 값을 최대화하는 action을 선택**(위 식에 의해)  
만약 여러 action을 취했을 때 계산한 **Q값이 모두 동일 하면 random 한 action 선택(Q table에 있는)**  
<br>
### Exploitation vs Exploration  
위에 언급 한 방식대로 **Q값을 최대화 하는 action을 선택하는 것을 exploitation**이라고 함  
그저 **exploitation만 할 경우**는 **구해지지 않은 action에대한 Q값은 알 수 없음**  
**안 구해진 action이 더 큰 reward를 가져다 줄 수 있음**  
이 때문에 **안 구해진 action을 탐험해야할 필요**가 있음, 이를 **exploration**이라고 함  
따라서 **exploitation과 exploration을 적절히** 해야함  
<br>
## POMDP  
**Partially Observable Markov Decision Process**의 약어  
MDP의 한 종류  
state들이 완전히 관측 가능해질 때를 MDP  
state들이 완전히 관측 못해질 때, 즉 **부분적으로 관측 가능**해질 때를 **POMDP**라고 함  
<br>
예를 들면 **Tiger problem** 생각  
양쪽 문에 각각 **호랑이** 혹은 **보물 상자**가 있음  
그들은 문 뒤에 있기 때문에 **문을 열어야 상태**를 확인 할 수 있음  
문을 **여는 행위를 action**이라 함  
문을 열면 상태를 **관측(observation)** 하게 되고 **보상(reward)**를 얻음(-값이든 +값이든)  
<br>
즉 MDP는 action을 취하면 **reward만**을 얻게 되지만,  
POMDP는 action을 취하면 **observation과 reward**를 얻게 됨  
<br>
POMDP는 위와 같이 **환경(environment)에 대한 불확실성(uncertainty)**를 가질 때 정의 됨  
(agent는 environment와 상호 작용함)  
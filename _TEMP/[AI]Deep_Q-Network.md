---
layout: post 
tag: AI
title: Deep Q-Network
date: 2018.04.25
---
참고 사이트
- [Deep-Q Network (DQN) - Simulation](https://jay.tech.blog/2017/01/10/deep-q-network-dqn/)

<br>
## Deep Q-Network  
### Concept  
**구글 딥마인드**가 개발한 딥 러닝 알고리즘  
**Action-value function**을 **CNN(Convolutional Neural Networks)**을 사용하여 **Q-value**를 예측  
Q-Learning을 사용할 경우 state를 유한적인 갯수가 나올 수 있게 정의하면 괜찮지만, **이미지로 정의** 할 경우 **무한한 state가 파생** 할 수 있음(한 이미지에 딸린 모든 픽셀의 변화를 고려하기 때문)  
그래서 **Neural Network**를 이용하여 **이미지의 특징(feature)**을 잡아 **state 수를 줄임**  
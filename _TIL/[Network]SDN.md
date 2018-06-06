---
layout: post 
tag: Network
title: SDN
date: 2018.06.06
---
참고 사이트
- [http://www.itworld.co.kr/news/105686](http://www.itworld.co.kr/news/105686)  
- [https://ko.wikipedia.org/wiki/소프트웨어_정의_네트워킹](https://ko.wikipedia.org/wiki/소프트웨어_정의_네트워킹)
- [https://www.netmanias.com/ko/post/blog/13359/sdn-nfv-sk-telecom/sdn-nfv-in-the-5g-era-1-how-will-sdn-change-the-world](https://www.netmanias.com/ko/post/blog/13359/sdn-nfv-sk-telecom/sdn-nfv-in-the-5g-era-1-how-will-sdn-change-the-world)

<br>
## SDN  
### Concept  
**S**oftware **D**efined **N**etworking의 약어  
개방형 API인 **OpenFlow**를 통해 네트워크의 **트래픽 전달 동작**을  **SDN Controller에서 제어 및 관리** 하는 접근 방식  
SDN은 **data plane**과 **control plane 분리**함  
이를 통해 네트워크 관리 유연성을 높이고 세분화된 보안 정책을 쉽게 구현할 수 있음  
<br>
### OpenFlow API  
SDN에서 **Control plane과 Data plane 사이의 표준 통신 인터페이스** 역할을 함  
Data plane을 **제어**하기 위한 명령어 (Match & Action)과  
네트워크 장비의 정보를 **수집**하기 위한 명령어로 이루어짐  
<br>
### Elements  
구조적 요소들은 다음과 같다  
- SDN Application  
- SDN Controller  
- SDN Datapath  
- SDN Control to Data-Plain Interface (CDPI)  
- SDN Northbound Interfaces (NBI)  
<br>
### Examples  
**경로 최적화**  
- WAN 분야에서의 경로 최적화, A에서 B로 향할 때 빠른 경로를 제공  
**데이터 센터**  
- 데이터 센터 내의 네트워크 장비를 SDN 컨트롤러와 조합하여 비용 축소  
**가상 네트워크**  
- 하나의 네트워크에 여러 서비스 제공  
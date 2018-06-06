---
layout: post 
tag: Network
title: Hostapd
date: 2018.06.06
---
참고 사이트
- [https://en.wikipedia.org/wiki/Hostapd](https://en.wikipedia.org/wiki/Hostapd)  
- [https://wiki.gentoo.org/wiki/Hostapd](https://wiki.gentoo.org/wiki/Hostapd)  
- [http://twinw.tistory.com/198](http://twinw.tistory.com/198)  

<br>
## Hostapd  
### Concept  
**Host A**ccess **P**oint **D**aemon의 약어   
NIC(Network Interface Card)를 **AP(Access Point)와 Authentication Server로 변형**하는 user space daemon   
**무선 랜 카드** 이용해서 **AP**를 만든다고 생각하면 됨  
다양한 종류의 hostapd가 있음  

<br>
### Capability  
- AP를 만들 수 있음  
- 동일한 카드에 최대 8개까지의  AP를 만들 수 있음  
- Wireless Ethernet Switch를 만듦, 하지만 IP 프로토콜은 지원 가능 하지 않음  

<br>
### Install  
hostapd 관련 파일을 설치  
```
apt-get install hostapd bridge-utils
```
<br>
### Configuration  
설정 파일을 만듦
```
vim /etc/hostapd/hostapd.conf
```
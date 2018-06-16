---
layout: post 
tag: Ubuntu
title: 네트워크 설정 - /etc/network/interfaces
date: 2018.06.16
---
참고 사이트  
- [http://promobile.tistory.com/300](http://promobile.tistory.com/300)  
- [https://askubuntu.com/questions/411616/what-does-keywords-in-my-etc-network-interfaces-means](https://askubuntu.com/questions/411616/what-does-keywords-in-my-etc-network-interfaces-means)  
[http://minimonk.net/745](http://minimonk.net/745)  

## /etc/network/interfaces  
### 개요  
리눅스에서 네트워크 설정은 `/etc/network/interfaces`에서 한다   
수정은 vi 편집기나 에디터 툴을 이용해서 한다  
```
vi /etc/network/interfaces
```
<br>
### 수정  
```
auto lo
iface lo inet loopback
```
초기에 `/etc/network/interfaces`에는 위의 내용이 저장되어 있다   
**위 내용 아래에** 설정하고 싶은 내용을 적는다  
존재하고 있는 인터페이스 확인은 아래 명령어를 통해 한다  
```
ifconfig
```
<br>
유선 인터페이스 `eth0`이 있다고 가정  
1. 유동 IP 설정  
아래 내용을 추가해준다  
```
auto eth0
iface eth0 inet dhcp
```
2. 고정 IP 설정  
아래 내용을 **참고해** 추가해준다  
```
auto eth0
iface eth0 inet static
  address xxx.xxx.xxx.xxx
  netmask xxx.xxx.xxx.xxx
  gateway xxx.xxx.xxx.xxx
  dns-nameservers 8.8.8.8 xxx.xxx.xxx.xxx
```
**dhcp**는 유동 IP를 부여할 때 사용하고 **static**은 고정 IP를 부여할 때 사용한다  
**inet**은 TCP/IP 네트워크를 사용한다는 의미  
<br>
무선 인터페이스도 유선 인터페이스와 유사하다  
몇가지 **추가적인 옵션**이 있는데, 그들의 역할은 아래와 같다  
인터페이스 이름은 `wlan0`이라 가정  

| 옵션 | 역할|
|:---|:---|
| allow-hotplug wlan0 | 물리적으로 연결이 되면 자동적으로 설정 |
|  wpa-ssid "name" | name이란 ssid를 가진 AP에 연결 |
| wpa-psk "password" | name이란 ssid를 가진 AP에 연결시 사용될 비밀번호 |
<br>
### 적용  
수정한 내용을 네트워크에 적용하려면 아래 명령어를 통해 적용하거나 재부팅하는 방법이 있다  
```
service networking restart
```

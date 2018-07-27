---
layout: post 
tag: Ubuntu
title: (VMware)인터넷 설정
date: 2018.07.27
---

## (VMware) 인터넷 설정  
### Virtual Network Editor 다운 받기  
본 내용은 VM Workstation Player 기준으로 정리했습니다. Player는 VM Workstation의 **무료 버전**으로써 사용할 수 있는 **기능이 제한**되어있습니다. 인터넷 설정을 하려면 **Virtual Network Editor가 필요**한데 Player버전은 인터넷에서 **별도로 다운 받아야**합니다.  
인터넷에서 **Virtual Network Editor(vmnetcfg.exe)를 다운 받은 후**, `vmplayer.exe`가 있는 곳에 **저장**을 합니다.  
<br>
### Bridged VS NAT  
VM ware에 인터넷 설정을 하는 방법은 크게 **Bridged**와 **NAT** 방식이 있습니다. **Bridged** 방식의 경우 호스트(가상 머신을 구동시키는 컴퓨터)와 가상머신에 **각각 다른 IP를 부여**합니다. **NAT**방식의 경우는 호스트와 가상머신 **동일한 IP를 부여**합니다.  
VMware Player에서는 **VMnet0에서 Bridged**, **VMnet8에서 NAT**방식을 사용합니다.
<br>
### Bridged  

<img src="{{site.url}}/images/vM_인터넷_설정1.jpg?raw=true">  

**Edit Virtual Machine Settings**를 클릭  

<img src="{{site.url}}/images/vM_인터넷_설정2.jpg?raw=true">  

**Network Adapter** 선택 후 **Custom** 체크하고 `VMnet0` 선택  
설정이 다 되었으면 `OK`클릭  

<img src="{{site.url}}/images/vM_인터넷_설정3.jpg?raw=true">  

다운 받은 **vmnetcfg.exe를 실행**하고 `Change Settings`를 클릭  

<img src="{{site.url}}/images/vM_인터넷_설정4.jpg?raw=true">  

잠시 기다리면 **VMnet0이 생성된 것을 확인**할 수 있음  
**VMnet0를 선택**하고 실제 **호스트 컴퓨터가 사용하는 랜카드**를 선택  
선택이 완료됬으면 `Apply`, `OK` 순으로 버튼을 눌러 설정을 완료함  

<img src="{{site.url}}/images/vM_인터넷_설정5.jpg?raw=true">  

실제 **VMWare Player를 가동**하고 **가상 머신 안**에서 사용할 **고정 IP 설정**  
<br>
### NAT  

<img src="{{site.url}}/images/vM_인터넷_설정1.jpg?raw=true">  

VMWare에서 **Edit Virtual Machine Settings**를 클릭  

<img src="{{site.url}}/images/vM_인터넷_설정7.jpg?raw=true">  

**Network Adapter** 선택 후 **NAT** 체크 후 `OK`클릭  
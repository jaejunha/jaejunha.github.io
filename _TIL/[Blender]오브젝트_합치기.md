---
layout: post 
tag: Blender
title: 오브젝트 합치기
date: 2018.07.29
---

## 오브젝트 합치기  
### Union연산  

단순히 오브젝트를 합치는데에는 `Ctrl` + `J`키를 눌러서 할 수 있습니다. 하지만 이 것의 **단점은** 말 그대로 오브젝트를 합치기만 하기 때문에 **중복 되는 부분을 처리하지 않아** 복잡도를 늘립니다. 블렌더에서는 **Modifier 기능에서 Union연산**을 통해 **중복되는 부분을 제거하면서 두 오브젝트를 합**칠 수 있습니다.

<img src="{{site.url}}/images/오브젝트_합치기1.jpg?raw=true">  

오브젝트 **하나를 선택**  
우측에서 **Modifier 아이콘** 클릭  
**Add Modifier** 선택  

<img src="{{site.url}}/images/오브젝트_합치기2.jpg?raw=true">  

**Boolean**을 선택  

<img src="{{site.url}}/images/오브젝트_합치기3.jpg?raw=true">  

**스포이드 아이콘**을 누르고 합치려는 오브젝트를 선택  

<img src="{{site.url}}/images/오브젝트_합치기4.jpg?raw=true">  

기본 값으로 설정된 **Intersect**을 클릭  
값을 **Union**으로 변경  

<img src="{{site.url}}/images/오브젝트_합치기5.jpg?raw=true">  

**Apply**를 클릭  
<br>
위 과정을 마치면 **한 오브젝트는 그대로 존재**하고 다른 오브젝트는 두개가 합쳐진 오브젝트가 됩니다. 필요에 따라 그대로 존재하는 오브젝트를 삭제하면 됩니다.  


---
layout: post 
tag: Blender
title: 애니메이션 추출(Three.js) - 폰트
date: 2018.07.09
---

## 애니메이션 추출(Three.js) - 폰트  
### 폰트를 메쉬로 변경하기  
Blender에서 폰트는 일반 메쉬랑 달라 바로 json으로 추출이 불가능합니다. 그래서 가장 먼저 해야하는 작업은 폰트를 메쉬로 변경하는 것입니다.   

<img src="{{site.url}}/images/애니메이션_추출_폰트1.jpg?raw=true">   

<img src="{{site.url}}/images/애니메이션_추출_폰트2.jpg?raw=true">   

`Shift+A` 키를 눌러 **Text**를 생성   

<img src="{{site.url}}/images/애니메이션_추출_폰트3.jpg?raw=true">   

`Alt+C` 키를 누르고 **Mesh from Curve/Meta/Surf/Text**를 선택  

<img src="{{site.url}}/images/애니메이션_추출_폰트4.jpg?raw=true">   

위 과정을 거치면 Text가** Mesh로 변경된 것**을 확인 할 수 있음  
<br>

(리깅 및 애니메이션 과정은 **생략...**)  

<br>

<img src="{{site.url}}/images/애니메이션_추출_폰트5.jpg?raw=true">   

Text Mesh를 선택 한후, 하단에 있는 **연장 아이콘** 클릭  

<img src="{{site.url}}/images/애니메이션_추출_폰트6.jpg?raw=true">   

**Add Modifier** 선택 후, **Armature** 클릭  

<img src="{{site.url}}/images/애니메이션_추출_폰트7.jpg?raw=true">   

**Object 아래**를 클릭하고 **연결시킬 Armature** 선택  
<br>
위 과정을 모두 마치면 Font도 일반 Mesh처럼 **애니메이션 추출이 가능**하다  
(애니메이션 추출 과정은 **생략...**)
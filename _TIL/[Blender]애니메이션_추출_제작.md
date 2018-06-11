---
layout: post 
tag: Blender
title: 애니메이션 추출(Three.js) - 제작 작업
date: 2018.06.12
---

## 애니메이션 추출(Three.js) - 제작 작업  
### 뼈대 연결하기  
애니메이션을 만드려면 가정 먼저 해야할일이 움직이는 대상을 만드는 것입니다. 움직이는 대상은 **뼈대**와 **3D 모형**으로 이루어져있기 때문에 둘을 각각 만든 후 **연결하는 작업**을 거칩니다. 이 때 연결하는 작업을 **리깅(Rigging)**이라고 부릅니다. 이 파트에서는 간단하게 리깅하는 작업까지 진행할 것입니다.   

<img src="{{site.url}}/images/애니메이션_추출_제작1.jpg?raw=true">   

(3D 모델을 만들었다고 가정) `Shift+A` 키를 눌러  **Armature** > **Single bone**을 선택   

<img src="{{site.url}}/images/애니메이션_추출_제작2.jpg?raw=true">   

Pose 모드로 넘어가기 위하여 **먼저 Object** 선택하고 `Shift` 키를 누르고 **Bone**을 선택(**순서**를 지켜야 함)   
Object 모드에서 **Pose 모드** 선택  

<img src="{{site.url}}/images/애니메이션_추출_제작3.jpg?raw=true">   

오브젝트와 뼈대를 **연결**하기 위해 `Ctrl+P` 키를 누르고 **With Automatic Weights**를 선택  
<br>
### 애니메이션 추가 하기  
위 과정을 통해 뼈대와 3D 모형을 연결하였습니다. 다음은 **애니메이션 제작**을 간단하게 알아보겠습니다.  

<img src="{{site.url}}/images/애니메이션_추출_제작4.jpg?raw=true">   

상단에서 **Animation** 선택   

<img src="{{site.url}}/images/애니메이션_추출_제작5.jpg?raw=true">   

Animation을 선택하면 위과 같은 화면이 나온다  

<img src="{{site.url}}/images/애니메이션_추출_제작6.jpg?raw=true">   

**좌측 중간**에 보이는 Dope Sheet을 눌러 Dope Sheet에서 **Action Editor**로 변경  

<img src="{{site.url}}/images/애니메이션_추출_제작7.jpg?raw=true">   

애니메이션 추가를 위해 **New** 버튼을 눌러준다  

<img src="{{site.url}}/images/애니메이션_추출_제작8.jpg?raw=true">   

추가된 애니메이션의 **이름**을 지정할 수 있다  
또한 **+** 버튼을 통해 **여러개의 애니메이션**을 추가할 수 있다  

<img src="{{site.url}}/images/애니메이션_추출_제작9.jpg?raw=true">   

좌측의 버튼을 통해 만든 애니메이션을 **선택 및 확인**할 수 있다   

<img src="{{site.url}}/images/애니메이션_추출_제작10.jpg?raw=true">   

애니메이션 **초기화**를 위해 Animation1을 선택하고 하단에 보이는 빨간색 버튼을 눌러 애니메이션 **녹화를 시작**한다  

<img src="{{site.url}}/images/애니메이션_추출_제작11.jpg?raw=true">   

이전에 만든 **뼈대를 선택**한다   

<img src="{{site.url}}/images/애니메이션_추출_제작12.jpg?raw=true">   

하단에 보이는 **Start 값을 1에서 0으로** 수정하고 오브젝트에 보이는 **화살표 버튼을 클릭**해준다  

<img src="{{site.url}}/images/애니메이션_추출_제작13.jpg?raw=true">   

위 과정을 마치면 시간 0일때 화살표 버튼을 클릭했을 때 동작이 기록된다  

<img src="{{site.url}}/images/애니메이션_추출_제작14.jpg?raw=true">   

시간 75일 때 동작을 추가 해보자  
하단에서 **시간이 75 정도 되는 구간에서 클릭**을 해준다  
클릭이 제대로 됬다면 위와 같은 화면이 나온다  

<img src="{{site.url}}/images/애니메이션_추출_제작15.jpg?raw=true">   

점프 하는 동작을 넣기 위해 **뼈대를 움직**였더니 좌측에 **동작이 추가** 되었다  
이와 같은 방법으로 Animation2, Animation3도 다양한 동작을 넣어주자  
<br>
### 애니메이션 추출하기   
애니메이션을 만들었다면 Three.js에서 사용할 수 있게 **json파일로 추출**해야합니다. 이 과정을 간단하게 보여주겠습니다  

<img src="{{site.url}}/images/애니메이션_추출_제작16.jpg?raw=true">   

먼저 우측에서 **뼈대가 아닌** **만든 오브젝트를 선택**한다  

<img src="{{site.url}}/images/애니메이션_추출_제작17.jpg?raw=true">   

애니메이션을 추출하기 위해 **File** > **Export** > **Three.js (json)**을 선택한다  

<img src="{{site.url}}/images/애니메이션_추출_제작18.jpg?raw=true">   

Three.js (json)을 선택하면 위와 같은 화면이 나온다  
애니메이션을 추출하기 위해서는 **설정이 필요**한데,  
**건드려야 할 곳은 빨간색 박스 친 부분**이다  

<img src="{{site.url}}/images/애니메이션_추출_제작19.jpg?raw=true">   
<img src="{{site.url}}/images/애니메이션_추출_제작20.jpg?raw=true">   
<img src="{{site.url}}/images/애니메이션_추출_제작21.jpg?raw=true">   

위와 같이 설정을 바꿔준다  

<img src="{{site.url}}/images/애니메이션_추출_제작22.jpg?raw=true">   

우측 상단에 보이는 **Export THREE** 버튼을 클릭한다  
추출 버튼을 통해  Three.js에서 사용 가능한 **json이 추출**되어진다  

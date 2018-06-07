---
layout: post 
tag: Blender
title: 애니메이션 추출(Three.js) - 제작 작업
date: 2018.06.07
---

## 애니메이션 추출(Three.js) - 제작 작업  
### 뼈대 연결하기  
애니메이션을 만드려면 **뼈대**와 **3D 모형**을 만들어야 합니다. 이 둘을 만든 후 **연결하는 작업**이 필요한데 이를 **리깅(Rigging)**이라 합니다. 이 파트에서는 간단하게 리깅하는 작업까지 보여드리겠습니다.   

<img src="{{site.url}}/images/애니메이션_추출_제작1.jpg?raw=true">   

(3D 모델을 만들었다고 가정)`Shift+A` 키를 눌러  **Armature>Single bone**을 선택   

<img src="{{site.url}}/images/애니메이션_추출_제작2.jpg?raw=true">   

**먼저 Object** 선택 그리고 `Shift` 키를 누르고 **Bone**을 선택  
Object 모드에서 **Pose 모드** 선택  

<img src="{{site.url}}/images/애니메이션_추출_제작3.jpg?raw=true">   

`Ctrl+P` 키를 누르고 **With Automatic Weights**를 선택  
<br>
### 애니메이션 추가 하기  
위 과정을 통해 뼈대와 3D 모형을 연결하였습니다. 다음 과정은 애니메이션 추출을 위한 애니메이션 제작입니다.  
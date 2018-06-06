---
layout: post 
tag: Blender
title: 애니메이션 추출(Three.js) - 초기 작업
date: 2018.06.07
---

## 애니메이션 추출(Three.js) - 초기 작업  
### Three.js 다운로드  
기본적으로 Blender와 Three.js는 **서로 연관성이 없습니다.** 그래서 Three.js가 Blender에서 만든 모델을 사용하려면 Blender에 **Three.js의 add-on 파일**(둘 사이의 관계를 이어주는 역할)을 추가해주어야 합니다.  

<img src="{{site.url}}/images/애니메이션_추출_초기1.jpg?raw=true">   

[Three.js 홈페이지](https://threejs.org/)에서 최신버전의 Three.js를 받는다  
다운로드가 완료되면 **three.js-master > utils > exporters > blender > addons** 로 이동하자  
io_three 폴더가 보이는 데 이 **폴더를 .zip 파일로 압축**하자  
<br>
### Three.js export 설정 추가하기  
이 과정은 앞에서 압축한 **Add-on 파일**을 Blender에 **추가하는 과정**입니다.  
<img src="{{site.url}}/images/애니메이션_추출_초기2.jpg?raw=true">  

**File > User Preferences** 메뉴로 들어간다  

<img src="{{site.url}}/images/애니메이션_추출_초기3.jpg?raw=true">  

**Install Add-on from File...**를 클릭  

<img src="{{site.url}}/images/애니메이션_추출_초기4.jpg?raw=true">  

이전에 압축한 **io_three.zip을 찾아** 더블 클릭  

<img src="{{site.url}}/images/애니메이션_추출_초기5.jpg?raw=true">  

**three.js를 검색**한 후 **체크 박스를 선택**한다  
그리고 **Save User Settings**를 눌러 적용 후 닫기 버튼을 누른다   
<br>
위 과정을 모두 마치면 Blender에서 Three.js를 위한 애니메이션을 **추출할 수 있게 됩니다**.  




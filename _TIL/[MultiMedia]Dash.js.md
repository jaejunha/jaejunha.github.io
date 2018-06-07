---
layout: post 
tag: MultiMedia
title: Dash.js
date: 2018.06.07
---
참고 사이트
- [https://docs.microsoft.com/ko-kr/azure/media-services/previous/media-services-embed-mpeg-dash-in-html5](https://docs.microsoft.com/ko-kr/azure/media-services/previous/media-services-embed-mpeg-dash-in-html5)  

## Dash.js  
### concept  
오픈 소스 MPEG-DASH 비디오 플레이어  

<br>
### MPEG-DASH  
비디오 컨텐츠를 위한 **적응형 스트리밍의 ISO 표준**   
**네트워크 상황**에 따라 **bit rate를 조절**하여 **끊김 없는 영상**을 제공 하도록 함  

<br>
### Test code  
**아래 코드는 [마이크로소프트 사이트](https://docs.microsoft.com/ko-kr/azure/media-services/previous/media-services-embed-mpeg-dash-in-html5) 에서 가져온 html 코드입니다.**  
**변수 url**에는 **mpd파일의 경로**를 넣습니다.  
```
<!DOCTYPE html>
<html>
	<head>
		<title>Adaptive Streaming in HTML5</title>
		<script src="js/dash.all.js"></script>
		<script>
		// setup the video element and attach it to the Dash player
		function setupVideo() {
			var url = "http://xxx/xxx.mpd";
			var context = new Dash.di.DashContext();
			var player = new MediaPlayer(context);
			player.startup();
			player.attachView(document.querySelector("#videoplayer"));
			player.attachSource(url);
		}
		</script>
		<style>
		video {
			width: 80%;
			height: 80%;
		}
    </style>
	</head>
	<body onload="setupVideo()">
		<h1>Adaptive Streaming with HTML5</h1>
		<video id="videoplayer" controls></video>
	</body>
</html>
```
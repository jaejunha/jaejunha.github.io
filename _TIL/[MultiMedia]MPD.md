---
layout: post 
tag: MultiMedia
title: MPD
date: 2018.06.08
---
참고 사이트
- [http://unipro.tistory.com/109](http://unipro.tistory.com/109)  
- [https://www.tta.or.kr/data/weekly_view.jsp?news_id=3747](https://www.tta.or.kr/data/weekly_view.jsp?news_id=3747)  

## MPD  
### Concept   
**M**edia **P**resentation **D**escription의 약어  
스트림의 정보를 나타내는 **XML**   
세그먼트 파일들에 대한 모든 **URL** 제공  
URL외에도 **timing**, **video resolution**, **bit rate**에 관한 정보들을 담고 있음  
**DASH 클라이언트**는 가장 **먼저** 하는 일이 **MPD를 받아 해독**하는 것  
**MPEG-DASH 표준**은 크게 두 부분으로 나뉜다  
- **MPD** 규정  
- **세그먼트**에 대한 규정  

<br>
### MPEG-DASH  
클라이언트는 MPD를 보고 자신에게 **적합한 bitrate**와 **resolution**을 **선택**해 **적절한 세그먼트를 요청**   

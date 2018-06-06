---
layout: post 
tag: MultiMedia
title: SSIMplus
date: 2018.06.07
---
참고 사이트
- Image Quality Assessment: From Error Visibility to
Structural Similarity
- [The SSIMplus Index for Video Quality-of-Experience Assessment](https://ece.uwaterloo.ca/~z70wang/research/ssimplus/)
- [ICY 영상 분석툴을 이용한 SSIM, MSE, PSNR 평가방법 - 네이버 블로그](http://blog.naver.com/PostView.nhn?blogId=y4769&logNo=220505513170&parentCategoryNo=&categoryNo=&viewDate=&isShowPopularPosts=false&from=postView)
- [Structural similarity - Wikipedia](https://en.wikipedia.org/wiki/Structural_similarity)
- [Structural Similarity Index (SSIM) for measuring image quality - MATLAB ssim - MathWorks 한국](https://kr.mathworks.com/help/images/ref/ssim.html)
- [Why is SSIM Not Good Enough? - SSIMWAVE](https://www.ssimwave.com/from-the-experts/why-is-ssim-not-good-enough/)

## SSIM  
### concept  
**Structural Similarity Index Measure**의 약어  
두 이미지의 **유사성**을 측정함  
압축 및 변환에 의해 발생하는 왜곡에 대하여 원본 영상에 대한 유사도를 측정하는 방법  
기존의 **MSE** 측정 방식과 **PSNR** 측정 방식을 개선하기 위해 개발  
자세한 적용 방법은 아래 사이트 참고  
[https://kr.mathworks.com/help/images/ref/ssim.html](https://kr.mathworks.com/help/images/ref/ssim.html)  
<br>
## SSIMplus  
### concept  
SSIMplus는 객관적인 **perceptual quality를 측정하는 지표**  
값의 범위는 0~100사이  
SSIM의 **확장판**  
Zhou Wang 교수가 개발  
<br>
### SSIM에 비해 개선한 점  
- SSIM의 경우 **device size(비디오 압축 정도)에 상관 없이 같은 perception QoE 값**을 가짐(SSIM의 목적은 인간의 시각 시스템을 모방, 당연히 크기에 따라 다른 느낌을 받아야함)  
- **HDR(High Dynamic Range)video가 SDR(Standard Dynamic Range) video로 변환(이미지 손실이 상당히 일어남)이 될 때 동일한 값**을 가짐   

이러한 점들을 개선(더 있음, 아래 사이트 참조)  
[https://www.ssimwave.com/from-the-experts/why-is-ssim-not-good-enough/](https://www.ssimwave.com/from-the-experts/why-is-ssim-not-good-enough/)  
<br>
### SQM  
**SSIMplus Quality-of-experience Monitor**의 약어  
SSIMplus 지표를 측정하도록 만들어진 **소프트웨어**  

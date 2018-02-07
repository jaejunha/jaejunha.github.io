# Graphics  
## Word  
- 1 (2018.01.28~29)  
  - **Stencil Buffer**  
  - 스텐실 버퍼는 렌더링시 **마스크 픽셀**을 이용하여 픽셀을 그릴지 안 그릴지 여부를 나타냅니다.  
  - 스텐실 버퍼는 **거울**에 의해 반사된 상을 표현할 때 많이 사용되는데, 거울이 있는 곳, 즉 <u>반사된 물체가 보여지는 곳</u>에만 그림을 그려지도록 하는 방식으로 사용이 됩니다.  
- 2 (2018.02.03)  
  - **Depth Buffer**
  - 물체가 **가깝고 멀고를 표현**하기 위해 z 값을 저장하는 버퍼  
- 3 (2018.01.30~2018.01.31)  
  - **MeshLab**  
  - 3D triangular mesh를 편집하는 Open Source 소프트웨어  
  - 주로 렌더링 하는 프로그램은 아닙니다.  
  - page : http://www.meshlab.net/   
- 4 (2018.01.31)  
  - **안티 알리아싱**
  - 알리아싱 상태는 이미지의 픽셀들의 경계가 뚜렷하게 보이는 현상입니다.  
  - 안티 알리아싱은 이미지 **경계들을 부드럽게** 해주는 효과입니다.  
- 5 (2018.02.01)  
  - **Interlace**  
  - 영상을 **홀수와 짝수 가로줄로 나눠 번갈아가면서** 표시해주는 방식입니다.  
  - **눈의 착시 현상**으로 인해 일반 출력처럼 보이고, 효과로 **대역폭을 반감**시킬 수 있습니다.  
  - 요즘에는 잘 쓰이지 않습니다.  
- 6 (2018.02.02)  
  - **Progressive scanning**  
  - Interlace와 달리 화면에 표시할 내용을 다 표시  
  - Interlace와 비교시 깜박임이 적어 선명한 영상 표현 가능  
- 7 (2018.02.04, 02.07)  
  - **Raster Graphics**  
  - 비트맵이라고도 불리며, **사각형 구조**의 픽셀들로 이루어진 이미지  
  - 파일 확장자로는 jpeg, png, mpeg4 등이 많이 쓰입니다.  
- 8 (2018.02.07)  
  - **Vector Graphics**  
  - **점과 선을 수학적으로 표현**하여 이미지를 저장합니다  
  - 확대 해도 깨지지 않는 장점이 있습니다.  
  - 파일 확장자로는 svg, eps, pdf로 많이 쓰입니다.  
  - **색상의 표현에 제약**이 있어, 고해상도의 경우는 Vector 보다는 Raster를 주로 사용합니다.  
- extrapolation, 베지어 곡선, blending, curling 등  
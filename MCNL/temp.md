**video coding standards**:**bitstream syntax**, **language** which will be used by decoder and encoder.<br>
Good compression algorithm is also needed.<br>
Mainly **H.263** will be treated.<br>
<br>
Because **there are a large number of bits**, compression is prerequisite.<br>
Two main organization : **ITU-T**, **ISO**<br>
difference : **operating bit rates**, **applications**<br>
<br>
two types of redundancy : **spatial**, **temporal**<br>
spatial coding is like intra coding<br>
temporal coding is like inter coding<br>
pixel has three components : **one luminance**, **two chrominance**<br>
<br>
H.263 uses block-based coding scheme.<br>
<br>
**Transform Coding**<br>
**Motion Compensation**<br>
<br>
Coding Mode<br>

- UMV(Unrestricted Motion Vector)<br>
- SAC(Syntax-Based Arithmetic Coding<br>
- Advanced Prediction Mode<br>
- PB Frame Mode<br>
- Advanced Intra Coding Mode<br>
- Alternate Inter VLC Mode<br>
- Modified Quantization Mode<br>
- Deblocking Filter Mode<br>
- Improved PB Frame Mode<br>
  <br>

**Variable Bit Rate Video Coding**<br>
**VBR**:(Variable Bit Rate)<br>
produce variable bits per frame<br>
**CBR**:(Constant Bit Rate)<br>
Because level of redundancy varies from frame to frame, bit rate is different<br>
frame I, B, P<br>
preencoded vs live<br>
<br>
There are two kinds of redundancy<br>

- spatial(intra coding)<br>
- temporal(inter coding)<br>
  Pixel can be represented by three components<br>
- Y(luminance)<br>
- two C(chrominance)<br>
  H.263 uses block-based coding scheme<br>
  block is 8x8 pixels<br>

**DCT**:(Discrete Cosine Transform)<br>
<br>
**Subsampling**:to reduce dimension of video<br>
<br>

<br>
**MPD**:(Media Presentation Description)<br>
It is XML Document including media content<br>
**exabytes**:10^18bytes<br>
**bottle neck**:If one component is slow in network, then it affects whole system.<br>
**SDN**:(Software Defined Networking)<br>
using OverFlow API, control and manage network traffic. Its control plane is separated from data plane in routers and switches.<br> 
**MPEG-DASH**:standard of HTTP Adaptive Streaming<br>
**DASH**:(Dynamic Adaptive Streaming over HTTP)<br>
It changes data rate according to network condition.<br>
**PSNR**:<br>(Peak signal-to-noise ratio)<br>
<br>
I study contents of MCNL homepage.<br>
I read some papers<br>
**CCN**:(Content Centric Networking)<br>
give name to information. So, we can get information refering name.(not using IP address)<br>
**NFV**:(Network Fuction Virtualization)<br>
combine hardware and software and network functionality into administrative entity(from wiki).<br>
**Offloading**:things worked at DataBase server is treated at storage<br>
**raptor code**:one type of foutain codes.<br>
**3GPP**:(3rd Generation Partnership Project)<br>
<br>

<br>

**Error Concealment**<br>
It is necessary for decoder to perform error concealment<br>
Detection is first!<br>
<br>
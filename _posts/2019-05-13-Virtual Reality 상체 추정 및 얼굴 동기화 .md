---
layout: post
featured-img: vr-1
---


## 1. 목적 

> 

## 2. 개요

<div>
<h2>3. 구현</h2>
<h3 style="margin-left: 40px;">1) AVATAR 상체 동기화 </h3>
<h4 style="margin-left: 50px;">a) AVATAR 상체 동기화 </h4>
    <div>
    <img src="/assets/img/posts/hand-sub1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub1-1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>Contour 알고리즘을 통해 영역을 분리, 저장</li>
      <br>
      <li>ConvexHull 알고리즘을 이용하여 손가락 사이의 골의  좌표를 획득</li>
      <br>
      <li>좌표 계산을 통해 ROI(Region Of Interest)를 실행</li>
      <br>
    </ul>
   </div>
   <div>
    <img src="/assets/img/posts/hand-sub2.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub1-2.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
      <ul >
      <li>Canny 함수로 가장자리를 감지하여 Edge 검출</li>
      <br>
      <li>Sobel 함수를 사용하여 Canny된 이미지를 Masking으로 추출하여 가장자리 인식 </li>
      <br>
      <li>Closing 함수를 통해 그림의 불필요한 노이즈를 제거 및 떨어져 있는 선들을 연결</li>
      <br>
    </ul>
   </div>

<h3 style="margin-left: 40px;">2) 사용자 음성 처리 및 AVATAR 얼굴 동기화 </h3>



<div>
<h2>4. 결과</h2>
<h3 style="margin-left: 40px;">1) AVATAR 상체 동기화 </h3>
    <div>
    <img src="/assets/img/posts/hand-sub1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub1-1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>Contour 알고리즘을 통해 영역을 분리, 저장</li>
      <br>
      <li>ConvexHull 알고리즘을 이용하여 손가락 사이의 골의  좌표를 획득</li>
      <br>
      <li>좌표 계산을 통해 ROI(Region Of Interest)를 실행</li>
      <br>
    </ul>
   </div>
   <div>
    <img src="/assets/img/posts/hand-sub2.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub1-2.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
      <ul >
      <li>Canny 함수로 가장자리를 감지하여 Edge 검출</li>
      <br>
      <li>Sobel 함수를 사용하여 Canny된 이미지를 Masking으로 추출하여 가장자리 인식 </li>
      <br>
      <li>Closing 함수를 통해 그림의 불필요한 노이즈를 제거 및 떨어져 있는 선들을 연결</li>
      <br>
    </ul>
   </div>

<h3 style="margin-left: 40px;">2) 사용자 음성 처리 및 AVATAR 얼굴 동기화 </h3>

> 
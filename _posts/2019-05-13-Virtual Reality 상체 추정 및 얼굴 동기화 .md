---
layout: post
featured-img: vr-1
---


## 1. 목적 
> 대화형 가상 현실 어플리케이션의 증가로 인해, 사용자와 일치하게 움직이는 아바타는 사용자의 몰입감를 높이는 데 도움. 몰입감 향상을 위해 상반신 동기화와 함께, 가상의 입술을 애니메이션화 및 말하는 얼굴을 가상현실에서 적용하는 방법을 제안

## 2. 개요
> 가상 현실 단일 사용자 및 다중 사용자 어플리케이션 아바타 동기화를 위해 HMD(Head Mounted Display)와 컨트롤러, 오디오로 사용자의 얼굴과 상반신 표현

<div>
<h2>3. 구현</h2>
<h3 style="margin-left: 40px;">1) AVATAR 상체 동기화 </h3>
    <div>
     <ul>
      <li>상반신-IK 알고리즘 적용</li>
      <br>
      <li>Adjust Neck Orientation</li>
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
 
---
layout: post
featured-img: gismain
---


## 1. 기술 스택 
> node.js 18.12.1 / spring boot 2.7.8   / gradle / jar   
> bootstrap 5.2 / Maria / Thymeleaf
> geoserver  / openlayer


## 2. 구현
<div>
<h2>3. 구현</h2>
<h3 style="margin-left: 40px;">1) 위치 권한</h3>
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

<h3 style="margin-left: 40px;">2) V-WORLD 및 OPENLAYER</h3>
  <div>
    <img src="/assets/img/posts/hand-sub4.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub3.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
      <ul >
      <li>R.O.I 및 전처리  작업을 통한 좌표를 이용하여, 손금 영역의 손금을 추출</li>
      <br>
      <li>손금의 영역은 HoughLine 알고리즘을 통하여 손금의 좌표를 return</li>
      <br>
      <li>Return받은 lines의 좌표를 통해 손금의 데이터만을 가져와 새로운 좌표평면에 손금을 생성</li>
      <br>
    </ul>
   </div>
<h3 style="margin-left: 40px;">3) DATA Geoserver</h3>
<div>
    <img src="/assets/img/posts/hand-sub5.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/hand-sub6.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
      <ul>
      <li>Gaussian Pyramed를 생성한 후, DoG(Difference of Gaussian)을 구해서 극점인 부분의 특징점 후보자 추출</li>
      <br>
      <li>테일러 급수를 사용하여 특징점 후보자 중에서 정확하지 않는 특징점을 제거</li>
      <br>
      <li>Gaussian Weight Function을 활용하여 서술자를 생성</li>
      <br>
      <li>이미지에서 SIFT 특징을 각각 추출한 다음에 서로 가장 비슷한 특징끼리 매칭</li>
      <br>
    </ul>
   </div>

</div>

## 4. 결과

<div>
    <img src="/assets/img/posts/hand-sub7.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
       이 프로젝트는 기존의 알고리즘 기반으로 개인의 <strong>특징을 추출하고 매칭</strong>.
       <br><strong>Contour, ConvexHull, Closing, R.O.I</strong> 등의 알고리즘으로 <strong>MySQL과 연동</strong>하며, 
       <br>개인 이미지 식별의 <strong>정확도</strong>는 <strong>72.5%</strong>
    </ul>
  
</div>


 
 
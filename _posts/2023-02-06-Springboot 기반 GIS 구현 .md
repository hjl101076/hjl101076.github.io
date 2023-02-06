---
layout: post
featured-img: gismain
---


## 기술 스택 
<h3 style="margin-left: 40px;" > node.js 18.12.1 / spring boot 2.7.8   / gradle / jar   
<br> bootstrap 5.2 / Maria / Thymeleaf
<br> geoserver  / openlayer</h3>


<div>
<h2>구현</h2>
<h3 style="margin-left: 40px;">1) 위치 권한</h3>
    <div>
    <img src="/assets/img/posts/1.위치 권한 o.png"  width="50%" height="50%" style="margin-left: 33px; "/>
    <img src="/assets/img/posts/1.위치 권한 x.png"  width="50%" height="50%" style="margin-left: 33px; "/>
        <img src="/assets/img/posts/1.위치 권한 여부.png"  width="50%" height="50%" style="margin-left: 33px; "/>
     <ul>
      <li>프로그램 시작 시 위치 권한 여부 확인</li>
      <br>
      <li>위치 권한 허용할 시, 사용자의 위치로 확대</li>
      <br>
      <li>권한을 거부하면 지도 전체를 보여줄 수 있게 설정</li>
      <br>
    </ul>
   </div>

<h3 style="margin-left: 40px;">2) V-WORLD 및 OPENLAYER</h3>
  <div>
    <img src="/assets/img/posts/2.화면-1.png"  width="50%" height="50%" style="margin-left: 33px; "/>
    <img src="/assets/img/posts/2.화면-2.png"  width="50%" height="50%" style="margin-left: 33px; "/>
     <img src="/assets/img/posts/2.화면-3.png"  width="50%" height="50%" style="margin-left: 33px; "/>
      <ul >
      <li>R.O.I 및 전처리  작업을 통한 좌표를 이용하여, 손금 영역의 손금을 추출</li>
      <br>
      <li>손금의 영역은 HoughLine 알고리즘을 통하여 손금의 좌표를 return</li>
      <br>
      <li>Return받은 lines의 좌표를 통해 손금의 데이터만을 가져와 새로운 좌표평면에 손금을 생성</li>
      <br>
    </ul>
   </div>
 <div>
    <img src="/assets/img/posts/2.vworld 이용한 화면 배열로 담기.png"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts2.화면 타겟에 올리기.png"  width="50%" height="50%" style="margin-left: 40px; "/>
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


 
 
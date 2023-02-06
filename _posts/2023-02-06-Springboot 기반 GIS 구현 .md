---
layout: post
featured-img: gismain
---


## 기술 스택 
<h3 style="margin-left: 40px;" > TOOL : node.js 18.12.1 / spring boot 2.7.8 / Thymeleaf / bootstrap 5.2  / gradle / jar
<br>DB :   Maria DB 
<br>GIS :  geoserver  / openlayers</h3>


<div>
<h2>구현</h2>
<h3 style="margin-left: 40px;">1) GPS 위치 권한</h3>
    <div>
    <img src="/assets/img/posts/1.위치 권한 o.png"  width="50%" height="50%" style="margin-left: 33px; "/>
    <img src="/assets/img/posts/1.위치 권한 x.png"  width="50%" height="50%" style="margin-left: 33px; "/>
        <img src="/assets/img/posts/1.위치 권한 여부.png"  width="50%" height="50%" style="margin-left: 33px; "/>
     <ul>
      <li>위치 권한 허용 - 사용자의 위치로 확대 , 위치 권한 반대 - 지도 전체를 보여줄 수 있게 설정</li>
      <br>
      <li>현재 위치 정보를 알 수 있도록 함수 getCurrentPosition() 사용</li>
      <br>
      <li>함수 centerMap() 화면 확대 및 함수 setGeoLocation() 위치 저장</li>
      <br>
    </ul>
   </div>

<h3 style="margin-left: 40px;">2) V-WORLD 및 OPENLAYER</h3>
  <div>
    <img src="/assets/img/posts/2.화면-1.png"  width="50%" height="50%" style="margin-left: 33px; "/>
    <img src="/assets/img/posts/2.화면-2.png"  width="50%" height="50%" style="margin-left: 33px; "/>
     <img src="/assets/img/posts/2.화면-3.png"  width="50%" height="50%" style="margin-left: 33px; "/>
      <ul >
      <li>Openlayer를 이용한 V-world 배경지도 생성</li>
      <br>
    </ul>
   </div>
 <div>
    <img src="/assets/img/posts/2.vworld 이용한 화면 배열로 담기.png"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/2.화면 타겟에 올리기.png"  width="50%" height="50%" style="margin-left: 40px; "/>
      <ul >
      <li>일반(Base),영상(Satellite),하이브리드(Hybrid) 레이어 PUSH</li>
      <br>
      <li>함수 ol.layer.Group 사용하여 그룹화</li>
      <br>
      <li>ol.Map 함수 안에서 'layers'는 ol.layer.Group 사용 및 'target'은 ID 값 가져와서 지도 생성</li>
      <br>
       <li>지도 선택 시, Visibility로 설정</li>
    </ul>
   </div>

<h3 style="margin-left: 40px;">3) DATA Geoserver</h3>
<div>
    <img src="/assets/img/posts/3.3개의 하천 geoserver.png"  width="50%" height="50%" style="margin-left: 40px; "/>
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

<h3 style="margin-left: 40px;">4) SHP 및 DB 연동</h3>
<div>
    <img src="/assets/img/posts/4.클릭시 줌인 및 하천정보 팝업 출력.png"  width="50%" height="50%" style="margin-left: 40px; "/>
    <img src="/assets/img/posts/4.클릭시 가져온정보로 그 shp의 위치 줌인.png"  width="50%" height="50%" style="margin-left: 40px; "/>
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



 
 
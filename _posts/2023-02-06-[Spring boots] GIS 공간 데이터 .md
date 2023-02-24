---
layout: post
featured-img: gismain
---


## * 기술 스택 
<h4 style="margin-left: 40px;" > TOOL : node.js 18.12.1 / spring boot 2.7.8 / Thymeleaf / bootstrap 5.2 / gradle / jar / Intellij / VS code
<br>DB :   Maria DB 
<br>GIS :  geoserver  / openlayers</h4>


## * 개요
<h4 style="margin-left: 40px;"><strong>Geoserver,DB 연동</strong> 및 <strong>공간 데이터 표출</strong></h4>


<div >
<h2>* 구현</h2>
<h4>1) GPS 위치 권한</h4>
    <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
    <img src="/assets/img/posts/1.위치 권한 o.png"   style="width: 50%;  height: 300px;"/>
    <img src="/assets/img/posts/1.위치 권한 x.png"   style="width: 50%;  height: 300px;  "/>
        <img src="/assets/img/posts/1.위치 권한 여부.png"  />
     <ul>
      <li>위치 권한 허용 - 사용자의 위치로 확대 , 위치 권한 거부 - 지도 전체를 보여줄 수 있게 설정</li>
      <br>
      <li>현재 위치 정보를 알 수 있도록 함수 getCurrentPosition() 사용</li>
      <br>
      <li>함수 centerMap() 화면 확대 및 함수 setGeoLocation() 위치 저장</li>
      <br>
    </ul>
   </div>

<h4>2) Map 및 OPENLAYER 구현</h4>
  <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
    <img src="/assets/img/posts/2.화면-1.png"   style="width: 33%; height: 300px; "/>
    <img src="/assets/img/posts/2.화면-2.png"   style="width: 33%; height: 300px;  "/>
     <img src="/assets/img/posts/2.화면-3.png"   style="width: 33%; height: 300px;  "/>
         <img src="/assets/img/posts/2.vworld 이용한 화면 배열로 담기.png"   style="width: 50%; height: 300px;"/>
    <img src="/assets/img/posts/2.화면 타겟에 올리기.png"   style="width: 50%; height: 300px;"/>
      <ul >
      <li>Openlayer를 이용한 V-world 배경지도 생성</li>
      <br>
      <li>일반(Base),영상(Satellite),하이브리드(Hybrid) 레이어 PUSH</li>
      <br>
      <li>함수 ol.layer.Group으로 배경지도 그룹화</li>
      <br>
       <li>함수 ol.Map으로 'target' 지도 출력</li>
      <br>
    </ul>
   </div>

<h4>3) GIS, Maria DB 데이터 연동</h4>
<div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
    <img src="/assets/img/posts/3.3개의 하천 geoserver.png" style="width:100%; "/>
    <img src="/assets/img/posts/4.클릭시 줌인 및 하천정보 팝업 출력.png"   style="width:100% "/>
     <img src="/assets/img/posts/re_타임리프.jpg"   style="width:33%;"/>
    <img src="/assets/img/posts/4.클릭시 가져온정보로 그 shp의 위치 줌인.png"   style="width:33% ;"/>
      <img src="/assets/img/posts/4.타임리프 데이터.png"   style="width:34%; "/>
      <ul >
      <li>Geoserver에 SHP(지도상에서는 빨강, 하늘, 파랑) 파일 업로드</li>
      <br>
      <li>지도에 보여지는 SHP 레이어 클릭 시, 클릭한 마우스 좌표를 5186으로 변환하여 Geoserver 데이터 전송</li>
      <br>
      <li>SHP 범위 안에 클릭한 좌표가 포함된다면 SHP 정보 표출 및 확대</li>
      <br>
      <li>SHP의 ID 값과 DB의 ID 값 비교하여 데이터 출력</li>
      <br>
    </ul>
   </div>

</div>

<video src="/assets/img/posts/demo.mp4"  style="width: 100%;" controls autoplay muted></video>


 
 
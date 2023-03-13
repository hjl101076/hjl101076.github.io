---
layout: post
featured-img: title
---


## * 기술 스택 
<h4 style="margin-left: 40px;" > TOOL : Flutter / PHP / VS code / XAMPP / Google map
<br>DB :   MySQL </h4>
<br>



## * 개요
<h4 style="margin-left: 40px;">Flutter 와 PHP,MySQL 서버 통신으로 <strong>회원가입, 로그인, 사진  저장, 불러오기 구현</strong> 및 <strong>(*추가) 사진 찍은 위치(GPS) 정보를 google map 위에 마커</strong> 생성</h4>


<div>
<br>
<h2>* 구현</h2>
<h4>1) MySQL 및 백엔드(php)</h4>
    <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
      <img src="/assets/img/posts/1.galleryDB.png"   style="width: 50%; height: 300px; "/>
      <img src="/assets/img/posts/1.userDB.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/1.phpconnection.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/1.apiconnection.png"   style="width: 50%; height: 300px;  "/>
       <ul>
      <li>MySQL database 안에 gallery,user 테이블 생성</li>
      <br>
      <li>각 테이블의 기본키(ID)는 AI 설정 및 그 외 칼럼들은 varchar 설정</li>
      <br>
      <li>백엔드 Xampp 툴을 사용해서 php 소켓 통신</li>
      <br>
      <li>소켓 통신할 수 있게끔 flutter 내부에 Api 클래스 생성</li>
      <br>
    </ul>
    
   </div>
<h4>2) 회원가입 및 이메일 중복 체크</h4>
    <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
        <video src="/assets/img/posts/flutter-2.mp4"  style="width: 50%;height:600px" controls autoplay muted></video>
    <img src="/assets/img/posts/2.checkemail.png"   style="width: 50%; height: 600px; "/>
      <img src="/assets/img/posts/2.checkemaiphp.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/2.signipphp.png"   style="width: 50%; height: 300px;  "/>
     <ul>
      <li>http 라이브러리를 사용해서 API 클래스 내부에 지정된 경로로 소켓 통신</li>
      <br>
      <li>회원가입 시 checkEmail() 함수를 통해 emailcheck.php으로 통신, $resultQuery로 이메일 중복 확인</li>
      <br>
      <li>이메일 중복 체크 후, signup.php 통신으로 db에 회원 정보 저장</li>
    </ul>


   </div>
<br>
<h4>3) 로그인 </h4>
  <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
 
 <video src="/assets/img/posts/flutter-3.mp4"  style="width: 50%;height:600px" controls autoplay muted></video>
    <img src="/assets/img/posts/3.login.png"   style="width: 50%; height: 600px; "/>
    <ul>
      <li>로그인 정보(이메일,비밀번호)를 signin.php 으로 전달 후, 사용자 여부 확인 및 해당하는 유저의 정보를 배열로 가져옴</li>
      <br>
      <li>DB에서 가져온 유저의 정보를 세션의 저장하여 페이지 이동 시, 유저 정보 전달</li>
      <br>
      <li>로그인 후, 네비게이션의 유저 정보 표츌</li>
    </ul>
   </div>

<br>
<h4>4) 카메라 촬영 및 저장,불러오기</h4>
<div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
    <video src="/assets/img/posts/flutter-4.mp4"  style="width: 50%;height:600px" controls autoplay muted></video>
    <img src="/assets/img/posts/4.imgsave2.png"   style="width: 50%; height: 600px; "/>
     <img src="/assets/img/posts/4.imgsave.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/4.imgsavephp.png"   style="width: 50%; height: 300px;  "/>
      <ul>
      <li>image_picker 라이브러리를 사용하며, 비동기 처리를 통해 카메라와 갤러리에서 이미지를 가져옴</li>
      <br>
      <li>이미지는 images 폴더와 갤러리에 저장하고, 이미지 이름과 유저 이메일을 gallery DB 저장</li>
      <br>
      <li>로그인한 유저가 저장한 이미지를 mysqli_fetch_all() 리스트로 불러오고 사진 정보 탭에서 리스트의 개수만큼 화면에 출력</li>
    </ul>
       <img src="/assets/img/posts/5.listimg.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/5.listimgphp.png"   style="width: 50%; height: 300px;  "/>
      <div>

<br>
<h4>*추가 5) google map 및 GPS</h4>

<div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
      <ul>
      <li>google_maps_flutter 라이브러리로 구글 맵 생성</li>
      <br>
      <li>사진 찍은 핸드폰 위치 정보(위경도)를 DB에 저장</li>
      <br>
      <li>지도 정보 탭 누를 시, DB 정보를 JSON로 가져와 구글 맵 위에 마커 생성</li>
    </ul>
      <div>

 
 
---
layout: post
featured-img: gismain
---


## * 기술 스택 
<h4 style="margin-left: 40px;" > TOOL : Flutter / PHP / VS code / XAMPP 
<br>DB :   MySQL </h4>



## * 개요
<h4 style="margin-left: 40px;">PHP 소켓 통신으로<strong> 회원가입,로그인</strong> 및 <strong>카메라 촬영,저장,불러오기</strong></h4>


<div>
<br>
<h2>* 구현</h2>
<br>
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
      <li>통신할 수 있는 flutter 내부에 Api 클래스 생성</li>
      <br>
    </ul>
    
   </div>
<h4>2) 회원가입 및 이메일 중복 체크</h4>
    <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
    <img src="/assets/img/posts/2.checkemail.png"   style="width: 50%; height: 300px; "/>
      <img src="/assets/img/posts/2.checkemaiphp.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/2.signip.png"   style="width: 50%; height: 300px;  "/>
      <img src="/assets/img/posts/2.signipphp.png"   style="width: 50%; height: 300px;  "/>
     <ul>
      <li>회원가입 시 checkEmail() 함수를 통해 emailcheck.php으로 통신, $resultQuery로 이메일 중복 확인</li>
      <br>
      <li>이메일 중복 체크 후, signup.php 통신으로 db에 회원 정보 저장</li>
      <br>
      <li></li>
      <br>
      <li></li>
      <br>
    </ul>
    <video src="/assets/img/posts/flutter-2.mp4"  style="width: 100%;height:20%" controls autoplay muted></video>

   </div>
<br>
<h4>3) 로그인 </h4>
  <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >

   </div>
 <div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
   
   </div>
<br>
<h4>4) 카메라 촬영 및 저장</h4>
<div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
   

</div>

<br>
<h4>5) 찍은 사진 불러오기</h4>
<div style=" display: flex;mjustify-content: space-between; flex-wrap: wrap;" >
   

</div>



 
 
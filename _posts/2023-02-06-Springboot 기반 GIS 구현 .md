---
layout: post
featured-img: vr-1
---


## 1. 기술 스택 
> node.js 18.12.1 / spring boot 2.7.8   / gradle / jar   
  bootstrap 5.2 / Maria / Thymeleaf
  geoserver  / openlayer


## 2. 구현
<h3 style="margin-left: 40px;">1) AVATAR 상체 동기화 </h3>
    <div>
        <img src="/assets/img/posts/vr-sub1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>Final-IK 알고리즘 적용하여 아바타와 사용자 동기화</li>
      <br>
      <li>HMD,컨트롤러를 통한 아바타 scale 조절하여 초기 신체 사이즈 셋업</li>
      <br>
      <li>무거운 Headsetd을 착용한 사용자는 움직임을 최소화하는 경향이 있으므로, 아바타의 사실적인 움직임을 위해 40ms마다 목의 방향 조정</li>
      <br>      
    </ul>
   </div>

 
 
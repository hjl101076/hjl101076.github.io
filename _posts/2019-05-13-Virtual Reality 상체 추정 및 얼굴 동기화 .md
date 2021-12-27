---
layout: post
featured-img: vr-1
---


## 1. 목적 
> 대화형 가상 현실 어플리케이션의 증가로 인해, 사용자와 일치하게 움직이는 아바타는 사용자의 **몰입감**를 높이는 데 도움. 몰입감 향상을 위해 **상반신 동기화**와 함께, 가상의 입술을 **애니메이션화 및 말하는 얼굴***을 가상현실에서 적용하는 방법을 제안

## 2. 개요
> 가상 현실 단일 사용자 및 다중 사용자 어플리케이션 아바타 동기화를 위해 HMD(Head Mounted Display)와 컨트롤러, 오디오로 사용자의 얼굴과 상반신 표현

<div>
<h2>3. 구현</h2>
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

<h3 style="margin-left: 40px;">2) 사용자 음성 처리  </h3>
    <div>
        <img src="/assets/img/posts/vr-sub2.jpg"  width="50%" height="50%" style="margin-left: 55px; "/>
     <ul>
      <li>STT(Speech-To-Text) 알고리즘 통해 사용자 음성 데이터 획득</li>
      <br>
      <li>어느 나라의 언이인지 분석하여 한국어 발음으로 변환</li>
      <br>
      <li></li>
      <br>      
    </ul>
   </div>
   <div>
        <img src="/assets/img/posts/vr-sub3.jpg"  width="50%" height="50%" style="margin-left: 55px; "/>
     <ul>
      <li>음절의 개수로 발화 시간 추정</li>
      <br>
      <li>평균 발화 시간 : 𝑇_𝑀, 발화 시작 시간 : 𝑇_𝑠, 끝 시간 : 𝑇_𝑒, 음절 개수 : N</li>
      <br>
      <li>발화 시간 : 𝑇_𝑀=(𝑇_𝑒  −𝑇_𝑠 )  / N</li>
      <br>      
    </ul>
   </div>

<h3 style="margin-left: 40px;">3) AVATAR 얼굴 동기화 </h3>
    <div>
        <img src="/assets/img/posts/vr-sub1.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>Final-IK 알고리즘 적용하여 아바타와 사용자 동기화</li>
      <br>
      <li>HMD,컨트롤러를 통한 아바타 scale 조절하여 초기 신체 사이즈 셋업</li>
      <br>
      <li>컨트롤러 이용하여 목의 방향 조정</li>
      <br>      
    </ul>
   </div>


<div>
<h2>4. 결과</h2>
 
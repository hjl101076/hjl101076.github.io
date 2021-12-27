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
        <img src="/assets/img/posts/vr-sub2.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>STT(Speech-To-Text) 알고리즘 통해 사용자 음성 데이터 획득</li>
      <br>
      <li>음성 데이터의 언어를 분석하여 한국어 발음으로 변환</li>
      <br>
      <li>한국어의 발음 유성음과 무성음이 존재하기 때문에 [f], [p], [v]와 [b]처럼 구분이 힘든 발음을 정확하게 판단</li>
      <br>      
    </ul>
   </div>
   <div>
        <img src="/assets/img/posts/vr-sub3.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
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
        <img src="/assets/img/posts/vr-sub4.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>9개 발음 기호로 동적 입 애니메이션 구축</li>
      <br>
      <li>초성이 순음(ㅁ,ㅂ,ㅍ)인 경우에는 도입 부분의 입을 다문 모습 추가</li>
      <br>
      <li>아바타를 사람과 비슷하게 만들기 위해서 눈 깜빡임 적용</li>
      <br>      
    </ul>
   </div>

<div>
<h2>4. 결과</h2>
<h3 style="margin-left: 40px;">1) Questions</h3>
    <div>
        <img src="/assets/img/posts/vr-sub4.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>사용자와 인터렉션의 차이에 대한 몰입감 측정</li>
      <br>
      <li>시각화 및 인식률 측정</li>
      <br>
      <li>남성 11명, 여성 7명 총 18명 설문 조사</li>
      <br>      
    </ul>
   </div>

<div>

<h3 style="margin-left: 40px;">2) 실험 환경</h3>
    <div>
        <img src="/assets/img/posts/vr-sub4.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>H1,H2,H3을 확인하기 위한 1인칭 시점과 RPC(Remote Procedure Calls) 통신 멀티 유저 환경</li>
      <br>
      <li>H1: 사용자 본인과 동기화된 가상의 아바타가 미러링 될 때, 얼굴의 입 모양 또한 동기화되어 표현되는 경우에 몰입감이 증대된다.</li>
      <br>
      <li>H2: 다중 사용자가 공동의 가상환경을 공유할 때, 타인을 시각화한 아바타의 자세뿐만 아니라 얼굴 입모양까지 동기화될 때 몰입감이 증대된다.</li>
      <br>
      <li>H3: 다중 사용자 가상현실 체험 시스템에서, 정보를 전달하는 아바타의 립싱크가 맞는 경우가 인식률이 높다.</li>
      <br>     
    </ul>
   </div>

<div>

<h3 style="margin-left: 40px;">3) 만족도</h3>
    <div>
        <img src="/assets/img/posts/vr-sub4.jpg"  width="50%" height="50%" style="margin-left: 40px; "/>
     <ul>
      <li>9개 발음 기호로 동적 입 애니메이션 구축</li>
      <br>
      <li>초성이 순음(ㅁ,ㅂ,ㅍ)인 경우에는 도입 부분의 입을 다문 모습 추가</li>
      <br>
      <li>아바타를 사람과 비슷하게 만들기 위해서 눈 깜빡임 적용</li>
      <br>      
    </ul>
   </div>

<div>
 
 
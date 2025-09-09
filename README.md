<table>
  <tr>
    <td align="center"><img src="https://github.com/user-attachments/assets/16718841-7a79-4187-86f9-4134cd4aae6c" width="1300" /></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/12bbb73f-0bcf-40bc-ba8b-62eb5d9a2d83" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/a5947ee8-37e2-4173-a958-75f46a2d2df7" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/4d70299d-f045-464c-bbb7-270c0b316086" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/d09d3065-f01a-415c-8c6c-492f6a966d10" width="1300"/></td>
    <td align="center"><img src="https://github.com/user-attachments/assets/4f097953-3860-4d2e-8203-fc791a10ac71" width="1300"/></td>
  </tr>
  <tr>
    <td align="center"><a href="https://github.com/Jangwoo0710">박장우</a></td>
    <td align="center"><a href="https://github.com/Joonspar">박준서</a></td>
    <td align="center"><a href="https://github.com/oyk0510">오유경</a></td>
    <td align="center"><a href="https://github.com/lddocy">윤채영</a></td>
    <td align="center"><a href="https://github.com/kkkwid">이승재</a></td>
    <td align="center"><a href="https://github.com/Cho-Hyun-Seung">조현승</a></td>
  </tr>
</table>

# 🍅 KATCHUP 프로젝트
> **MCN 기업 전용 광고주 관리 및 캠페인 협업을 위한 CRM 플랫폼**

---

## 📍 목차
<a href="#1">1. 프로젝트 기획</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-1">1-1. 프로젝트 소개</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-2">1-2. 주요 기능</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#1-3">1-3. 기술 스택</a>

<a href="#2">2. 설계 문서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-1">2-1. 요구사항 명세서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-2">2-2. WBS</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-3">2-3. ERDCloud</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-4">2-4. FIGMA 화면 설계서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-5">2-5. 아키텍처 구조도</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-6">2-6. REST API 명세서</a>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<a href="#2-7">2-7. 기능별 프로세스 흐름도</a>

<a href="#3">3. Back & Front 테스트 결과 </a>

<a href="#4">4. 트러블 슈팅 </a>

<a href="#4">5. 팀원 회고 </a>

<a href="#5">6. 추후 개선 사항 </a>
<br>

---
## <p id="1"> 🪐 1. 프로젝트 기획</p>
## <p id="1-1">1-1. 프로젝트 소개</p>
### 📌 프로젝트 개요

**프로젝트명**: `KATCHUP`  
**주제**: MCN의 인플루언서 마케팅 업무를 한눈에 관리하는 캠페인 특화 CRM 시스템  
> 💡 **MCN (Multi Channel Networks)이란?**  
여러 인플루언서를 관리하며 고객사(광고업체)와의 캠페인을 기획·실행·분석까지 진행하는 기획사
  
> 💡 **캠페인 (Campaign)이란?**  
광고주가 인플루언서와 함께 콘텐츠 제작 및 홍보를 진행하는 일련의 마케팅 활동 (≒ 광고)

---

### 🖼️ 프로젝트 배경

### 📈 1) 인플루언서 마케팅 시장의 성장  
인플루언서 마케팅은 MZ세대의 소비 결정에 큰 영향을 미치고 있습니다.  
- 최근 리포트에 따르면    
  → **MZ세대의 72.3%** 가 인플루언서 추천으로 제품을 구매한 경험이 있으며,  
  → **88%의 광고주**는 인플루언서 마케팅을 지속할 계획입니다.
  
👉 **브랜딩과 판매 전략으로서의 효과성**이 입증되며, 본 프로젝트는 이러한 시장 흐름에 따라 기획되었습니다.

### 📊 2) 캠페인 성과 측정의 어려움  
인플루언서 마케팅은 **다양한 플랫폼**에서 진행되며, 이에 따라 다음과 같은 문제점이 발생합니다.  
- **성과 지표가 파편화**되어 있음
- 플랫폼마다 **클릭수, 좋아요, 댓글, 도달률** 등의 기준이 상이함
- 데이터를 **통합적으로 분석하기 어려움**
- 콘텐츠 반응은 있지만 **매출 기여도와의 연계**가 어려움
- **브랜드 인지도 향상과의 상관관계**도 명확하지 않음
   
👉 성과 지표의 **정량화 및 통합 분석 시스템** 구축의 필요성이 커지고 있습니다.

### 🔄 3) 업무의 불연속성  
현업에서는 다음과 같은 커뮤니케이션/업무 관리 문제가 나타납니다:  
- 고객과의 상담, 피드백 이력이 체계적으로 관리되지 않음  
  → 요구사항 파악이 어려워지고, 반복적 커뮤니케이션 발생
  
업무 인수인계가 비효율적  
  → 담당자 변경 시 히스토리 파악에 시간 소요, 업무 연속성 단절
  
### 💡 KATCHUP의 솔루션  
> **KATCHUP은 광고주 중심의 업무 프로세스를 통합 CRM 시스템으로 연결**하고,  
> 인플루언서 콘텐츠 성과 분석, 캠페인 단계별 파이프라인 관리, 계약서 자동화 기능 등을 통해  
> **MCN 기업의 운영 효율성과 데이터 기반 의사결정**을 효과적으로 지원합니다.

---

### 🗓️ 프로젝트 기간
- **시작일**: 2025년 5월 28일
- **종료일**: 2025년 7월 21일
- **총 기간**: 54일

---

### 🎯 프로젝트 목표
- 광고주–인플루언서 협업 과정 시스템화 및 자동화
- 캠페인 성과 통합 분석 및 시각화
- 문서 기반 업무 전자화 및 이력 관리
- 고객 커뮤니케이션 이력 기록 및 만족도 측정

---

### 👥 타겟 사용자
- 마케팅 실무자 
- 캠페인 운영/기획 담당자
- 영업 담당자

---

### 💡 기대 효과
| ❌ 기존 문제점                      | ✅ KATCHUP의 해결 방식                      |
| :---------------------------- | :------------------------------------ |
| **플랫폼별 개별 분석 (유튜브, 인스타그램 등)** | **콘텐츠 통합 조회 및 성과 시각화**로 전체 흐름을 한눈에 파악 |
| **엑셀·수기 관리로 인한 데이터 누락 위험**    | **CRM 기반 통합 시스템**으로 데이터 정합성 및 일관성 확보  |
| **캠페인 진행 상황 파악 어려움**          | **7단계 캠페인 파이프라인 관리**로 실시간 진행 현황 추적    |
| **커뮤니케이션 이력 공유 및 기록의 어려움**    | **고객사별 히스토리 관리**로 실무 연속성과 인수인계 용이     |
| **제안서, 계약서 등의 반복적인 수작업**      | **템플릿 기반 자동 생성**으로 문서 작업 효율화          |


---

### 🚀 추가 개발 제안
- AI 기반 콘텐츠 추천 기능
- Google Calendar API 연동
- TikTok, X(Twitter) 연동 확장
- 광고주 전용 외부 포털 뷰 제공

---

## <p id="1-2">1-2. ⚙️ 주요 기능</p>
### 🔎 1. 인플루언서 계정 및 성과 분석
- YouTube, Instagram 연동
- 평균 조회수, 구독자 변화율, 시청자 분석
- 인기 콘텐츠 자동 분류 및 캠페인별 성과 분석

### 📊 2. 캠페인 대시보드
- 콘텐츠 유입 경로, 검색 비율 분석
- 성과 리포트 생성 및 자동 전송

### 💼 3. 파이프라인 및 영업 기회 관리
- 제안서, 견적서, 계약서 등록 및 의견 관리
- 전자계약서 PDF 업로드/전송

### 💰 4. 매출 및 문서 관리
- 계약 기반 매출 등록 및 문서 이력 자동화

### 👤 5. 광고주 및 고객사 관리
- 광고 업체 및 담당자 관리, 메일 전송
- 커뮤니케이션 이력 통합 관리

### 💬 6. 채팅 및 커뮤니케이션
- 실시간 채팅, 파일 첨부, 읽음 여부 확인

### ⏰ 7. 알림 및 일정 기능
- 계약 상태 및 이벤트 알림
- 팀/개인 일정 관리

---

## <p id="1-3">1-3. 🛠️ 기술 스택</p>
<div align="center">

<h3>Backend & DB</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white"/>
<img src="https://img.shields.io/badge/springboot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white">
<img src="https://img.shields.io/badge/Spring%20Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white"/>
<img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=JSON%20web%20tokens&logoColor=white"/>
<img src="https://img.shields.io/badge/gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white">
<img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white">
<img src="https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white">
<img src="https://img.shields.io/badge/Redis-FF4438?style=for-the-badge&logo=redis&logoColor=white">
<img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
</div>

<h3>Frontend</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> 
<img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
<img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> 
<img src="https://img.shields.io/badge/bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white">
<img src="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white"/>
<img src="https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white"/>
</div>

<h3>Devops</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white">
<img src="https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Argo-EF7B4D?style=for-the-badge&logo=argo&logoColor=white"/>
</div>

<h3>Tools & Communication</h3>
<div dir="auto">
<img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
<img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=Postman&logoColor=white"/>
<img src="https://img.shields.io/badge/ERDCLOUD-339AF0?style=for-the-badge&logoColor=white">
<img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=notion&logoColor=white">
<img src="https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white"/>
<img src="https://img.shields.io/badge/jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white"/>
<img src="https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white"/>
<img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white"/>
</div>
</div>

---
## <p id="2"> 2. 📁 설계 문서</p>
## <p id="2-1">2-1. 요구사항 명세서</p>
[![요구사항명세서](https://img.shields.io/badge/요구사항명세서-바로가기-yellow?style=for-the-badge)](https://docs.google.com/spreadsheets/d/1q12NH0h5hOcvCFU6CqA1my5h5tuPUZwJ_3G9Ezj80LA/edit?gid=759019660#gid=759019660)

---
## <p id="2-2">2-2. WBS</p>
[![WBS](https://img.shields.io/badge/WBS-바로가기-pink?style=for-the-badge)](https://docs.google.com/spreadsheets/d/1q12NH0h5hOcvCFU6CqA1my5h5tuPUZwJ_3G9Ezj80LA/edit?gid=764235756#gid=764235756)

---
## <p id="2-3">2-3. ERDCloud</p>
[![화면설계서](https://img.shields.io/badge/ERDCLoud-바로가기-purple?style=for-the-badge)](https://www.erdcloud.com/d/oHcHYPjm2Z4JXpG8f)
![image](https://github.com/user-attachments/assets/add751a8-5c6c-4e84-8c81-1c0aa7f10b80)

---
## <p id="2-4">2-4. FIGMA 화면 설계서</p>
[![화면설계서](https://img.shields.io/badge/Figma-바로가기-blue?style=for-the-badge)](https://www.figma.com/design/qBcsAhrNiPfBEJJqcAIGZk/%F0%9F%8D%85?node-id=0-1&t=q3nKm5IJwOSsfwtd-1)

---
## <p id="2-5">2-5. 아키텍처 구조도</p>
[![화면설계서](https://img.shields.io/badge/Architecture-바로가기-red?style=for-the-badge)](https://file.notion.so/f/f/d5de5c40-db63-8184-b2a5-00036fc324c3/feb97e5b-0d4b-4936-8108-4e3847f189db/%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98_%EA%B5%AC%EC%A1%B0%EB%8F%84.png?table=block&id=217e5c40-db63-8066-9741-fa2604c03940&spaceId=d5de5c40-db63-8184-b2a5-00036fc324c3&expirationTimestamp=1750377600000&signature=ZcBROztnF72hEGIFp6Z2Z47BoWMNGVdKxQm2zEEpT18&downloadName=%EC%95%84%ED%82%A4%ED%85%8D%EC%B2%98+%EA%B5%AC%EC%A1%B0%EB%8F%84.png)
![Image](https://github.com/user-attachments/assets/7b189246-8c8d-4816-b684-baf17627a9f3)

---
## <p id="2-6">2-6. REST API 명세서</p>
<details>
<summary>API 명세서 보기</summary>
<br>
<img alt="api 명세서" src="https://github.com/user-attachments/assets/55805390-7bee-47ea-ac49-cb4b20001051" />

</details>

---

## <p id="2-7">2-7. 기능별 프로세스 흐름도</p>
<img width="1704" height="686" alt="Tomato Katchup - 발표본" src="https://github.com/user-attachments/assets/bf8e32a4-c632-4112-8fcd-feb5aec2898a" />

---
## <p id="3"> 3. Back & Front 테스트 결과</p>

<details>
<summary>AI 인플루언서 추천 매칭</summary>
<div>
    <img src="https://github.com/user-attachments/assets/f3db3337-c4a2-449e-9b1e-68c622bcc753"/>
</div>
</details>

<details>
<summary>인플루언서 관리</summary>
<div>
    <h5>인플루언서 등록</h5>
    <img src="https://github.com/user-attachments/assets/414f0d64-bb69-4f3d-9293-a458d341eee4"/>
    <h5>인플루언서 검색</h5>
    <img src="https://github.com/user-attachments/assets/6eec4127-4882-4673-ac79-2c9c68a65ac1"/>
    <h5>인플루언서 수정</h5>
    <img src="https://github.com/user-attachments/assets/1b86c9ff-f769-41f1-944b-a1442dfa890d"/>
    <h5>인플루언서 목록 조회</h5>
    <img src="https://github.com/user-attachments/assets/2d392d41-6574-45dd-bc00-5ab3079796bb"/>
</div>
</details>

<details>
  <summary>인플루언서 분석 대시보드</summary>
  <div>
      <h5>유튜브 대시보드</h5>
      <img src="https://github.com/user-attachments/assets/2f48d23a-e2e8-4633-bcd9-0566a05a5deb"/>
      <img src="https://github.com/user-attachments/assets/7da417a4-255e-4928-8d3f-f8f78a1540c4"/>
    <h5>인스타그램 대시보드</h5>
      <img src="https://github.com/user-attachments/assets/c34b5761-9ac7-4593-8477-452ff442f416"/>
      <img src="https://github.com/user-attachments/assets/da54655b-4c0c-410e-9cf2-b3be7c86b31b"/>
  </div>
</details>

<details>
  <summary>캠페인 성과 대시보드</summary>
  <div><img src=""/></div>
</details>

<details>
  <summary>메인 대시보드</summary>
  <div>
    <img src="https://github.com/user-attachments/assets/79a1a241-aa92-4e0c-b4f3-00010ed22c66"/>
  </div>
</details>

<details>
  <summary>파이프라인</summary>
  <div>
      <h5>파이프라인 목록 조회</h5>
      <img src="https://github.com/user-attachments/assets/ae4613a1-22b6-4a8b-8260-93f53a153aaf"/>
      <summary>파이프라인 상세 조회</summary>
      <img src="https://github.com/user-attachments/assets/52567f62-dbbf-40f3-9a25-2ce64b5b470d"/>
      <h5>파이프라인 등록</summary>
      <img src="https://github.com/user-attachments/assets/893c635b-807d-4f4d-a088-beaa0c928cf1"/>
      <h5>파이프라인 수정</h5>
      <div><img src="https://github.com/user-attachments/assets/a5ff56ed-ea59-4054-ac81-7c19884675f2"/>
      <h5>파이프라인 삭제</h5>
      <img src="https://github.com/user-attachments/assets/2b269ea2-cd72-4087-8a95-ef77450faa91"/>
  </div>
</details>

<details>
  <summary>고객관리</summary>
  <div>
      <h4>고객사</h4>
          <h5>고객사 등록</h5>
          <img src="https://github.com/user-attachments/assets/ab53acdd-39cb-4bd2-815a-54f6e30e484a"/>
          <h5>고객사 수정</h5>
          <img src="https://github.com/user-attachments/assets/09ea095c-487e-4d0d-bee0-5fd37e5f8cbc"/>
          <h5>고객사 삭제</h5>
          <img src="https://github.com/user-attachments/assets/1f2f62f3-3302-499d-9573-5937209b0ad2"/>
          <h5>고객사 목록 조회</h5>
          <img src="https://github.com/user-attachments/assets/2b466d45-5a1b-4bc2-a908-aee890d1acf2"/>
          <h5>고객사 상세</h5>
          <img src="https://github.com/user-attachments/assets/a7f46710-0e37-424c-94c7-761676a5ec0e"/>
      <h4>고객사 사원</h4>
          <h5>고객사 등록</h5>
          <img src="https://github.com/user-attachments/assets/0ac61992-0356-436f-b815-4cbf9890aa11"/>
          <h5>고객사 수정</h5>
          <img src="https://github.com/user-attachments/assets/9a5ac5ad-f7a5-4a30-bd11-358922f4c3a4"/>
          <h5>고객사 삭제</h5>
          <img src="https://github.com/user-attachments/assets/5db83b5a-4718-4e77-8ae8-0f4699001b18"/>
      <h4>만족도 평가</h4>
        <h5>만족도 조사 목록 / 응답률, 평균 만족도 조회</h5>
        <img src="https://github.com/user-attachments/assets/384e65c4-4bdf-4cd0-9f84-47731914bdeb"/>
  </div>
</details>

<details>
  <summary>전자계약서</summary>
  <div>
    <h5>계약서 등록</h5>
    <img src="https://github.com/user-attachments/assets/caea9e8a-b04a-462e-a15f-0c09f53544b0"/>
    <h5>계약서 템플릿 등록</h5>
    <img src="https://github.com/user-attachments/assets/f1e9008a-c356-45c0-b7a9-fb6d8126beb4"/>
    <h5>계약서 템플릿 목록 조회</h5>
    <img src="https://github.com/user-attachments/assets/b78e9f8e-bf34-447c-a0c1-ea60f426ebd6"/>
    <h5>계약서 다운로드 조회</h5>
    <img src="https://github.com/user-attachments/assets/18570452-a083-4e3a-b3bd-c5cd41edac70"/>
    <h5>계약서 이메일 전송</h5>
    <img src="https://github.com/user-attachments/assets/a1f31051-aec2-4c7d-b4f9-b48b1d6484f5"/>
  </div>
</details>

<details>
<summary>회원</summary>
<div>
  <h5>로그인&로그아웃</h5>
  <img src="https://github.com/user-attachments/assets/b4da52ef-60b6-4afc-8210-35370e042bb0"/>
  
  <h5>비밀번호 찾기</h5>
  <img src="https://github.com/user-attachments/assets/35b78789-4708-4257-bf73-75754b201c67"/>
  
  <h5>비밀번호 변경</h5>
  <img src="https://github.com/user-attachments/assets/4716a1b0-a9e5-4f01-86ac-0df572aca666"/>
  
  <h5>개인정보 및 프로필사진 수정</h5>
  <img src="https://github.com/user-attachments/assets/e5d19cb8-5ff1-44e6-8431-c95e94d8cd22"/>
  
  <h5>담당 인플루언서 목록 조회</h5>
  <img src="https://github.com/user-attachments/assets/765c9852-3e90-4ea1-b253-e9870a2201e8"/>
</div>
</details>

<details>
  <summary>알림</summary>
  <div>
      <h5>알림 전체 조회</h5>
      <img src="https://github.com/user-attachments/assets/7dfc4df1-e7b9-4f44-a30d-1b54a3fd71b5"/>
      <h5>알림 확인</h5>
      <img src="https://github.com/user-attachments/assets/382b4a80-4b42-4d7b-b283-a12582c5cdef"/>
      <h5>알림 수신 개수 조회</h5>
      <img src="https://github.com/user-attachments/assets/3542c7d7-b787-4363-9d03-4ad3ef043d14"/>
      <h5>알림 삭제</h5>
      <img src="https://github.com/user-attachments/assets/201bf2fb-34fb-4a6f-b428-d0c7f0a9f3bd"/>
  </div>
</details>

<details>
  <summary>채팅</summary>
  <div>
      <h5>채팅방 생성</h5>
      <img src="https://github.com/user-attachments/assets/95c133c8-06a7-4c39-8b30-a97df7fd8cf6"/>
      <h5>채팅방 퇴장</h5>
      <img src="https://github.com/user-attachments/assets/b9b7070e-511c-45af-ab3a-015dd10d9151"/>
      <h5>채팅방 목록 / 읽지 않은 메시지 수 / 마지막 수신 메시지 조회</h5>
      <img src="https://github.com/user-attachments/assets/8fa9b9c3-fa24-4929-9ca7-40ad41e16b1d"/>
      <h5>특정 채팅방  상세 조회, 메세지 전송</h5>
      <img src="https://github.com/user-attachments/assets/c1256a87-324b-4382-968d-45ddcca6195c"/>
    <h5>채팅방 검색</h5>
      <img src="https://github.com/user-attachments/assets/c5ea7d47-055d-45ce-98ec-93f71e09dba1"/>
    <h5>채팅방 초대</h5>
    <img src="https://github.com/user-attachments/assets/3f813de9-b15e-4390-ae1a-2cc8889293cb"/>
  </div>
</details>

<details>
  <summary>이메일시스템</summary>
  <div>
      <h5>만족도 평가 요청</h5>
      <img src="https://github.com/user-attachments/assets/f261f981-4f94-412d-bc28-e5eef1789e1d"/>
      <h5>만족도 평가 조회</h5>
      <img src="https://github.com/user-attachments/assets/beb61bec-34b4-47c1-b242-2ad5c2fa468c"/>
  </div>
</details>

<details>
  <summary>캘린더</summary>
  <div>
      <h5>일정 조회</h5>
      <img src="https://github.com/user-attachments/assets/b08ee222-99e1-4dea-9eb1-2cd0e1fddd10"/>
      <h5>일정 등록</h5>
      <img src="https://github.com/user-attachments/assets/b020b06b-7010-4ce0-b3c9-5cfd4fa1b237"/>
      <h5>일정 수정</h5>
      <img src="https://github.com/user-attachments/assets/f26b7fce-d4a2-407c-a2ba-35f88cab5a30"/>
      <h5>일정 삭제</h5>
      <img src="https://github.com/user-attachments/assets/cbaefb95-812c-41a7-8735-542ad7b4f3b1"/>
  </div>
</details>

---

## <p id="4"> 4. 트러블 슈팅</p>

### ✅ [TOMATO] JWT 에러 상태 값 수정하기

#### 1️⃣ 문제 상황

Axios 인터셉터를 활용하여 JWT 만료 시 토큰을 재발급하는 로직을 구성하려고 했으나,  
서버로부터 오는 에러 응답의 상태 코드가 항상 `500` 또는 `400`으로 고정되어 있었다.  
JWT 토큰 만료와 같은 인증 관련 에러는 `401 Unauthorized`로 받고 싶었다.

#### 2️⃣ 문제 해결 시도

#### 🔸 1. `@ExceptionHandler`로 처리 시도 ❌

- `BusinessException`을 핸들링하는 `GlobalExceptionHandler`에 로깅 추가

```java
@RestControllerAdvice
@Slf4j
public class GlobalExceptionHandler {

    @ExceptionHandler(BusinessException.class)
    public ResponseEntity<ApiResponse<Void>> handleBusinessException(BusinessException e) {
        ErrorCode errorCode = e.getErrorCode();
        log.error("에러코드 : {}", errorCode.getHttpStatus());
        ApiResponse<Void> response = ApiResponse.failure(errorCode.getCode(), errorCode.getMessage());
        return new ResponseEntity<>(response, errorCode.getHttpStatus());
    }
}
```

🔸 2. JwtErrorResponse를 통해 명시적으로 상태 코드 지정 ⭕

- 기존에는 검증 실패 시 단순히 예외를 던졌기 때문에 Spring Security의 기본 예외 처리기가 500을 반환
- JwtErrorResponse를 활용하여 직접 상태 코드를 설정하도록 변경.

🔧 개선 전 코드

```java
if (token != null && jwtTokenProvider.validateToken(token)) {
    // 검증 실패 시 예외 발생
}
```

🔧 개선 후 코드

```java
public class JwtAuthenticationFilter extends OncePerRequestFilter {

    private final JwtTokenProvider jwtTokenProvider;
    private final JwtErrorResponse jwtErrorResponse;

    @Override
    protected void doFilterInternal(HttpServletRequest request, HttpServletResponse response, FilterChain filterChain)
        throws ServletException, IOException {
        try {
            String upgradeHeader = request.getHeader("Upgrade");
            if ("websocket".equalsIgnoreCase(upgradeHeader)) {
                filterChain.doFilter(request, response);
                return;
            }

            String token = parseToken(request);
            if (token != null && jwtTokenProvider.validateToken(token)) {
                // 인증 성공 로직
                ...
            }

            filterChain.doFilter(request, response);
        } catch (BusinessException e) {
            jwtErrorResponse.setErrorResponse(response, e.getErrorCode()); // ✅ 에러 상태 코드 직접 지정
        } catch (Exception e) {
            jwtErrorResponse.setErrorResponse(response, GlobalErrorCode.INTERNAL_SERVER_ERROR);
        }
    }
}
```

#### 3️⃣ 결과

- 백엔드에서 JWT 토큰 오류 시 401 Unauthorized 상태 코드를 정상적으로 응답
- 프론트엔드는 해당 응답을 감지하여 토큰을 재발급 받고 기존 요청을 자동 재시도
- 최종적으로 JWT 재발급 로직이 안정적으로 동작함을 확인

---

## <p id="5"> 5. 🤝 팀원 회고</p>

| 이름  | 회고 |
|:---:|-|
| 박장우 |벌써 5번째 수행해보는 프로젝트이다 보니 꽤 많이 익숙해져서 감도 많이 잡힌 것 같고 팀원들과 소통하고 협업하는 것에도 많이 능숙해진 것 같다. 전체적인 6개월을 돌이켜봤을 때 우리가 평소에 사용하는 프로그램이 어떤 식으로 이루어져 있고 또 어떻게 만들어지는지를 직접 해봄으로써 잘 알 수 있게 되었고 특히 이번 최종 프로젝트는 주제가 실무와 밀접하게 연관되어 있었던 만큼 현업에 대한 이해도까지 같이 올릴 수 있었던 것 같아 좋은 경험이 되었던 것 같다. 팀원들의 많은 도움을 받아 내 역할을 해낼 수 있었던 경험도 값진 것이었지만 한편으로는 많은 역할을 하지 못했던 건 아쉬움으로 남는다. 이번 최종 프로잭트 경험을 밑거름 삼아 졸업 프로젝트를 포함한 앞으로 수행해나갈 많은 과제들에서 좋은 성과를 낼 수 있도록 개인적인 노력을 기울여야겠다.|
| 박준서 |파이널 프로젝트는 이전까지 경험했었던 프로젝트와 많이 달랐던 것을 느꼈다. 기획부터 구현과 배포까지 했던 점이 꽤 많은 노력을 하여서 뿌듯하다고 느낀다. 이번 부트캠프가 아니였다면, 수많은 기술들을 다루지 못하였다고 생각을 하였고 이번 부트캠프를 통해 기술적인 부분 뿐만 아니라 협업적인 부분에서도 많은 성장을 했다고 생각한다. 부트캠프가 끝나고 나서도 이 경험을 통해 회사나 다른 프로젝트에서 많은 성장을 할 수있기를 기대한다.|
| 오유경 |이번 최종 프로젝트 토마토 케찹은 단순한 기능 구현을 넘어서, 기획 → 설계 → 개발 → 배포까지 전 과정을 팀과 함께 완성해본 정말 값진 경험이었습니다. 처음으로 B2B 프로젝트를 기획하고 구현해보는 경험이었고, 팀원들 모두 실제 회사에서 일해본 경험이 없다 보니 처음엔 어떤 기능이 필요한지조차 감이 잘 오지 않았습니다. 하지만 수많은 시장 조사와 사용자 리서치, 그리고 반복적인 회의를 통해 우리가 만들고자 하는 서비스의 방향성과 핵심 기능을 하나씩 명확하게 정리해갈 수 있었습니다. 그 과정에서 단순히 의견을 나누는 것을 넘어서, 각자의 시야를 하나로 모으고 팀 전체가 납득할 수 있는 기준을 만들어가는 과정이 무척 뜻깊었습니다. 서로 다른 의견을 존중하면서도 함께 더 나은 방향을 찾아가는 과정에서 진짜 협업이 무엇인지 체감할 수 있었고, 단순한 코딩이 아닌 "서비스를 만든다"는 관점에서 문제를 바라보는 눈도 함께 키울 수 있었습니다. 또한 팀원들과의 협업을 통해 의견을 조율하고, GitHub Flow, Jira, Notion, Discord 등 협업 툴을 적극적으로 활용하면서 실제 현업에서의 개발 문화를 경험해볼 수 있었던 것도 큰 자산이 되었습니다.|
| 윤채영 |이번 프로젝트를 통해 가장 크게 느낀 점은 사전 계획(WBS)의 중요성과 팀 내 소통의 핵심성이었습니다. 초기에 전체 일정을 세분화하고 역할을 명확히 나누지 않으면, 후반에 일정이 꼬이거나 커뮤니케이션에 혼선이 생긴다는 걸 직접 경험하면서, 계획 수립의 중요성을 다시 한 번 체감했습니다. 또한 내가 직접 구현하지 않은 기능이라도, 팀원들이 개발한 부분을 이해하고 함께 고민하려는 자세가 프로젝트 전체의 품질을 높이는 데 큰 도움이 된다는 걸 배웠습니다. 협업은 단순한 역할 분담을 넘어 함께 방향을 맞춰가는 과정이라는 걸 느꼈습니다. 기술적으로는 유튜브와 인스타그램 API를 연동해 데이터를 수집하고, 서비스 요구에 맞게 데이터를 가공·정제하여 스케줄러를 통한 자동 업데이트 구조까지 구축하면서, 실제 운영 환경에서 중요한 백엔드 파이프라인 설계 경험을 쌓을 수 있었습니다. 성과적인 측면에서는, 도메인을 직접 구매하고 AWS 환경에서 서비스를 배포해 본 것이 가장 인상 깊었습니다. 마지막으로, 각 페이지 기능을 테스트하고 반복적으로 버그를 수정해가며 결과물의 완성도를 끌어올렸던 과정이 기억에 남습니다. 특히 UX 설계의 중요성을 새삼 느꼈고, 단순히 예쁘게 만드는 것보다 사용자 흐름을 고려한 기획이 훨씬 더 중요하다는 것을 몸소 배웠습니다.|
| 이승재 |이번 프로젝트를 통해 기술적인 성장뿐 아니라 협업과 커뮤니케이션의 중요성을 다시 한 번 느꼈다. 새로운 기술(FCM, SSE, 외부API연동)을 실제 서비스에 적용해보면서 실무 감각을 익힐 수 있었고, 문제 상황에 직접 부딪히며 해결하는 경험을 통해 개발자로서 자신감도 생긴거 같다. 아쉬운 점도 있었지만, 이를 통해 다음 프로젝트에서는 더 효율적으로 일할 수 있을 거란 확신이 들었다.|
| 조현승 |이번 프로젝트를 수행하면서 단순히 기능 구현을 넘어서, 서비스 전체 흐름을 이해하고 운영까지 고려한 개발의 중요성을 깊이 느꼈습니다. 서브쿼리, 윈도우 함수, CTE, 다중 JOIN 등을 직접 활용해 복잡한 데이터를 처리하는 경험 자체가 큰 도전이었고, 그 과정에서 SQL 작성 능력과 데이터 해석력이 눈에 띄게 향상되었습니다.또한, 배포 단계에서는 Terraform을 통해 AWS 인프라를 코드로 구성하고, GitHub Actions를 활용한 CI/CD 자동화를 구축함으로써 인프라 설계와 배포 자동화에 대한 실질적인 경험을 쌓을 수 있었습니다.|

---

## <p id="6"> 6. 🛠️ 추후 개선 사항</p>
### 1) 모니터링 시스템 개선    
- 기존: 장애 발생 시 **즉각적인 대응이 어려움**
- 개선: **AWS CloudWatch 기반 정적 모니터링 시스템 구축**
> ✨ **시스템 상태 및 오류에 대한 실시간 모니터링과 알림**을 통해 장애 대응 시간을 단축하고 서비스 안정성 확보

### 2) 검색 성능 개선  
- 기존: 인플루언서 및 캠페인 검색 시 **복합 조건 처리로 인한 성능 저하 가능성**  
- 개선: **ElasticSearch 도입**
> ✨ 대용량 데이터에 대한 **빠르고 유연한 검색** 제공 사용자 경험(UX) 향상 및 시스템 확장성 확보  

### 3) 계약 프로세스 효율화  
- 기존: 결제 완료된 계약서를 **이메일로 수동 전송 후 업로드**,  
→ 이로 인해 **문서 관리 분산** 및 **추적 어려움** 발생  
- 개선: **전자 계약서 시스템** 도입
> ✨ 계약 과정의 **전산화 및 시스템 통합**을 통해 **업무 효율성 향상** 및 **문서 일관성 확보**  

---

<div align="center">
  <b>Made with 💖 by Team TOMATO</b><br/>
  <i>“Catch up with your campaign. Catch up with KATCHUP.”</i>
</div>

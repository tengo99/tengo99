# CHOI KI WON | 최기원

백엔드 개발을 중심으로  
**AI·클라우드·MSA 환경에서 실제로 동작하는 서비스를 구현하는 개발자**입니다.

단순한 기능 구현에 그치지 않고,  
**확장 가능한 서비스 구조와 실제 사용 흐름을 고려한 설계**를 중요하게 생각합니다.

---

## About Me

- 컴퓨터공학 전공
- Backend Developer
- Spring Boot / FastAPI 기반 백엔드 개발
- GPT / Whisper를 활용한 AI 서비스 개발
- MSA, 실시간 통신, AI 파이프라인에 관심이 있습니다.
- 데이터를 분석하고 실제 의사결정에 활용할 수 있는 서비스 개발을 지향합니다.

---

## Tech Stack

### Backend

![Java](https://img.shields.io/badge/Java-17%20%7C%2021-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

- Spring Boot
- FastAPI
- JPA / Hibernate
- REST API 설계
- WebSocket / STOMP / SockJS
- OpenFeign

### AI

![OpenAI](https://img.shields.io/badge/OpenAI-GPT%20API-412991?style=flat-square&logo=openai&logoColor=white)
![Whisper](https://img.shields.io/badge/OpenAI-Whisper-412991?style=flat-square&logo=openai&logoColor=white)

- OpenAI GPT API
- OpenAI Whisper
- AI 응답 구조화
- AI 파이프라인 설계 및 자동화
- 프롬프트 기반 인사이트 및 콘텐츠 생성

### Data Analysis

![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white)

- Pandas 기반 데이터 정제 및 분석
- Streamlit 기반 분석 서비스 구현
- Plotly 기반 데이터 시각화
- KPI 계산 및 규칙 기반 성과 진단

### Cloud / Infra

![AWS](https://img.shields.io/badge/AWS-EC2%20%7C%20S3%20%7C%20RDS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-NKS-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![NGINX](https://img.shields.io/badge/NGINX-009639?style=flat-square&logo=nginx&logoColor=white)

- AWS EC2 / S3 / RDS / IAM
- Docker
- Kubernetes
- NGINX
- CI/CD Pipeline

### Database / Cache

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

- MySQL
- Redis

---

## Featured Projects

### 1. UnPlug

#### MSA 기반 AI 디지털 디톡스 서비스

스마트폰 과의존을 줄일 수 있도록 챗봇, 사용 제한 및 챌린지 기능을 제공하는  
**MSA 기반 디지털 디톡스 서비스**입니다.

저는 Chat Service의 백엔드 개발을 담당하여 실시간 메시징, AI 자동 응답,  
메시지 저장 및 사용자 인증 연동 기능을 구현했습니다.

#### 주요 구현 내용

- API Gateway, User Service, Chat Service로 구성된 MSA 구조
- Gateway 중심의 JWT 인증 및 사용자 정보 전달 구조
- WebSocket, STOMP, SockJS 기반 실시간 메시징
- OpenAI GPT API를 활용한 챗봇 자동 응답
- OpenFeign을 활용한 서비스 간 통신
- 메시지 저장 및 대화 내역 조회
- 사용자별 채팅방 접근 권한과 소유권 검증
- MySQL 기반 메시지 영속화
- Redis 기반 일부 상태 및 세션 관리
- `userId` 기반 인증 구조를 `username` 기반으로 리팩터링

#### Tech Stack

`Java` `Spring Boot` `JPA` `WebSocket` `STOMP` `SockJS`  
`JWT` `OpenFeign` `MySQL` `Redis` `OpenAI API` `Docker`

**Repository**

https://github.com/BridgeON-Team/unplug-chatbot

---

### 2. AI Video Summarization Pipeline

#### Whisper & GPT 기반 AI 영상 요약 파이프라인

대용량 영상 파일을 업로드하면 음성을 추출하고 텍스트로 변환한 뒤,  
GPT를 활용해 영상의 핵심 내용을 자동으로 요약하는 백엔드 파이프라인입니다.

#### 주요 구현 내용

- FastAPI 기반 대용량 영상 업로드 API
- AWS S3 기반 원본 영상 및 결과 파일 관리
- ffmpeg를 활용한 오디오 추출 및 분할
- Whisper 기반 음성 인식
- 분할된 음성 인식 결과 병합
- GPT API 기반 핵심 내용 자동 요약
- Redis 기반 작업 상태 관리
- 처리 실패를 고려한 작업 복구 구조
- 임시 파일 삭제 및 리소스 정리
- 처리 비용, 속도, 품질을 고려한 파이프라인 설계

#### Tech Stack

`Python` `FastAPI` `ffmpeg` `Whisper` `GPT API`  
`AWS EC2` `AWS S3` `AWS RDS` `Redis`

**Repository**

https://github.com/tengo99/video-summary-service

---

### 3. We-RO

#### Spring Boot 기반 감정 공유형 SNS

사용자가 자신의 고민과 감정을 기록하고 다른 사용자와 공감할 수 있도록 설계한  
**감정 공유형 SNS 서비스**입니다.

서비스 기획과 백엔드 개발을 담당했으며, 사용자 시나리오를 기반으로  
게시글 작성부터 공감과 댓글로 이어지는 사용자 흐름을 설계했습니다.

#### 주요 구현 내용

- 사용자 페르소나 및 서비스 이용 시나리오 정의
- 회원가입 및 로그인
- 사용자 프로필 관리
- 게시글 CRUD
- 좋아요 및 공감 기능
- 북마크 기능
- 댓글 기능
- User, Post, Like, Bookmark 중심의 ERD 설계
- Controller, Service, Repository 계층 구성
- REST API 설계
- JPA 기반 데이터 접근 구조 구현

#### Tech Stack

`Java 17` `Spring Boot` `JPA` `Hibernate` `REST API`  
`MySQL` `React` `Gradle` `Docker` `AWS`

**Repository**

https://github.com/tengo99/wero-sns

---

### 4. Review2Campaign

#### AI 리뷰 분석 및 캠페인 추천 플랫폼

고객 리뷰 CSV 데이터를 분석하여 주요 의견과 고객 인사이트를 도출하고,  
OpenAI API를 활용해 마케팅 캠페인 아이디어를 생성하는 AI 데이터 분석 서비스입니다.

단순히 AI에 원본 데이터를 전달하는 방식이 아니라, 데이터를 먼저 정제하고  
규칙 기반 분석 결과를 생성한 후 이를 AI 분석과 연결하도록 구현했습니다.

#### 주요 구현 내용

- CSV 리뷰 데이터 업로드
- UTF-8, CP949 등 다양한 파일 인코딩 처리
- 결측값, 중복값 및 비정상 데이터 정제
- 리뷰 데이터 기반 핵심 키워드 분석
- 긍정·부정 의견 및 주요 고객 반응 분석
- 분석 결과 대시보드 시각화
- 규칙 기반 고객 인사이트 생성
- OpenAI API 기반 AI 인사이트 생성
- 고객 리뷰 기반 캠페인 아이디어 추천
- Pydantic을 활용한 AI 응답 구조화
- 분석 결과 및 캠페인 결과 내보내기
- 데이터 처리, AI 분석, UI 모듈 분리

#### Tech Stack

`Python` `Streamlit` `Pandas` `Plotly`  
`OpenAI API` `Pydantic`

**Repository**

https://github.com/tengo99/review2campaign

---

### 5. CampaignPulse

#### 광고 성과 분석 및 의사결정 지원 대시보드

광고 집행 CSV 데이터를 분석하여 주요 KPI를 계산하고,  
채널·캠페인·소재·타깃별 성과를 진단하는 데이터 분석 서비스입니다.

성과를 시각적으로 보여주는 것에 그치지 않고, 규칙 기반 진단을 통해  
실행 가능한 개선 방안과 A/B 테스트 가설까지 제안하도록 구현했습니다.

#### 주요 구현 내용

- 광고 집행 CSV 데이터 업로드
- UTF-8, BOM, CP949, EUC-KR 인코딩 자동 처리
- 필수 컬럼과 데이터 형식 검증
- 중복 데이터 및 비정상 값 정제
- CTR, CPC, CPM, CVR, CPA, ROAS 등 KPI 자동 계산
- 날짜, 채널, 캠페인, 소재, 타깃별 필터
- 채널·캠페인·소재·타깃별 성과 집계
- Plotly 기반 광고 성과 시각화
- 노출부터 구매까지의 퍼널 분석
- 중앙값과 최소 표본을 고려한 규칙 기반 성과 진단
- 0~100점 기반 성과 점수 산출
- 예산 조정 및 실행 액션 제안
- A/B 테스트 가설 자동 생성
- Markdown 및 CSV 보고서 다운로드
- 단위 테스트를 통한 데이터 처리 로직 검증

#### Tech Stack

`Python` `Streamlit` `Pandas` `Plotly` `unittest`

**Repository**

https://github.com/tengo99/campaignpulse

---

## What I Focus On

- 단순 CRUD 구현을 넘어선 **서비스 구조 설계**
- 요구사항과 사용자 흐름을 고려한 백엔드 개발
- AI 기능을 실제 서비스에 적용하는 방법
- 서비스 간 책임 분리와 확장 가능한 구조
- 데이터 분석 결과를 실제 의사결정으로 연결하는 기능
- 클라우드 환경에서의 배포와 운영
- 팀 프로젝트에서의 협업과 역할 분담
- 지속적인 리팩터링과 테스트를 통한 코드 품질 개선

---

## Contact

- **Email:** [longvaca0213@gmail.com](mailto:longvaca0213@gmail.com)
- **GitHub:** https://github.com/tengo99

---

> 지속적으로 배우고 기록하며, 실제로 동작하는 서비스를 만드는 개발자가 되겠습니다.

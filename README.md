<!-- 
capsule-render, 배너 설정

type: waving
  -> 렌더링 스타일
color: c0c0c0 (라이트) / 3a3a3a (다크)
  -> 배경 색상
height: 120
  -> 배너의 높이 (픽셀 단위)
text: Taejin Kang's GitHub
  -> 표시될 텍스트 내용
fontColor: 333333 (라이트) / e8e8e8 (다크)
  -> 글자 색상
fontSize: 40
  -> 글자 크기 (픽셀 단위)
-->

<picture>
  <source media="(prefers-color-scheme: dark)"
    srcset="https://capsule-render.vercel.app/api?type=waving&color=3a3a3a&fontColor=e8e8e8&height=120&section=header&text=Taejin%20Kang%27s%20GitHub&fontSize=40"/>
  <img src="https://capsule-render.vercel.app/api?type=waving&color=c0c0c0&fontColor=333333&height=120&section=header&text=Taejin%20Kang%27s%20GitHub&fontSize=40"/>
</picture>

<!-- Introduce -->
## Introduction
### 강태진 (Taejin Kang)
- 호기심 많은 개발자
- 고민하고, 문제를 탐구하는 것을 좋아하는 사람
- Email: mireutale@gmail.com

<!-- Open Source -->
## Open Source
### [rhwp](https://github.com/edwardkim/rhwp) · Rust 기반 HWP 뷰어·에디터
- 2026.06 · HWPX → HWP 저장 시 데이터 손실 수정 **PR 4건 반영**
  - 표 테두리 대각선 방향 정보 유지 ([#1311](https://github.com/edwardkim/rhwp/pull/1311))
  - 문단 번호 겹침 방지 ([#1222](https://github.com/edwardkim/rhwp/pull/1222))
  - 그림의 그림자·효과 정보 보존 ([#1349](https://github.com/edwardkim/rhwp/pull/1349))
  - 표 칸 안의 탭·줄바꿈 저장 ([#1360](https://github.com/edwardkim/rhwp/pull/1360))
- 처음 보는 Rust 코드를 AI로 빠르게 파악하되, 제안을 그대로 쓰지 않고 기존 코드 방식과 테스트로 직접 검증
- 모든 수정에 회귀 테스트 추가

<!-- Project -->
## Projects
### [Fruition](https://github.com/FruitionKR) · AI Agent 지식 워크스페이스
- 2026.04 ~ 현재 · AI·SW 마에스트로 17기 · 3인 팀 팀장 · 기획 · 아키텍처 · 프론트 · AWS 인프라 · DevOps · 일정·배포 관리
- 🌐 [fruition.wiki](https://fruition.wiki/)
- 문서를 올리면 AI가 핵심 개념과 관계를 뽑아 원문 출처가 연결된 LLM Wiki로 쌓아 주는 AI Agent 지식 워크스페이스 (웹 SaaS)
- 📝 소프트웨어 저작권 등록 · 특허 출원 (2026.11) · 베타 테스트 진행
- AWS EKS 기반 MSA 아키텍처 설계 (Spring Boot · Kafka · Redis · PostgreSQL · S3)
- Terraform IaC, GitHub Actions CI/CD·모니터링 구축
- Next.js 프론트엔드·UI/UX 구현
- 문제 정의·기획, 1주 단위 스프린트·회고, FE·BE·AI 간 연동 조율, 실사용자 유치와 피드백 반영
- AI Native 개발 환경 구성: 팀 공통 규칙과 프로젝트 맥락을 문서화하고 반복 작업을 스킬로 만들어, 모든 팀원의 AI가 같은 기준으로 작업하도록 구성
- 현업 멘토링 피드백을 기능 우선순위와 설계에 반영

### [Pilltip](https://github.com/PillTipKR/Pilltip) · 개인맞춤 AI 안심복약 솔루션
- 2025.03 ~ 2025.12 · 4인 팀 · 백엔드 · 웹 프론트 · 온프레미스 인프라 · AI 모델
- 🎬 [서비스 시연 영상](https://youtu.be/IpjfK8htpEg)
- 🏆 졸업과제 금상 · 부산 데이터 위크 최우수상 · Google.org L:AUNCH 3위 · SW중심대학 디지털 경진대회 후원기업상 · SK AI SUMMIT 2025 우수사례 전시
- 복약 이력과 건강 상태를 바탕으로 개인맞춤 DUR 검사, AI 복약 가이드·알림, 디지털 문진, 약물 정보 조회를 제공하는 Android 앱
- Spring Boot 서버 개발 (Java 17 · Spring Boot 3.4 · MySQL · Elasticsearch · Redis)
- 온프레미스 서버 구축·운영: 연구실 지원 서버를 학교 내부망 밖에서 호출할 수 있도록 NGINX·포트포워딩 구성, ZeroSSL 인증서로 HTTPS 적용, 도메인 연결
- YOLOv8 알약 이미지 인식 모델 학습: **최종 정답률 92%**
  - AI-Hub 경구약제 이미지 데이터 사용, 서버 용량 한계로 데이터를 나눠 받아 이전 가중치에서 이어 학습하는 점진적 학습 수행
  - 이전 학습 이미지 10%를 랜덤하게 섞어 학습하고, 정답률 90% 이상일 때만 다음 단계로 진행 (미달 시 에포크·가중치 조정 후 재학습)
  - 한 장의 사진에서 여러 알약의 바운딩 박스를 모두 찾도록 학습
- [웹 문진표](https://github.com/PillTipKR/Pilltip_vercel) 개발 (Next.js · TypeScript): 앱에 입력된 사용자 정보를 병원에 빠르게 제공

### [분산 동시성 스트레스 테스트](https://github.com/Mireutale/java-Distributed-Concurrency-Stress-Test)
- 2025.11 · 개인 프로젝트 · 설계 · 구현 · 측정
- 수강신청은 왜 터지는가. 로드밸런서·서버 3대·우선순위 큐를 직접 만들고 k6로 부하를 걸어 확인한 실험
<!-- TODO: k6 측정 결과 한 줄 추가 (예: 처리량 N → M req/s, p95 지연 X ms → Y ms) -->

### [당근마켓 API 리버싱](https://github.com/Mireutale/Project_API)
- 2025.02 · 팀 프로젝트 · 기획 · 설계 · 백엔드 · PNU Mini Bootcamp
- 당근마켓 API를 리버싱해 FastAPI로 백엔드를 구현하고 React 프론트와 연결

### [지역별 날씨 기반 옷차림 추천](https://github.com/Mireutale/cloudComputingProject)
- 2025.03 ~ 2025.05 · 팀 프로젝트 · 기획 · 설계 · 백엔드 · 클라우드컴퓨팅 수업
- 검색한 지역의 실시간 날씨를 OpenWeather에서 받아 GPT가 자연어로 옷차림을 추천하는 웹 서비스

<!-- Award -->
## Awards
|    날짜    |                       대회명                        |       상        |   팀    |                주관 / 수여                |
| :--------: | :-------------------------------------------------: | :-------------: | :-----: | :---------------------------------------: |
| 2025.10.01 |  부산대학교 정보컴퓨터공학부<br>졸업과제 SW/AI 분과  |    금상, 1위    | Pilltip |  **부산대학교**<br>정보의생명공학대학장   |
| 2025.10.01 |    SW중심대학 마일스톤 장학생<br>SW전문인재S 선정    |     장학생      |    -    | **부산대학교**<br>소프트웨어융합교육원장  |
| 2025.09.28 |      Google.org AI 커리어스쿨<br>창업톤 L:AUNCH      |   장려상, 3위   | Pilltip | **Google.org**<br>KRYPTON X / Root Impact |
| 2025.09.23 | 부산 데이터 위크 2025<br>데이터활용 우수사례 공모전 | 최우수상<br>1위 | Pilltip |      **부산광역시**<br>부산광역시장       |
| 2025.08.12 |          SW중심대학 디지털 경진대회 SW부문          |   후원기업상    | Pilltip |    **SW중심대학협의회**<br>㈜딥노이드     |

<!-- Experience -->
## Experience
### AI·SW 마에스트로
- 2026.04 ~ 현재 · 서울 센터 17기 연수생
- 팀 Fruition 팀장 · 기획 · 아키텍처 · 프론트 · AWS 인프라 · DevOps 담당 ([프로젝트 상세](#fruition--ai-agent-지식-워크스페이스))

### 주식회사 뉴아이 · 개발 인턴
- 2025.06 ~ 2025.08
- OCR과 UNIPASS API를 연동한 무역 서류(수출입) 자동화 시스템 개발
- React·Next.js로 로그인·회원가입 웹 페이지 개발

### PNU Mini Bootcamp 백엔드/클라우드 과정
- 2025.02.03 ~ 2025.02.14 · 부산대학교 정보컴퓨터공학부 주최 · 멋쟁이사자처럼 운영
- FastAPI(Router·의존성 주입), SQLModel, Pydantic, JWT·bcrypt 인증, Redis 캐싱, WebSocket·비동기 처리
- AWS Lightsail에 Gunicorn·systemd·nginx로 배포
- 팀 프로젝트: [당근마켓 API 리버싱](https://github.com/Mireutale/Project_API) 백엔드 개발, 설계 담당

<!-- Education -->
## Education
### 부산대학교 정보컴퓨터공학 학사
- 2020.02 ~ 2026.02
- 보안동아리 KEEPER 14기 (2022.08 ~ 2026.02) · 멘토 및 학술부장 (2024.08 ~ 2025.08)
- 부산대학교 대표 참가: 2025 K-ICT in Busan (2025.07.17), SK AI SUMMIT 2025 (2025.11.02)

## Certifications
- 정보처리기사 (2026.06.12)
- TOPCIT Level 3, 640점 (2026.10.10)
- PCCP Lv.2 (2025.05.31)
- OPIc IM2 (2026.02.19)

## Training
- **AWS Training & Certification**: Architecting on AWS · Agentic AI Foundations · Building Agentic AI with Amazon Bedrock AgentCore
- **Inflearn**: [쉽게 설명하는 AWS 기초 강의](https://www.inflearn.com/certificate/1805614-333984-15365691) · [AWS 배포 완벽가이드](https://www.inflearn.com/certificate/1805614-331548-15365695) · [AWS 클라우드 서비스 인프라 구축 이해와 해킹, 보안](https://www.inflearn.com/certificate/1805614-326695-15365696)

## Tech Stack
### Languages
<div align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=OpenJDK&logoColor=white">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white">
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white">
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=C%2B%2B&logoColor=white">
</div>

### Frontend
<div align="left">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
</div>

### Backend
<div align="left">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=for-the-badge&logo=SpringBoot&logoColor=white">
  <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
  <img src="https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white">
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
</div>

### Databases
<div align="left">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white">
</div>

### Infra & DevOps
<div align="left">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white">
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=Linux&logoColor=black">
  <img src="https://img.shields.io/badge/Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white">
  <img src="https://img.shields.io/badge/k6-7D64FF?style=for-the-badge&logo=k6&logoColor=white">
</div>

### Collaboration
<div align="left">
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=Git&logoColor=white">
  <img src="https://img.shields.io/badge/Github-181717?style=for-the-badge&logo=Github&logoColor=white">
  <img src="https://img.shields.io/badge/Notion-000000?style=for-the-badge&logo=Notion&logoColor=white">
  <img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=Discord&logoColor=white">
</div>

## Problem Solving
<div align="center">
  <img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=priaselay">
</div>

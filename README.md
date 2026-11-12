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
## 🧑‍💻 Introduction
### 강태진 (Taejin Kang)
- 호기심 많은 개발자
- 고민하고, 문제를 탐구하는 것을 좋아하는 사람
- Email: mireutale@gmail.com

<!-- Open Source -->
## 🤝 Open Source
### [rhwp](https://github.com/edwardkim/rhwp) · Rust 기반 HWP 뷰어·에디터
- 2026.06
- HWPX → HWP 저장 시 데이터 손실 수정 **PR 4건 반영**
  - 표 테두리 대각선 방향 정보 유지 ([#1311](https://github.com/edwardkim/rhwp/pull/1311))
  - 문단 번호 겹침 방지 ([#1222](https://github.com/edwardkim/rhwp/pull/1222))
  - 그림의 그림자·효과 정보 보존 ([#1349](https://github.com/edwardkim/rhwp/pull/1349))
  - 표 칸 안의 탭·줄바꿈 저장 ([#1360](https://github.com/edwardkim/rhwp/pull/1360))
- 처음 보는 Rust 코드를 AI로 빠르게 파악하되, 제안을 그대로 쓰지 않고 기존 코드 방식과 테스트로 직접 검증
- 모든 수정에 회귀 테스트 추가

<!-- Project -->
## 🗂️ Projects
### [Fruition](https://github.com/FruitionKR) · AI Agent 지식 워크스페이스
- 2026.04 ~ 현재 · AI·SW 마에스트로 17기 · 3인 팀 팀장
- 🌐 [fruition.wiki](https://fruition.wiki/)
- 문서를 올리면 AI가 핵심 개념과 관계를 뽑아 원문 출처가 연결된 LLM Wiki로 쌓아 주는 웹 SaaS
- 📝 소프트웨어 저작권 등록 (2026.10) · 임시 특허 출원 (2026.11) · 베타 테스트 진행
- AWS EKS 기반 MSA 아키텍처 설계 (Spring Boot · Kafka · Redis · PostgreSQL · S3)
- Terraform IaC, GitHub Actions CI/CD·모니터링 구축
- Next.js 프론트엔드·UI/UX 구현
- Notion 가져오기 구현: 내보내기 zip을 폴더 구조·본문·이미지·표·PDF째 옮기고 Wiki 편입까지 연결
- 문제 정의·기획, 일정·배포 관리, 1주 단위 스프린트·회고, FE·BE·AI 간 연동 조율, 실사용자 유치와 피드백 반영
- AI Native 개발 환경 구성: 팀 공통 규칙과 프로젝트 맥락을 문서화하고 반복 작업을 스킬로 만들어, 모든 팀원의 AI가 같은 기준으로 작업하도록 구성
- 현업 멘토링 피드백을 기능 우선순위와 설계에 반영

### [Pilltip](https://github.com/PillTipKR/Pilltip) · 개인맞춤 AI 안심복약 솔루션
- 2025.03 ~ 2025.12 · 졸업과제 · 4인 팀
- 🎬 [서비스 시연 영상](https://youtu.be/IpjfK8htpEg)
- 복약 이력과 건강 상태를 바탕으로 개인맞춤 DUR 검사, AI 복약 가이드·알림, 디지털 문진, 약물 정보 조회를 제공하는 Android 앱
- Spring Boot 서버 개발 (Java 17 · Spring Boot 3.4 · MySQL · Elasticsearch · Redis)
- 온프레미스 서버 구축·운영: 연구실 지원 서버를 학교 내부망 밖에서 호출할 수 있도록 NGINX·포트포워딩 구성, ZeroSSL 인증서로 HTTPS 적용, 도메인 연결
- YOLOv8 알약 이미지 인식 모델 학습: **최종 정답률 92%**
  - AI-Hub 경구약제 이미지 데이터 사용, 서버 용량 한계로 데이터를 나눠 받아 이전 가중치에서 이어 학습하는 점진적 학습 수행
  - 이전 학습 이미지 10%를 랜덤하게 섞어 학습하고, 정답률 90% 이상일 때만 다음 단계로 진행 (미달 시 에포크·가중치 조정 후 재학습)
  - 한 장의 사진에서 여러 알약의 바운딩 박스를 모두 찾도록 학습
- 웹 문진표 개발 (Next.js · TypeScript): 앱에 입력된 사용자 정보를 병원에 빠르게 제공

### [분산 동시성 스트레스 테스트](https://github.com/Mireutale/java-Distributed-Concurrency-Stress-Test)
- 2025.11 · 우아한테크코스 8기 프리코스 오픈미션 · 개인 프로젝트
- 과부하 상태의 서버는 어떻게 해야 안전하게 요청을 처리할 수 있을까?. 
  - 로드밸런서·서버 3대·우선순위 큐를 직접 만들고 k6로 부하를 걸어 확인한 실험
- 라운드로빈 로드밸런서(WebFlux)를 두어 서버 3대가 공유 PostgreSQL에 접근하는 구조, 우선순위 큐와 최대 동시 처리 수로 요청 제어
- 부하를 10배씩 늘리며 한계 지점 측정 후, 과부하 여부에 따라 동시 처리 수를 적응형으로 제어하도록 구성하여 실패율 감소를 확인
  - 초당 2,000건 수강신청: 실패율 **20.8% → 0%**, p95 응답 **11.7s → 462ms**
- Java 21 · Spring Boot 3.2 · JPA · PostgreSQL · Docker · k6

### [당근마켓 API 리버싱](https://github.com/Mireutale/Project_API)
- 2025.02 · PNU Mini Bootcamp · 4인 팀
- 당근마켓 API를 리버싱해 FastAPI로 백엔드를 구현하고 [React 프론트](https://github.com/ddoed/Project_API-front)와 연결
- 회원가입·로그인(JWT·bcrypt), 상품 등록·수정, 댓글, 좋아요·구매 내역, WebSocket 실시간 채팅 API 구현
- FastAPI · SQLModel · Pydantic · WebSocket

### [지역별 날씨 기반 옷차림 추천](https://github.com/Mireutale/cloudComputingProject)
- 2025.03 ~ 2025.05 · 클라우드컴퓨팅 수업 · 4인 팀
- 검색한 지역의 실시간 날씨를 OpenWeather에서 받아 GPT가 자연어로 옷차림을 추천하는 웹 서비스, 로그인 없이 바로 사용
- OpenWeather Geocoding으로 도시명을 좌표로 바꿔 날씨를 조회하고, 날씨 정보를 프롬프트로 구성해 GPT 추천 생성하는 백엔드 담당
  - 클라우드 컴퓨팅 학습을 위해 구현한 프론트·백엔드를 Docker로 컨테이너화 하여 개인 AWS EC2에 배포 경험
- Flask · OpenAI API · OpenWeather API · Docker · AWS EC2

<!-- Award -->
## 🏆 Awards

|    날짜    |                       대회명                        |       상        |   팀    |                주관 / 수여                |
| :--------: | :-------------------------------------------------: | :-------------: | :-----: | :---------------------------------------: |
| 2025.10.01 |  부산대학교 정보컴퓨터공학부<br>졸업과제 SW/AI 분과  | [금상](img/awards/capstone-gold.png) | Pilltip |  **부산대학교**<br>정보의생명공학대학장   |
| 2025.10.01 |    SW중심대학 마일스톤 장학생<br>SW전문인재S 선정    | [장학생](img/awards/sw-milestone-scholarship.png) |    -    | **부산대학교**<br>소프트웨어융합교육원장  |
| 2025.09.28 |      Google.org AI 커리어스쿨<br>창업톤 L:AUNCH      | [장려상](img/awards/launch-startupthon.png) | Pilltip | **Google.org**<br>KRYPTON X / Root Impact |
| 2025.09.23 | 부산 데이터 위크 2025<br>데이터활용 우수사례 공모전 | [최우수상](img/awards/busan-data-week-2025.png) | Pilltip |      **부산광역시**<br>부산광역시장       |
| 2025.08.12 |          SW중심대학 디지털 경진대회 SW부문          | [후원기업상](img/awards/sw-digital-contest-2025.png) | Pilltip |    **SW중심대학협의회**<br>㈜딥노이드     |

<!-- Experience -->
## 💼 Experience
### AI·SW 마에스트로
- 2026.04 ~ 현재 · 서울 센터 17기 연수생 · 3인 팀 팀장
- 현업 전문가 정규·자유 멘토링 참여
  - 서비스 기획과 MVP 범위 설정, 소프트웨어 개발 방법론
  - 백엔드 아키텍처 설계와 시스템 안정화, Agentic AI 활용 방식
  - 받은 피드백을 기능 우선순위와 설계·개발 과정에 반영
- 생성형 AI와 코딩 에이전트를 활용한 AI Native 개발 방식 학습·적용
  - 요구사항 구체화, 구현 계획, 코드 작성, 테스트, 문서화 전 과정에 AI 활용
  - AI가 만든 결과물은 코드 리뷰와 테스트로 검증한 뒤 반영
- AWS 공식 교육 Cloud Architecture 트랙 수료: Architecting on AWS · Agentic AI Foundations · Building Agentic AI with Amazon Bedrock AgentCore

### 주식회사 뉴아이 · 개발 인턴
- 2025.06 ~ 2025.08
- OCR과 UNIPASS API를 연동한 무역 서류(수출입) 자동화 시스템 개발
- React·Next.js로 로그인·회원가입 웹 페이지 개발

### PNU Mini Bootcamp 백엔드/클라우드 과정
- 2025.02.03 ~ 2025.02.14 · 부산대학교 정보컴퓨터공학부 주최 · 멋쟁이사자처럼 운영
- API 기초: HTTP 요청·응답 구조와 간단한 HTTP 서버 직접 구현, RESTful API 설계 원칙
- FastAPI: Path·Query·Body 파라미터와 응답 모델, Router로 경로별 파일 분리, Dependency(의존성 주입)
- 데이터: SQLModel로 DB 연동과 서비스 계층 분리, Pydantic으로 데이터 검증, 환경변수 관리
- 성능·실시간: Redis 캐싱 전략(TTL, API 응답 캐싱), async/await 비동기 처리, WebSocket 채팅, Background Tasks
- 인증: JWT 발급·검증, 비밀번호 해싱, 회원가입·로그인 구현
- 배포: AWS Lightsail(Ubuntu)에 Gunicorn·systemd·nginx로 서비스 배포

<!-- Education -->
## 🎓 Learning
### Education
**부산대학교 정보컴퓨터공학 학사**
- 2020.02 ~ 2026.02
- 보안동아리 KEEPER 14기 (2022.08 ~ 2026.02) · 멘토 및 학술부장 (2024.08 ~ 2025.08)
- 부산대학교 대표 참가: 2025 K-ICT in Busan (2025.07.17), SK AI SUMMIT 2025 (2025.11.03 ~ 2025.11.04)

### Certifications
- 정보처리기사 (2026.06.12)
- TOPCIT Level 3, 640점 (2026.10.10)
- PCCP Lv.2 (2025.05.31)
- OPIc IM2 (2026.02.19)

### Training
- **AWS Training & Certification** (AI·SW 마에스트로 제공 · Cloud Architecture 트랙)
  - [Architecting on AWS](img/aws-architecting-on-aws.png)
  - [Agentic AI Foundations](img/aws-agentic-ai-foundations.png)
  - [Building Agentic AI with Amazon Bedrock AgentCore](img/aws-bedrock-agentcore.png)
- **Inflearn**
  - [쉽게 설명하는 AWS 기초 강의](https://www.inflearn.com/certificate/1805614-333984-15365691)
  - [AWS 배포 완벽가이드](https://www.inflearn.com/certificate/1805614-331548-15365695)
  - [AWS 클라우드 서비스 인프라 구축 이해와 해킹, 보안](https://www.inflearn.com/certificate/1805614-326695-15365696)

## 🛠️ Tech Stack
### Languages
<div align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=OpenJDK&logoColor=white">
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white">
  <img src="https://img.shields.io/badge/C-A8B9CC?style=for-the-badge&logo=c&logoColor=white">
  <img src="https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=C%2B%2B&logoColor=white">
</div>

### Frameworks & Libraries
<div align="left">
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/Spring Boot-6DB33F?style=for-the-badge&logo=SpringBoot&logoColor=white">
  <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white">
  <img src="https://img.shields.io/badge/JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white">
  <img src="https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white">
  <img src="https://img.shields.io/badge/YOLOv8-111F68?style=for-the-badge">
</div>

### Databases
<div align="left">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/Elasticsearch-005571?style=for-the-badge&logo=elasticsearch&logoColor=white">
</div>

### Infra & DevOps
<div align="left">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white">
  <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white">
  <img src="https://img.shields.io/badge/Terraform-844FBA?style=for-the-badge&logo=terraform&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white">
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

## 🧩 Problem Solving
<div align="center">
  <img src="https://mazassumnida.wtf/api/v2/generate_badge?boj=priaselay">
</div>

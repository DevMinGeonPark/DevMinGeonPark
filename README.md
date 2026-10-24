한국어 | [English](README.en.md)

## 박민건 (Mingeon Park)

**현업과 함께 사내 AI를 만들고, 직접 쓰고 고칠 수 있게 넘겨주는 개발자입니다.**
업무 인터뷰로 AI를 붙일 곳을 찾고, 서비스를 만들어 운영하고, 담당자가 이어서 쓸 수 있도록 교육과 이관까지 합니다.

### 사내 AI 도입 — ㈜큐엠텍 (2025.09 – 2026.09, 대표이사 직속)
AI 서비스 개발·운영과 사내 AX 지원을 맡았습니다(관계사 업무 포함). 사내 코드는 비공개라 링크 없이 설명만 적습니다.

**1. 안전관리 ERP** — Java Spring · Next.js · Linux · Docker, 사내 온프레미스
- 안전관리 담당자와 요구사항을 맞추며 단독 개발. 기존 엑셀 업무는 살리고 반복 작업을 자동화하는 방향으로 기획
- LLM으로 안전 문서 초안 작성. 경량 모델을 기본으로 쓰고 어려운 작업만 상위 모델로 보내 비용 관리
- 개인정보는 마스킹 전용 MCP 서버를 거쳐 LLM에 전달. 관리 화면은 사내망(Tailscale) 전용, 현장 점검은 입력만 되는 1회용·시간 만료 링크로 분리
- 담당자가 직접 수정할 수 있도록 작업 규칙을 정리해 이관

**2. 산업안전 법령 RAG 챗봇**
- 국가법령정보센터 Open API로 중대재해처벌법·산업안전보건법·화학물질관리법 자동 수집, 3일 주기 갱신
- 채팅 질의응답, 조문 요약, 근거 조문 기반 문서 초안 생성. 초안마다 근거 조문과 원문 링크를 표시하고 담당자 확인 후 확정
- 담당자가 승인한 예시를 검색 대상에 쌓아 프롬프트·규칙을 주기적으로 개선
- 문서 초안 작성 시간: 2~3시간 → 10분 이내 (현업 피드백 기준)
- 공개용 재구성: [constrained-rag](https://github.com/DevMinGeonPark/constrained-rag) — 합성 데이터로 닫힌 집합 출력·결정론적 검증·법령 인용 구조를 재현

**3. 사내 AI 교육** — 관계사 임직원 약 30명
- 전체 강의 2시간 × 2회(2026.06, 2026.08) 후 90분 예약제 개별 세션: Claude 기초, 부서별 자동화 대상 발굴, 실습
- 출처·근거 요구, 업무별 지침 설정, 에이전트 간 교차 검증을 교육
- 안전관리 담당자 1명이 사이트를 직접 관리하고 안전 문서 초안을 스스로 만드는 단계까지 도달
- 실험실: 교육 이후 환각이 줄었다는 반응 (현업 피드백, 측정치 아님)

### 개인 프로젝트 — AIRO (2026.09 –)
**여행 계획 AI 어시스턴트.** 대화로 일정을 만들고, 지도 위 실제 도로 경로로 확인하고, 장소·예약 자료·예산을 여행 단위로 모읍니다.
- 여행·일정·장소·경로 도구를 하나의 계약(스키마·권한)으로 정의하고, 웹 채팅·Android 앱·MCP 클라이언트(Claude·Cursor 등)가 같은 계약을 거쳐 같은 여행을 편집
- Supabase Auth + 테이블 RLS. MCP 요청도 사용자 본인 권한으로 실행해 다른 계정의 여행에는 접근 불가
- Next.js · TypeScript · Supabase(Postgres) · OpenAI function calling · MCP
- 서비스: https://airo.dev-heptivision.com · 저장소: [DevMinGeonPark/AIRO](https://github.com/DevMinGeonPark/AIRO) (AGPL-3.0)

### 연구
| 저장소 | 내용 | 소속 · 결과 |
|---|---|---|
| [RoIFuzz](https://github.com/DevMinGeonPark/RoIFuzz) | SROS 2 보안 정책을 켠 상태에서 ROS 2 IDL 메시지를 변이하는 퍼저 | 세종대 정보보호학과 ISLab (2024.04–2024.12) · 한국정보보호학회 CISC-W'24 구두발표 |
| [reinforced-robofuzz](https://github.com/DevMinGeonPark/reinforced-robofuzz) | RoIFuzz 이전 단계: RoboFuzz의 IDL 오라클 강화 실험 | 같은 연구의 초기 코드 (2024.10) |
| [Grounding-Dino-experiment](https://github.com/DevMinGeonPark/Grounding-Dino-experiment) | 학습·라벨링 없이 텍스트 프롬프트로 결정 결함을 찾는 open-set 탐지 실험 | 한국생산기술연구원 제조AI연구센터 인턴 (2025.04–2025.06) |
| [EEG2SDiff](https://github.com/DevMinGeonPark/EEG2SDiff) | 뇌파를 이미지 클래스가 구분되는 임베딩으로 바꾸는 인코더 (학부 졸업연구) | 한국지능정보시스템학회 2023 춘계학술대회 구두발표 |
| [Drowsiness-Detection](https://github.com/DevMinGeonPark/Drowsiness-Detection-classification-performance-improvements-resarch) | EEG 졸음 탐지 연구의 데이터 전처리 | 동서대 ICaN Lab 학부 연구생 |

**특허 출원 (공동 발명자)**
- 로봇 소프트웨어 테스트 시스템 및 방법 (10-2024-0197496, 세종대학교 산학협력단)
- 블루투스 기반 스마트 이동장치의 보안 취약점 분석 시스템 및 방법 (10-2024-0196091, 세종대학교 산학협력단)
- 인공지능 기술기반 직무경험 큐레이팅 시스템 (10-2023-0171430, 동서대학교 산학협력단)

### 강의
2026.07 외부 강의 강사(7시간) — 현대엔지비·㈜삼우이머션·제주대학교 VE·AI 교육과정, 완성차 제조 부문 임직원 대상 "LLM 활용 업무 자동화" · 코더랜드 강사(2022.07–2024.05)

### 그 밖의 공개 작업
- [cs-translation-gpt](https://github.com/DevMinGeonPark/cs-translation-gpt) — 다국어 CS 문의를 번역하고 회신 초안을 만드는 크롬 확장. 단기 근무 중 만든 사내 도구를 데이터 없이 다시 구현
- [agent-eval-harness](https://github.com/DevMinGeonPark/agent-eval-harness) · [rite](https://github.com/DevMinGeonPark/rite) · [gaejo](https://github.com/DevMinGeonPark/gaejo) · [amux](https://github.com/DevMinGeonPark/amux) — 에이전트 평가와 AI 코딩 작업 관리를 위한 개인 도구

### 기술
- **언어** — Python(FastAPI·PyTorch) · Java(Spring) · C · TypeScript(Next.js·React·React Native) · SQL(PostgreSQL)
- **인프라** — Linux · Docker · AWS(Lambda·DynamoDB·CDK) · Supabase
- **AI** — RAG · Function Calling · MCP · LLM 평가

### 연락
devmin7985@gmail.com

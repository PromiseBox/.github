<div align="center">

# 약속상자 · PromiseBox

### 약손 AI — 노인 복약 안전을 위한 AI 에이전트
### Yakson AI — An AI-powered Polypharmacy Safety Agent for Older Adults

[한국어](#한국어) | [English](#english)

</div>

---

<a name="한국어"></a>

## 🇰🇷 한국어

### 약손 AI란?

**약손 AI**는 보호자가 어르신의 약 정보를 입력하면, 식약처·심평원의 **DUR(의약품 안전사용 서비스, Drug Utilization Review)** 공식 데이터를 기반으로 복약 위험을 점검해 알기 쉬운 리포트로 돌려주는 서비스입니다.

여러 약을 동시에 복용하는 노인(다제약물, Polypharmacy) 환경에서, 병용금기·노인부적절약물·중복처방 같은 위험을 보호자가 미리 인지하도록 돕는 것을 목표로 합니다.

> ⚠️ 약손 AI는 진단·처방을 대체하지 않는 **보조 참고 수단**입니다. 최종 판단은 반드시 의사·약사와 상담하세요.

### 핵심 기능

- **간단 입력** — 어르신 기본정보(별칭·나이·성별)와 약 정보를 텍스트 또는 약봉투 사진(OCR)으로 입력
- **DUR 기반 위험 점검** — 병용금기, 노인부적절약물(PIM), 동일효능 중복, 연령·임부금기, 용량·투여기간 주의를 공식 데이터로 점검
- **보호자 눈높이 리포트** — 위험/주의/정상 등급과 근거, 보호자 행동 안내, 약사 인계자료 제공

### 설계 원칙

- **안전 우선** — AI가 위험을 임의 판단하지 않고, 국가 공인 DUR 데이터를 근거로 판정
- **출처 있는 판정** — 모든 경고에 근거를 연결하고 환각·출처를 검증(Eval)
- **의료행위 비대체** — 진단·처방이 아닌 보조 수단임을 화면에 명시
- **고령 친화 · 모바일 퍼스트** — 위험도를 색상·아이콘으로 직관화

### 기술 스택

| 영역 | 기술 |
| --- | --- |
| 프론트엔드 | Next.js (React), Vercel |
| 백엔드 | FastAPI, GCP Cloud Run |
| 데이터베이스 | Cloud SQL (PostgreSQL), Graph DB (Neo4j) |
| AI 오케스트레이션 | LangGraph, LangSmith |
| AI / 데이터 | Vertex AI, 식약처 DUR · 심평원 OpenAPI |
| 데이터 파이프라인 | ETL (Apache Airflow) |

### 저장소

| 저장소 | 설명 |
| --- | --- |
| [`yaksson-ai`](https://github.com/PromiseBox/yaksson-ai) | 기획·문서 저장소 (아키텍처, 화면정의서, DB 설계) |
| [`ui_prototype`](https://github.com/PromiseBox/ui_prototype) | Google AI Studio 기반 UI 프로토타입 |

### 팀 — 약속상자(PromiseBox)

> 프로젝트는 팀 전반의 협의와 기본적인 협업을 바탕으로 진행되었으며, 아래는 대략적인 담당입니다.

| 이름 | GitHub | 담당 |
| --- | --- | --- |
| 이규원 | [@Kyoo32](https://github.com/Kyoo32) | 설계, UI, 검증(LangSmith) |
| 유근일 | [@spacegiyou](https://github.com/spacegiyou) | 기획, Agent(LangGraph) |
| 임성빈 | [@jazdr](https://github.com/jazdr) | LLM 설정, GCP 인프라, DB 설정, CI/CD |
| 정재상 | [@dwarves1](https://github.com/dwarves1) | 데이터베이스 설계, ETL 코드, 검증 쿼리, 산출물 문서 관리 |

---

<a name="english"></a>

## 🇺🇸 English

### What is Yakson AI?

**Yakson AI** is a service where caregivers enter an older adult's medication details and receive an easy-to-read safety report, powered by official **DUR (Drug Utilization Review)** data from Korea's Ministry of Food and Drug Safety (MFDS) and HIRA.

It is designed for polypharmacy settings — where older adults take multiple medications at once — helping caregivers recognize risks such as drug-drug contraindications, potentially inappropriate medications, and therapeutic duplication before they become problems.

> ⚠️ Yakson AI is a **supportive reference tool** and does not replace diagnosis or prescription. Always consult a doctor or pharmacist for final decisions.

### Key Features

- **Simple input** — Enter basic info (nickname, age, sex) and medications via text or a photo of the medication label (OCR)
- **DUR-based risk check** — Screens for contraindicated combinations, potentially inappropriate medications (PIM), therapeutic duplication, age/pregnancy contraindications, and dose/duration cautions using official data
- **Caregiver-friendly report** — Risk/caution/normal grades with evidence, caregiver guidance, and a pharmacist handover sheet

### Design Principles

- **Safety first** — The AI does not judge risk on its own; all decisions are grounded in government-certified DUR data
- **Sourced decisions** — Every alert is linked to its evidence, with hallucination and source verification (Eval)
- **Not a substitute for medical care** — The interface clearly states it is a supportive tool, not diagnosis or prescription
- **Senior-friendly & mobile-first** — Risk levels conveyed through color and icons

### Tech Stack

| Area | Technology |
| --- | --- |
| Frontend | Next.js (React), Vercel |
| Backend | FastAPI, GCP Cloud Run |
| Database | Cloud SQL (PostgreSQL), Graph DB (Neo4j) |
| AI Orchestration | LangGraph, LangSmith |
| AI / Data | Vertex AI, MFDS DUR · HIRA OpenAPI |
| Data Pipeline | ETL (Apache Airflow) |

### Repositories

| Repository | Description |
| --- | --- |
| [`yaksson-ai`](https://github.com/PromiseBox/yaksson-ai) | Planning & documentation (architecture, screen specs, DB design) |
| [`ui_prototype`](https://github.com/PromiseBox/ui_prototype) | UI prototype built with Google AI Studio |

### Team — PromiseBox (약속상자)

> This project was carried out through team-wide discussion and close collaboration. The breakdown below reflects each member's general area of responsibility.

| Name | GitHub | Responsibilities |
| --- | --- | --- |
| Kyuwon Lee | [@Kyoo32](https://github.com/Kyoo32) | Design, UI, Evaluation (LangSmith) |
| Geunil Yoo | [@spacegiyou](https://github.com/spacegiyou) | Planning, Agent (LangGraph) |
| Seongbin Lim | [@jazdr](https://github.com/jazdr) | LLM setup, GCP infrastructure, DB setup, CI/CD |
| Jaesang Jeong | [@dwarves1](https://github.com/dwarves1) | Database design, ETL code, validation queries, deliverable docs |

---

<div align="center">
<sub>© 2026 PromiseBox · 약속상자</sub>
</div>

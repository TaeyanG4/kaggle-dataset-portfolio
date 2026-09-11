# Kaggle Dataset Portfolio

[English](README.md) | **한국어** | [日本語](README.ja.md) | [简体中文](README.zh-CN.md)

**Kaggle Dataset Grandmaster**를 목표로 구축한 재현 가능한 데이터셋 프로젝트의 공개 포트폴리오이자 운영 현황판입니다.

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4  
**기계 판독 상태:** [`portfolio.json`](portfolio.json)  
**업데이트 체크리스트:** [`UPDATE_CHECKLIST.md`](UPDATE_CHECKLIST.md)

## 이 저장소를 사용하는 방법

이 저장소는 **프로젝트 간 통합 인덱스**이며, 개별 프로젝트 저장소나 Kaggle의 실시간 상태를 대체하지 않습니다.

새 AI/채팅/CLI 세션에서는 다음 순서로 확인합니다.

1. 새 대형 데이터셋을 제안하거나 포트폴리오 작업을 재개하기 전에 이 README와 `portfolio.json`을 읽습니다.
2. 각 프로젝트의 코드, QA, provenance, release invariant, 이력은 연결된 프로젝트 저장소를 source of truth로 사용합니다.
3. 현재 Dataset 버전, processing 상태, live 파일, metadata, Usability, downloads, votes, notebook 상태는 live Kaggle readback을 source of truth로 사용합니다.
4. 이 저장소의 지표는 특정 시점의 snapshot이므로 현재 adoption이 중요한 의사결정 전에는 다시 조회합니다.
5. 프로젝트가 완료/종료 milestone에 도달했거나, material release·positioning·adoption·next action이 바뀌면 이 포트폴리오를 갱신합니다.

이 공개 저장소에는 secret이나 private machine/session 정보를 저장하지 않습니다. API key, OAuth token, authorization header, cookie, credential이 포함된 `.env`, 로컬 절대경로, machine identifier, 이메일·개인 연락처, private account/repository identifier를 제외합니다.

### 문서 언어

모든 공개 프로젝트 저장소는 원칙적으로 다음 네 개의 root README를 동기화합니다.

- `README.md` — English
- `README.ko.md` — 한국어
- `README.ja.md` — 日本語
- `README.zh-CN.md` — 简体中文

명령어, URL, 실측값, release 상태, source/rights 주장, 해석상 주의사항은 네 언어에서 의미가 같아야 합니다. 번역 과정에서 새로운 사실을 만들어내지 않습니다.

### 문자 인코딩

모든 텍스트 파일은 유효한 **UTF-8**을 유지합니다. 한글과 기타 비 ASCII 문자를 정확히 보존하며, 디코딩 오류를 무시하거나 대체문자로 바꿔서 통과시키지 않습니다. JSON은 소비자가 다른 형식을 요구하지 않는 한 UTF-8 without BOM으로 저장합니다.

## 운영 원칙

목표는 행 수나 엔지니어링 복잡성을 최대화하는 것이 아니라 실제 사용자 adoption을 높이는 것입니다.

```text
market validation -> source/rights -> pilot -> collect/build -> QA
-> simple release -> Kaggle CLI -> live readback -> showcase notebook
-> adoption diagnosis -> iterate or stop -> portfolio sync
```

핵심 원칙:

- 대규모 수집 전에 수요를 검증합니다.
- 공식 bulk export/API와 명확한 재배포 권리를 우선합니다.
- 수집 및 빌드를 재시작 가능하고 재현 가능하게 만듭니다.
- Kaggle 공개 파일은 과업에 필요한 만큼만 단순하게 유지합니다.
- 게시에는 Kaggle CLI를 우선 사용하고 중요한 write 뒤에는 live readback을 확인합니다.
- Usability 10/10은 품질 baseline이지 수요의 증거가 아닙니다.
- 공개 후 downloads, votes, external notebooks, comments 등 adoption signal을 추적합니다.
- 프로젝트가 완료/종료 milestone에 도달하면 이 포트폴리오를 반드시 동기화합니다.

## 공개된 데이터셋

Snapshot: **2026-09-11 (KST)**. 이후의 최신 수치는 각 Kaggle 페이지가 source of truth입니다.

| 프로젝트 | 데이터 제품 | GitHub | Kaggle | 규모 | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | 입찰·투찰·낙찰·계약 및 관련 entity를 연결한 한국 공공조달 데이터 | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | 약 2.77 GB / 8 files | 10.0 |
| **South Korea Power Grid 5-Minute Data** | KPX 전력수요 예측, 발전기 dispatch target, state-estimated output을 5분 단위로 정리 | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 10억+ rows / 전체 Parquet 1.99 GB + 7월 CSV 0.50 GB / 5 files | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | Smithsonian Open Access 기반 rights-audited image-text와 leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / live 약 916 MB | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | partner country × 월 × 10-digit HSK 무역 및 HSK10에서 파생한 하위 HS grain | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / live 약 1.17 GB | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | 일반음식점·휴게음식점·제과점의 전국 current permit snapshot | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / live 약 403 MB | 10.0 |
| **Autonomous Driving Crash Reports — NHTSA** | 현행 third-amended NHTSA SGO의 ADS/Level 2 ADAS 사고보고와 narrative text | [repo](https://github.com/TaeyanG4/nhtsa-autonomous-driving-crashes) | [dataset](https://www.kaggle.com/datasets/taeyangg4/nhtsa-autonomous-driving-crashes) | 3,263 rows × 123 cols / CSV 1개 4.73 MB | 7.06 |

## Adoption snapshot

**2026-09-11** live Kaggle CLI readback 기준:

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 0 | 0 |
| South Korea Power Grid 5-Minute Data | 6 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 1 | 0 |
| South Korea Customs Trade 2012-2026 HSK10 | 14 | 0 |
| South Korea Food-Service Permits - Snapshot | 16 | 1 |
| Autonomous Driving Crash Reports — NHTSA | 3 | — |

이 수치는 품질 점수가 아니라 adoption funnel로 사용합니다. views가 낮으면 discovery/positioning, views 대비 downloads가 낮으면 activation friction, downloads 대비 votes가 낮으면 differentiation 또는 value communication 문제를 우선 점검합니다.

NHTSA의 vote 수는 현재 live readback에서 반환되지 않아 추정값 0 대신 —로 표시합니다.

## 최근 완료 프로젝트: NHTSA ADS/ADAS crashes

`nhtsa-autonomous-driving-crashes`는 GitHub와 Kaggle에 공개됐습니다. V1은 2021~2025년 6월 archive를 억지로 같은 schema에 합치지 않고 **현행 third-amended NHTSA reporting regime**만 사용합니다.

현재 실측 release:

- source snapshot ID: `20260827`
- source rows: 3,413
- canonical latest Report IDs: 3,263
- columns: 123
- public artifact: `data.csv` 1개
- incident-month coverage: 2023-01 ~ 2026-07
- current regime report submission coverage: 2025-06 ~ 2026-07
- latest-version selection mismatches: 0
- public narratives present: 3,262 / 3,263
- Kaggle version / status: `1 / ready`
- Kaggle Usability: `7.06 / 10`
- launch adoption snapshot: `5 views / 3 downloads`; 현재 readback에서는 vote 수를 확인할 수 없음
- showcase notebook: [What Do Reported Self-Driving Crashes Look Like?](https://www.kaggle.com/code/taeyangg4/what-do-reported-self-driving-crashes-look-like) — `COMPLETE`; 본문 H1은 긴 autonomous-driving 제목을 그대로 보존

중요한 해석 제한: reporting entity나 vehicle make의 raw count는 **crash rate나 safety ranking이 아닙니다.** reporting capability, fleet exposure, operating domain, reporting criteria가 서로 다르기 때문입니다.

## 포트폴리오 구성

| 프로젝트 | 상태 | 지역 | Modality / grain | 주요 사용자 | 역할 |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Published | United States | tabular + narrative text | autonomous driving, safety, NLP | Evergreen |

포트폴리오는 한국/정형 데이터 편중을 줄이기 위해 multimodal과 미국·글로벌 관심 주제로 확장하고 있습니다.

## 공개 정책

프로젝트 저장소에는 재현 가능한 collection/build logic, QA, source note, provenance를 보관합니다. 대용량 raw/runtime artifact는 일반적으로 Git에서 제외합니다. Kaggle 공개본은 파일 선택 friction을 최소화합니다.

- 일반 tabular: 가능하면 `data.csv` 하나
- supervised benchmark: split이 실제로 의미 있을 때만 `train.csv` + `test.csv`
- 대형 tabular: CSV가 size/speed/type fidelity에 실질적 손해를 줄 때 Parquet
- media: media folder와 metadata table 등 최소 root artifact
- 단지 completeness를 위해 동일 데이터를 CSV + Parquet + JSON으로 중복 공개하지 않음

## 프로젝트별 최소 기록

각 프로젝트에 대해 공개 가능하고 유용한 다음 정보를 최신 상태로 유지합니다.

- state / archetype
- geography, modality/grain, target audience, primary task
- GitHub URL / Kaggle URL
- public release shape / high-level scale
- source authority / rights posture
- 최신 검증 Kaggle status / Usability
- `as_of` 날짜가 있는 adoption snapshot
- current bottleneck / concrete next action
- 해석에 영향을 주는 public caveat

`portfolio.json`은 새 세션이나 agent가 모든 프로젝트 README를 긁지 않고도 이 상태를 빠르게 읽을 수 있도록 만든 기계 판독 인덱스입니다.

## 현재 우선순위

1. NHTSA 출시 후 약 1주 checkpoint에서 adoption 지표를 다시 측정하고, Data Explorer metadata blocker는 문서화한 채 불필요한 content version churn을 피합니다.
2. 새로운 대형 flagship을 시작하기 전에 공개된 6개 Dataset의 discovery, activation, vote conversion을 진단합니다.
3. 공식 source가 갱신될 때 강한 evergreen/flagship을 유지하되 사용자 가치 없는 version churn은 피합니다.
4. 모든 공개 프로젝트 README를 영어·한국어·일본어·중국어 간체로 동기화합니다.
5. 모든 프로젝트 완료/종료 milestone 및 material state change 뒤 `portfolio.json`과 네 언어 README를 갱신합니다.

---

이 저장소는 포트폴리오/인덱스입니다. 각 프로젝트의 pipeline, QA, provenance, release history는 해당 프로젝트 저장소가 source of truth이며, 현재 platform 상태는 live Kaggle readback이 최종 기준입니다.

# Kaggle Dataset Portfolio

Public portfolio and operating tracker for reproducible Kaggle datasets built on the path to **Kaggle Dataset Grandmaster**.

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4

> 한국어: 공식·공개 원천을 재현 가능한 파이프라인으로 수집·검증하고, Kaggle 사용자가 빠르게 이해하고 활용할 수 있는 데이터 제품으로 공개하는 프로젝트 모음입니다.

## Operating principle

The goal is not to maximize row count or engineering complexity. Each project is treated as a data product:

```text
market validation -> source/rights -> pilot -> collect/build -> QA
-> simple release -> Kaggle CLI -> live readback -> showcase notebook
-> adoption diagnosis -> iterate or stop
```

Core rules:

- validate user demand before a large collection
- prefer official bulk exports/APIs and explicit redistribution rights
- make collection and builds restartable and reproducible
- keep the public Kaggle release as simple as the task allows
- use Kaggle CLI first for publication and verify important writes with live readback
- treat Usability 10/10 as a quality baseline, not proof of demand
- track downloads, votes, external notebooks, comments, and other adoption signals after launch

## Published datasets

Snapshot: **2026-09-11 (KST)**. Kaggle pages are the source of truth for newer metrics.

| Project | Data product | GitHub | Kaggle | Scale | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | South Korean public procurement covering bids, awards, contracts and related entities | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | ~2.6 GB / 7 files | 7.1 |
| **South Korea Power Grid 5-Minute Data** | KPX demand forecasts, generator dispatch targets and state-estimated output at 5-minute resolution | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 1.0B+ rows / ~2.0 GB primary release | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | Rights-audited Smithsonian Open Access image-text data with leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / ~916 MB live | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | Monthly trade by partner country and Korean 10-digit HSK product, with lower HS grains derived from HSK10 | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / ~1.17 GB live | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | Nationwide current permit snapshot for restaurants, cafes and bakeries | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / ~403 MB live | 10.0 |

## Adoption snapshot

Point-in-time metrics from the Kaggle CLI on **2026-09-11**:

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 0 | 0 |
| South Korea Power Grid 5-Minute Data | 6 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 1 | 0 |
| South Korea Customs Trade 2012-2026 HSK10 | 14 | 0 |
| South Korea Food-Service Permits - Snapshot | 16 | 1 |

These counts are intentionally tracked as an adoption funnel rather than treated as a quality score. Low views suggest a discovery/positioning problem; views without downloads suggest activation friction; downloads without votes suggest differentiation or value-communication work is still needed.

## In progress

### `nhtsa-autonomous-driving-crashes`

**Status:** local project created; market validation / pilot next.  
**Planned product:** an analysis-ready dataset built from official NHTSA Standing General Order reports involving ADS and Level 2 ADAS systems, including vehicle, road, severity and incident-narrative fields.

Planned V1 principles:

- official NHTSA sources only
- inspect current and historical reporting regimes before harmonizing schemas
- preserve report/version semantics and source provenance
- do not turn raw manufacturer report counts into unsupported crash-rate or safety rankings
- prefer one obvious `data.csv` for the public V1 if practical
- pair the release with a fast EDA/NLP showcase notebook
- stop after the pilot if the market or schema evidence does not justify a full historical build

**GitHub:** pending  
**Kaggle:** pending

## Portfolio shape

| Project | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|
| KONEPS | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | United States | tabular + narrative text | autonomous driving, safety, NLP | Trend / experiment |

The portfolio is deliberately moving beyond a Korea-only/tabular concentration by adding multimodal and globally relevant or US-focused products.

## Release policy

Project repositories contain the reproducible collection/build logic, QA, source notes and provenance. Large raw/runtime artifacts are normally kept out of Git. Kaggle-facing releases should minimize file-choice friction:

- generic tabular: prefer one `data.csv`
- supervised benchmark: use `train.csv` + `test.csv` only when the split is meaningful
- large tabular: use Parquet when CSV materially hurts size, speed or type fidelity
- media: keep root choices minimal, typically media folder(s) + one metadata table
- do not publish redundant full CSV + Parquet + JSON copies merely for completeness

## Current priorities

1. Finish KONEPS live metadata/usability cleanup without creating unnecessary data versions.
2. Run the NHTSA market-validation and source/schema pilot before any large historical build.
3. Diagnose adoption for the five published datasets before starting another large flagship collection.
4. Update this portfolio when a dataset is materially released, repositioned, or gains meaningful external adoption.

---

This repository is a portfolio/index. Each linked project repository remains the source of truth for its own pipeline, QA, provenance and release history.

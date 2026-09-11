# Kaggle Dataset Portfolio

Public portfolio and operating tracker for reproducible Kaggle datasets built on the path to **Kaggle Dataset Grandmaster**.

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4  
**Machine-readable state:** [`portfolio.json`](portfolio.json)  
**Update checklist:** [`UPDATE_CHECKLIST.md`](UPDATE_CHECKLIST.md)

> 한국어: 공식·공개 원천을 재현 가능한 파이프라인으로 수집·검증하고, Kaggle 사용자가 빠르게 이해하고 활용할 수 있는 데이터 제품으로 공개하는 프로젝트 모음입니다.

## How to use this repository

This repository is the **cross-project index**, not a replacement for project repositories or live Kaggle state.

For a new AI/chat/CLI session:

1. Read this README and `portfolio.json` before proposing another large dataset or resuming portfolio work.
2. Use the linked project repository as the source of truth for that project's code, QA, provenance, release invariants, and history.
3. Use live Kaggle readback as the source of truth for current dataset version, processing status, files, metadata, Usability, downloads, votes, and notebook state.
4. Treat point-in-time metrics in this repository as snapshots. Refresh them before making a decision that depends on current adoption.
5. Update this portfolio after a material release, positioning change, new public repository, meaningful adoption change, or a major next-action change.

Do not store secrets or private machine/session data here. Keep API keys, OAuth tokens, authorization headers, cookies, credential-bearing `.env` files, local absolute paths, machine identifiers, email addresses, and private account/repository identifiers out of this public portfolio.

### Text encoding

All text files in this portfolio should remain valid **UTF-8**. Preserve Korean and other non-ASCII text exactly; never "fix" encoding by silently dropping or replacing undecodable characters. JSON should be written as UTF-8 without BOM unless a consuming tool explicitly requires something else.

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

**Status:** local repository scaffold exists; no commits or public GitHub repository yet; market validation / source-schema-rights pilot next.  
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

| Project | State | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Planning/pilot | United States | tabular + narrative text | autonomous driving, safety, NLP | Trend / experiment |

The portfolio is deliberately moving beyond a Korea-only/tabular concentration by adding multimodal and globally relevant or US-focused products.

## Release policy

Project repositories contain the reproducible collection/build logic, QA, source notes and provenance. Large raw/runtime artifacts are normally kept out of Git. Kaggle-facing releases should minimize file-choice friction:

- generic tabular: prefer one `data.csv`
- supervised benchmark: use `train.csv` + `test.csv` only when the split is meaningful
- large tabular: use Parquet when CSV materially hurts size, speed or type fidelity
- media: keep root choices minimal, typically media folder(s) + one metadata table
- do not publish redundant full CSV + Parquet + JSON copies merely for completeness

## Minimum project record

For each portfolio project, keep these public, non-sensitive fields current when they are known:

- state and archetype
- geography, modality/grain, target audience, and primary task
- GitHub URL and Kaggle URL
- public release shape and high-level scale
- source authority and rights posture at a high level
- latest verified Kaggle status/Usability when relevant
- point-in-time adoption metrics with an `as_of` date
- current bottleneck and one concrete next action
- important public caveats that affect interpretation

`portfolio.json` is intended to make these fields easy for a new session or agent to inspect without scraping prose from every repository.

## Current priorities

1. Finish KONEPS live metadata/usability cleanup without creating unnecessary data versions.
2. Run the NHTSA market-validation and source/schema/rights pilot before any large historical build.
3. Diagnose adoption for the five published datasets before starting another large flagship collection.
4. Create and link the NHTSA GitHub repository only after the local project has a meaningful initial commit worth publishing.
5. Refresh `portfolio.json` and this README when state or adoption materially changes.

---

This repository is a portfolio/index. Each linked project repository remains the source of truth for its own pipeline, QA, provenance and release history, and live Kaggle readback remains authoritative for current platform state.

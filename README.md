# Kaggle Dataset Portfolio

**English** | [한국어](README.ko.md) | [日本語](README.ja.md) | [简体中文](README.zh-CN.md)

Public portfolio and operating tracker for reproducible Kaggle datasets built on the path to **Kaggle Dataset Grandmaster**.

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4  
**Machine-readable state:** [`portfolio.json`](portfolio.json)  
**Update checklist:** [`UPDATE_CHECKLIST.md`](UPDATE_CHECKLIST.md)

## How to use this repository

This repository is the **cross-project index**, not a replacement for project repositories or live Kaggle state.

For a new AI/chat/CLI session:

1. Read this README and `portfolio.json` before proposing another large dataset or resuming portfolio work.
2. Use the linked project repository as the source of truth for that project's code, QA, provenance, release invariants, and history.
3. Use live Kaggle readback as the source of truth for current dataset version, processing status, files, metadata, Usability, downloads, votes, and notebook state.
4. Treat point-in-time metrics in this repository as snapshots. Refresh them before making a decision that depends on current adoption.
5. Update this portfolio after every project completion/terminal milestone and after a material release, positioning change, meaningful adoption change, or major next-action change.

Do not store secrets or private machine/session data here. Keep API keys, OAuth tokens, authorization headers, cookies, credential-bearing `.env` files, local absolute paths, machine identifiers, email addresses, and private account/repository identifiers out of this public portfolio.

### Documentation languages

Every public project repository should maintain synchronized root READMEs in four languages:

- `README.md` — English
- `README.ko.md` — Korean
- `README.ja.md` — Japanese
- `README.zh-CN.md` — Simplified Chinese

Keep commands, URLs, measured values, release status, source/rights claims, and interpretation caveats aligned across all four. Translate prose faithfully; do not invent facts during translation.

### Text encoding

All text files should remain valid **UTF-8**. Preserve Korean and other non-ASCII text exactly; never "fix" encoding by silently dropping or replacing undecodable characters. JSON should be written as UTF-8 without BOM unless a consuming tool explicitly requires something else.

## Operating principle

The goal is not to maximize row count or engineering complexity. Each project is treated as a data product:

```text
market validation -> source/rights -> pilot -> collect/build -> QA
-> simple release -> Kaggle CLI -> live readback -> showcase notebook
-> adoption diagnosis -> iterate or stop -> portfolio sync
```

Core rules:

- validate user demand before a large collection
- prefer official bulk exports/APIs and explicit redistribution rights
- make collection and builds restartable and reproducible
- keep the public Kaggle release as simple as the task allows
- use Kaggle CLI first for publication and verify important writes with live readback
- treat Usability 10/10 as a quality baseline, not proof of demand
- track downloads, votes, external notebooks, comments, and other adoption signals after launch
- update this portfolio when a project reaches a completion/terminal milestone

## Published datasets

Snapshot: **2026-10-25 (KST)**. Kaggle pages are the source of truth for newer metrics.

| Project | Data product | GitHub | Kaggle | Scale | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | South Korean public procurement covering bids, submissions, awards, contracts and related entities | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | ~2.77 GB / 8 files | 10.0 |
| **South Korea Power Grid 5-Minute Data** | KPX demand forecasts, generator dispatch targets and state-estimated output at 5-minute resolution | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 1.0B+ rows / 1.99 GB full Parquet + 0.50 GB July CSV / 5 files | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | Rights-audited Smithsonian Open Access image-text data with leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / ~916 MB live | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | Monthly trade by partner country and Korean 10-digit HSK product, with lower HS grains derived from HSK10 | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / ~1.17 GB live | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | Nationwide current permit snapshot for restaurants, cafes and bakeries | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / ~403 MB live | 10.0 |
| **Autonomous Driving Crash Reports — NHTSA** | Current third-amended NHTSA SGO ADS/Level 2 ADAS crash reports with narrative text | [repo](https://github.com/TaeyanG4/nhtsa-autonomous-driving-crashes) | [dataset](https://www.kaggle.com/datasets/taeyangg4/nhtsa-autonomous-driving-crashes) | 3,263 rows × 123 cols / one 4.73 MB CSV | 10.0 |
| **Kaggle Top Solutions and Strategies** | Public solution writeups of finished Kaggle competitions at every rank, with the techniques each writeup reports, source links and rank status | [repo](https://github.com/TaeyanG4/kaggle-top-solutions-and-strategies) | [dataset](https://www.kaggle.com/datasets/taeyangg4/kaggle-top-solutions-and-strategies) | 70,576 rows / 4 files / ~76.1 MB live | 10.0 |

## Adoption snapshot

Point-in-time metrics from live Kaggle CLI readback on **2026-10-25**:

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 24 | 0 |
| South Korea Power Grid 5-Minute Data | 69 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 103 | 1 |
| South Korea Customs Trade 2012-2026 HSK10 | 73 | 0 |
| South Korea Food-Service Permits - Snapshot | 130 | 1 |
| Autonomous Driving Crash Reports — NHTSA | 26 | 0 |
| Kaggle Top Solutions and Strategies | 41 | 1 |

These counts are intentionally tracked as an adoption funnel rather than treated as a quality score. Low views suggest a discovery/positioning problem; views without downloads suggest activation friction; downloads without votes suggest differentiation or value-communication work is still needed.

The dataset list readback returns downloads, votes and Usability but not per-dataset views, so the earlier view counts kept in `portfolio.json` keep their own `2026-09-11` date. Votes remain the weakest step of the funnel: four of the seven datasets still have none.

## Latest completed project: Kaggle Top Solutions and Strategies

`kaggle-top-solutions-and-strategies` is now public on GitHub and Kaggle. It indexes the **public solution writeups of finished Kaggle competitions at every rank**, with the techniques each writeup reports, the source link and an explicit rank status. The public files carry links and summaries only; solution full text and evidence quotes stay internal.

Current measured release facts from the project repository and Kaggle readback:

- release / Kaggle version: `0.6.0` / `6` (uploaded 2026-10-24 07:13 UTC)
- public artifacts: the merged `kaggle_all_solutions_and_strategies_merged.csv` plus `competitions.csv`, `solutions.csv` and `strategies.csv`
- public rows: 70,576 (competitions 678, solutions 7,237, technique rows 62,661)
- live files: 4 files / 102 columns / 76,105,813 bytes
- competition coverage: 678 finished competitions, 2010-2026, from Meta Kaggle official fields
- official ranks: 6,016; `rank_status` separates official, reported and unknown instead of guessing a rank
- solutions by rank: 6,035 inside the top 100, 920 outside it, 282 with an unknown rank
- technique rows by usage: 53,977 final_used, 4,286 tested_rejected, 2,731 failed
- Kaggle version / status: `6 / ready`
- Kaggle Usability: `10.0 / 10` (8.24 right after the upload, 10.00 after the column descriptions)
- Data Explorer descriptions: files `4/4`; columns `102/102`
- adoption snapshot: `41 downloads / 1 vote` on 2026-10-25
- showcase notebook: [Getting Started with Kaggle Top Solutions](https://www.kaggle.com/code/taeyangg4/getting-started-with-kaggle-top-solutions) — `COMPLETE` (version 12)
- rights: the data compilation is CC BY-NC-SA 4.0 and preserves the MIT/Apache notices of its sources; this is a non-commercial research project

Important caveat: the per-solution summaries and technique judgements are **a model's reading of what the author claimed** (Codex `gpt-6.1-sol`), checked against the source text in code but not against a human-judged gold set. A separate LLM session cross-checked 200 cards on 2026-10-23 and found 99.0% of the technique judgements correct; that is same-model-family agreement, not human evaluation. A missing label is not evidence that a technique was not used.

## Portfolio shape

| Project | State | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Published | United States | tabular + narrative text | autonomous driving, safety, NLP | Evergreen |
| Kaggle Top Solutions | Published | Global / Kaggle platform | writeup metadata + technique rows | Kaggle competitors, ML practitioners, AI agents | Competition painkiller |

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
- point-in-time adoption metrics with an explicit `as_of` date
- current bottleneck and one concrete next action
- important public caveats that affect interpretation

`portfolio.json` is intended to make these fields easy for a new session or agent to inspect without scraping prose from every repository.

## Current priorities

1. Diagnose discovery, activation, and vote conversion across the seven published datasets before starting another large flagship collection.
2. For Kaggle Top Solutions and Strategies, build a human-judged label sample before claiming accuracy, and leave the periodic `kts update` schedule for the owner to register.
3. Keep the strongest evergreen/flagship datasets current when their official sources update, but avoid version churn without user value.
4. Keep all public project READMEs synchronized in English, Korean, Japanese, and Simplified Chinese.
5. Refresh `portfolio.json` and all four portfolio READMEs after every project completion/terminal milestone and material state change.

---

This repository is a portfolio/index. Each linked project repository remains the source of truth for its own pipeline, QA, provenance and release history, and live Kaggle readback remains authoritative for current platform state.

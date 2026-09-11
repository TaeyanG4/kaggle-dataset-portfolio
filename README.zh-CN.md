# Kaggle Dataset Portfolio

[English](README.md) | [한국어](README.ko.md) | [日本語](README.ja.md) | **简体中文**

这是一个面向 **Kaggle Dataset Grandmaster** 目标构建的可复现数据集项目公开作品集与运营状态索引。

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4  
**机器可读状态:** [`portfolio.json`](portfolio.json)  
**更新清单:** [`UPDATE_CHECKLIST.md`](UPDATE_CHECKLIST.md)

## 如何使用本仓库

本仓库是**跨项目索引**，不会取代各项目仓库或 Kaggle 的实时状态。

在新的 AI / chat / CLI 会话中，按以下顺序检查：

1. 在提出新的大型 Dataset 或恢复作品集工作之前，先阅读本 README 与 `portfolio.json`。
2. 每个项目的 code、QA、provenance、release invariant 与历史，以对应的 project repository 为 source of truth。
3. 当前 Dataset version、processing status、live files、metadata、Usability、downloads、votes 与 notebook state，以 live Kaggle readback 为 source of truth。
4. 本仓库中的指标是 point-in-time snapshot；如果决策依赖当前 adoption，必须重新获取实时值。
5. 当项目达到 completion / terminal milestone，或发生 material release、positioning、adoption、next action 变化时，更新本作品集。

本公开仓库不得保存 secret 或 private machine/session 信息。排除 API key、OAuth token、authorization header、cookie、包含凭据的 `.env`、本地绝对路径、machine identifier、邮箱或个人联系方式、private account/repository identifier。

### 文档语言

所有公开 project repository 原则上都应维护并同步以下四个 root README：

- `README.md` — English
- `README.ko.md` — Korean
- `README.ja.md` — Japanese
- `README.zh-CN.md` — Simplified Chinese

命令、URL、实测值、release status、source/rights claim 与解释性 caveat 在四种语言中必须保持语义一致。翻译过程中不得补造事实。

### 文本编码

所有文本文件保持有效 **UTF-8**。准确保留韩文、日文、中文以及其他 non-ASCII 字符，不得通过 silent ignore / replacement 隐藏 decode error。除非下游工具明确要求其他格式，JSON 使用 UTF-8 without BOM。

## 运营原则

目标不是最大化行数或 engineering complexity，而是提高真实用户 adoption。

```text
market validation -> source/rights -> pilot -> collect/build -> QA
-> simple release -> Kaggle CLI -> live readback -> showcase notebook
-> adoption diagnosis -> iterate or stop -> portfolio sync
```

核心规则：

- 在大型采集前验证真实需求
- 优先 official bulk export/API 与明确的 redistribution rights
- 让 collection/build 可重启且可复现
- Kaggle 公共发布保持与 task 相匹配的最小复杂度
- 发布优先使用 Kaggle CLI，重要 write 后通过 live readback 验证
- Usability 10/10 是 quality baseline，不是需求证明
- 发布后跟踪 downloads、votes、external notebooks、comments 等 adoption signal
- 项目达到 completion / terminal milestone 后同步本作品集

## 已发布 Dataset

Snapshot: **2026-09-11 (KST)**。之后的最新值以各 Kaggle page 为 source of truth。

| Project | Data product | GitHub | Kaggle | Scale | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | 连接招标、投标、授标、合同及相关实体的韩国公共采购数据 | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | 约 2.77 GB / 8 files | 10.0 |
| **South Korea Power Grid 5-Minute Data** | KPX 需求预测、generator dispatch target 与 state-estimated output，5 分钟粒度 | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 10亿+ rows / 完整 Parquet 1.99 GB + 7月 CSV 0.50 GB / 5 files | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | 基于 Smithsonian Open Access 的 rights-audited image-text data 与 leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / live 约 916 MB | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | partner country × month × 10-digit HSK 贸易，以及由 HSK10 派生的 lower HS grain | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / live 约 1.17 GB | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | 餐厅、咖啡店、烘焙店的全国 current permit snapshot | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / live 约 403 MB | 10.0 |
| **Autonomous Driving Crash Reports — NHTSA** | 当前 third-amended NHTSA SGO 的 ADS / Level 2 ADAS crash reports 与 narrative text | [repo](https://github.com/TaeyanG4/nhtsa-autonomous-driving-crashes) | [dataset](https://www.kaggle.com/datasets/taeyangg4/nhtsa-autonomous-driving-crashes) | 3,263 rows × 123 cols / 单个 CSV 4.73 MB | 6.47 |

## Adoption snapshot

基于 **2026-09-11** live Kaggle CLI readback：

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 0 | 0 |
| South Korea Power Grid 5-Minute Data | 6 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 1 | 0 |
| South Korea Customs Trade 2012-2026 HSK10 | 14 | 0 |
| South Korea Food-Service Permits - Snapshot | 16 | 1 |
| Autonomous Driving Crash Reports — NHTSA | 0 | 0 |

这些数字不是 quality score，而是 adoption funnel。views 低时优先诊断 discovery/positioning；views 相对高但 downloads 低时诊断 activation friction；downloads 有但 votes 低时诊断 differentiation 或 value communication。

## 最近完成的项目：NHTSA ADS/ADAS crashes

`nhtsa-autonomous-driving-crashes` 已公开到 GitHub 和 Kaggle。V1 没有强行把 2021 至 2025 年 6 月 archive 合并到同一个 schema，而是仅使用 **current third-amended NHTSA reporting regime**。

当前实测 release：

- source snapshot ID: `20260827`
- source rows: 3,413
- canonical latest Report IDs: 3,263
- columns: 123
- public artifact: 1 个 `data.csv`
- incident-month coverage: 2023-01 至 2026-07
- current regime report submission coverage: 2025-06 至 2026-07
- latest-version selection mismatches: 0
- public narratives present: 3,262 / 3,263
- Kaggle status: `ready`

重要解释限制：reporting entity 或 vehicle make 的 raw count **不是 crash rate，也不是 safety ranking**。reporting capability、fleet exposure、operating domain 与 reporting criteria 并不相同。

## 作品集结构

| Project | State | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Published | United States | tabular + narrative text | autonomous driving, safety, NLP | Trend / experiment |

作品集正在降低 Korea-only / tabular 的集中度，并增加 multimodal 以及面向美国和全球受众的主题。

## Release policy

Project repository 保存 reproducible collection/build logic、QA、source note 与 provenance。大型 raw/runtime artifact 通常不纳入 Git。Kaggle-facing release 应尽量降低 file-choice friction。

- generic tabular：优先一个 `data.csv`
- supervised benchmark：仅在 split 真正有意义时使用 `train.csv` + `test.csv`
- large tabular：当 CSV 在 size/speed/type fidelity 上造成实质损失时使用 Parquet
- media：保持最少的 root artifact，例如 media folder + metadata table
- 不为了 completeness 而重复发布完整 CSV + Parquet + JSON

## 每个 project 的最小记录

每个 project 应保持以下公开、非敏感信息为最新状态：

- state / archetype
- geography、modality/grain、target audience、primary task
- GitHub URL / Kaggle URL
- public release shape / high-level scale
- source authority / rights posture
- 最新验证的 Kaggle status / Usability
- 带 `as_of` 日期的 adoption snapshot
- current bottleneck / concrete next action
- 影响解释的 public caveat

`portfolio.json` 是 machine-readable index，使新 session/agent 不必抓取所有 project README 也能快速恢复整体状态。

## 当前优先级

1. 不创建不必要的 content version，优先提升 NHTSA 有实际价值的 metadata / Data Explorer Usability。
2. 在启动新的大型 flagship 前，诊断 6 个已发布 Dataset 的 discovery、activation 与 vote conversion。
3. official source 更新时维护强 evergreen/flagship，但避免没有 user value 的 version churn。
4. 所有公开 project README 保持 English / Korean / Japanese / Simplified Chinese 同步。
5. 所有 project completion / terminal milestone 与 material state change 后，更新 `portfolio.json` 与四种语言 README。

---

本仓库是 portfolio/index。各 project 的 pipeline、QA、provenance、release history 以对应 project repository 为 source of truth；当前 platform state 以 live Kaggle readback 为最终依据。

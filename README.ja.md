# Kaggle Dataset Portfolio

[English](README.md) | [한국어](README.ko.md) | **日本語** | [简体中文](README.zh-CN.md)

**Kaggle Dataset Grandmaster** を目指して構築している、再現可能なデータセット・プロジェクトの公開ポートフォリオ兼運用トラッカーです。

**Kaggle:** https://www.kaggle.com/taeyangg4  
**GitHub:** https://github.com/TaeyanG4  
**機械可読ステータス:** [`portfolio.json`](portfolio.json)  
**更新チェックリスト:** [`UPDATE_CHECKLIST.md`](UPDATE_CHECKLIST.md)

## このリポジトリの使い方

このリポジトリは **プロジェクト横断インデックス** であり、各プロジェクトのリポジトリや Kaggle の live state を置き換えるものではありません。

新しい AI / chat / CLI セッションでは次の順序で確認します。

1. 新しい大規模 Dataset を提案したり、ポートフォリオ作業を再開したりする前に、この README と `portfolio.json` を読みます。
2. 各プロジェクトの code、QA、provenance、release invariant、履歴は、リンク先の project repository を source of truth とします。
3. 現在の Dataset version、processing status、live files、metadata、Usability、downloads、votes、notebook state は live Kaggle readback を source of truth とします。
4. このリポジトリの指標は point-in-time snapshot なので、adoption に依存する判断の前には再取得します。
5. プロジェクトが completion / terminal milestone に到達したとき、または material release・positioning・adoption・next action が変わったとき、このポートフォリオを更新します。

この公開リポジトリには secret や private machine/session 情報を保存しません。API key、OAuth token、authorization header、cookie、credential を含む `.env`、ローカル絶対パス、machine identifier、メールアドレス・個人連絡先、private account/repository identifier は除外します。

### ドキュメント言語

すべての公開 project repository では、原則として次の 4 つの root README を同期して維持します。

- `README.md` — English
- `README.ko.md` — Korean
- `README.ja.md` — Japanese
- `README.zh-CN.md` — Simplified Chinese

コマンド、URL、実測値、release status、source/rights claim、解釈上の caveat は 4 言語で意味を一致させます。翻訳時に新しい事実を作りません。

### 文字エンコーディング

すべてのテキストファイルは有効な **UTF-8** を維持します。韓国語・日本語・中国語などの non-ASCII 文字を正確に保持し、decode error を silent ignore / replacement で隠しません。JSON は、利用側が別形式を要求しない限り UTF-8 without BOM で保存します。

## 運用原則

目的は行数や engineering complexity を最大化することではなく、実ユーザーの adoption を高めることです。

```text
market validation -> source/rights -> pilot -> collect/build -> QA
-> simple release -> Kaggle CLI -> live readback -> showcase notebook
-> adoption diagnosis -> iterate or stop -> portfolio sync
```

主要ルール:

- 大規模収集の前に需要を検証する
- official bulk export/API と明確な redistribution rights を優先する
- collection/build を restartable かつ reproducible にする
- Kaggle 公開物は task に必要な範囲で最小・明快にする
- publication は Kaggle CLI を優先し、重要な write 後は live readback で確認する
- Usability 10/10 は quality baseline であり、需要の証明ではない
- 公開後は downloads、votes、external notebooks、comments などの adoption signal を追跡する
- project completion / terminal milestone の後は portfolio を同期する

## 公開済み Dataset

Snapshot: **2026-09-11 (KST)**。それ以降の最新値は各 Kaggle page が source of truth です。

| Project | Data product | GitHub | Kaggle | Scale | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | 入札・応札・落札・契約などをつないだ韓国公共調達データ | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | 約 2.77 GB / 8 files | 10.0 |
| **South Korea Power Grid 5-Minute Data** | KPX の需要予測、generator dispatch target、state-estimated output を 5 分粒度で整理 | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 10億+ rows / 全履歴 Parquet 1.99 GB + 7月 CSV 0.50 GB / 5 files | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | Smithsonian Open Access を rights-audited した image-text data と leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / live 約 916 MB | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | partner country × month × 10-digit HSK 貿易と HSK10 から派生した lower HS grain | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / live 約 1.17 GB | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | restaurant / cafe / bakery の全国 current permit snapshot | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / live 約 403 MB | 10.0 |
| **Autonomous Driving Crash Reports — NHTSA** | current third-amended NHTSA SGO の ADS / Level 2 ADAS crash report と narrative text | [repo](https://github.com/TaeyanG4/nhtsa-autonomous-driving-crashes) | [dataset](https://www.kaggle.com/datasets/taeyangg4/nhtsa-autonomous-driving-crashes) | 3,263 rows × 123 cols / 1 CSV 4.73 MB | 10.0 |

## Adoption snapshot

**2026-09-11** の live Kaggle CLI readback:

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 0 | 0 |
| South Korea Power Grid 5-Minute Data | 6 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 1 | 0 |
| South Korea Customs Trade 2012-2026 HSK10 | 14 | 0 |
| South Korea Food-Service Permits - Snapshot | 16 | 1 |
| Autonomous Driving Crash Reports — NHTSA | 3 | — |

これらは quality score ではなく adoption funnel として扱います。views が少なければ discovery/positioning、views に比べ downloads が少なければ activation friction、downloads に比べ votes が少なければ differentiation または value communication を優先的に確認します。

NHTSA の vote 数は今回の live readback では返されなかったため、0 と推測せず — と表示します。

## 直近の完了プロジェクト: NHTSA ADS/ADAS crashes

`nhtsa-autonomous-driving-crashes` は GitHub と Kaggle で公開済みです。V1 は 2021〜2025年6月の archive を無理に同じ schema に統合せず、**current third-amended NHTSA reporting regime** のみを採用しています。

現在の実測 release:

- source snapshot ID: `20260827`
- source rows: 3,413
- canonical latest Report IDs: 3,263
- columns: 123
- public artifact: 1 `data.csv`
- incident-month coverage: 2023-01 〜 2026-07
- current regime report submission coverage: 2025-06 〜 2026-07
- latest-version selection mismatches: 0
- public narratives present: 3,262 / 3,263
- Kaggle version / status: `1 / ready`
- Kaggle Usability: `10.0 / 10`
- Data Explorer descriptions: file `1/1` exact, columns `123/123` exact
- launch adoption snapshot: `5 views / 3 downloads`; vote 数は今回の readback では取得不可
- showcase notebook: [What Do Reported Self-Driving Crashes Look Like?](https://www.kaggle.com/code/taeyangg4/what-do-reported-self-driving-crashes-look-like) — `COMPLETE`; notebook H1 は長い autonomous-driving タイトルを保持

重要な解釈上の制限: reporting entity や vehicle make の raw count は **crash rate や safety ranking ではありません**。reporting capability、fleet exposure、operating domain、reporting criteria が異なるためです。

## ポートフォリオ構成

| Project | State | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Published | United States | tabular + narrative text | autonomous driving, safety, NLP | Evergreen |

ポートフォリオは Korea-only / tabular への偏りを減らすため、multimodal や US/global interest のテーマへ広げています。

## Release policy

Project repository には reproducible collection/build logic、QA、source note、provenance を保存します。大容量 raw/runtime artifact は通常 Git から除外します。Kaggle-facing release は file-choice friction を最小化します。

- generic tabular: 可能なら `data.csv` 1つ
- supervised benchmark: split が本当に意味を持つ場合のみ `train.csv` + `test.csv`
- large tabular: CSV が size/speed/type fidelity を実質的に損なう場合に Parquet
- media: media folder + metadata table など最小限の root artifact
- completeness だけを目的に同一データを CSV + Parquet + JSON で重複公開しない

## 各 project の最小記録

各 project では、公開可能で有用な次の情報を最新に保ちます。

- state / archetype
- geography, modality/grain, target audience, primary task
- GitHub URL / Kaggle URL
- public release shape / high-level scale
- source authority / rights posture
- 最新確認済み Kaggle status / Usability
- `as_of` 日付付き adoption snapshot
- current bottleneck / concrete next action
- 解釈に影響する public caveat

`portfolio.json` は、新しい session/agent が全 project README を読み取らなくても、この状態を高速に把握できる machine-readable index です。

## 現在の優先事項

1. NHTSA 公開後およそ1週間の checkpoint で adoption 指標を再測定する。Usability / Data Explorer の quality gate は完了したため、不要な content version churn は避ける。
2. 新しい大規模 flagship を始める前に、公開済み 6 Dataset の discovery、activation、vote conversion を診断する。
3. official source 更新時に強い evergreen/flagship を維持するが、user value のない version churn は避ける。
4. すべての公開 project README を English / Korean / Japanese / Simplified Chinese で同期する。
5. すべての project completion / terminal milestone と material state change の後に `portfolio.json` と 4 言語 README を更新する。

---

このリポジトリは portfolio/index です。各 project の pipeline、QA、provenance、release history は該当 project repository が source of truth であり、現在の platform state は live Kaggle readback が最終基準です。

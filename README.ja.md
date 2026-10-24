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

Snapshot: **2026-10-25 (KST)**。それ以降の最新値は各 Kaggle page が source of truth です。

| Project | Data product | GitHub | Kaggle | Scale | Usability |
|---|---|---|---|---:|---:|
| **KONEPS Public Procurement Intelligence** | 入札・応札・落札・契約などをつないだ韓国公共調達データ | [repo](https://github.com/TaeyanG4/koneps-procurement-intelligence) | [dataset](https://www.kaggle.com/datasets/taeyangg4/koneps-public-procurement-intelligence) | 約 2.77 GB / 8 files | 10.0 |
| **South Korea Power Grid 5-Minute Data** | KPX の需要予測、generator dispatch target、state-estimated output を 5 分粒度で整理 | [repo](https://github.com/TaeyanG4/korea-power-grid) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-power-grid-5-minute) | 10億+ rows / 全履歴 Parquet 1.99 GB + 7月 CSV 0.50 GB / 5 files | 10.0 |
| **Smithsonian 25K Museum Image-Text Dataset** | Smithsonian Open Access を rights-audited した image-text data と leakage-safe object splits | [repo](https://github.com/TaeyanG4/smithsonian-image-text) | [dataset](https://www.kaggle.com/datasets/taeyangg4/smithsonian-25k-museum-image-text) | 24,972 images / live 約 916 MB | 10.0 |
| **South Korea Customs Trade 2012-2026 HSK10** | partner country × month × 10-digit HSK 貿易と HSK10 から派生した lower HS grain | [repo](https://github.com/TaeyanG4/korea-customs-trade) | [dataset](https://www.kaggle.com/datasets/taeyangg4/south-korea-customs-trade-hsk10) | 22.35M HSK10 rows / live 約 1.17 GB | 10.0 |
| **South Korea Food-Service Permits - Snapshot** | restaurant / cafe / bakery の全国 current permit snapshot | [repo](https://github.com/TaeyanG4/korea-business-lifecycle) | [dataset](https://www.kaggle.com/datasets/taeyangg4/korea-food-service-permits) | 3.01M rows / live 約 403 MB | 10.0 |
| **Autonomous Driving Crash Reports — NHTSA** | current third-amended NHTSA SGO の ADS / Level 2 ADAS crash report と narrative text | [repo](https://github.com/TaeyanG4/nhtsa-autonomous-driving-crashes) | [dataset](https://www.kaggle.com/datasets/taeyangg4/nhtsa-autonomous-driving-crashes) | 3,263 rows × 123 cols / 1 CSV 4.73 MB | 10.0 |
| **Kaggle Top Solutions and Strategies** | 終了した Kaggle competition の公開 solution writeup を順位に関係なく集め、writeup ごとの技法・原文リンク・順位根拠を整理 | [repo](https://github.com/TaeyanG4/kaggle-top-solutions-and-strategies) | [dataset](https://www.kaggle.com/datasets/taeyangg4/kaggle-top-solutions-and-strategies) | 70,576 rows / 4 files / live 約 76.1 MB | 10.0 |

## Adoption snapshot

**2026-10-25** の live Kaggle CLI readback:

| Dataset | Downloads | Votes |
|---|---:|---:|
| KONEPS Public Procurement Intelligence | 24 | 0 |
| South Korea Power Grid 5-Minute Data | 69 | 0 |
| Smithsonian 25K Museum Image-Text Dataset | 103 | 1 |
| South Korea Customs Trade 2012-2026 HSK10 | 73 | 0 |
| South Korea Food-Service Permits - Snapshot | 130 | 1 |
| Autonomous Driving Crash Reports — NHTSA | 26 | 0 |
| Kaggle Top Solutions and Strategies | 41 | 1 |

これらは quality score ではなく adoption funnel として扱います。views が少なければ discovery/positioning、views に比べ downloads が少なければ activation friction、downloads に比べ votes が少なければ differentiation または value communication を優先的に確認します。

dataset list の readback は downloads・votes・Usability を返しますが dataset ごとの views は返しません。そのため `portfolio.json` に残る views は以前の `2026-09-11` の日付を保持します。funnel で最も弱い段階は依然 votes で、7件のうち4件はまだ vote が 0 です。

## 直近の完了プロジェクト: Kaggle Top Solutions and Strategies

`kaggle-top-solutions-and-strategies` を GitHub と Kaggle で公開しました。**終了した Kaggle competition の公開 solution writeup を順位に関係なく**集め、writeup ごとに報告された技法、原文リンク、明示的な rank status を併記します。公開ファイルにはリンクと要約のみを入れ、solution 原文と引用は内部に残します。

現在の実測 release:

- release / Kaggle version: `0.6.0` / `6`（2026-10-24 07:13 UTC アップロード）
- public artifact: merged `kaggle_all_solutions_and_strategies_merged.csv` と `competitions.csv`、`solutions.csv`、`strategies.csv`
- public rows: 70,576（competition 678、solution 7,237、技法行 62,661）
- live files: 4 files / 102 columns / 76,105,813 bytes
- competition coverage: Meta Kaggle の公式フィールドに基づく終了 competition 678件、2010〜2026
- 公式順位: 6,016件。`rank_status` で official / reported / unknown を区別し、順位を推測しない
- 順位別 solution: top 100 以内 6,035、top 100 外 920、順位不明 282
- 使用状態別の技法行: final_used 53,977、tested_rejected 4,286、failed 2,731
- Kaggle version / status: `6 / ready`
- Kaggle Usability: `10.0 / 10`（アップロード直後 8.24、column description 入力後 10.00）
- Data Explorer descriptions: file `4/4`、columns `102/102`
- adoption snapshot: 2026-10-25 時点で `41 downloads / 1 vote`
- showcase notebook: [Getting Started with Kaggle Top Solutions](https://www.kaggle.com/code/taeyangg4/getting-started-with-kaggle-top-solutions) — `COMPLETE`（version 12）
- 権利: データ編集物は CC BY-NC-SA 4.0 で、source の MIT/Apache 表示を保持します。非商用の研究プロジェクトです

重要な解釈上の制限: solution の要約と技法判定は **モデルが読み取った著者の主張**（Codex `gpt-6.1-sol`）であり、原文との照合はコードで行っていますが、人が判定した gold set では検証していません。2026-10-23 に別の LLM session が card 200件を cross-check し、技法判定の 99.0% が正しいと判断しましたが、これは同系列モデルの一致であり人による評価ではありません。label が無いことは、その技法を使わなかった証拠にはなりません。

## ポートフォリオ構成

| Project | State | Geography | Modality / grain | Primary audience | Role |
|---|---|---|---|---|---|
| KONEPS | Published | South Korea | relational/tabular procurement | economics, procurement, business ML | Flagship |
| Power Grid | Published | South Korea | high-frequency time series | energy, forecasting, operations | Flagship |
| Smithsonian | Published | Global / US institution | image + text | CV, CLIP, VLM, multimodal | Evergreen / diversification |
| Customs Trade | Published | South Korea + global partners | monthly product-country tabular | trade, supply chain, forecasting | Flagship |
| Food-Service Permits | Published | South Korea | business/location tabular | market analysis, forecasting | Evergreen |
| NHTSA ADS/ADAS Crashes | Published | United States | tabular + narrative text | autonomous driving, safety, NLP | Evergreen |
| Kaggle Top Solutions | Published | Global / Kaggle platform | writeup metadata + technique rows | Kaggle competitors, ML practitioners, AI agents | Competition painkiller |

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

1. 新しい大規模 flagship を始める前に、公開済み 7 Dataset の discovery、activation、vote conversion を診断する。
2. Kaggle Top Solutions and Strategies は、精度を主張する前に人が判定した label サンプルを作る。定期更新 `kts update` の予約登録は owner 自身が実行する。
3. official source 更新時に強い evergreen/flagship を維持するが、user value のない version churn は避ける。
4. すべての公開 project README を English / Korean / Japanese / Simplified Chinese で同期する。
5. すべての project completion / terminal milestone と material state change の後に `portfolio.json` と 4 言語 README を更新する。

---

このリポジトリは portfolio/index です。各 project の pipeline、QA、provenance、release history は該当 project repository が source of truth であり、現在の platform state は live Kaggle readback が最終基準です。

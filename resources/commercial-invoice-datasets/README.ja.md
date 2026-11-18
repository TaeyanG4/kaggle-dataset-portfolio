# 商用利用可能な請求書・物流データセットへのリンク

[English](README.md) | [한국어](README.ko.md) | **日本語** | [简体中文](README.zh-CN.md)

**ラベルがあり、記載した範囲で商用利用が明示的に許可されている14のデータセット系列**をまとめました。確認日は**2026-11-18**です。このディレクトリには公式配布元へのリンクと説明情報のみを掲載しています。各データには配布元の利用条件が適用され、商用モデルでの利用と元文書の再配布は別々の許可として扱います。

[詳細カタログ（JSON）](datasets.json) · [ポートフォリオ](../../README.ja.md)

## 公式配布元

件数は配布元の公開版の規模であり、このリポジトリに保存されているファイル数ではありません。規模の異なる版、レンダリング、スキャン画質の変種は同じ系列にまとめています。

| データセット／公式配布元 | 配布元の規模 | 利用できるラベル | 商用利用ライセンス／根拠 |
|---|---|---|---|
| [AI Hub OCR — Finance & Logistics](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71301) | 実際の物流書類：CI 26,044、PL 27,388、B/L 26,541、C/O 11,137 | OCRポリゴンと文字起こし；品目フィールドと行の対応を示す正解は未確認 | [AI Hubの利用条件](https://aihub.or.kr/aihubnews/faq/list.do) |
| [Company Documents v2](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2) | 合成PDF 353,580件、うち請求書48,158件；架空の企業60社 | ヘッダーとitems[] JSON；フィールド・単語の座標 | [Apache-2.0；元データのMIT/BSD表示](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2/blob/main/README.md) |
| [Invoice Extraction Benchmark v1 — DrewKraken](https://github.com/DrewKraken/invoice-extraction-benchmark) | 合成文書181件／220ページ；運賃関連文書16件 | ヘッダーとlines[]の正解 | [データ：CC BY 4.0；コード：MIT](https://github.com/DrewKraken/invoice-extraction-benchmark/blob/main/DATA_LICENSE) |
| [Shopify Invoice Test Pack — SalorWorks](https://github.com/SalorWorks/shopify-invoice-test-pack) | 合成シナリオ15件 | PDF/PNG＋expected.json；品目、運賃、関税、割引 | [CC BY 4.0](https://github.com/SalorWorks/shopify-invoice-test-pack/blob/main/LICENSE) |
| [InvoiceOCR-Synth](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic) | 基本文書938件／画質を変えた画像2,814件 | 32フィールドとline_items[]；数量、価格、税額 | [データ：CC BY 4.0；生成コード：MIT](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic/blob/main/README.md) |
| [KatanaML invoices-donut-data-v1](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1) | 分割内訳の合計501件：train 425／test 26／validation 50；カードには500件と記載 | 画像＋ground_truth.gt_parse.items | [加工部分：MIT＋元文書：CC BY 4.0](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1/blob/main/README.md) |
| [Sinabis synthetic PDF family](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf) · [10K](https://huggingface.co/datasets/sinabis-group/sinabis-10k-synthetic-pdf) | 1M版：PDF 1,006,000件；請求書281,680／運賃30,180／梱包20,120 | メタデータ・ヘッダー項目・テキスト；品目行の正解は未確認 | [CC BY 4.0](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf/blob/main/README.md) |
| [ExtractBench Pro — synthetic subset only](https://huggingface.co/datasets/llamaindex/ExtractBenchPro) | 合成文書100件；複数の文書種類を含む | JSONスキーマと期待出力；該当する文書では繰り返し配列 | [Apache-2.0](https://github.com/run-llama/ExtractBench) |
| [FATURA2](https://zenodo.org/records/10371464) | 異なる合成請求書10,000件／テンプレート50種類 | ヘッダー項目、テキスト・bbox、表全体のTABLE領域 | [データセット：CC BY 4.0](https://zenodo.org/records/10371464) |
| [MIDD](https://zenodo.org/records/5113009) | 元となる請求書630件／レイアウト4種類；公開版はIOBテキスト | ヘッダー中心のNERラベル11種類 | [CC BY 4.0](https://zenodo.org/records/5113009) |
| [InvoicesReceiptsPT](https://zenodo.org/records/6371710) · [個人用](https://zenodo.org/records/7213544) | 文書1,003件：事業用813＋個人用190 | ポルトガル語の請求書・レシートに対するヘッダー8項目 | [Zenodo原本のCC BY 4.0](https://zenodo.org/records/6371710) |
| [jngb-labs/InvoiceBenchmark](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark) | 合成請求書200件 | 税額、小計、割引、合計、意図的な誤りの正解 | [MIT](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark/blob/main/README.md) |
| [Invoice Parsing — Mendeley](https://data.mendeley.com/datasets/dcbshwmfct/1) | 請求書800件を基にしたと説明；公開版はOCR後処理用ファイル | 入力テキストとGeminiが生成した構造化出力 | [CC BY 4.0](https://data.mendeley.com/datasets/dcbshwmfct/1) |
| [CORD v2](https://huggingface.co/datasets/naver-clova-ix/cord-v2) | 公開レシート1,000件：train 800／validation 100／test 100 | テキスト・bbox、意味フィールド、メニュー／品目の行グループ、gt_parse | [CC BY 4.0](https://github.com/clovaai/cord) |

## 商用利用の条件

- **CC BY 4.0：** 著作者と出典を表示し、ライセンスへのリンクを提供し、関連する表示を保持して、変更内容を明記します。[公式ライセンス](https://creativecommons.org/licenses/by/4.0/)を参照してください。
- **MIT / Apache-2.0：** 適用される著作権・ライセンス表示を保持します。Apacheでは関連するNOTICEと変更の表示も必要です。Katanaは加工部分のライセンスに加えて、Mendeley原本のCC BY条件も保持してください。Company Documentsには元データのMIT/BSD表示もあります。
- **AI Hub：** [公式FAQ](https://aihub.or.kr/aihubnews/faq/list.do)に従って出典を表示することで、AIモデル、サービス、研究成果を商用利用できます。通常の利用条件では、元データおよび単純加工したデータの再配布は認められていません。申請資格と承認が必要であり、[利用方針](https://aihub.or.kr/intrcn/guid/usagepolicy.do)により国外での利用・国外への移転には別途合意が必要です。
- ExtractBenchは**合成文書のPro版のみ**を掲載しています。InvoicesReceiptsPTとFATURA2については、表でリンクしたファイルに適用されるZenodo原本のデータセットライセンスを基準とします。論文や再パッケージ版のカードには異なる条件が記載されている場合があります。

JSONには各項目のライセンスの根拠、帰属表示、許可された範囲と条件を記録しています。これは記載した版・範囲について公開資料に基づく判断であり、考え得るすべての第三者の権利を無条件に確認・保証するものではありません。新しい版を採用する場合や利用方法を変更する場合は、リンク先の条件を確認してください。

## 複数の取引先に対応するための選び方

品目行の抽出では、構造化された品目ラベルを備える**Company Documents v2、Drewのベンチマーク、Shopify Test Pack、InvoiceOCR-Synth、KatanaML**をまず比較できます。**AI Hub**は実際の通関・物流OCRに直接関係しますが、OCRラベルがあるだけでは、品目フィールドと行の対応を示す正解があるとはいえません。**CORD**は品目のグループ化を補う資料として利用できますが、対象分野は小売レシートです。

これはラベル構造に基づく用途の提案であり、測定した精度の順位ではありません。学習に使っていない取引先とレイアウトで評価し、同じ基本文書のレンダリングや画質の変種はすべて同じデータ分割に配置してください。どの公開データも、単独で新規取引先100～200社への性能を証明するものではありません。

## 対象範囲とラベルに関する注意点

- **AI Hub OCR — Finance & Logistics：** 物流の詳細表では合計107,918画像、概要では107,919画像と記載されています。金融文書50,000画像は別枠です。OCRラベルを意味フィールドや品目行の正解と解釈しないでください。申請は韓国籍の人に限られます。
- **Company Documents v2：** invoice、packing slip、shipping order、purchase orderのサブセットを含みます。ページ数や画質劣化版を独立した取引件数に加算しないでください。
- **Invoice Extraction Benchmark v1 — DrewKraken：** 運賃関連の例には通関手数料のケースも含まれます。小規模な機能評価に役立ちますが、実際の取引先の多様性を広く代表する標本ではありません。
- **Shopify Invoice Test Pack — SalorWorks：** ケース単位の梱包、無償品目、英語・アラビア語文書などの例外的なケースを含みます。同じシナリオのPDFとPNGは同じ標本です。
- **InvoiceOCR-Synth：** 6種類のテンプレートを用いた複数種類の合成業務文書です。clean/faded/bad_scan画像は同じ元レコードを共有するため、各基本文書を異なる評価分割にまたがって配置しないでください。
- **KatanaML invoices-donut-data-v1：** 加工部分のライセンスは元文書のライセンス条件を解除しません。公開カードの説明と分割内訳の件数が一致していません。
- **Sinabis synthetic PDF family：** 1K/10K/100K/1Mの版を含みます。各版の件数を独立した文書数として合算しないでください。PDFアーカイブとメタデータのParquetは役割が異なります。
- **ExtractBench Pro — synthetic subset only：** 100件すべてが請求書というわけではありません。別の基本版には実際の公開文書が含まれ、このカタログの確認対象範囲から除外しています。
- **FATURA2：** 表領域の注釈は、品目・セル単位の正解ではありません。白背景と色付き背景は変種です。論文とデータセットのライセンスは区別してください。
- **MIDD：** 公開IOB.rarには元の請求書画像や、品目フィールドと行の対応を示す正解は含まれていません。
- **InvoicesReceiptsPT：** 2つの原本配布版をリンクしています。ヘッダーのラベルであり、完全な品目行の正解は含まれていません。
- **jngb-labs/InvoiceBenchmark：** 金額検証のベンチマークとして扱うのが適切です。品目行の抽出ラベルがすべて揃っているという意味ではありません。
- **Invoice Parsing — Mendeley：** 確認した公開ルートファイルはXLSX 2個、JSON 1個、TXT 1個で、画像は添付されていません。機械生成の出力を、人が検証した正解とはみなせません。
- **CORD v2：** 小売レシートは関連する補助分野であり、通関用請求書ではありません。対象は公開された1,000文書のサブセットで、研究で使用されたコーパス全体ではありません。

## 選定の範囲

非商用に限定されたデータセットと、商用利用の許可を確認できていない配布元はこの一覧から除外しています。Kaggleの「High Quality Invoice Images for OCR」は、表示されているODbL/DbCL自体は商用利用を認めていますが、今回の調査では含まれる請求書原本の出所と権利の根拠を十分に確認できなかったため掲載していません。これは慎重な選定判断であり、そのデータが必ず違法または非商用であるという主張ではありません。

このディレクトリでは、元の請求書、画像、PDF、データアーカイブ、ダウンロードスクリプトを公開していません。データの規模やラベルの品質は実運用の精度を示す指標ではありません。このカタログは確認した公開資料を選定したもので、インターネット上のすべてのデータセットを網羅したという意味ではありません。

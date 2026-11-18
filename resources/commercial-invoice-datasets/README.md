# Commercial invoice and logistics dataset links

**English** | [한국어](README.ko.md) | [日本語](README.ja.md) | [简体中文](README.zh-CN.md)

**14 dataset families** with labels and explicit commercial-use permission for the stated scope, reviewed **2026-11-18**. This directory contains official source links and editorial metadata only. Each source retains its own terms; commercial model use and redistribution of source documents are separate permissions.

[Detailed catalogue (JSON)](datasets.json) · [Portfolio](../../README.md)

## Official sources

Counts describe the source release, not files hosted in this repository. Related sizes, renderings and scan-quality variants are grouped into one family.

| Dataset / official source | Source scale | Available labels | Commercial-use license / evidence |
|---|---|---|---|
| [AI Hub OCR — Finance & Logistics](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71301) | Real logistics documents; CI 26,044, PL 27,388, B/L 26,541, C/O 11,137 | OCR polygons and transcription; linked line-item gold unverified | [AI Hub terms](https://aihub.or.kr/aihubnews/faq/list.do) |
| [Company Documents v2](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2) | 353,580 synthetic PDFs; 48,158 invoices; 60 fictional companies | Header and items[] JSON; field/word coordinates | [Apache-2.0; MIT/BSD seed notices](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2/blob/main/README.md) |
| [Invoice Extraction Benchmark v1 — DrewKraken](https://github.com/DrewKraken/invoice-extraction-benchmark) | 181 synthetic documents / 220 pages; 16 freight documents | Header and lines[] ground truth | [CC BY 4.0 data; MIT code](https://github.com/DrewKraken/invoice-extraction-benchmark/blob/main/DATA_LICENSE) |
| [Shopify Invoice Test Pack — SalorWorks](https://github.com/SalorWorks/shopify-invoice-test-pack) | 15 synthetic scenarios | PDF/PNG + expected.json; items, freight, duty, discounts | [CC BY 4.0](https://github.com/SalorWorks/shopify-invoice-test-pack/blob/main/LICENSE) |
| [InvoiceOCR-Synth](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic) | 938 base documents / 2,814 quality-variant images | 32 fields and line_items[]; quantities, prices, taxes | [CC BY 4.0 data; MIT generation code](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic/blob/main/README.md) |
| [KatanaML invoices-donut-data-v1](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1) | 501 split records: train 425 / test 26 / validation 50; card says 500 | Images + ground_truth.gt_parse.items | [MIT processing + CC BY 4.0 source documents](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1/blob/main/README.md) |
| [Sinabis synthetic PDF family](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf) · [10K](https://huggingface.co/datasets/sinabis-group/sinabis-10k-synthetic-pdf) | 1M edition: 1,006,000 PDFs; invoices 281,680 / freight 30,180 / packing 20,120 | Metadata/header fields and text; line-item gold unverified | [CC BY 4.0](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf/blob/main/README.md) |
| [ExtractBench Pro — synthetic subset only](https://huggingface.co/datasets/llamaindex/ExtractBenchPro) | 100 synthetic documents; mixed document types | JSON schemas and expected outputs; repeated arrays where applicable | [Apache-2.0](https://github.com/run-llama/ExtractBench) |
| [FATURA2](https://zenodo.org/records/10371464) | 10,000 unique synthetic invoices / 50 templates | Header fields, text/bboxes and whole-TABLE regions | [CC BY 4.0 dataset](https://zenodo.org/records/10371464) |
| [MIDD](https://zenodo.org/records/5113009) | 630 source invoices / 4 layouts; public release is IOB text | 11 header-oriented NER labels | [CC BY 4.0](https://zenodo.org/records/5113009) |
| [InvoicesReceiptsPT](https://zenodo.org/records/6371710) · [personal](https://zenodo.org/records/7213544) | 1,003 documents: business 813 + personal 190 | Eight header fields; Portuguese invoices/receipts | [CC BY 4.0 original Zenodo records](https://zenodo.org/records/6371710) |
| [jngb-labs/InvoiceBenchmark](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark) | 200 synthetic invoices | Tax, subtotal, discount, total and intentional-error ground truth | [MIT](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark/blob/main/README.md) |
| [Invoice Parsing — Mendeley](https://data.mendeley.com/datasets/dcbshwmfct/1) | Described as based on 800 invoices; public release has post-OCR files | Input text and Gemini-generated structured output | [CC BY 4.0](https://data.mendeley.com/datasets/dcbshwmfct/1) |
| [CORD v2](https://huggingface.co/datasets/naver-clova-ix/cord-v2) | 1,000 public receipts: train 800 / validation 100 / test 100 | Text/bboxes, semantic fields, grouped menu/item rows and gt_parse | [CC BY 4.0](https://github.com/clovaai/cord) |

## Commercial-use conditions

- **CC BY 4.0:** credit the creators and source, provide the license link, preserve relevant notices and indicate changes. See the [official license](https://creativecommons.org/licenses/by/4.0/).
- **MIT / Apache-2.0:** retain the applicable copyright/license notices; Apache also requires relevant NOTICE and modification notices. For Katana, retain the original Mendeley CC BY conditions as well as the processing license. Company Documents also has MIT/BSD seed-source notices.
- **AI Hub:** commercial AI models, services and research results are permitted with attribution under the [FAQ](https://aihub.or.kr/aihubnews/faq/list.do). Raw or simply processed data cannot be redistributed under the standard terms. Application eligibility and approval apply; overseas use or transfer requires separate agreement under the [usage policy](https://aihub.or.kr/intrcn/guid/usagepolicy.do).
- The **Pro synthetic release only** is included for ExtractBench. For InvoicesReceiptsPT and FATURA2, the original Zenodo dataset license is authoritative for the listed files. A paper or repackaged card may carry different terms.

The JSON records each entry’s license evidence, credit, permitted scope and conditions. These are source-based findings for the listed versions/scopes, not an unconditional clearance of every possible third-party right. Check the linked terms when adopting a new version or changing how the data will be used.

## Choosing data for multiple suppliers

For line-item extraction, start by comparing **Company Documents v2, Drew’s benchmark, Shopify Test Pack, InvoiceOCR-Synth and KatanaML**. They expose structured item labels. **AI Hub** is directly relevant to real customs/logistics OCR, but its OCR labels do not establish linked item-field gold. **CORD** can supplement item grouping, while remaining a retail-receipt domain.

This is a task-fit recommendation from the label structure, not a measured accuracy ranking. Evaluate on suppliers and layouts held out from training; keep all renderings and quality variants of the same base document in the same split. None of these sources establishes performance on 100–200 new suppliers by itself.

## Scope and label caveats

- **AI Hub OCR — Finance & Logistics:** The detailed logistics table totals 107,918 images; the overview says 107,919. Financial documents are a separate 50,000 images. Do not treat OCR labels as semantic item fields. Applications are limited to Korean nationals.
- **Company Documents v2:** Includes invoice, packing slip, shipping order and purchase order subsets. Page counts and degraded variants are not additional independent transactions.
- **Invoice Extraction Benchmark v1 — DrewKraken:** Freight examples include customs-clearing cases. A useful small benchmark; not a broad sample of real suppliers.
- **Shopify Invoice Test Pack — SalorWorks:** Edge cases include case packs, free-of-charge items and English/Arabic documents. PDF and PNG of one scenario are the same example.
- **InvoiceOCR-Synth:** Synthetic business-document mix with six templates. Clean/faded/bad_scan images share underlying records; keep each base document in one evaluation split.
- **KatanaML invoices-donut-data-v1:** The processing license does not remove the original-document license. The published card and split count disagree.
- **Sinabis synthetic PDF family:** Includes 1K/10K/100K/1M variants. Do not add variant counts as unique documents. PDF archives and metadata Parquet serve different purposes.
- **ExtractBench Pro — synthetic subset only:** Not 100 invoices. The separate base release contains real public documents and is outside this catalogue’s approved scope.
- **FATURA2:** A table-region annotation is not item/cell-level gold. White/colored backgrounds are variants; the paper’s license is distinct from the dataset license.
- **MIDD:** The public IOB.rar does not provide the original invoice images or linked item rows.
- **InvoicesReceiptsPT:** Two original releases are linked. Header labels do not include complete item-row gold.
- **jngb-labs/InvoiceBenchmark:** Best treated as an amount-validation benchmark, not a claim of complete line-item extraction labels.
- **Invoice Parsing — Mendeley:** Public root files are two XLSX, one JSON and one TXT; no images were attached. Machine-generated outputs are not verified human gold.
- **CORD v2:** Retail receipts are an adjacent domain, not customs invoices. This entry covers the public 1,000-document subset, not the full research corpus.

## Selection boundary

Noncommercial-only datasets and sources with unresolved commercial permissions are outside this list. Kaggle “High Quality Invoice Images for OCR” was not included: its declared ODbL/DbCL terms allow commercial use, but the underlying invoice-document provenance was not sufficiently established in this review. This is a conservative inclusion decision, not a claim that the dataset is necessarily unlawful or noncommercial.

No original invoices, images, PDFs, data archives or downloader scripts are published in this directory. Dataset size and label quality are not measures of production accuracy. This catalogue reflects the sources reviewed, not a claim that every dataset on the internet has been found.

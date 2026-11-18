# 상업 이용 가능한 인보이스·물류 데이터 링크

[English](README.md) | **한국어** | [日本語](README.ja.md) | [简体中文](README.zh-CN.md)

**라벨이 있고, 명시한 범위에서 상업 이용이 허용되는 14개 데이터셋 계열**을 정리했습니다. 확인일은 **2026-11-18**입니다. 이 폴더에는 공식 출처 링크와 설명만 게시합니다. 데이터마다 원본의 이용 조건이 적용되며, 상업용 모델·서비스 활용 허용과 원본 문서 재배포 허용은 별도로 구분합니다.

[상세 목록(JSON)](datasets.json) · [포트폴리오](../../README.ko.md)

## 공식 데이터 링크

수량은 원본 배포의 규모입니다. 이 저장소에 해당 데이터를 보관한다는 뜻은 아닙니다. 크기·렌더링·스캔 품질 변형은 같은 데이터셋 계열로 묶었습니다.

| 데이터셋 / 공식 링크 | 원본 규모 | 제공 라벨 | 상업 이용 라이선스 / 근거 |
|---|---|---|---|
| [AI Hub OCR — Finance & Logistics](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71301) | 실제 물류 문서: CI 26,044 / PL 27,388 / B/L 26,541 / C/O 11,137 | OCR 폴리곤·전사; 품목행 연결 정답 미확인 | [AI Hub terms](https://aihub.or.kr/aihubnews/faq/list.do) |
| [Company Documents v2](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2) | 합성 PDF 353,580개 중 인보이스 48,158개; 가상 회사 60곳 | 헤더·items[] JSON, 필드·단어 좌표 | [Apache-2.0; MIT/BSD seed notices](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2/blob/main/README.md) |
| [Invoice Extraction Benchmark v1 — DrewKraken](https://github.com/DrewKraken/invoice-extraction-benchmark) | 합성 문서 181개 / 220페이지; freight 문서 16개 | 헤더·lines[] 품목행 정답 | [CC BY 4.0 data; MIT code](https://github.com/DrewKraken/invoice-extraction-benchmark/blob/main/DATA_LICENSE) |
| [Shopify Invoice Test Pack — SalorWorks](https://github.com/SalorWorks/shopify-invoice-test-pack) | 합성 시나리오 15개 | PDF/PNG + expected.json; 품목·운임·관세·할인 | [CC BY 4.0](https://github.com/SalorWorks/shopify-invoice-test-pack/blob/main/LICENSE) |
| [InvoiceOCR-Synth](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic) | 기본 문서 938개 / 품질 변형 이미지 2,814개 | 32개 필드·line_items[]; 수량·단가·세금 | [CC BY 4.0 data; MIT generation code](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic/blob/main/README.md) |
| [KatanaML invoices-donut-data-v1](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1) | 분할 합계 501건: train 425 / test 26 / validation 50; 카드 설명 500건 | 이미지 + ground_truth.gt_parse.items | [MIT processing + CC BY 4.0 source documents](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1/blob/main/README.md) |
| [Sinabis synthetic PDF family](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf) · [10K](https://huggingface.co/datasets/sinabis-group/sinabis-10k-synthetic-pdf) | 1M판: PDF 1,006,000개; 인보이스 281,680 / 운임 30,180 / 포장 20,120 | 메타데이터·헤더·텍스트; 품목행 정답 미확인 | [CC BY 4.0](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf/blob/main/README.md) |
| [ExtractBench Pro — synthetic subset only](https://huggingface.co/datasets/llamaindex/ExtractBenchPro) | 합성 문서 100개; 여러 문서 유형 혼합 | JSON 스키마·expected output; 문서에 따라 반복 배열 | [Apache-2.0](https://github.com/run-llama/ExtractBench) |
| [FATURA2](https://zenodo.org/records/10371464) | 고유 합성 인보이스 10,000개 / 50개 템플릿 | 헤더·텍스트·bbox·전체 TABLE 영역 | [CC BY 4.0 dataset](https://zenodo.org/records/10371464) |
| [MIDD](https://zenodo.org/records/5113009) | 원천 인보이스 630개 / 4개 레이아웃; 공개본은 IOB 텍스트 | 헤더 중심 NER 라벨 11개 | [CC BY 4.0](https://zenodo.org/records/5113009) |
| [InvoicesReceiptsPT](https://zenodo.org/records/6371710) · [개인용](https://zenodo.org/records/7213544) | 문서 1,003개: 사업용 813 + 개인용 190 | 포르투갈어 인보이스·영수증의 헤더 필드 8개 | [CC BY 4.0 original Zenodo records](https://zenodo.org/records/6371710) |
| [jngb-labs/InvoiceBenchmark](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark) | 합성 인보이스 200개 | 세액·소계·할인·합계·의도적 오류 정답 | [MIT](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark/blob/main/README.md) |
| [Invoice Parsing — Mendeley](https://data.mendeley.com/datasets/dcbshwmfct/1) | 800개 인보이스 기반이라고 설명; 공개본은 OCR 후처리 파일 | 입력 텍스트와 Gemini 생성 구조화 출력 | [CC BY 4.0](https://data.mendeley.com/datasets/dcbshwmfct/1) |
| [CORD v2](https://huggingface.co/datasets/naver-clova-ix/cord-v2) | 공개 영수증 1,000개: train 800 / validation 100 / test 100 | 텍스트·bbox·의미 필드·메뉴/품목행 그룹·gt_parse | [CC BY 4.0](https://github.com/clovaai/cord) |

## 상업 이용 조건

- **CC BY 4.0:** 저작자·원본 출처·라이선스 링크와 관련 고지를 보존하고 변경 사실을 표시합니다. [공식 라이선스](https://creativecommons.org/licenses/by/4.0/)를 참고하세요.
- **MIT / Apache-2.0:** 해당 저작권·라이선스 고지를 보존합니다. Apache는 관련 NOTICE와 변경 고지도 필요합니다. Katana는 가공본 라이선스와 함께 Mendeley 원본의 CC BY 조건을 준수하고, Company Documents는 seed 데이터의 MIT/BSD 고지도 보존합니다.
- **AI Hub:** [공식 FAQ](https://aihub.or.kr/aihubnews/faq/list.do)에 따라 출처를 표시하고 AI 모델·서비스·연구 결과물을 상업 활용할 수 있습니다. 일반 약관상 원본·단순 가공 데이터 재배포는 금지됩니다. 신청 자격·승인이 필요하며 [이용정책](https://aihub.or.kr/intrcn/guid/usagepolicy.do)에 따라 국외 이용·반출은 별도 합의가 필요합니다.
- **ExtractBench는 합성 Pro 판본만** 포함했습니다. InvoicesReceiptsPT와 FATURA2는 표에 연결한 원본 Zenodo의 데이터 라이선스를 기준으로 합니다. 논문이나 재포장 카드의 라이선스와 다를 수 있습니다.

JSON에는 항목별 라이선스 근거, 출처 표시, 허용 범위와 조건을 기록했습니다. 위 판단은 명시된 판본·범위의 공개 근거에 따른 것으로, 모든 제삼자 권리를 무조건 보증한다는 뜻은 아닙니다. 새 버전이나 다른 이용 방식에 적용할 때 원문 조건을 확인하세요.

## 여러 거래처의 인보이스를 처리할 때

품목행 추출용으로는 구조화된 품목 라벨이 있는 **Company Documents v2, Drew 벤치마크, Shopify Test Pack, InvoiceOCR-Synth, KatanaML**을 먼저 비교할 수 있습니다. **AI Hub**는 실제 통관·물류 OCR와 직접 관련되지만, OCR 라벨만으로 품목 필드와 행 연결 정답이 확보되는 것은 아닙니다. **CORD**는 품목 그룹 학습을 보완할 수 있는 소매 영수증 자료입니다.

이는 라벨 구조를 기준으로 한 용도 제안이며, 측정한 정확도 순위가 아닙니다. 학습에 쓰지 않은 거래처·양식으로 평가하고 동일 원문의 렌더링·품질 변형은 같은 분할에 배치하세요. 어느 공개 데이터셋도 단독으로 신규 거래처 100~200곳에서의 성능을 입증하지는 않습니다.

## 범위와 라벨 해석

- **AI Hub OCR — Finance & Logistics:** 물류 상세표 합계 107,918장과 개요 107,919장에 1장 차이가 있음. 금융 50,000장은 별도. OCR 라벨을 의미 필드·품목행 정답으로 해석하지 않음. 내국인 신청 제한.
- **Company Documents v2:** 인보이스·packing slip·shipping order·purchase order 하위셋 포함. 페이지 수·훼손 변형을 독립 거래 수로 더하지 않음.
- **Invoice Extraction Benchmark v1 — DrewKraken:** 운임 자료에 통관 수수료 사례 포함. 소규모 기능 평가에 적합하며 실제 거래처 다양성을 대표하지 않음.
- **Shopify Invoice Test Pack — SalorWorks:** case pack·무상 품목·영어/아랍어 문서 등 예외 사례. 동일 시나리오의 PDF와 PNG는 같은 표본.
- **InvoiceOCR-Synth:** 6개 템플릿의 합성 업무 문서 혼합. clean/faded/bad_scan은 같은 원문 변형이므로 같은 기본 문서를 서로 다른 평가 분할에 넣지 않음.
- **KatanaML invoices-donut-data-v1:** 가공본 라이선스가 원본 문서 조건을 제거하지 않음. 카드 설명과 공개 분할 수가 불일치.
- **Sinabis synthetic PDF family:** 1K/10K/100K/1M 크기 변형은 독립 문서 수로 합산하지 않음. PDF와 메타데이터 Parquet를 구분.
- **ExtractBench Pro — synthetic subset only:** 100개 전부 인보이스가 아님. 실제 공개 문서가 포함된 별도 기본판은 이 목록의 확인 범위에서 제외.
- **FATURA2:** TABLE 영역 라벨은 품목·셀 단위 정답이 아님. 흰색·컬러 배경은 변형본. 논문과 데이터 라이선스를 구분.
- **MIDD:** 공개 IOB.rar에는 원본 이미지 및 연결된 품목행 정답이 제공되지 않음.
- **InvoicesReceiptsPT:** 원본 배포 2개를 연결. 헤더 라벨이며 전체 품목행 정답은 없음.
- **jngb-labs/InvoiceBenchmark:** 금액 검증 벤치마크로 활용. 전체 품목행 추출 정답이 완비된 것으로 해석하지 않음.
- **Invoice Parsing — Mendeley:** 확인한 공개 루트 파일은 XLSX 2개·JSON 1개·TXT 1개이며 이미지 미첨부. 기계 출력을 사람이 검수한 정답으로 간주하지 않음.
- **CORD v2:** 소매 영수증 보조 자료이며 통관 인보이스가 아님. 논문의 전체 코퍼스가 아닌 공개 1,000개 하위셋만 해당.

## 선정 범위

비상업 전용 자료와 상업 이용 권한을 확인하지 못한 자료는 목록에서 제외했습니다. Kaggle의 “High Quality Invoice Images for OCR”는 ODbL/DbCL 표기 자체는 상업 이용을 허용하지만, 이번 조사에서 인보이스 원문들의 출처·권리 근거를 충분히 확인하지 못해 포함하지 않았습니다. 이는 보수적인 선정 판단이며, 해당 자료가 반드시 위법하거나 비상업용이라는 뜻은 아닙니다.

이 폴더에는 원본 인보이스·이미지·PDF·데이터 압축파일·다운로드 스크립트를 게시하지 않습니다. 데이터 규모와 라벨 유무가 실무 정확도를 뜻하지는 않습니다. 이 목록은 확인한 공개 자료의 선별 결과이며, 인터넷의 모든 데이터셋을 빠짐없이 찾았다는 의미는 아닙니다.

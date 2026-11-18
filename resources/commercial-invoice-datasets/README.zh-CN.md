# 可商用的发票与物流数据集链接

[English](README.md) | [한국어](README.ko.md) | [日本語](README.ja.md) | **简体中文**

本目录整理了**14个带标签、且在所列范围内明确允许商业使用的数据集系列**，核查日期为**2026-11-18**。本目录仅发布官方来源链接及说明信息。各来源仍适用其自身条款；用于商业模型与再分发原始文档是两种不同的权限。

[详细目录（JSON）](datasets.json) · [项目集](../../README.zh-CN.md)

## 官方来源

数量描述的是来源发布版本的规模，并非本仓库存放的文件数量。不同规模版本、渲染形式及扫描画质变体归为同一数据集系列。

| 数据集／官方来源 | 来源规模 | 提供的标签 | 商业使用许可／依据 |
|---|---|---|---|
| [AI Hub OCR — Finance & Logistics](https://aihub.or.kr/aihubdata/data/view.do?dataSetSn=71301) | 真实物流文档：CI 26,044、PL 27,388、B/L 26,541、C/O 11,137 | OCR多边形与转写文本；品项字段与行关联的标准答案未确认 | [AI Hub使用条款](https://aihub.or.kr/aihubnews/faq/list.do) |
| [Company Documents v2](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2) | 353,580份合成PDF，其中发票48,158份；60家虚构公司 | 表头与items[] JSON；字段、词语坐标 | [Apache-2.0；源数据MIT/BSD声明](https://huggingface.co/datasets/AyoubChLin/Company-document-dataset-v2/blob/main/README.md) |
| [Invoice Extraction Benchmark v1 — DrewKraken](https://github.com/DrewKraken/invoice-extraction-benchmark) | 181份合成文档／220页；16份运费文档 | 表头与lines[]标准答案 | [数据：CC BY 4.0；代码：MIT](https://github.com/DrewKraken/invoice-extraction-benchmark/blob/main/DATA_LICENSE) |
| [Shopify Invoice Test Pack — SalorWorks](https://github.com/SalorWorks/shopify-invoice-test-pack) | 15个合成场景 | PDF/PNG＋expected.json；品项、运费、关税、折扣 | [CC BY 4.0](https://github.com/SalorWorks/shopify-invoice-test-pack/blob/main/LICENSE) |
| [InvoiceOCR-Synth](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic) | 938份基础文档／2,814张画质变体图像 | 32个字段与line_items[]；数量、价格、税额 | [数据：CC BY 4.0；生成代码：MIT](https://huggingface.co/datasets/alamgirqazi/invoice-ocr-synthetic/blob/main/README.md) |
| [KatanaML invoices-donut-data-v1](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1) | 划分合计501条：train 425／test 26／validation 50；数据卡标为500条 | 图像＋ground_truth.gt_parse.items | [加工部分：MIT＋原始文档：CC BY 4.0](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1/blob/main/README.md) |
| [Sinabis synthetic PDF family](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf) · [10K](https://huggingface.co/datasets/sinabis-group/sinabis-10k-synthetic-pdf) | 1M版：1,006,000份PDF；发票281,680／运费30,180／装箱20,120 | 元数据、表头字段与文本；品项行标准答案未确认 | [CC BY 4.0](https://huggingface.co/datasets/sinabis-group/sinabis-1m-synthetic-pdf/blob/main/README.md) |
| [ExtractBench Pro — synthetic subset only](https://huggingface.co/datasets/llamaindex/ExtractBenchPro) | 100份合成文档；混合多种文档类型 | JSON模式与预期输出；适用时包含重复数组 | [Apache-2.0](https://github.com/run-llama/ExtractBench) |
| [FATURA2](https://zenodo.org/records/10371464) | 10,000份不同的合成发票／50种模板 | 表头字段、文本／bbox及整张表的TABLE区域 | [数据集：CC BY 4.0](https://zenodo.org/records/10371464) |
| [MIDD](https://zenodo.org/records/5113009) | 来源为630份发票／4种版式；公开版本为IOB文本 | 11种以表头为主的NER标签 | [CC BY 4.0](https://zenodo.org/records/5113009) |
| [InvoicesReceiptsPT](https://zenodo.org/records/6371710) · [个人](https://zenodo.org/records/7213544) | 1,003份文档：企业813＋个人190 | 葡萄牙语发票／收据的8个表头字段 | [Zenodo原始发布：CC BY 4.0](https://zenodo.org/records/6371710) |
| [jngb-labs/InvoiceBenchmark](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark) | 200份合成发票 | 税额、小计、折扣、总额及故意引入错误的标准答案 | [MIT](https://huggingface.co/datasets/jngb-labs/InvoiceBenchmark/blob/main/README.md) |
| [Invoice Parsing — Mendeley](https://data.mendeley.com/datasets/dcbshwmfct/1) | 说明称基于800份发票；公开版本为OCR后处理文件 | 输入文本与Gemini生成的结构化输出 | [CC BY 4.0](https://data.mendeley.com/datasets/dcbshwmfct/1) |
| [CORD v2](https://huggingface.co/datasets/naver-clova-ix/cord-v2) | 1,000份公开收据：train 800／validation 100／test 100 | 文本／bbox、语义字段、菜单／品项行分组及gt_parse | [CC BY 4.0](https://github.com/clovaai/cord) |

## 商业使用条件

- **CC BY 4.0：** 注明创作者与原始来源，提供许可证链接，保留相关声明，并标明修改内容。参见[官方许可证](https://creativecommons.org/licenses/by/4.0/)。
- **MIT / Apache-2.0：** 保留适用的版权与许可声明；Apache还要求保留相关NOTICE及修改声明。Katana除加工部分的许可证外，也须保留Mendeley原始文档的CC BY条件。Company Documents还包含源数据的MIT/BSD声明。
- **AI Hub：** 根据[官方FAQ](https://aihub.or.kr/aihubnews/faq/list.do)，注明来源后可将AI模型、服务和研究成果用于商业用途。标准条款不允许再分发原始或仅经简单处理的数据。使用须符合申请资格并获得批准；根据[使用政策](https://aihub.or.kr/intrcn/guid/usagepolicy.do)，在韩国境外使用或向境外传输须另行达成协议。
- ExtractBench仅列入**合成文档Pro版本**。InvoicesReceiptsPT和FATURA2以表中所链接文件的Zenodo原始数据集许可证为准；论文或重新打包的数据卡可能采用不同条款。

JSON记录了各项的许可依据、署名、允许范围及条件。这些结论基于所列版本和范围的公开资料，并非对所有可能涉及的第三方权利作出无条件确认或保证。采用新版本或改变使用方式时，请核对链接中的原始条款。

## 面向多家交易伙伴的数据选择

针对品项行提取，可先比较提供结构化品项标签的**Company Documents v2、Drew基准、Shopify Test Pack、InvoiceOCR-Synth和KatanaML**。**AI Hub**与真实通关、物流OCR直接相关，但有OCR标签不代表已有品项字段及行关联的标准答案。**CORD**可补充品项分组训练，但其领域仍是零售收据。

这是依据标签结构提出的用途建议，并非实测准确率排名。应使用未参与训练的交易伙伴和版式进行评估，并将同一基础文档的所有渲染形式和画质变体放在同一数据划分中。任何单个公开来源都不能独自证明系统对100～200家新交易伙伴的表现。

## 范围与标签解读

- **AI Hub OCR — Finance & Logistics：** 物流明细表合计107,918张图像，概览则为107,919张。金融文档的50,000张图像另计。不要将OCR标签视为语义字段或品项行标准答案。申请仅限韩国国籍人士。
- **Company Documents v2：** 包含invoice、packing slip、shipping order、purchase order子集。不要将页数或画质劣化变体计为额外的独立交易。
- **Invoice Extraction Benchmark v1 — DrewKraken：** 运费样例包含通关手续费案例。适合小规模功能评估，并不广泛代表真实交易伙伴的多样性。
- **Shopify Invoice Test Pack — SalorWorks：** 包含整箱包装、免费品项、英语／阿拉伯语文档等边界案例。同一场景的PDF和PNG是同一个样本。
- **InvoiceOCR-Synth：** 使用6种模板生成的混合业务文档。clean/faded/bad_scan图像共享底层记录；同一基础文档应始终放在同一评估划分中。
- **KatanaML invoices-donut-data-v1：** 加工部分的许可证不会解除原始文档的许可条件。公开数据卡与划分记录总数不一致。
- **Sinabis synthetic PDF family：** 包含1K/10K/100K/1M版本。不要将不同版本的数量相加作为独立文档总数。PDF压缩包和元数据Parquet承担不同用途。
- **ExtractBench Pro — synthetic subset only：** 并非100份文档全部都是发票。另一个基础版本包含真实公开文档，不在本目录确认的范围内。
- **FATURA2：** 表格区域标注不是品项或单元格级标准答案。白色与彩色背景是变体；论文许可证与数据集许可证须区分。
- **MIDD：** 公开的IOB.rar不提供原始发票图像，也不提供品项字段与行关联的标准答案。
- **InvoicesReceiptsPT：** 链接指向两个原始发布版本。提供表头标签，不包含完整的品项行标准答案。
- **jngb-labs/InvoiceBenchmark：** 更适合作为金额校验基准，不应解读为已提供完整的品项行提取标签。
- **Invoice Parsing — Mendeley：** 已核查的公开根目录文件为2个XLSX、1个JSON和1个TXT，没有附带图像。机器生成输出不是经过人工验证的标准答案。
- **CORD v2：** 零售收据属于相关辅助领域，并非通关发票。本条目仅涵盖公开的1,000份文档子集，不是研究使用的完整语料库。

## 筛选范围

本列表不包含仅限非商业用途的数据集，以及商业使用权限尚未确认的来源。Kaggle的“High Quality Invoice Images for OCR”未被列入：其声明的ODbL/DbCL条款本身允许商业使用，但本次核查未能充分确认其中原始发票文档的来源与权利依据。这是审慎的筛选决定，并非断言该数据集必然违法或只能用于非商业用途。

本目录不发布原始发票、图像、PDF、数据压缩包或下载脚本。数据规模和标签质量不能代表实际业务准确率。本目录反映的是已核查的公开来源，并不表示已经找到了互联网上的所有数据集。

# 实例：GPT-1 科研全仿真

- 原论文：Radford, Narasimhan, Salimans, Sutskever, 2018, *Improving Language Understanding by Generative Pre-Training*
- 原文链接（本仓库按版权原则不转载原文）：https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf

> 本目录所有第一人称叙事均为基于公开材料的合理重构，不代表作者本人或 OpenAI 的真实经历、观点或言论。

## 文件

| 文件 | 内容 |
|---|---|
| S1.md – S6.md | 仿真成品（idea 诞生 → 文献 → 建模迭代 → 数据+实验 → 困难与转折 → 成文），原样保留，修订处以【修订注】标注 |
| S7.md | 隔离审稿（子代理实现会话隔离）+ rebuttal + 核查附注 |
| S8.md | 第三方核查：27 组对上 / 10 条幻觉（含 2 条 P0 事实级错误）/ 10 条覆盖度缺口 + 修订记录 |
| S9.md | 成稿：面向外行的第一人称五幕长文（正文 7,443 汉字，占 S1–S8 叙事正文的 61.7%）+ 章末注（20 余条重构点留痕）+ 附录《勘误与对照》+《档案 · S9》 |
| GPT-1_科研全仿真_完整版.pdf / .html | S1–S8 合订版（24 页） |
| GPT-1_S9_成稿.pdf / .html | S9 成稿独立成册（9 页） |

## 审计摘要

首轮仿真约 60 条断言逐条核查：**17% 存在 P0–P2 级问题，3.3%（2 条）与论文事实直接矛盾**。两条 P0：①S1 声称"全文未提 GLUE"（论文 §1/§4.2/Table 4 caption/脚注 1 均出现）；②S4 声称辅助语言建模目标"在小数据上正则效果比预期大"（Table 5 逐任务差值恰恰相反）。全部已回改并保留修订注。

本流程的独立发现：论文 §5 的两句概括（"helps on the NLI tasks" + "larger datasets benefit ... smaller do not"）在 RTE（全场最小数据集，却因辅助目标涨 1.6 分）上互相打架；隔离审稿人与 rebuttal 各自只引用了对己有利的一半。

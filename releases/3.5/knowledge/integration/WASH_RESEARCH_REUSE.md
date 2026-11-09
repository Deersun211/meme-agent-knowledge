# 刷量检测复用候选 — 2026-10-19

论文：Victor / Weintraud，2021，arXiv:2102.07001v1。已审阅方法与讨论小节，未全面审阅全文，未复现。适用对象为IDEX和EtherDelta订单簿交易；SCC候选与近零头寸匹配可作为研究思路，不是Solana AMM即插即用检测器。

作者仓库：https://github.com/friedhelmvictor/lob-dex-wash-trading-paper 。完整readme已读（blob74533b759fc46c41cefd0f79854332c231d0da50），执行代码/许可证未审计。文档描述Python预处理及R依赖，作者称全量需32GB RAM或足够swap；未在我们的环境测量。没有安装或合并代码。

数据：https://zenodo.org/records/4540223 ，DOI10.5281/zenodo.4540223，记录v1.0，2021-02-13发布。清单含EtherDeltaTrades.csv、IDEXTrades.csv、EtherDollarPrice.csv和token_decimals.json，总计约3.2GB。仅元信息已读，未下载、解码、校验或验证许可，不能称已接入可用样本。

下一步最小实验见E21：先免费本地合成正反例，保持套利/正常用户及共享池反例；许可确认后才考虑旧数据小样复现。Chainalysis公开方法可作AMM域对照，但不使用其付费工具、未公开标签或全市场估计。只有新时期Solana模拟对照才能讨论本项目收益。

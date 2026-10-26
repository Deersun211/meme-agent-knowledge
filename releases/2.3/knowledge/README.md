# MEME 新币交易知识库 v1.1

审阅日期：2026-10-14（Asia/Shanghai）。主要范围：Solana 新币、pump.fun、Raydium、Jupiter。其他链的权限和机制不能直接套用。

这是可复用的外部知识资料包，不是盈利策略成品。43条知识卡、21条来源、14个待运行实验、13类不应直接相信的断言、27个模型评估问题。尚无本项目实证的盈利优势；所有知识卡 profit_edge 均为 unvalidated。

## 从哪里开始

先读 GUIDE.md。通用模型可读取 GUIDE.md 与 core/knowledge_cards.jsonl；小上下文模型按问题检索少量知识卡，再加入 prompts/research_agent_zh.txt。模型需具备文件读取或由你的本地工具把文本传给它。并非任意软件都支持直接导入ZIP。

本包提供 Markdown、UTF-8 JSON/JSONL，不依赖 Groq、GMGN、付费API或指定模型。支持检索增强（RAG）与普通上下文使用；它不会自动改变模型权重，也不是已完成的微调训练集。微调可训练表达/流程，但不能代替证据更新或收益验证。

## 如何给 Agent 提速

知识机制审查 → 提出少量候选 → 历史回放/成本压力 → 样本外 → 影子前向模拟 → 保留或回滚。

机制卡可消除明显错误，研究观察可生成假设，原创方法卡约束实验。不得把论文的简化收益、关联现象、交易截图当作已实现策略优势。

此前1.0内容已用于GMGN Agent的知识上下文；本次1.1没有自动同步至你的本机，需通过程序支持的知识导入流程加载。integration/AGENT_PLAN.md保留通用接入规格。E01–E14均未执行。网页和论文审阅也不构成全部源码审计。

## 文件

| 文件 | 用途 |
|---|---|
| GUIDE.md | 中文阅读、辨伪与使用指南 |
| core/knowledge_cards.jsonl | 每行一个带证据和边界的知识卡 |
| evidence/source_registry.json | 原始链接、审阅状态与局限 |
| hypotheses/experiment_specs.jsonl | 可证伪实验模板；均未运行 |
| quarantine/unsupported_claims.jsonl | 误导性断言隔离区 |
| eval/cases.jsonl | 模型是否理解关键边界的问答评估 |
| integration/ | 接入流程和来源无关字段契约 |
| prompts/research_agent_zh.txt | 通用研究模型指令模板 |
| tools/retrieve.py | 零依赖关键词检索；不是语义向量检索 |
| tools/validate_kb.py | 结构、引用、实验状态和文件哈希检查 |
| UPDATE_PROTOCOL.md | 更新、纠错、升级与撤回规范 |

Windows 已装 Python 时：解压后在目录内执行 `python tools/validate_kb.py`。检索示例：`python tools/retrieve.py "聪明钱 净买入" --top 4`。返回检索卡可复制进模型上下文。不会调用付费服务或发送交易。

内容为原创摘要与研究设计，仅链接原始资料；不打包整篇论文、视频或帖子。工具代码可自由修改复用；对原始资料的许可仍以原作者规定为准。

当前包版本1.1；更新内容见CHANGELOG。原有知识ID保留，费用研究新增E13/E14均未执行。

当前版本：2.3（2026-10-26）。新增交易模拟—执行差异与状态新鲜度研究，E28未执行；以manifest及CHANGELOG为准。

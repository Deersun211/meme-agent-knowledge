# 现有 Agent 的接入规格（尚未实施）

1. 加载知识卡：只接受schema和引用校验通过的active卡。将证据层与收益验证层分开。
2. 数据适配：GMGN、公开链上记录或已保存文件统一到feature_contract.json。字段语义与时间不能靠模型猜；来源冲突保留双方与裁决记录。
3. 研究提案：模型用少量相关卡生成实验JSON。确定性校验器拒绝缺字段、未来数据、无成本、无对照、未授权实盘等提案。
4. 提速路径：已有历史数据上并行候选回放，统一净收益、回撤、尾部、容量和失败退出；不改候选全集以挑赢家。合成故障只测鲁棒性。
5. 晋级：锁定参数后做时间外测试及影子前向模拟。结果不足保持inconclusive。知识库的证据标签不得直接晋级交易规则。
6. 模拟部署与回滚：新规则记录版本、知识ID、数据集hash、成本版本和全试验清单。原规则并行保留，按预先定义的退化标准回滚。全程模拟。
7. 可见性：界面显示研究开关、实际研究状态、最近实验、知识版本、候选/已验证规则、模拟净收益和失败原因。下载包与知识卡不能替代这些运行状态。

建议实验报告字段：experiment_id、knowledge_ids、data_hash、code_version、rule_version、train_window、test_window、feature_availability、cost_model_version、trial_count、baseline_metrics、candidate_metrics、uncertainty、failure_cases、decision、limitations。

当前资料包只包含知识和接入规格；没有修改你的GMGN程序，也没有运行候选回测或模型调用。

# KAMCHIU｜广告算法工程师

约 3 年工作经验 · 香港科技大学硕士（EE）· 中山大学本科

工作方向包括 **生成式出价、oCPD 双目标优化与 Agent 工具集成**。公开研究聚焦一个问题：预测转化率发生偏移时，如何在预算 / CPA 约束下保留转化，并判断复杂模型是否值得引入。

## 从这里开始

| 想了解什么 | 推荐入口 |
| --- | --- |
| 研究问题、方案与运行方式 | [TrajectoryLab 中文介绍](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/README.zh-CN.md) |
| 提升是否成立、在哪些条件下成立 | [确认结果、对照与适用边界](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/docs/bidding-findings.md) |
| 生成模型怎么实现、为何没有直接带来更好决策 | [Flow 实现](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/src/trajectorylab/bidding_generative_learning.py) · [复核与机制诊断](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/docs/bidding-generative-findings.md) |

## 代表项目 · [TrajectoryLab](https://github.com/KAMCHIU-LAB/trajectory-lab)

基于公开 AuctionNet 构建的独立研究，重点包括：

- **拆开预测与控制**：在同一响应模型下比较出价规则，检查转化、预算消耗与 CPA 违约的取舍。
- **实现条件生成模型**：用 Flow Matching 联合采样不同候选动作的响应，比较分布决策、点预测和简单反馈。
- **建立证据链**：冻结比较方案，在新模拟市场按市场配对统计；保留失败实验、停止规则和来源哈希。

**局部确认结果**：pCVR 高估 50% 时，3 个冻结响应模型在 24 个新模拟市场相对冻结反馈基线，CPA 惩罚 score **+17.6%**、转化 **+8.4%**、CPA 违约频率 **−24.8 个百分点**。

以上是自定义固定对手模拟器中的场景结论。低估场景仍有不足；Flow 相对强对照的额外决策价值尚未确认。完整记录区分开发集发现与独立确认，不将模拟提升解释为线上收益。

## 其他工程实践

[Stock Monitor](https://github.com/KAMCHIU-LAB/Stock_Monitor)：多市场数据接入、数据质量检查、规则分析与结构化终端报告。作为数据处理和工程实现的补充作品，评分的适用范围见[数据质量说明](https://github.com/KAMCHIU-LAB/Stock_Monitor/blob/main/AUDIT.md)。

## 技术与交流

Python · PyTorch · SQL · Transformer · Flow Matching · RTB / oCPX · 仿真与实验设计

欢迎通过 [项目 Issue](https://github.com/KAMCHIU-LAB/trajectory-lab/issues) 交流出价建模、实验设计和复现问题。

公开研究使用公开来源与独立实现，不含雇主代码、业务数据或内部系统；方法来源、实验边界及 AI 编程辅助说明见项目文档。

# KAM｜广告算法工程师

关注 **生成式出价、离线强化学习与成本约束优化**。将响应建模、决策控制和效果评估拆开，用公开模拟实验检查方法在什么条件下有效。

## 代表项目 · [TrajectoryLab](https://github.com/KAMCHIU-LAB/trajectory-lab)

基于公开 AuctionNet 的独立研究：条件响应模型、预算 / CPA 控制、Flow Matching 联合响应生成，以及按市场配对的压力评测。

| 阅读入口 | 看什么 |
| --- | --- |
| [中文项目介绍](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/README.zh-CN.md) | 研究问题、系统分工、实现与实验流程 |
| [确认结果与适用边界](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/docs/bidding-findings.md) | 3 个冻结模型、24 个新模拟市场、4,320 条评估 |
| [生成式复核与机制诊断](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/docs/bidding-generative-findings.md) | 训练种子停止规则、强对照、低估场景与负结果 |
| [Flow 实现](https://github.com/KAMCHIU-LAB/trajectory-lab/blob/main/src/trajectorylab/bidding_generative_learning.py) | 历史条件联合响应采样，与独立控制器配合 |

**已确认的局部结果：**pCVR 高估 50% 时，固定响应模型相对冻结反馈的 CPA 惩罚 score **+17.6%**、转化 **+8.4%**、CPA 违约频率 **−24.8 个百分点**。结论条件于三个冻结检查点和自定义固定对手模拟器，不代表线上效果或全面领先。

**研究判断：**Flow 的分布拟合诊断与决策增量分开验收；第二训练种子未过全部业务门槛，生成式增量尚未确认。保留失败结果与证据哈希，避免把开发集改善写成独立确认。

## 技术方向

Python · PyTorch · TensorFlow · SQL · Transformer · 离线强化学习 · 条件生成模型 · RTB / oCPX · 成本约束优化 · 仿真与实验设计

公开仓库仅包含独立实现、公开来源与模拟实验，不含雇主代码、业务数据或内部系统。项目说明保留方法来源、实验边界和 AI 编程辅助披露。

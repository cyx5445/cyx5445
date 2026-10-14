# 褚宇翔 Yuxiang Chu

**LLM 与 AI Agent 算法研究 · 华东理工大学计算机科学与技术硕士**

我关注如何让大模型在复杂任务中可靠地获取证据、使用工具并持续推进任务。研究与实践围绕 **Agent 后训练、长程任务规划与记忆、生成偏好对齐，以及医疗场景的大模型应用** 展开。

[GitHub](https://github.com/cyx5445) · [Email](mailto:13758277604@163.com)

## 研究方向

- **Agent 后训练与泛化**：从真实执行轨迹诊断能力缺口，构建可执行、可校验的增广数据，研究 SFT 与 GRPO 训练。
- **长程 Agent 系统**：Planner–Executor、DAG 调度、动态重规划，以及患者状态和决策进度的记忆管理。
- **RAG 与偏好对齐**：面向下游生成质量的文档集合选择与排序，偏好数据构建及 SFT / DPO。
- **领域适配**：通过知识与任务两个维度组织训练课程，兼顾专业能力与通用能力。

## 论文与研究

| 工作 | 研究内容 | 状态与署名 |
| --- | --- | --- |
| **Balancing Knowledge Breadth and Task Depth for Effective Domain Adaptation Fine-Tuning** | 知识广度与任务深度协同的二维课程学习 | ACL 2026 · CCF-A · 第一作者 |
| **Rank4Gen: RAG-Preference-Aligned Document Set Selection and Ranking** | 生成器偏好驱动的 RAG 文档集合选择与排序；PRISM 数据构建与 SFT / DPO | EMNLP 2026 · CCF-B · 第一作者 |
| **PsychēChat: An Empathic Framework Focused on Emotion Shift Tracking and Safety Risk Analysis in Psychological Counseling** | 多轮情绪追踪、回应风险分析与多智能体协作 | EMNLP 2026 · CCF-B · 第二作者 |
| **RelDAPT: Relation-Diagnosis-Guided Adaptive Policy Training for Medical Tool-Use Agents** | 执行轨迹诊断驱动的自适应 Agent 训练，结合 SFT 与 GRPO | 2026 年 10 月 ARR 在审 · 第一作者 |

## 项目实践

### ZhongshanAgent 医疗决策智能体

**项目 Owner · 与中山医院合作**

面向多专科及 ICU 的多轮决策支持，负责核心架构与算法设计。通过 Planner–Executor 将任务组织为 DAG，结合执行反馈与病历更新修补计划；分层维护患者状态、决策进度与历史信息，支撑长程任务推进。设计领域路由、任务 Skill 和原子 Action 体系，接入循证检索与医学影像分析工具。

### RJ-DecisionEngine 互联网问诊决策引擎

**主要算法设计与实现 · 与仁济医院合作**

结合专家决策流程与大模型处理在线问诊。负责 JSON 决策树遍历、跨树跳转、条件判断策略路由及多轮状态衔接；通过事实提取、原文核查、知识筛选和摘要生成，减少错误向后续条件判断与回复生成传播。

### EMR 电子病历出院小结生成

**项目 Owner · 与瑞金医院、肿瘤医院合作**

负责可配置字段级规则链、按字段生成与格式校验，以及生成结果与原始病历的溯源匹配。组织抽取、推理、判断和摘要步骤，结合病历事实约束生成内容，为医生提供可核对、可编辑的出院小结。

项目代码暂不公开，以上展示个人职责和技术设计。

## 开源贡献

| 项目 | 具体贡献 | 状态与证据 |
| --- | --- | --- |
| **LlamaFactory** | 修复默认工具格式化器处理数字、布尔值及混合类型枚举时的 `TypeError`，新增 10 个回归组合；本地格式化测试 56 项通过 | [PR #10891](https://github.com/hiyouga/LlamaFactory/pull/10891) · 已提交，待审核 |

## 技术实践

**训练与评估**：SFT、LoRA、DPO、GRPO、课程学习、Agent 轨迹与证据评测。  
**Agent 与检索**：Planner–Executor、DAG、动态重规划、Memory、Skill、MCP、RAG。  
**工程工具**：Python、LlamaFactory、vLLM、Git、Docker。

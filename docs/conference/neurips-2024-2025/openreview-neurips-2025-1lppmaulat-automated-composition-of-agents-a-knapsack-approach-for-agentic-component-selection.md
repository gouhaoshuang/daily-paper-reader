---
title: "Automated Composition of Agents: A Knapsack Approach for Agentic Component Selection"
title_zh: 智能体的自动化组合：面向智能体组件选择的背包方法
authors: "Michelle Yuan, Khushbu Pahwa, Shuaichen Chang, Mustafa Devrim Kaba, Jiarong Jiang, Xiaofei Ma, Yi Zhang, MONICA SUNKARA"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=1LPPMAUlaT"
tags: ["query:eca"]
score: 5.0
evidence: 自动智能体组合框架
tldr: 现有智能体组合依赖静态语义检索，无法基于实时能力和成本进行有效选择。本文借鉴背包问题，提出自动化智能体组合框架，由作曲家智能体根据能力、成本和实时效用系统化地识别、选择和组合组件。实验表明该方法比静态检索更高效，为端云协同中动态编排AI代理提供了可落地的方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-1lppmaulat/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1377, \"height\": 472, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1lppmaulat/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1245, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1lppmaulat/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1441, \"height\": 1152, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1lppmaulat/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1439, \"height\": 575, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1515, \"height\": 1041, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 570, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1438, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 1004, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1457, \"height\": 1101, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1457, \"height\": 619, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1458, \"height\": 770, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1457, \"height\": 835, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1456, \"height\": 808, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1457, \"height\": 834, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1457, \"height\": 833, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1452, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1lppmaulat/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1458, \"height\": 830, \"label\": \"Table\"}]"
motivation: 智能体系统组合时，静态语义检索无法考虑实时能力和成本，导致选择低效。
method: 基于背包问题的框架，由作曲家智能体根据能力、成本和效用进行组件选择与组合。
result: 在多个任务上，组合质量优于静态语义检索方法，且成本更低。
conclusion: 背包启发式方法能高效解决动态环境中的智能体组合问题。
---

## Abstract
Designing effective agentic systems requires the seamless composition and integration of agents, tools, and models within dynamic and uncertain environments. Most existing methods rely on static, semantic retrieval approaches for tool or agent discovery. However, effective reuse and composition of existing components remain challenging due to incomplete capability descriptions and the limitations of retrieval methods. 
Component selection suffers because the decisions are not based on capability, cost, and real-time utility.
To address these challenges, we introduce a structured, automated framework for agentic system composition that is inspired by the knapsack problem. Our framework enables a composer agent to systematically identify, select, and assemble an optimal set of agentic components by jointly considering performance, budget constraints, and compatibility. By dynamically testing candidate components and modeling their utility in real-time, our approach streamlines the assembly of agentic systems and facilitates scalable reuse of resources. Empirical evaluation with Claude 3.5 Sonnet across five benchmarking datasets shows that our online-knapsack-based composer consistently lies on the Pareto frontier, achieving higher success rates at significantly lower component costs compared to our baselines. 
In the single-agent setup, the online knapsack composer shows a success rate improvement of up to 31.6\% in comparison to the retrieval baselines. 
In multi-agent systems, the online knapsack composer increases success rate from 37\% to 87\% when agents are selected from an agent inventory of 100+ agents. 
The substantial performance gap confirms the robust adaptability of our method across diverse domains and budget constraints.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：设计有效的智能体系统需要无缝组合智能体、工具和模型，但现有方法依赖静态语义检索来选择工具或智能体，忽略能力描述的不完整性、成本-效用权衡以及动态环境变化，导致组件选择低效。
- **核心问题**：如何自动从现有组件库中选出最优子集，在满足预算约束下最大化任务成功率？作者将这一问题形式化为**背包问题**，引入“作曲家智能体（composer agent）”进行实时能力测试和动态选择。

## 2. 论文提出的方法论

### 2.1 核心思想
- 将智能体组件（工具/子智能体）视为背包中的物品，每个组件有成本 \(c_i\) 和价值（对任务成功的贡献 \(p_\tau(S)\)），目标是在总成本不超过预算 \(B\) 下最大化成功率。
- 提出了**在线背包作曲家**：通过生成技能（skills）和测试查询（test queries），对候选组件进行实时沙箱评估，计算其价值-成本比，并利用 ZCL 在线背包算法动态决定是否选取。

### 2.2 关键技术细节
1. **技能生成**：根据任务描述，由 LLM 生成不超过6个技能，每个技能附带名称、描述、重要性权重和3个测试查询及参考计划。
2. **候选检索**：对每个技能，使用语义检索从库存中获取 Top-K 组件。
3. **沙箱评估**：对候选组件运行测试查询，由 LLM 判断组件是否“有帮助”（helpful）、“损坏”（broken）。若损坏则永久排除。
4. **在线背包算法（ZCL）**：
   - 设定价值-成本比的下界 \(L\) 和上界 \(U\)。
   - 动态阈值 \(\Psi = (U/e^L)^{z} \cdot L / e\)，其中 \(z\) 为已花费预算比例。
   - 仅当组件价值-成本比 \(\rho_i \geq \Psi\) 时才接受，并更新已覆盖技能集，避免重复。
5. **提示优化（可选）**：利用沙箱轨迹，通过 AvaTaR 方法优化智能体系统提示，进一步提升工具使用效率。

### 2.3 算法流程（文字描述）
- 输入：组件库存 \(A\)、任务描述 \(x\)、预算 \(B\)。
- 生成技能列表 \(M\)（含名称、描述、测试查询、重要性）。
- 对每个技能检索 Top-K 候选。
- 依次遍历候选组件，若未损坏且技能未覆盖且成本 ≤ 剩余预算，则执行沙箱评估，计算价值（仅来自未覆盖技能），若价值-成本比 ≥ 当前 ZCL 阈值，则选中该组件，更新已覆盖技能集和剩余预算。
- 返回所选组件集合。

## 3. 实验设计

### 3.1 数据集/场景
- **单智能体组合**：GAIA（通用AI助手）、SimpleQA（事实问答）、MedQA（医学考试问答）。
- **多智能体组合**：MAC 框架下的旅行（Travel）和抵押贷款（Mortgage）两个企业领域。
- **组件库存**：单智能体使用120个工具（来自 Langchain 和 ToolRet 数据集，含免费/付费API）；多智能体使用117个子智能体（原MAC的20个+合成生成的干扰智能体）。

### 3.2 基准方法（Baselines）
- **Identity**：使用全部组件（无筛选）。
- **Top-1 Retrieval**：对每个技能只取语义检索最匹配的一个组件。
- **Offline Knapsack**：基于语义相似度评分作为价值，用线性规划求解多选背包问题。
- **Online Knapsack**（本文方法）：使用 ZCL 算法动态选择。
- **Online Knapsack + OPT**：额外进行提示优化（AvaTaR）。

### 3.3 模型与设置
- 主要评估LLM：Claude 3.5 Sonnet（默认），也测试了 Claude 3.5 Haiku、Claude 3.7 Sonnet、Qwen 2.5 72B、Llama 3.3 70B、Llama 4 Maverick/Scout。
- 嵌入模型：BGE-Large-English。
- 预算设置：单智能体 $10 或 $30；多智能体 $3 或 $6（所有子智能体统一价格 $1）。
- 评估指标：成功率（Success Rate）和总成本（Budget Spent），同时绘制 Pareto 前沿。

## 4. 资源与算力

- **未明确说明**：论文未给出 GPU 型号、数量、训练时长等具体算力信息。实验主要调用外部 LLM API（Claude、Qwen、Llama等），沙箱评估和推理均在云上完成，但未披露计算节点配置。
- 仅提及每次沙箱耗时约10-30分钟（取决于预算），以及总运行时间记录在附录表格中（如 SimpleQA 平均每秒约11-17秒）。

## 5. 实验数量与充分性

- **实验组数丰富**：共涉及3个单智能体数据集 × 10+种方法（含不同预算和优化变体） + 2个多智能体数据集 × 6种方法；覆盖7种不同LLM（含多个版本）；对 SimpleQA 进行了3次独立运行（表12），标准差很小，证明结果稳定。
- **消融与对比**：比较了纯检索、离线背包、在线背包及其变体；多智能体实验中还验证了对抗干扰智能体时的鲁棒性；提示优化的消融（OPT）也做了。
- **充分性评价**：实验设计较为全面，数据集覆盖通用、事实性、医学、企业领域，方法对比公平（相同预算、相同评估流程）。但未与更复杂的组合策略（如基于 MDP 的强化学习）进行对比，也未测试组件间非加性交互（论文在问题定义中提及但未实验验证）。总体而言，实验在支撑主要结论方面是充分的。

## 6. 论文的主要结论与发现

- **在线背包作曲家始终位于 Pareto 前沿**：在相同或更低成本下，成功率显著高于检索和离线背包方法。
- **单智能体**：在线背包 + 提示优化（$30预算）在GAIA、SimpleQA、MedQA上成功率最高，比检索基线提升最多31.6%（SimpleQA）。
- **多智能体**：在线背包（$6预算）在旅行和抵押贷款上成功率从37%提升至87%，能有效避开干扰智能体。
- **提示优化进一步改善**：尤其在 SimpleQA 上效果明显，优化后的提示使工具调用更精准、错误恢复更强。
- **静态检索的局限性**：语义匹配无法反映真实工具能力，离线背包因依赖不可靠的描述而失效。
- **鲁棒性验证**：不同LLM（Claude、Qwen、Llama）均得到一致性结论。

## 7. 优点（方法或实验设计的亮点）

- **问题形式化创新**：将智能体组合转化为约束优化问题（背包问题），为系统性组件选择奠定理论框架。
- **实时效用评估**：通过沙箱测试动态衡量组件真实价值，克服静态描述的不可靠性。
- **算法高效可部署**：ZCL 在线算法具有理论竞争比（ln(U/L)+1），并加入早停、跳过已覆盖技能等优化，控制实际运行时间。
- **提示优化集成**：利用沙箱轨迹进行提示自适应，无需额外标注成本。
- **多维度实验验证**：涵盖单/多智能体、多个数据集、多种LLM、多次运行，结果稳健；Pareto前沿分析清晰展示成本-性能 trade-off。

## 8. 不足与局限

- **依赖清晰任务描述**：问题定义要求任务规范明确，对于模糊或探索性任务不适用（论文自身承认）。
- **组件间交互缺失**：当前方法独立评估每个组件，未考虑正/负协同效应（如工具冲突或互补），论文问题定义中提及但未实验处理。
- **沙箱测试耗时**：每次组合需10-30分钟，可能不适合实时性要求高的场景；未来需优化。
- **提示优化存在回归**：某些设置下（如 Haiku 的 SimpleQA）优化后性能反而下降，表明该方法不够稳健。
- **安全性局限**：未讨论恶意组件被选入系统的风险，需要额外的安全监控机制。
- **对比基线不够完整**：未与基于强化学习/图优化的动态选择方法（如 DyLAN、AgentPrune）进行直接对比，仅与简单基线和离线背包对比。
- **多智能体实验偏合成**：干扰智能体是人工构造的，真实场景的多样性可能更强；且子智能体成本统一为$1，忽略了实际成本差异。

（完）

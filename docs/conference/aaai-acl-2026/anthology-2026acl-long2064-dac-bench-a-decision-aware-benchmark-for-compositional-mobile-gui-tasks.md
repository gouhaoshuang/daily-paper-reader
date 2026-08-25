---
title: "DAC-Bench: A Decision-Aware Benchmark for Compositional Mobile GUI Tasks"
title_zh: DAC-Bench：面向组合式移动GUI任务的决策感知基准
authors: "Yuqing Zhang, Honghui Sheng, Xueyu Hu, Shengyu Zhang, Fei Wu"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.2064.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 面向组合式移动GUI任务、关注决策的评测基准
tldr: 现有移动GUI基准多聚焦短线性流程和步骤级准确率，对长程规划和分支决策缺乏洞察。提出DAC-Bench，一个面向决策的组合式任务基准，包含35个安卓和iOS应用上的830个回合、11345个动作步骤，任务涵盖序列、合取、条件与层级结构。并引入加权最长公共子序列以捕捉长度敏感进展与分支决策准确率。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1654, \"height\": 681, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1659, \"height\": 918, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 658, \"height\": 432, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1661, \"height\": 334, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 646, \"height\": 901, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2064/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1246, \"height\": 1732, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1649, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1645, \"height\": 745, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 803, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 809, \"height\": 493, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1393, \"height\": 2552, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1622, \"height\": 2320, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1621, \"height\": 2498, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1620, \"height\": 1256, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1490, \"height\": 1762, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2064/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1504, \"height\": 1824, \"label\": \"Table\"}]"
motivation: 现有基准难以评估长程规划和分支决策能力。
method: 构建包含830回合和多类结构任务的基准，并提出加权最长公共子序列评估指标。
result: 能够更全面地量化和分析移动GUI智能体的决策性能。
conclusion: 为长程、分支移动任务决策评估提供了重要工具。
---

## Abstract
Mobile GUI agents powered by LMMs can perceive screens and follow instructions, yet existing benchmarks largely target short, linear workflows and step-level accuracy, offering limited insight into long-horizon planning and decision-making under branching structures. We present DAC-Bench, a decision-aware benchmark with compositional tasks comprising 830 episodes and 11,345 action steps across 35 applications on Android and iOS. Tasks are organized into Sequential, Conjunctive, Conditional, and Hierarchical structures, reflecting real-world multi-step and branching interaction patterns. To complement standard step-level evaluation, we introduce weighted longest common subsequence to capture length-sensitive progress and decision accuracy for branch correctness. Evaluations across 7 diverse agents show substantial performance degradation compared to prior benchmarks, with success rates dropping below 5% on 6–8 step tasks and branch accuracy averaging 38%, highlighting challenges in conditional decision-making. By exposing these failure modes, DAC-Bench provides a challenging and diagnostic benchmark for advancing decision-aware mobile GUI agents. Our code and dataset are available at: https://github.com/YuqingZhangMirror12/DAC-Bench.

---

## 论文详细总结（自动生成）

## DAC-Bench：面向组合式移动GUI任务的决策感知基准

### 1. 核心问题与整体含义（研究动机和背景）

- **背景**：大型多模态模型（LMMs）显著提升了视觉理解、指令跟随和多步任务规划能力，使得移动GUI智能体成为实际可行的范式。移动GUI智能体通过感知屏幕内容并执行结构化动作来操作现有软件环境，在智能手机普及的背景下具有广阔的应用前景。
- **现状不足**：现有移动GUI基准存在三大局限：
  1. **指令多样性不足**：多数基准通过模板替换或短指令线性拼接来扩展任务，导致语义重复，难以覆盖真实用户的指令多样性。
  2. **工作流过于线性**：现有数据集通常将任务形式化为线性步骤链，忽略了条件分支、回退策略、多条件过滤等决策感知行为。真实用户常根据中间结果调整交互策略（如“若便宜商品缺货则购买高价商品”）。
  3. **评估协议有限**：当前指标主要评估步骤级正确性或整体任务成功率，无法充分反映长工作流中的进度和决策点的准确率。
- **本文目标**：提出 DAC-Bench，一个面向长时程、决策感知的组合式移动GUI任务基准，以更真实地模拟用户移动交互模式，并诊断现有智能体在条件决策方面的能力边界。

### 2. 方法论

#### 2.1 任务形式化

每个任务 Tj 表示为一系列GUI交互片段：
```
Tj = {(I, i_t, c_t, g_t, a_t)}_{t=1}^{T}
```
其中 I 为全局任务指令，i_t 为第 t 步的原子指令，c_t 为约束，g_t 为当前截图，a_t 为执行的GUI动作。原子指令可能内部对应多个低层动作和截图，但仍作为单个高层指令处理。

#### 2.2 原子指令与约束构建

采用**人机协作的多阶段流水线**：

1. **人类种子标注**：标注员为每个应用策划可执行的原子指令种子集。
2. **LLM扩充**：使用多个LLM（GPT-4、Claude、DeepSeek）基于应用名称、应用商店描述和种子指令迭代生成额外的原子指令。
3. **约束归纳**：LLM为每条原子指令提出最多3个与应用上下文相关的候选约束，约束分类包括：数值范围（预算内价格）、阈值（评分≥4.5）、布尔属性（免运费）、时间条件（开始时间设为下午3点）、基于偏好的过滤（查找体育新闻）等。
4. **过滤与验证**：LLM自动预过滤去除不可行或冗余输出，再进行人工验证确保可执行性、真实性和多样性。仅在槽填充实体或词汇上略有差异的指令被视为重复。

#### 2.3 组合式任务构建

每个任务内部表示为**有向图 G = (V, E)**，节点为原子指令，边为约束（应用特定条件、GUI状态、上下文信号及必要谓词/依赖）。

**四种图结构类型**：

| 结构类型 | 说明 |
|---------|------|
| **Conjunctive（合取）** | 多个子约束必须全部满足，执行顺序灵活 |
| **Sequential（顺序）** | 原子指令链形成长时程任务 |
| **Conditional（条件）** | 包含二元决策节点和两个可选分支（if/else） |
| **Hierarchical（层级）** | 嵌套条件分支形成的多级决策结构，模拟用户的回退和自适应行为 |

**质量管控**：采用**多生成器混合策略**——观察到不同LLM有互补行为（GPT擅长连贯组合但可能产生不自然的决策规则；DeepSeek产生详细推理但逻辑较浅；Gemini生成更一致的分支工作流），因此从多个LLM采样构建任务。所有候选任务经LLM可行性/连贯性检查后，再进行人工验证。

#### 2.4 数据标注

- 20名训练有素的标注员，在Android和iOS实体手机上完成标注。
- 每步记录截图、低层指令、动作类型和动作参数。动作类型限定为：{Click, Scroll, Type, Navigate to Home, Navigate to Previous Page, Long Press, Complete}。
- 标注员可将违反应用使用惯例的任务标记为“IMPOSSIBLE”。
- 所有标注数据经两名独立校对者和作者的多阶段审查。

#### 2.5 数据集统计

- **规模**：830个复杂任务片段，共11,345个动作步骤，覆盖35个应用（7个类别：生产力、旅行、工具、娱乐、社交、新闻、购物与支付）
- **复杂度**：平均高层指令长度32.54 token；每个任务平均3.5个原子指令和4个关联约束；平均执行深度13.3步
- **多样性**：2,665个原子动作和3,037个约束；结构分布：合取（24.3%）、顺序（33.4%）、条件（24.0%）、层级（18.3%）；12.5%任务涉及跨应用交互
- **平台覆盖**：881个Android任务（版本11-15），199个iOS任务（18.5版），14.1%任务双平台可用；覆盖8个手机品牌、16种设备型号
- **对照组**：另含250个单原子指令任务作为消融控制组

#### 2.6 新评估指标

**加权最长公共子序列（W-LCS）**：
```
W-LCS(T̂, T*) = Σ_{j∈J} j / (Σ_{j=1}^{N} j)
```
其中 J 为预测序列与金标准序列 LCS 匹配的步骤位置集合，N 为金标准序列长度。该指标对后续步骤赋予更高权重，反映长时程执行中维持正确性的难度，输出范围 [0,1]。

**决策准确率（Decision Accuracy）**：额外评估智能体在遇到决策约束时是否选择正确分支，补充步骤级执行之外的决策能力视角。

### 3. 实验设计

#### 3.1 数据集 / Benchmark

- **主基准**：DAC-Bench，830个组合任务片段，11,345个动作步骤，涵盖Android和iOS双平台35个应用
- **对照基准**：单原子指令子集（250个任务）用于与先前的单步基准（如AndroidControl）比较，确认基准的难度不是数据构造的伪影

#### 3.2 对比方法（7类智能体）

| 类别 | 模型 |
|------|------|
| 通用GUI智能体 | AGUVIS-7B、UI-TARS-7B、Qwen2.5-VL-7B、OS-Atlas-Pro-7B |
| 移动特化智能体 | AgentCPM-GUI-8B |
| 推理智能体 | InfiGUI-R1-3B、InfiGUI-R1-3B（思考模式） |
| 通用LMM | GPT-5.1、GPT-4o、Claude-sonnet-4.5、Gemini 3 Pro Preview |

- 每个智能体每步接收：全局高层指令 I、低层指令 i_t、约束 c_t（如适用）和对应截图 g_t
- 使用各智能体官方实现，统一动作映射到预定义动作集

#### 3.3 评估协议

- **指标**：EM（精确匹配）、TM（类型匹配）、SR（成功率）、GP（目标进度）、W-LCS（加权最长公共子序列）、决策准确率
- **两个层级**：低层（逐步指定）指令和高层（仅目标）指令

### 4. 资源与算力

论文**未明确说明**使用的具体GPU型号、数量或训练时长。仅提到：

- 实验使用各智能体的官方开源实现，未进行额外训练或修改
- 补充实验中提到对Qwen2.5-VL使用GRPO微调，使用200个DAC-Bench决策节点，但未给出具体算力资源

### 5. 实验数量与充分性

#### 实验组数

1. **主实验**：12个模型 × 5种任务结构（单原子/合取/顺序/条件/层级）× 2种指令层级（高层/低层）× 4个指标
2. **对比实验**：与AndroidControl等先前基准的比较（含单原子控制组）
3. **长度敏感性实验**：不同步骤长度下GP和W-LCS的变化（附录详列6种变体指标的完整数据）
4. **分支结构实验**：决策准确率按分支深度分析（第一决策 vs 更深决策），含GRPO微调实验
5. **动作类型分析**：不同动作类型下各模型的TM/EM
6. **历史窗口长度实验**：不同历史步长的影响
7. **语言实验**：英文 vs 中文指令
8. **平台实验**：Android vs iOS
9. **错误分析**：基于InfiGUI-R1-3B的推理轨迹进行案例研究

#### 充分性与公正性评估

- **充分性**：实验覆盖全面，从整体性能、结构复杂度、任务长度、分支深度、动作类型、历史长度、语言、平台等多个维度进行系统分析，实验量充足。
- **公正性**：使用各模型官方实现，确保公平性；统一动作映射保证可比较性；引入单原子控制组验证数据质量；对比多个先前基准。
- **潜在偏差**：每任务仅使用单一金标准轨迹，可能低估替代但有效的策略；离线静态评估为主，未涵盖在线交互环境的随机动态。

### 6. 主要结论与发现

1. **显著性能退化**：相比先前基准，DAC-Bench上所有智能体性能大幅下降。层级结构下平均SR降至14.00%（低层设置），高层设置下GP平均仅13.10%。在6-8步任务中成功率降至5%以下，分支准确率平均仅38%。

2. **层级指令vs低层指令差异显著**：低层指令下EM/TM普遍较高，转向高层指令后TM平均下降24.11%，EM降至32.78%以下，揭示当前智能体强于视觉定位/导航而弱于全局任务推理。

3. **条件决策是核心瓶颈**：条件/层级任务因单一错误决策导致后续执行无效，性能下降比顺序/合取任务更显著。第一决策节点平均准确率仅36.85%，层级任务中更深的节点再下降7.08%。推理导向训练的InfiGUI-R1系列表现更优，GRPO微调可提升第一分支决策3.46%、后续决策8.47%。

4. **失败模式分类**：
   - **感知相关错误**：UI交互暗示误解、屏幕外/隐藏UI访问失败、定位精度不足、终止状态推断错误
   - **推理相关错误**：忽略分支约束、产生看似合理但与自身推理矛盾的行动

5. **动作类型影响**：长按（Long Press）准确率最低（比Click/Type平均低66.31%）；Complete动作的终止识别问题显著影响SR。

6. **历史窗口长度**：最优历史长度因模型而异，过长历史可能导致上下文过载、视觉降采样和推理延迟增加。

### 7. 优点

1. **问题导向明确**：准确定位了现有移动GUI基准的三大缺陷（指令多样性、线性工作流、评估协议），针对性地设计解决方案。
2. **任务设计创新**：引入图结构化的组合任务，覆盖合取、顺序、条件、层级四种结构，更真实地模拟用户决策行为，包括回退策略和自适应行为。
3. **人机协同构建流水线**：融合人类知识、多LLM增强和严格过滤验证，兼顾任务可执行性与语义多样性。采用混合生成器策略利用不同LLM的互补优势。
4. **评估指标改进**：提出W-LCS和决策准确率两个新指标，弥补了传统指标在长时程任务和分支结构上的分辨率不足。
5. **广泛的数据覆盖**：830个任务、35个应用、双平台（Android/iOS）、双语指令（中英文）、多设备型号，规模远超多数同类基准。
6. **多维度诊断**：丰富的实验设计（长度、分支深度、动作类型、语言、平台等）提供系统性诊断洞见，而不只是报告性能数字。
7. **严格的质控流程**：IMPOSSIBLE标记机制、LLM预过滤、双重人工审查等多层质量控制确保数据质量。

### 8. 不足与局限

1. **离线静态评估范式**：采用离线记录的回放范式，未完全捕捉在线交互环境的挑战（非平稳应用内内容、系统中断如通知/权限提示、随机动态如广告横幅）。
2. **单一金标准轨迹**：每集仅与单一参考轨迹比较，可能低估搜索优先 vs. 分类导航等替代但有效的策略。
3. **文化语言范围有限**：虽覆盖中英文和多种应用类别，但文化/语言多样性仍有限，未覆盖更多设备品牌（如平板/iPad）、更多应用类别（医疗、教育、游戏）。
4. **标注近似性**：当前流程是人类-LLM对真实用户行为的近似，可能无法完全反映所有用户案例和复杂决策；少量低层指令可能存在歧义。
5. **指令风格标准化**：高层指令的语言多样性有限，多为相对标准化的表达，缺少真实用户的口语化、模糊表达。
6. **数据重叠风险**：未系统验证DAC-Bench与其他智能体训练数据的重叠情况，无法完全排除少量任务模式出现在其他智能体训练集中的可能性。
7. **长按动作缺失**：标注者指出双触（Double-Tap）动作在多数智能体动作空间和训练数据中几乎缺失，影响泛化能力的评估。
8. **算力资源未公开**：论文未报告实验使用的GPU型号、数量和训练/推理时长，影响可复现性的完备性。

（完）

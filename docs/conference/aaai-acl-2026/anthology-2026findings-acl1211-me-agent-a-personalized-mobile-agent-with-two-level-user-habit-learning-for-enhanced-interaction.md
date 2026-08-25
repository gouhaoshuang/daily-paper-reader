---
title: "Me-Agent: A Personalized Mobile Agent with Two-Level User Habit Learning for Enhanced Interaction"
title_zh: Me-Agent：基于两级用户习惯学习的个性化移动智能体
authors: "Shuoxin Wang, Chang Liu, Gowen Loo, Lifan Zheng, Kaiwen Wei, Huanqian Yan, Xinyi Zeng, Jingyuan Zhang, Yu Tian"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.findings-acl.1211.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 通过两级用户习惯学习执行任务的个性化移动智能体
tldr: 针对现有移动智能体忽视用户个性化需求、无法理解模糊指令且不会从交互历史中学习的问题，提出Me-Agent个性化移动智能体框架，通过提示级别和交互级别两级用户习惯学习策略，结合个人奖励模型，使用户智能体能够记忆用户习惯并处理个性化指令。实验表明该方法显著提升了移动任务执行中的个性化交互效果。该工作为手机端智能体从通用指令执行走向个性化自主任务完成提供了有效方案。
source: ACL-2026-Findings
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1211/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 797, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1211/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1619, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1211/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 768, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-findings/anthology-2026findings-acl1211/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1643, \"height\": 676, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1318, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 651, \"height\": 521, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 834, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1684, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1789, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1675, \"height\": 1475, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1446, \"height\": 1112, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-findings/anthology-2026findings-acl1211/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1871, \"height\": 728, \"label\": \"Table\"}]"
motivation: 现有移动智能体缺乏个性化上下文，难以理解模糊指令并利用用户交互历史。
method: 提出提示级与交互级的两级用户习惯学习策略，并用个人奖励模型增强偏好学习。
result: 实验验证该方法在理解模糊指令和处理个性化指令上显著优于基线。
conclusion: 两级用户习惯学习有效提升移动智能体的个性化交互与任务执行能力。
---

## Abstract
Large Language Model (LLM)-based mobile agents have made significant performance advancements. However, these agents often follow explicit user instructions while overlooking personalized needs, leading to significant limitations for real users, particularly without personalized context: (1) inability to interpret ambiguous instructions, (2) lack of learning from user interaction history, and (3) failure to handle personalized instructions. To alleviate the above challenges, we propose Me-Agent, a learnable and memorable personalized mobile agent. Specifically, Me-Agent incorporates a two-level user habit learning approach. At the prompt level, we design a user preference learning strategy enhanced with a Personal Reward Model to improve personalization performance. At the memory level, we design a Hierarchical Preference Memory, which stores users’ long-term memory and app-specific memory in different level memory. To validate the personalization capabilities of mobile agents, we introduce User FingerTip, a new benchmark featuring numerous ambiguous instructions for daily life. Extensive experiments on User FingerTip and general benchmarks demonstrate that Me-Agent achieves state-of-the-art performance in personalization while maintaining competitive instruction execution performance.

---

## 论文详细总结（自动生成）

## Me-Agent：基于两级用户习惯学习的个性化移动智能体 —— 论文中文总结

### 一、核心问题与整体含义（研究动机与背景）

- **研究对象**：基于大语言模型（LLM）的移动智能体（Mobile Agent），即通过自然语言指令驱动手机应用操作的自主智能体。
- **核心问题**：现有移动智能体严重依赖显式、完整的用户指令，缺乏对用户潜在偏好和个性化需求的系统建模。在缺少用户背景信息或场景复杂多变时，表现出三大缺陷：
  1. **无法解读模糊指令**：用户常省略应用名（如"我想听音乐"）或用模糊指代（如"播我常听的"），现有智能体无法推断意图；
  2. **无法从交互历史中学习**：缺少跨多轮交互持续更新用户行为模式的能力；
  3. **无法处理个性化指令**：对偏好配置和个性化内容（如"我的最爱"）处理能力有限。
- **整体含义**：该研究旨在将移动智能体从"通用指令执行器"升级为"个性化自主任务代理"，使其能够基于用户历史行为隐式推理偏好，在不修改模型参数的前提下实现长期、动态的个性化适应。

### 二、方法论：Me-Agent 框架

#### 2.1 核心思想

Me-Agent 采用**两级用户习惯学习**架构，无需任何模型微调或参数更新，适用于纯API部署场景：

- **提示级（Prompt Level）**：通过 **User Preference Learning（UPL）** 在上下文空间中优化策略；
- **记忆级（Memory Level）**：通过 **Hierarchical Preference Memory（HPM）** 存储和按需检索应用级与用户级知识。

#### 2.2 技术细节

**（1）User Preference Learning（UPL）—— 参数无关的偏好建模模块**

受 Training-Free GRPO 启发，包含四个阶段：

- **Rollout（样本生成）**：对每个指令执行 G 次独立轨迹采样（采样温度 T=0.3），生成多样化执行路径；
- **Reward（奖励打分）**：基于 VLM（视觉语言模型）的奖励模型，从截图序列的四个维度（目标达成、步骤有效性、结果可见性、错误检测）对轨迹质量进行连续打分，奖励值域 [0,1]；
- **Advantage（经验提取）**：分两步进行——先将每条轨迹汇总为结构化经验，再通过"比较批判"（Comparative Critique）挖掘跨轨迹的通用经验，覆盖六类知识：用户偏好、UI导航、动作序列、元素识别、上下文感知、完成信号；
- **Optimization（经验整合）**：新经验与已有经验池通过 LLM 比较，分配 ADD / UPDATE / DELETE / KEEP 四种操作，实现经验的动态更新、冗余合并与冲突消解，避免提示无限膨胀。

**（2）Hierarchical Preference Memory（HPM）—— 层次化偏好记忆**

利用移动指令天然的两级结构（应用类别 → 应用内操作）：

- **L1 记忆**：按意图类别组织（如音乐、购物、阅读），记录类别下常用应用集合；
- **L2 记忆**：对每个应用存储"工作流"（操作模式、UI元素位置）和"内容偏好"（用户在该应用内的偏好内容），支持动态更新（基于嵌入相似度和成功次数合并相似工作流，基于频率统计调整内容偏好）。

**（3）两阶段个性化推理**

- **应用解析**：指令明确指定应用时直接使用；否则根据经验池推断偏好概率最高的应用：$a^{*} = \arg\max_{a \in A_{cat}(I)} P(a|E)$；
- **内容检索**：对模糊指代（如"我的最爱"），先从 HPM 中做语义相似性 top-k 候选检索，再由 LLM 结合用户历史推理出最合适的内容；
- **提示注入**：将解析出的应用、检索到的内容和相关经验注入提示，指导个性化执行。

### 三、实验设计

#### 3.1 数据集与基准

| 数据集 | 用途 | 规模与构成 |
|---|---|---|
| **User FingerTip**（新构建） | 评估个性化能力 | 60 用户、33 个应用、12 个功能类别；300 条 Type I（应用模糊）指令、267 条 Type II（内容模糊）指令；每用户 15 条训练 + 5 条测试，训练集与测试集无重叠 |
| **E 数据集**（既有通用基准） | 评估通用任务执行能力 | 复杂高难度多应用指令 |

- **个性化指标**：App 选择准确率（ASA）、BERTScore（Type II 仅用）、偏好分数（PS）、人类满意度分数（HSS，由应用选择正确性 0.4 + 内容匹配正确性 0.4 + 任务完成 0.2 加权合成）
- **性能指标**：任务完成率（TCR）、任务成功率（TSR）、动作保真度（AF）、反思精度（RP）、平均步数（Step）

#### 3.2 对比方法与实现配置

- **基线**：Mobile-Agent-v2、Mobile-Agent-E（同领域两个代表性多智能体移动操作框架）
- **感知模块**：DBNet（OCR检测）、ModelScope ConvNextViT-document（OCR识别）、GroundingDINO（图标定位）、GPT-4o（图标描述生成）
- **推理骨干**：GPT-4o、Claude-3.5-Sonnet、Gemini-2.5-Pro（用于骨干鲁棒性评估）
- **实现细节**：每组 rollout 数为 2、采样温度 0.3、训练 2 个 epoch、batch size 为 5；所有 LLM/VLM 均冻结。

### 四、资源与算力

- **论文未明确披露**具体 GPU 型号、数量或训练时长。
- 仅在实现细节中说明：**"所有实验均使用标准化云基础设施运行"**，并强调"为保障可复现性，所有实验保持相同软件版本和硬件配置"。
- 由于框架为免训练设计，推理成本集中于 LLM/VLM 调用次数，论文用"平均步数"作为间接效率指标（Me-Agent 在 E 数据集上 12.53 步 vs. 基线 18.40/20.20 步）。

### 五、实验数量与充分性评估

#### 已开展实验（共 6 组）

1. **User FingerTip 个性化评估**（表 3）：覆盖 Type I 和 Type II 两类模糊指令，报告 6~7 项指标；
2. **E 数据集通用性能评估**（表 4）：报告 5 项任务执行指标；
3. **消融实验**（图 3）：BASE、BASE+UPL、BASE+HPM、BASE+UPL+HPM 四种配置，验证模块贡献与互补性；
4. **骨干模型鲁棒性实验**（表 5）：三种不同 LLM 骨干 × Type I/II 任务；
5. **效率评估**：比较平均步数；
6. **案例研究**（图 4）：定性展示个性化行为。

#### 充分性评价

**积极方面**：
- 覆盖了个性化与通用性能两个维度，指标设计较全面；
- 消融实验清晰验证了每个模块的独立贡献和组合价值；
- 跨骨干实验增强了结论的泛化可信度；
- 数据划分（用户级别、训练/测试不重叠）保证评估有效性。

**不足方面**：
- **基线数量偏少**：仅对比 Mobile-Agent-v2 和 Mobile-Agent-E 两个同源方法，未包含 PerPilot 等已有个性化移动智能体对比；
- **指标覆盖不完整**：Type I 指令未报告 BERTScore 和 PS，个性化语义维度的评估在 Type I 上缺失；
- **人类评估样本有限**：仅招募计算机科学博士生作为评估者，样本代表性可能受限；
- 未提供多次运行的方差或显著性检验，统计稳健性无从判断。

### 六、主要结论与发现

1. **个性化能力显著领先**：Me-Agent 在 User FingerTip 上 Type I 和 Type II 的 ASA 均达到 1.000，而基线仅 0.2~0.6；HSS 达 0.890（Mobile-Agent-v2 仅 0.428），证明其能有效从历史行为中推断应用级和内容级偏好。
2. **任务执行性能同样优秀**：E 数据集上 TCR 达 0.893，较最好的基线（0.639）提升约 39.7%；AF（0.861）和 RP（0.978）均为最优。
3. **鲁棒性突出**：在三种推理骨干（GPT-4o、Claude-3.5-Sonnet、Gemini-2.5-Pro）下均保持稳定的个性化效果，说明模块设计对骨干模型不敏感。
4. **模块互补性得到验证**：UPL 擅长捕获通用用户偏好，HPM 提供细粒度应用执行知识，两者组合效果最佳。
5. **效率提升明显**：经验池和层次记忆提供结构先验，使执行步数显著减少（E 数据集 12.53 步 vs. 基线 18~20 步）。
6. **基线的局限被实证证实**：在从 Type I（应用模糊）到 Type II（内容模糊）难度升级时，基线性能大幅退化，而 Me-Agent 保持稳定。

### 七、方法亮点与优点

- **免训练设计**：完全在上下文空间优化，无需参数更新，适合移动端算力受限和 API 部署场景，规避云端微调的隐私与成本问题；
- **双层记忆架构**：外部存储 + 按需检索，有效解决提示无限膨胀和注意力稀释问题，同时支持动态更新并在应用更新后保留偏好知识；
- **自然语言经验**：偏好和经验以可解释、可编辑的自然语言形式沉淀，支持人工干预和持续迭代（ADD/UPDATE/DELETE/KEEP 四种操作）；
- **VLM 奖励模型**：直接从截图序列评估执行质量，无需额外的结构化日志或操作标注，数据采集成本低；
- **新基准构建**：User FingerTip 填补了移动智能体在模糊指令下隐式偏好推理评估的空白，区分了应用模糊和内容模糊两类现实挑战；
- **层次化推理机制**：将"选哪个应用"和"操作什么内容"分步解耦，与人类决策习惯一致。

### 八、不足与局限

#### 8.1 论文明确承认的局限

- **UI 动态性**：存储的 UI 位置和动作序列在应用更新或意外弹窗出现时可能失效，导致执行失败；
- **上下文因素单一**：个性化仅依赖历史偏好和行为模式，未纳入用户当前位置、情绪状态等动态情境因素，当用户当前情境与常规模式不同时推荐效果可能较差。

#### 8.2 客观观察到的其他限制

- **实验覆盖局限**：基线对比范围窄，未与 PerPilot 等直接相关的个性化移动智能体方法比较；
- **评估偏差风险**：人类评估员均为 CS 博士生，非真实终端用户群体，满意度分数的生态效度有待提升；评估者数量和评分者一致性（如 Kappa）未报告；
- **记忆失效风险**：对应用版本极度敏感，长期运行中经验库可能累积大量过时知识，论文未讨论自动过期机制；
- **奖励模型的设计细节有限**：VLM 奖励模型四个评分维度的具体 prompt 和打分校准过程披露不充分，可复现性受影响；
- **Type I 指令的语义评估缺失**：个性化能力的全面评估在应用模糊场景下缺少 BERTScore 和偏好分数的佐证；
- **统计验证不足**：未报告多次运行的方差、置信区间或显著性检验，单次运行结果可能存在偶然性。

### 总结

Me-Agent 通过"提示级偏好学习 + 记忆级层次存储"的双轨设计，在不训练任何参数的前提下实现了移动智能体的个性化能力突破，在模型无关性、执行效率和知识可解释性方面提供了有价值的思路。其构建的 User FingerTip 基准也为后续研究提供了可复用的评估工具。然而，UI 动态适应、情境感知丰富度和评估体系的完善程度仍是未来需要攻克的方向。

（完）

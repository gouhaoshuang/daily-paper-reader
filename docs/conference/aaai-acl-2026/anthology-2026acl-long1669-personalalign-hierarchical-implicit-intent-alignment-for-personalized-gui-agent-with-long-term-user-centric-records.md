---
title: "PersonalAlign: Hierarchical Implicit Intent Alignment for Personalized GUI Agent with Long-Term User-Centric Records"
title_zh: PersonalAlign：面向长期用户记录个性化GUI智能体的层次化隐式意图对齐
authors: "Yibo Lyu, Gongwei Chen, Rui Shao, Weili Guan, Liqiang Nie"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.1669.pdf"
tags: ["query:mobile-agent"]
score: 9.0
evidence: 个性化GUI智能体借助AndroidIntent基准实现主动移动辅助
tldr: 针对真实部署中GUI智能体需要理解用户隐式意图的问题，提出PersonalAlign任务，要求智能体利用长期用户记录解决模糊指令中的偏好遗漏，并根据用户状态预判潜在习惯以提供主动帮助。同时构建AndroidIntent基准来评测该能力，推动了移动端个性化智能体从仅执行显式指令向符合用户隐式意图的范式转变。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 791, \"height\": 737, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 795, \"height\": 886, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 794, \"height\": 410, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1642, \"height\": 562, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 811, \"height\": 815, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 816, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1643, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long1669/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1658, \"height\": 390, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1627, \"height\": 476, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 826, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 799, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1317, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 798, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 792, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 742, \"height\": 281, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long1669/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1300, \"height\": 248, \"label\": \"Table\"}]"
motivation: 现有GUI智能体难以处理模糊指令，无法利用长期用户记录进行个性化服务。
method: 提出层次化隐式意图对齐方法，将长期用户记录作为持久上下文进行推理。
result: 在AndroidIntent基准上验证了隐式意图对齐任务的必要性及现有模型的不足。
conclusion: 个性化意图对齐是移动GUI智能体实用化的关键方向。
---

## Abstract
While GUI agents have shown strong performance under explicit and completion instructions, real-world deployment requires aligning with users’ more complex implicit intents. In this work, we highlight Hierarchical Implicit Intent Alignment for Personalized GUI Agent (**PersonalAlign**), a new agent task that requires agents to leverage long-term user records as persistent context to resolve omitted preferences in vague instructions and anticipate latent routines by user state for proactive assistance. To facilitate this study, we introduce **AndroidIntent**, a benchmark designed to evaluate agents’ ability in resolving vague instructions and providing proactive suggestions through reasoning over long-term user records. We annotated 775 user-specific preferences and 215 routines from 20k long-term records across different users for evaluation. Furthermore, we introduce Hierarchical Intent Memory Agent (**HIM-Agent**), which maintains a continuously updating personal memory and hierarchically organizes user preferences and routines for personalization. Finally, we evaluate a range of GUI agents on AndroidIntent, including GPT-5, Qwen3-VL, and UI-TARS, further results show that HIM-Agent significantly improves both execution and proactive performance by 15.7% and 7.3%.

---

## 论文详细总结（自动生成）

# 论文中文结构化总结

## 一、核心问题与整体含义（研究动机与背景）

- **研究背景**：当前 GUI 智能体（如 GPT-5、Qwen3-VL、UI-TARS 等）在**显式、完整指令**下已展现出较强执行能力，但在真实部署中，用户的指令往往是不完整、模糊的，且隐含着大量未言明的个人偏好和日常习惯。现有智能体无法有效利用**长期用户记录**来弥合这种"意图空缺"。
- **核心问题**：论文提出并定义了新任务 **PersonalAlign（层次化隐式意图对齐）**，要求智能体将长期用户记录作为持续上下文，在**两个层面**实现个性化对齐：
  - **偏好意图（Preference Intent）**：从模糊指令中推断被省略的个人偏好，以修正执行轨迹；
  - **常规意图（Routine Intent）**：在无指令情况下，仅依据当前用户状态（时间、场景）预测潜在需求并**主动提供建议**。
- **整体含义**：该任务推动 GUI 智能体从"被动响应式执行器"向"能与用户共同演化的个性化伙伴"转变，强调通过共享历史上下文建立人机信任。

## 二、方法论

### 2.1 任务形式化定义（三范式）

将 GUI 交互记录表示为 Rᵢ = (Iᵢ, Tᵢ, Sᵢ, Aᵢ, Oᵢ)，按 80%/20% 划分为历史记录 H 和执行记录 E。三个范式分别为：

- **反应式执行**：Aᵗ ← fθ(Iᵗ; ∅)——仅依据显式指令执行，不使用历史；
- **偏好意图对齐**：Aᵗ ← fθ(Îᵗ; {(Iᵢ, Aᵢ)} ∈ H)——从模糊指令结合历史推断缺失偏好；
- **常规意图对齐**：I′ᵗ ← fθ(I∅; {(Iᵢ, Tᵢ, Sᵢ)} ∈ H)——在无指令时依据用户状态和历史规律主动生成建议。

### 2.2 AndroidIntent 基准构建（分层过滤-验证策略）

- **意图语义相似度**：使用 Qwen3-Embedding 计算执行记录与历史记录中 top-k 相似意图的平均余弦相似度，得分记为 Scos。
- **用户状态偏移**：计算时间偏移熵 ΔHt 和场景偏移熵 ΔHs，熵值越低说明用户在相似状态下的行为越稳定，越适合主动服务。
- **量化综合得分**：Qscore = Scos + ΔHt + ΔHs。在 20k 用户记录上绘制得分分布，呈现出**三个近似高斯分布的模式**，分别对应时刻意图、偏好意图和常规意图，据此实现高效候选筛选。
- **人工验证**：在筛选基础上，人工标注者对候选样本进行二次复核，并使用 LLM 生成多种"省略偏好信息的模糊指令"，由标注者选择最符合用户真实意图的一条。

### 2.3 HIM-Agent（层次化意图记忆智能体）

- **流式聚合模块（Streaming Aggregation Module）**：
  - 以记录原型 Pᵢ 作为基本记忆单元，将相似记录按日粒度增量聚合，避免原始记录的碎片化和长尾噪声；
  - 采用 MicroCluster（流式聚类）思想实现持续演化的个人记忆。
- **基于执行的偏好过滤器（Execution-based Preference Filter）**：
  - 综合**语义相似度**（稠密向量 Scos + 稀疏 Jaccard 重叠度）和**动作一致性**（DTW 动态时间规整衡量轨迹相似度）来计算记录与原型的一致性 Sconsist；
  - 过滤后形成**偏好意图记忆**，供模糊指令执行时提供偏好上下文。
- **基于状态的常规过滤器（State-based Routine Filter）**：
  - 对每个原型计算主动置信度 Φ(Pᵢ) = 状态稳定性 Hstate + 记录长度 Lrecord + 聚合权重 Rconsist；
  - 超过阈值 Φ 的原型存入**常规意图记忆**，当用户当前状态（时间+场景）匹配时，触发主动建议。

## 三、实验设计

### 3.1 数据集与 Benchmark

- **基础数据**：基于 **Fingertip20K**（91 名用户、2 个月、20,000 条 Android 交互记录）；
- **AndroidIntent 基准**：
  - 775 条偏好意图 + 215 条常规意图；
  - 覆盖 190 个应用（130 个用于偏好，60 个用于常规）；
  - 涉及 7,915 个 GUI 动作，包含 20k 历史记录作为上下文。

### 3.2 对比方法与基线

- **GUI 智能体**：GPT-5.1、GLM-4.5V、QwenVL-Max（闭源）；UI-TARS-1.5、GUI-Owl、Qwen3-VL（开源）及 Gemini3-Pro（补充实验）。
- **方法对比**：
  - Retrieve-based（检索近期/相关历史记录）；
  - LLM-UM（基于 LLM 生成用户画像摘要）；
  - HIM-Agent（本文方法）。

### 3.3 评估指标

- 执行：Type Accuracy（类型准确率）、SSR（逐步成功率）、CSR（累积成功率，新增关键步骤加权指标）；
- 主动：意图语义对齐（embedding 余弦 + 编辑距离）、LLM-as-Judgment 意图判断、精度/召回/误报率/F1（基于 100 条负样本用户状态）。

## 四、资源与算力

- **文中明确说明**：所有 GUI 智能体执行实验在一块 **NVIDIA A100 (40GB) GPU** 上完成；
- **未明确说明**：GPU 数量、训练/推理时长、参数规模对比（如相对 LLM-UM 的 token 开销虽有比较，但未给出具体硬件消耗细节）以及数据标注的人力成本细节。

## 五、实验数量与充分性

### 5.1 主要实验组

1. **指令退化影响实验**（表 3）：6 个模型在完整 vs 模糊指令下的执行性能对比；
2. **主动服务能力评估**（表 4）：6 个模型在主动建议任务上的意图对齐与识别对齐表现；
3. **执行性能方法对比**（表 5）：Qwen3-VL 基础上比较 Retrieve、Generalized、Recent Retrieve、LLM-UM 与 HIM-Agent；
4. **主动性能方法对比**（表 6）：GPT-5.1 基础上比较相同基线与 HIM-Agent；
5. **执行偏好过滤器消融**（表 7）：Dense/Sparse/Action 三组件的逐一组合消融；
6. **主动性能消融**（图 6）：时间/场景组件对误报率的影响；
7. **超参数鲁棒性验证**（图 8）：不同权重组合下的高斯分布稳定性；
8. **补充模型对比**（表 8）：Gemini3-Pro、Qwen-Max 等更多模型的主动能力；
9. **案例研究**（图 7）：HIM-Agent vs 反应式智能体的定性对比。

### 5.2 充分性评价

- **充分性较高**：覆盖了主客观评估、多模型横向对比、组件级消融、超参数敏感性分析、定性案例分析，证据链较完整；
- **可在以下方面进一步补充**：端到端在线真机评估（论文承认离线评估局限）；不同数据源（仅 Fingertip）的跨数据集泛化验证；对"主动建议是否会打扰用户"的主观满意度评估相对有限。

## 六、主要结论与发现

1. **模糊指令是执行性能的显著瓶颈**：模糊指令仅使类型准确率下降约 3%，但 SSR 下降约 20%、CSR 下降约 45%——说明 GUI 智能体能识别粗粒度目标，却在缺少个性化关键信息的细粒度步骤上失败。
2. **现有模型难以平衡主动服务的准确性与克制性**：除 GPT-5.1 外，多数模型倾向于过度主动，导致误报率极高（如 GLM-4.5V 误报率 94%），无法可靠判断"何时不需要打扰用户"。
3. **HIM-Agent 显著提升双重性能**：
   - 在模糊指令执行上，CSR 相对基线提升 15.7%（Qwen3-VL 上 26.6 → 42.3）；
   - 在主动建议上，F1 提升 7.3% 且误报率最低（49%），同时保持 token 效率（1605 vs LLM-UM 的 1161+6518）。
4. **层次化记忆设计有效且必要**：语义、动作、状态三要素缺一不可；移除状态过滤器会导致误报率升至约 70%。

## 七、优点

- **任务定义新颖且具有实践价值**：首次将"隐式意图"按层次拆分为偏好意图和常规意图，统一了此前割裂的"个性化执行"和"主动服务"两条研究线。
- **基准构建方法具有可扩展性**：分层过滤-验证策略将主观概念量化为可计算得分，三高斯分布自然呈现，兼顾客观性与可扩展性。
- **HIM-Agent 设计轻量高效**：流式聚合避免全量存储；层次化过滤器将记忆组织为可检索原型，无需额外大模型生成画像即可进行个性化推理，token 开销低。
- **离线评估指标设计合理**：新增 CSR 指标对关键步骤误差施加指数衰减权重，较好衔接离线与在线性能的鸿沟。
- **实验分析深入**：对"模糊指令造成精细步骤失败"和"主动误报高发"两种现象的定性+定量剖析具有启发性。
- **数据与代码开源**：提供了项目仓库（GitHub），有助于后续研究复现和扩展。

## 八、不足与局限

- **数据来源单一**：仅基于 Fingertip 数据集，缺乏跨平台（如 iOS、桌面 OS、Web）和多语言场景的验证，结论的泛化性有一定局限。
- **冷启动问题**：依赖足够的历史数据才能推断偏好和常规。对于新用户或使用频率低的交互，模型难以有效工作。
- **隐私风险**：利用长期用户记录进行建模涉及敏感的隐私问题；论文虽基于已获同意的数据集讨论隐私保护方向，但自身框架尚未实现具体方案。
- **评估环境局限**：主要采用离线评估，尽管论文论证了真机评估的困难，但离线轨迹跟随无法覆盖"多种合法路径达成同一意图"的现实多样性，对执行质量的评估可能存在偏差。
- **主动执行范围受限**：论文将主动行为限定在"建议生成"层面（不自主执行动作），真正的 Proactive Executing（如自动打开导航、自动下单）仅作为展望提出，尚无法在现有框架中落地。
- **LLM-as-Judgment 的主观性**：主动建议评估中引入 LLM 裁判可能存在偏见，虽然选用了 DeepSeek-V3 减轻自偏，但未与人类评估进行系统性一致性验证。
- **超参数依赖**：过滤器的阈值（θ=0.6、top-k=10 等）及 Qscore 权重需人工调整；虽然论文展示了鲁棒性，但对不同数据分布的适应性仍有待更多验证。

**（完）**

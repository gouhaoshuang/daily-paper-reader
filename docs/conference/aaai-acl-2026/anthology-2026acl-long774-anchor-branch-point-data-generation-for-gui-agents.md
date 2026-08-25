---
title: "Anchor: Branch-Point Data Generation for GUI Agents"
title_zh: Anchor：GUI智能体的分支点数据生成方法
authors: "Jinbiao Wei, Yilun Zhao, Kangqi Ni, Arman Cohan"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.774.pdf"
tags: ["query:mobile-agent"]
score: 6.0
evidence: 为GUI智能体提供数据生成技术，可迁移到移动端设备任务执行智能体的构建中
tldr: 端到端GUI智能体需要大量高质量交互数据，但人工示范昂贵且现有合成流程常产生低质量轨迹。为此，论文提出Anchor轨迹扩展框架，从少量已验证种子示范出发，通过识别分支点生成新任务变体，并由执行智能体产生轨迹、验证器确保任务完成。该方法在桌面环境验证了可扩展性，为移动GUI智能体的数据构建提供了可迁移技术。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long774/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1655, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long774/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 759, \"height\": 630, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long774/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 799, \"height\": 620, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long774/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1617, \"height\": 1085, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 537, \"height\": 358, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 772, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1615, \"height\": 523, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 778, \"height\": 469, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 789, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 731, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1582, \"height\": 1640, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long774/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1594, \"height\": 849, \"label\": \"Table\"}]"
motivation: GUI智能体训练数据获取成本高，现有合成数据方法存在任务多样性不足和轨迹质量差的问题。
method: 提出Anchor框架，利用分支点检测与新任务变体生成，从少量种子示范扩展高质量轨迹。
result: 在桌面GUI环境中生成了多样化且一致的高质量数据，降低了对人工示范的依赖。
conclusion: 为GUI智能体提供了可扩展的轨迹数据生成方法，可服务于移动端智能体的构建。
---

## Abstract
End-to-end GUI agents for real desktop environments require large amounts of high-quality interaction data, yet collecting human demonstrations is expensive and existing synthetic pipelines often suffer from limited task diversity or noisy, goal-drifting trajectories. We present a trajectory expansion framework Anchor that bootstraps scalable desktop supervision from a small set of verified seed demonstrations. Starting from each seed, we identify branch points that correspond to meaningful state changes and propose new, state-grounded task variants conditioned on the current GUI context. An executing agent then follows the proposed instructions to generate new trajectories, while a verifier enforces task completion via state-aware checks and trajectory-level consistency. To improve supervision quality, we further apply task-conditioned step-level filtering to remove ungrounded actions and denoise post-branch segments to maintain coherent intent. Experiments on standard desktop benchmarks, OSWorld and WindowsAgentArena, show that models fine-tuned on our expanded corpus achieve consistent improvements over zero-shot agents and representative synthesis baselines, and generalize across applications and operating systems.

---

## 论文详细总结（自动生成）

# ANCHOR：GUI智能体的分支点数据生成方法——论文详细中文总结

## 1. 论文的核心问题与整体含义

### 研究动机
- 端到端GUI智能体（如桌面环境中的自动化代理）需要大量高质量交互数据进行训练，但存在以下瓶颈：
  - **人工示范数据昂贵**：专家需要逐步骤记录动作、验证成功，难以规模化扩展。
  - **现有合成数据管线存在不足**：
    - *任务驱动方法*（如Explorer）：任务多样性受限于模型对UI的了解，且失败会截断轨迹，数据偏向简单任务。
    - *交互驱动方法*（如OS-Genesis、AutoPlay、GUI-ReWalk）：自由探索容易产生短轨迹或大量低信号游荡，难以提炼为有意义的长程监督。
    - *教程驱动方法*（如AgentTrek、TongUI）：覆盖范围受限于教程的可用性和多样性。
  - 桌面轨迹生成相对Web和移动端更加未被充分探索。
- **核心问题**：如何从少量高质量种子示范出发，规模化生成多样、目标一致、长程的桌面GUI交互轨迹？

### 整体含义
- 论文提出了一种**轨迹扩展框架 ANCHOR**，通过在验证过的种子轨迹上识别"分支点"（UI状态发生实质变化的决策节点），从这些状态出发生成新的任务变体并执行，从而以低成本获得高质量、长程、多样化的训练数据。核心思想是利用种子轨迹的可靠前缀来锚定探索，降低对执行模型完美度的依赖。

## 2. 方法论

### 核心思想
- **围绕少量规范化种子轨迹进行系统性分支扩展**，而非从零开始提出任务或进行无约束探索。
- 分支点定义为UI状态发生**实质性变化**的步骤（如新窗口出现、面板展开、滚动后显示新内容），这些状态揭示了新的界面可供性（affordances），可以自然衍生出多样化的下游任务。

### 技术流程（数据生成配方）

1. **种子轨迹采集**
   - 从OSWorld和WindowsAgentArena的交互环境中采样任务（OSWorld 117个、WindowsAgentArena 51个）。
   - 使用强模型获取成功运行，再经过**人工验证**：检查最终状态是否满足指令、动作是否高效、有无有害副作用；通过后保留最短的成功轨迹作为种子。

2. **分支点识别**
   - 使用GPT-5.1分析种子轨迹，识别3-5个UI状态发生实质变化的时间步作为候选分支点。

3. **分支任务提议**
   - 对每个分支点，先用GPT-5.1生成进度摘要，再基于当前UI状态提议一个或多个新任务描述。要求任务：
     - 扎根于当前可见界面
     - 是前一动作的自然延伸
     - 可在5–15步内完成
     - 与原始任务不同且互不重复

4. **任务执行**
   - 将环境重放到分支状态st，调用GUI智能体（Claude Sonnet 4.5）执行新任务。
   - 当动作偏离原始规范或环境状态不兼容时，模型会**在运行中修订任务描述**为可行的语义相近变体。

5. **轨迹总结**
   - 执行完成后，用总结器生成简洁的高层任务描述（抽象掉低层UI操作）。

6. **轨迹验证**
   - 验证器接收（任务描述，轨迹）判断最终GUI状态是否满足任务规范。要求执行智能体明确指示完成**且**验证器分类为成功才保留。

### 步骤级质量控制

7. **任务条件推理过滤（前缀共享步骤）**
   - 同一前缀可被多个后代任务共享，但每个动作在不同任务语境下的意图不同。
   - 为每个共享前缀步骤，以任务描述、交互历史和当前截图作为条件，采样M=10个候选行动-推理对；通过前后截图验证候选动作与真实动作的一致性；若无一匹配，则丢弃该步骤；若匹配，选择与观测状态转换相符的推理作为监督。

8. **分支后意图一致性去噪**
   - 对分支后的每一步，验证动作在当前上下文中是否合理、是否与前后截图的变化一致；不一致的步骤被标记为噪声并排除，但保留该轨迹中后续通过过滤的步骤。

### 模型分工
- **GPT-5.1**：分支点识别、任务提议、回放验证
- **Claude Sonnet 4.5**：轨迹执行
- **Qwen3-VL-32B**：步骤级过滤、任务总结、验证

## 3. 实验设计

### 基准数据集
- **OSWorld**：基于真实Ubuntu桌面VM，任务由自然语言指令+可复现VM快照+执行脚本检查器组成，agent通过截图和GUI动作交互。
- **WindowsAgentArena**：基于Windows 11 VM（Docker容器内），使用确定性Python评估器返回二元成功标志。

### 生成数据规模
- 总计 **1,777条成功轨迹**：1,174条Ubuntu轨迹 + 603条Windows轨迹。
- 平均轨迹长度 **17.24步**（远超现有合成管线）。
- 每条成功轨迹平均成本 **$0.47**。

### 对比方法
1. **Zero-Shot**：基础模型不做微调。
2. **Task-Driven**：实现代表性目标条件合成管线（用GPT-5.1生成任务指令，Claude 4.5执行）。
3. **Human Data**：使用AgentNet数据集（人类标注动作+合成推理），限制在匹配平台和应用子集。
4. **ANCHOR**：本方法生成的数据微调。

### 训练骨干模型
- **GLM-4.1V-9B-Base**
- **Qwen2.5-VL-7B-Instruct**
- **Qwen3-VL-8B-Instruct**

### 训练方式
- 轨迹级SFT，使用工具调用动作空间（`computer_use`函数）。
- 联合优化两个目标：
  - **L_plan**：预测步骤级推理状态rt和下一动作at
  - **L_act**：在给定推理的条件上预测动作at
- 每个步骤以当前截图+前两个截图+交互历史为条件。

## 4. 资源与算力

- **硬件**：4× NVIDIA H200 GPU（全参数微调）。
- **精度**：混合精度FP16。
- **优化器**：AdamW，学习率5×10⁻⁶，线性学习率调度，30步预热，梯度裁剪1.0。
- **批次**：每设备微批次1，梯度累积到全局批次16。
- **训练时长**：1个epoch（论文未具体说明训练时间）。
- 数据集总规模：2.3M tokens、30K张图像。

## 5. 实验数量与充分性

### 主要实验组
| 实验类型 | 说明 |
|---------|------|
| **OSWorld主实验** | 3种骨干模型 × 3种对比方法 × 10+应用域 |
| **WindowsAgentArena实验** | 3种骨干模型 × 3种对比方法 |
| **数据规模分析（In-domain）** | 0.3K/0.6K/1K轨迹量级缩放实验 |
| **数据规模分析（Cross-domain）** | Ubuntu+Windows混合数据对OSWorld的影响 |
| **消融实验** | 移除步骤级过滤+去噪 vs 完整ANCHOR |
| **人类审计** | 100条采样轨迹验证自动化验证器的可靠性（87%一致） |
| **定性分析** | 代表性长程任务（LibreOffice自动保存）的轨迹对比 |

### 充分性评估
- **优点**：覆盖多骨干模型（不同能力级别）、多平台（Ubuntu/Windows）、多应用域，并有消融和定性分析，整体实验设计较为全面。
- **公平性考量**：保证各方法使用相同训练预算（OSWorld 1,000条、WindowsAgentArena 600条），评估任务与数据生成种子任务严格分离。
- **潜在不足**：
  - VS Code子集仅11个任务，结果方差大，论文也承认这一局限性。
  - Human Data基线仅在"平台和应用匹配子集"上训练，可能与全量AgentNet数据效果不同。
  - 跨域增强实验仅用Qwen2.5-VL-7B，未覆盖其他骨干。

## 6. 主要结论与发现

1. **ANCHOR生成的数据在OSWorld和WindowsAgentArena上均显著提升性能**：
   - GLM-4.1V-9B：OSWorld从0.47→7.01；WindowsAgentArena从5.49→16.30
   - Qwen2.5-VL-7B：OSWorld从0.93→7.94；WindowsAgentArena从4.39→15.22
   - Qwen3-VL-8B：OSWorld从16.82→20.56；WindowsAgentArena从23.07→30.76

2. **一致优于Task-Driven合成基线和Human Data（AgentNet）**：在几乎所有评估设置下，ANCHOR均超过其他数据来源。

3. **数据规模提升带来持续增益**：在域内数据上，三个模型均随数据量增加而提升；跨域数据（Ubuntu+Windows）在较大规模下也有正向迁移。

4. **步骤级过滤和去噪对监督质量至关重要**：移除后所有模型性能下降（Qwen3-VL-8B：20.56→19.15；Qwen2.5-VL-7B：7.94→7.01；GLM-4.1V-9B：7.01→6.54）。

5. **长轨迹不等于低信号**：ANCHOR生成的17.24步平均长度来自结构化的多阶段工作流（如导航层级设置菜单），而非无约束探索。步骤级质量控制确保了每步的信号密度。

6. **分支策略的价值**：在视觉丰富、决策密集的状态（如LibreOffice Options对话框）分支，可产生覆盖广泛的派生任务族，共享可靠入口路径但覆盖不同设置面板和交互模式。

## 7. 优点

- **降低对模型完美度依赖**：通过种子轨迹锚定，仅需解决局部子任务，而非从头到尾完美执行。
- **系统化多样性与更少游荡**：分支点由UI状态定义，产生目标导向的长轨迹，避免自由探索的低信号问题。
- **步骤级质量控制创新**：
  - 任务条件推理过滤为共享前缀提供多样化、任务特定的解释；
  - 分支后意图一致性去噪保留有效动作和纠错行为，去除噪声。
- **跨平台泛化能力**：从Ubuntu扩展到Windows有正迁移。
- **高成本效益**：每条成功轨迹仅$0.47，明显低于人工标注成本。
- **人工验证保障**：种子验证+合成轨迹审计（87%验证器准确率），双重质量保障。
- **开源**：数据与代码将公开。

## 8. 不足与局限

### 实验覆盖
- **仅限桌面环境**：未在移动端或Web端验证，虽然论文声称管线平台无关，但缺少实证。
- **应用域覆盖有限**：OSWorld和WindowsAgentArena虽具有代表性，但无法覆盖真实世界中全部应用/工作流。
- **VS Code评估子集任务量少**（仅11个），导致结果波动大，影响该域结论可靠性。

### 偏差风险
- **LLM验证器不完美**：人类审计显示87%准确率，13%的边界案例可能引入噪声数据。
- **种子质量依赖人工**：种子轨迹的质量和代表性直接影响分支扩展的质量和多样性。
- **执行期间的任务修订**：将偏离行为"重新解释"为连贯任务可能引入伪目标，产生与原始意图不完全一致的监督信号。
- **数据来源模型偏差**：生成数据依赖Claude Sonnet 4.5和GPT-5.1，可能隐含这些模型的行为偏差和覆盖盲区。

### 方法局限
- **骨干模型在低数据量下性能不单调**（如Qwen3-VL-8B在0.3K时下降），说明格式不匹配问题需更大数据量缓解。
- **未充分研究分支点选择策略的影响**：不同分支数量、位置选择对数据质量的系统敏感性分析不足。
- **语义漂移风险**：运行中任务修订和总结器重写可能使任务描述偏离用户原始意图。

### 可扩展性
- **环境重放成本**：每次分支扩展需要将环境重放到特定状态，可能随轨迹长度和分支数量增加而产生可观的时间成本。
- **未来工作**：更强验证器、改进分支策略、扩展到更多环境和交互模态。

（完）

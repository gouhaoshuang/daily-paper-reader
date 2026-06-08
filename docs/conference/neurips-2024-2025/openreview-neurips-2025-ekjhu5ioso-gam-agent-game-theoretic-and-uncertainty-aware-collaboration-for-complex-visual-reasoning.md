---
title: "GAM-Agent: Game-Theoretic and Uncertainty-Aware Collaboration for Complex Visual Reasoning"
title_zh: GAM-Agent：面向复杂视觉推理的博弈论与不确定性感知协作
authors: "Jusheng Zhang, Yijia Fan, Wenjun Lin, Ruiqi Chen, Haoyi Jiang, Wenhao Chai, Jian Wang, Keze Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=EKJhU5ioSo"
tags: ["query:eca"]
score: 7.0
evidence: 多智能体协作框架
tldr: 现有视觉推理模型常采用单智能体或单一模型，缺乏多视角协作与不确定性处理。GAM-Agent将推理过程建模为非零和博弈，由基座智能体负责视觉感知，关键智能体验证逻辑一致性，并通过不确定性感知控制器动态调整协作，触发多轮辩论。在MMMU、MMBench等基准上取得了更鲁棒的预测结果，展现了多智能体博弈协作的有效性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1142, \"height\": 944, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1430, \"height\": 512, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 685, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1426, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1410, \"height\": 815, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1130, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1126, \"height\": 744, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 974, \"height\": 693, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 884, \"height\": 148, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1276, \"height\": 137, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 958, \"height\": 755, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 961, \"height\": 650, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1074, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 726, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 957, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ekjhu5ioso/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 957, \"height\": 517, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1100, \"height\": 1038, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1096, \"height\": 1070, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1460, \"height\": 1026, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1462, \"height\": 1191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1462, \"height\": 1350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1463, \"height\": 1287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1462, \"height\": 1314, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1464, \"height\": 1421, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ekjhu5ioso/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 1442, \"label\": \"Table\"}]"
motivation: 为提升视觉推理的鲁棒性和可解释性，引入多智能体博弈协作机制，解决单智能体模型的局限性。
method: 提出非零和博弈框架，基座智能体与验证智能体通过结构化声明和不确定性估计进行多轮辩论协作。
result: 在MMMU、MMBench等基准上，预测鲁棒性和准确性显著优于单智能体基线。
conclusion: 博弈论视角下的多智能体协作能有效提升复杂视觉推理任务的性能。
---

## Abstract
We propose **GAM-Agent**, a game-theoretic multi-agent framework for enhancing vision-language reasoning. Unlike prior single-agent or monolithic models, GAM-Agent formulates the reasoning process as a non-zero-sum game between base agents—each specializing in visual perception subtasks—and a critical agent that verifies logic consistency and factual correctness. Agents communicate via structured claims, evidence, and uncertainty estimates. The framework introduces an uncertainty-aware controller to dynamically adjust agent collaboration, triggering multi-round debates when disagreement or ambiguity is detected. This process yields more robust and interpretable predictions. Experiments on four challenging benchmarks—MMMU, MMBench, MVBench, and V*Bench—demonstrate that GAM-Agent significantly improves performance across various VLM backbones. Notably, GAM-Agent boosts the accuracy of small-to-mid scale models (e.g., Qwen2.5-VL-7B, InternVL3-14B) by 5–6\%, and still enhances strong models like GPT-4o by up to 2–3\%. Our approach is modular, scalable, and generalizable, offering a path toward reliable and explainable multi-agent multimodal reasoning.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：现有的视觉-语言模型（VLM）在复杂视觉推理任务中面临多重挑战：多步推理容易出错、视觉输入存在歧义，而单智能体或简单集成方法（如平均、投票）缺乏深度交互和策略协同，难以有效应对这些困难。  
- **研究动机**：受人类专家通过博弈式互动达成共识的启发，作者希望将博弈论引入视觉推理，使多个专用智能体能够通过结构化辩论、共享不确定性估计，动态调整协作策略，从而提升推理的鲁棒性、准确性和可解释性。  
- **整体含义**：提出一个名为 **GAM-Agent** 的框架，将视觉推理形式化为非零和博弈，让基座视觉智能体与关键验证智能体围绕不确定性进行多轮交互，最终收敛到高质量共识。这在多智能体视觉推理领域开辟了新方向。

---

### 2. 论文提出的方法论

- **核心思想**：将多智能体协作建模为 **非零和博弈**，通过量化每个智能体输出的不确定性来指导辩论和权重分配，实现自适应协作。  
- **关键技术细节**：  
  - **两类智能体**：  
    - **基座智能体（Base Agents）**：负责特定视觉感知子任务（物体识别、场景描述、OCR等），生成初始响应和证据。  
    - **关键智能体（Critical Agents）**：验证基座智能体输出的事实准确性、逻辑一致性和完整性（事实检查、完整性检查、逻辑检查）。  
  - **不确定性量化函数 Φ**：  
    - 当可获取 token 概率时，采用 **过程不确定性**：  
      \[
      \Phi_i^{gen+}(R_i)=\frac{1}{T_i}\sum_{t=1}^{T_i}[\alpha H(P_{i,t})+\beta\max(0,1-\Delta_{top}(P_{i,t}))]
      \]  
      其中 \(H\) 是信息熵（反映犹豫），\(\Delta_{top}\) 是 top-2 token 概率差（反映信心不足）。  
    - 否则，采用 **语义标记不确定性**：基于预定义不确定性词汇的频率和强度，经 sigmoid 归一化到 (0,1)。  
  - **初始集成与冲突检测**：根据不确定性计算每个智能体的初始权重 \(w_i^{(0)}\propto e^{-\beta U_i}\)，加权平均得到系统不确定性 \(U_{sys}^{(0)}\)，若超过阈值 \(\theta_U\) 或智能体间冲突分数 \(ConflictScore>\theta_C\) 则触发辩论。  
  - **证据映射与声明解析**：将智能体的非结构化响应解析为结构化元组 \((c_j,\sigma_j,e_j,r_j)\)，其中包含声明、置信度、文本证据、相关视觉区域。  
  - **迭代辩论过程**：每一轮确定争议焦点，各智能体针对性生成论证，动态更新权重（基于不确定性或信心变化），生成新一轮集成响应 \(R^{(k)}\)，计算 \(U_{sys}^{(k)}\)。终止条件：\(U_{sys}^{(k)}<\theta_U\) 或达到最大轮次 \(K_{\max}\) 或相邻轮次系统不确定性变化小于 \(\epsilon\)。  
- **公式与算法流程（文字说明）**：  
  1. 各基座智能体对输入图像和问题产生初始响应 \(R_i\) 及不确定性 \(U_i\)。  
  2. 声明解析与证据映射，形成结构化知识。  
  3. 计算初始权重和系统不确定性，判断是否触发辩论。  
  4. 若触发，进入迭代辩论：识别争议 → 智能体生成论证 → 更新权重 → 集成新响应 → 评估系统不确定性。  
  5. 满足终止条件后输出最终答案 \(R_{final}\)。

---

### 3. 实验设计

- **基准数据集**：MMMU（多学科多模态理解）、MMBench_V11_Test（视觉推理与感知）、MVBench_Test（视频时序推理）、V*Bench（精细视觉搜索，含属性识别和空间推理）。  
- **对比方法**：与5种多智能体框架对比——DMAD、DMPL、ChatEval、MAD、DebUnc，以及单基座模型基线。  
- **使用的VLM骨干**：Qwen2.5VL（7B、72B）、InternVL3（14B、78B）、GPT-4o-0513。  
- **实验设置**：每种框架使用3个基座智能体、3个关键智能体（需要时），最大辩论轮次为3，使用贪心解码。开源模型在本地NVIDIA A100 GPU运行，GPT-4o通过OpenRouter API访问。  
- **消融实验**：在MMBench上对InternVL3-14B进行了5种变体消融（删除多智能体、不确定性、声明解析、辩论、动态权重），并分析了最大辩论轮次、超参数敏感性。  
- **成本分析**：计算了不同配置下每指令的推理成本（token数或美元），并与API商业模式比较。

---

### 4. 资源与算力

- **GPU型号**：NVIDIA A100（40GB）。  
- **数量与时长**：论文未明确说明总GPU数量和训练/推理时长。附录中给出成本估算：AWS p4d.24xlarge实例（8×A100）约$32.77/小时，折算单卡$4.10/小时。开源模型本地部署，用于推理。  
- **API模型**：GPT-4o-0513通过OpenRouter调用，成本按API定价计算。  
- **备注**：论文强调多智能体辩论增加了推理开销，但通过自适应终止条件控制了成本。

---

### 5. 实验数量与充分性

- **实验数量**：  
  - 主实验：5个骨干 × 4个基准 × 6种框架 → 含双表的详细结果（表1、表2）。  
  - 消融实验：5种变体，带4项指标（准确率、平均辩论轮次、触发率、成本）。  
  - 最大辩论轮次研究：从0到9轮，记录准确率和实际轮次。  
  - 专家权重轨迹分析：8个VLM模型 × 3类专家，展示3轮辩论中权重和系统不确定性变化。  
  - 超参数消融（附录）：对β_weight、θ_U、θ_C、α_Φ等5组超参数进行敏感度分析。  
  - 成功/不成功案例分析（附录）。  
- **充分性与公平性**：  
  - 覆盖了从轻量到大型多个VLM，对比了当时主流多智能体方法，消融实验验证了各组件的必要性。  
  - 但缺乏统计显著性检验（如误差条、多次运行标准偏差），可能影响结果可靠性的量化描述。  
  - 未在大规模模型（如100B+）上进行实验，也未在真实应用场景验证。

---

### 6. 论文的主要结论与发现

- GAM-Agent在所有基准和所有VLM骨干上均取得最佳或最优性能，尤其对小模型提升显著（5-6%），对GPT-4o也有2-3%提升。  
- 不确定性驱动的辩论机制有效降低了系统不确定性，平均仅需1.76-2.1轮即可收敛（视模型而定），效率优于固定轮次方法。  
- 消融实验表明：每个组件（多智能体、不确定性量化、声明解析与证据映射、迭代辩论、动态权重）对最终性能均有贡献，缺一不可。  
- 专家权重轨迹显示：系统的动态调整能力随模型规模增大而增强，能自动降低高不确定性专家的影响，专注于可靠信号（如OCR）。  
- 成本-性能分析显示：在本地部署开源模型+GAM-Agent框架，可以达到甚至超越商业API模型的准确率，且成本低数倍。

---

### 7. 优点

- **方法创新**：首次将博弈论与不确定性量化系统性地融入多智能体视觉推理，设计了一套闭环的辩论机制，而非简单的投票或固定规则。  
- **模块化与可扩展**：基座智能体和关键智能体可独立替换，不确定性量化支持多种接入方式（token概率或语义标记），易于集成到不同VLM。  
- **实验全面**：涵盖图像、视频、精细视觉搜索等多种任务，对比了多种多智能体基线，消融和超参数分析详尽。  
- **理论支持**：提供了完整的数学形式化（效用函数、权重解析解、博弈均衡证明框架），增强了方法的可解释性和严谨性。  
- **成本效率**：通过自适应辩论终止，在保持高性能的同时控制了计算开销，并在附录中给出成本对比，证明本地部署的可行性。

---

### 8. 不足与局限

- **额外推理开销**：多智能体辩论需要多次调用VLM，虽可通过自适应终止缓解，但仍比单模型推理消耗更多计算时间。论文未报告实际推理时间。  
- **不确定性估计依赖**：当无法获取token概率时，使用的语义标记方法可能不够精确；不确定性量化误差會影响后续权重分配和辩论质量。  
- **辩论可能不收敛**：在部分复杂或歧义样本中，智能体可能无法达成一致，论文以最大轮次强制终止，但未分析这种情况下的错误模式。  
- **模型规模覆盖有限**：最大实验模型为78B（InternVL3-78B）和72B（Qwen2.5VL-72B），未包含100B+的模型（如Llama-405B等）。  
- **实验统计性**：所有结果无误差条，单次运行，无法评估结果稳定性。  
- **应用限制**：仅使用3个基座智能体和3个关键智能体，更多专家可能带来更丰富的视角但成本更高；未探索专家角色自动生成而非手工预设。  
- **偏差风险**：智能体的输出依赖于基座VLM的训练数据，可能继承偏见；关键智能体的验证标准也未进行公平性检验。

（完）

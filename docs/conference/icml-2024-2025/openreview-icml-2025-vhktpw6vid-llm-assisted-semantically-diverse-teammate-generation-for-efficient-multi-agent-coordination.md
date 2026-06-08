---
title: LLM-Assisted Semantically Diverse Teammate Generation for Efficient Multi-agent Coordination
title_zh: 基于LLM的语义多样化队友生成实现高效多智能体协调
authors: "Lihe Li, Lei Yuan, Pengsen Liu, Tao Jiang, Yang Yu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=Vhktpw6Vid"
tags: ["query:eca"]
score: 6.0
evidence: 通过语义多样化队友生成实现多智能体协调
tldr: 训练泛化智能体需要多样化队友，但现有方法缺乏语义信息。本文提出SemDiv，利用LLM发现语义层次的协调行为并生成多样化队友。实验证明SemDiv提升了智能体在未知环境中的适应性和协调效率。该方法为边缘云协同中的智能体协作训练提供了新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1743, \"height\": 569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1729, \"height\": 631, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1753, \"height\": 539, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 327, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 845, \"height\": 568, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1731, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1728, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1693, \"height\": 763, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1685, \"height\": 582, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vhktpw6vid/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1691, \"height\": 595, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1782, \"height\": 801, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1755, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1780, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1779, \"height\": 583, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1780, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1780, \"height\": 581, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vhktpw6vid/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1780, \"height\": 578, \"label\": \"Table\"}]"
motivation: 训练泛化智能体需要多样化的队友，但现有方法缺乏语义信息，效率低下。
method: 提出SemDiv框架，利用LLM发现和学习语义级别的多样化协调行为。
result: SemDiv生成语义丰富的队友，提升了智能体在未知环境中的适应性和协调效率。
conclusion: 语义驱动的队友生成为多智能体协作提供更高效和可迁移的训练策略。
---

## Abstract
Training with diverse teammates is the key for learning generalizable agents. Typical approaches aim to generate diverse teammates by utilizing techniques like randomization, designing regularization terms, or reducing policy compatibility, etc. However, such teammates lack semantic information, resulting in inefficient teammate generation and poor adaptability of the agents. To tackle these challenges, we propose Semantically Diverse Teammate Generation (SemDiv), a novel framework leveraging the capabilities of large language models (LLMs) to discover and learn diverse coordination behaviors at the semantic level. In each iteration, SemDiv first generates a novel coordination behavior described in natural language, then translates it into a reward function to train a teammate policy. Once the policy is verified to be meaningful, novel, and aligned with the behavior, the agents train a policy for coordination. Through this iterative process, SemDiv efficiently generates a diverse set of semantically grounded teammates, enabling agents to develop specialized policies, and select the most suitable ones through language-based reasoning to adapt to unseen teammates. Experiments show that SemDiv generates teammates covering a wide range of coordination behaviors, including those unreachable by baseline methods. Evaluation across four MARL environments, each with five unseen representative teammates, demonstrates SemDiv's superior coordination and adaptability. Our code is available at https://github.com/lilh76/SemDiv.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：在开放多智能体环境中，智能体经常需要与具有不同协调行为的未知队友协作（例如自动驾驶遇到不同人类驾驶员）。传统多智能体强化学习（MARL）方法在固定队友上训练，容易过拟合，泛化性差。
- **核心问题**：现有通过随机化、正则化或降低策略兼容性等方法生成的队友缺乏**语义信息**，导致两个挑战：(1) 队友策略空间探索低效（只在策略层面追求差异，而非发现语义层面的新协调行为）；(2) 智能体无法利用语义信息，只能通过试错交互适应队友，在昂贵任务中难以部署。
- **提出的解决方案**：利用大语言模型（LLM）在语义层面发现并学习多样化的协调行为，生成具有语义信息的队友，并训练智能体通过语言推理快速适应未知队友。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：提出 **SemDiv**（Semantically Diverse Teammate Generation）框架，迭代地利用LLM生成自然语言描述的协调行为，将其转化为奖励函数训练队友策略，验证后智能体通过多头策略网络持续学习，最终通过LLM选择最合适的策略头来适应未知队友。
- **关键技术细节**：
  - **迭代生成语义多样化协调行为**：LLM行为生成器根据任务描述、先前行为及相似性反馈，生成新的行为描述，确保逐步覆盖不同行为。
  - **将行为转化为队友策略**：LLM奖励生成器根据行为描述编写可执行的奖励函数（Python代码），结合任务奖励训练队友策略。奖励权重λ₂从1衰减到0，使队友学会完成任务。
  - **策略验证**：检查队友是否完成任务、奖励是否有效、行为是否对齐、是否与先前队友不同（通过式(2)的兼容性判断）。
  - **持续学习与多头架构**：每个智能体网络由共享特征提取器 \(f_{\phi_i}\) 和多个策略头 \(\{h_{\psi_{i,j}}\}\) 组成。每生成一个新队友，就新增一个策略头进行训练，同时通过正则化项 \(\alpha \|\phi_i - \bar{\phi}_i\|_p\) 防止灾难性遗忘。
  - **执行时LLM头选择**：根据未知队友的自然语言描述，LLM选择器从已学行为中选择最匹配的策略头，无需试错交互。
- **公式与算法流程**：文中主要优化目标为式(1)、(3)、(4)。整体流程如图2所示：a) 生成协调行为；b) 训练对齐的队友策略；c) 持续训练智能体。

## 3. 实验设计：使用了哪些数据集 / 场景，它的 benchmark 是什么，对比了哪些方法

- **环境（场景）**：四个经典MARL协调环境：
  - Level-Based Foraging (LBF) – 网格世界，收集食物。
  - Predator-Prey (PP) – 2D捕食者-猎物。
  - StarCraft Multi-Agent Challenge v2 (SMACv2) – 星际争霸微操作。
  - Google Research Football (GRF) – 谷歌足球。
- **测试队友**：每个环境训练5个具有不同代表性协调行为的未知队友（如GRF中偏好传球次数等），用于评估泛化性能。
- **评估指标**：
  - R1：任务成功率。
  - R2：满足队友偏好协调行为的成功率。
- **对比方法**：
  - **两阶段种群训练方法**：FCP、MEP、LIPO（生成队友种群后训练智能体）。
  - **迭代式方法**：Macop（通过最小化兼容性生成队友，类似SemDiv但无语义）。
  - **消融/变体**：SemDiv-PBT（用SemDiv队友做种群训练）、SemDiv-Dist（用T5嵌入距离选头）、SemDiv-R1/R2（作为上界）、LLM-Agent（纯LLM决策）。
  - **Oracle**：测试队友的自对弈性能作为上界。

## 4. 资源与算力：如果文中有提到，请总结使用了多少算力（GPU 型号、数量、训练时长等）。若未明确说明，也请指出这一点

- 文中未明确说明GPU型号、数量和训练时长。仅提到：
  - 使用GPT-4o（gpt-4o-2024-08-06）作为LLM。
  - 单次运行SemDiv的OpenAI API费用约$0.10，整个项目总费用约$300。
  - MARL算法使用MAPPO（GRF）和VDN（其他环境），基于PyMARL和HARL代码库，默认超参数。
- 未提供具体GPU算力信息，因此无法量化。

## 5. 实验数量与充分性：大概做了多少组实验（如不同数据集、消融实验等），这些实验是否充分、是否客观、公平

- **主要实验**：
  - 表1：在4个环境上，每种方法（包括SemDiv、多个消融、8种baseline）重复3个随机种子，报告均值±标准差。共约 (1+1+2+2+2+2+2+2+2+2+1) = 17种方法 × 4环境 × 5队友 × 3种子 × (R1,R2) → 大量实验。
  - 案例研究（Section 4.3）：GRF单次运行细节。
  - 图5：在GRF和LBF上，改变训练队友数量（1,3,6,12,24,48）比较性能。
  - 附录E：每个测试队友的详细结果（表3-7）、行为描述歧义性影响（图7(a)(b)）、LLM质量影响（图7(c)）。
- **充分性**：实验覆盖多种环境、多种baseline、多种消融、队友数量变化、歧义性和LLM变体，设计较充分。对比方法均为近期代表性工作，比较公平。但缺少真实人类队友实验，且所有队友由代码训练，非真实人类。

## 6. 论文的主要结论与发现

- SemDiv生成的队友覆盖了baseline无法达到的协调行为（如GRF中多次传球），且语义多样性显著优于策略层面方法（如t-SNE可视化显示更广的轨迹分布）。
- 在4个环境中，SemDiv在R1上平均优于最好baseline（Macop）19%，R2上优于39%。
- 多头架构相比单策略网络（PBT变体）效果更好，证明单策略难以适应多模态队友。
- LLM头选择器接近上界（-R1/-R2），而依赖嵌入距离的SemDiv-Dist显著下降，说明语言推理比单纯语义相似度更有效。
- 纯LLM智能体（LLM-Agent）在复杂环境（SMACv2、GRF）中性能严重退化，表明MARL的必要性。
- 增加训练队友数量时，SemDiv比FCP扩展更高效，且多头架构随数量增长优势更加明显。

## 7. 优点：方法或实验设计上有哪些亮点

- **语义驱动**：首次将LLM引入队友生成，实现从“策略级多样性”到“语义级多样性”的飞跃，可解释性强。
- **端到端流程**：从行为生成→奖励函数→策略训练→验证→持续学习→语言选头，形成完整闭环。
- **高效性**：语义探索比策略随机搜索更高效，且用LLM选头避免试错交互，适合部署。
- **实验全面**：覆盖多个难度递增的环境，与多种经典及最新方法对比，消融实验设计合理（如多头 vs 单头、LLM选头 vs 嵌入距离）。
- **代码开源**：提供GitHub仓库，可复现。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **LLM依赖**：使用GPT-4o，成本较高（$300/整个项目），且LLM可能生成有偏或失败的行为，需迭代验证。
- **实验局限**：
  - 所有队友均为代码训练的模拟队友，未涉及真实人类队友，实际人类行为可能更复杂、噪声更大。
  - 环境规模较小（LBF 6×6，PP 5个猎物等），未在更大规模（如多机器人、自动驾驶仿真）上验证。
  - 训练队友数量最大48个，但未说明在更多队友时多头的可扩展性边界。
- **偏差风险**：LLM本身可能存在社会文化偏见，生成的行为可能偏向某些模式，导致智能体适应偏差。
- **应用限制**：框架需要提前为每个环境编写任务描述和API接口；奖励函数自动生成可能不稳定，需要手动调整阈值和验证步骤。
- **未讨论安全性**：未考虑队友可能对抗性行为或环境中的分布外挑战。

（完）

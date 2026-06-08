---
title: Reflective Multi-Agent Collaboration based on Large Language Models
title_zh: 基于大型语言模型的反思式多智能体协作
authors: "Xiaohe Bo, Zeyu Zhang, Quanyu Dai, Xueyang Feng, Lei Wang, Rui Li, Xu Chen, Ji-Rong Wen"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=wWiAR5mqXq"
tags: ["query:eca"]
score: 9.0
evidence: "通过自我反思机制增强LLM智能体的协作能力，直接匹配'协作'需求"
tldr: LLM多智能体系统虽能处理复杂任务，但协作能力仍有提升空间。COPPER框架引入自我反思机制，通过微调共享反射器，利用反事实PPO机制自动调整演员模型的提示词，并使用反事实奖励评估每个智能体的贡献。该方法显著提升了多智能体系统的协作效果与任务完成质量。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1424, \"height\": 429, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 652, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1338, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1340, \"height\": 409, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1341, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1340, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1340, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1340, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 424, \"height\": 353, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1429, \"height\": 424, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 514, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1339, \"height\": 402, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1343, \"height\": 403, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1341, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1474, \"height\": 833, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1430, \"height\": 1425, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-wwiar5mqxq/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1427, \"height\": 1644, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-wwiar5mqxq/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1431, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-wwiar5mqxq/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1428, \"height\": 210, \"label\": \"Table\"}]"
motivation: 现有LLM多智能体系统的协作能力不足，需要有效的反思机制来提升。
method: 提出COPPER框架，包含共享反射器，通过反事实PPO机制微调以自动优化智能体提示。
result: 在多个任务上，该方法提升了多智能体系统的协作性能与任务完成质量。
conclusion: 反事实反思是提升多智能体协作的有效训练策略。
---

## Abstract
Benefiting from the powerful language expression and planning capabilities of Large Language Models (LLMs), LLM-based autonomous agents have achieved promising performance in various downstream tasks. Recently, based on the development of single-agent systems, researchers propose to construct LLM-based multi-agent systems to tackle more complicated tasks. In this paper, we propose a novel framework, named COPPER, to enhance the collaborative capabilities of LLM-based agents with the self-reflection mechanism. To improve the quality of reflections, we propose to fine-tune a shared reflector, which automatically tunes the prompts of actor models using our counterfactual PPO mechanism. On the one hand, we propose counterfactual rewards to assess the contribution of a single agent’s reflection within the system, alleviating the credit assignment problem. On the other hand, we propose to train a shared reflector, which enables the reflector to generate personalized reflections according to agent roles, while reducing the computational resource requirements and improving training stability. We conduct experiments on three datasets to evaluate the performance of our model in multi-hop question answering, mathematics, and chess scenarios. Experimental results show that COPPER possesses stronger reflection capabilities and exhibits excellent generalization performance across different actor models.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **背景**：大型语言模型（LLM）驱动的自主智能体在多种下游任务中表现优异，近期研究者开始构建基于LLM的多智能体系统以处理更复杂的任务。
- **核心问题**：尽管多智能体系统通过协作可促进事实性、推理和发散思维，但现有协作框架（如基于提示的AutoGen、MetaGPT等）受限于LLM的上下文理解能力，未能充分挖掘智能体的协作潜力。直接收集大量协作数据进行微调会损害模型的通用能力。
- **研究动机**：利用自我反思（self-reflection）机制将环境奖励转化为语言反馈，为多智能体协作提供额外上下文，但预训练冻结LLM产生的反射质量有限。Retroformer在单智能体系统中通过策略优化训练插件反射器，但扩展到多智能体时面临**信用分配问题**（无法区分各智能体反射的贡献）和**个性化反射需求**（反射器数量随智能体数量线性增长，计算资源需求高）。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想
- 提出 **COPPER** 框架：利用**反事实PPO机制**微调一个**共享反射器**，自动调整演员模型的提示词，提升多智能体协作能力。
- 关键创新：
  - **反事实奖励**：评估单个智能体反射的贡献，缓解信用分配问题。
  - **共享反射器**：统一训练一个反射器，通过提示区分角色，减少计算资源并提高训练稳定性。

### 2.2 关键技术细节

#### (1) 多智能体反射框架
- 每个智能体按预定顺序轮流产生响应，维护共享消息池。
- 引入**上下文模型**（短时记忆）递归更新交互历史，解决token限制问题。
- 反射过程：
  - 给定问题 \(k\)、试验次数 \(\lambda\)，智能体 \(i\) 的反射器输入：角色 \(p_i\)、各智能体短时记忆、环境奖励 \(r_{k,\lambda}\)。
  - 输出反射 \(y_{k,\lambda}^i\) 存入长时记忆，作为下一轮演员模型的额外上下文。

#### (2) 共享反射器的优化

**a. 指令与响应收集**
- 收集所有智能体、所有任务、所有试验的反射数据 \(D = \{(x_{k,\lambda}^i, y_{k,\lambda}^i)\}\)。

**b. 反事实奖励**
- **总体奖励**：\(G_{k,\lambda}^i = r_{k,\lambda+1} - r_{k,\lambda}\)
- **边际奖励**：单独移除智能体 \(i\) 的反射（保留其他智能体反射），获得新奖励 \(\hat{r}_{k,\lambda+1}\)，计算 \(\hat{G}_{k,\lambda}^i = \hat{r}_{k,\lambda+1} - r_{k,\lambda}\)
- **反事实奖励**：\(\tilde{G}_{k,\lambda}^i = G_{k,\lambda}^i - \hat{G}_{k,\lambda}^i\)，反映该反射的真实贡献。

**c. 反事实近端策略优化（Counterfactual PPO）**
- **步骤1：监督微调（SFT）**：用反事实奖励为正的反射数据训练 \(\pi_{\text{SFT}}\)，优化交叉熵损失。
- **步骤2：奖励模型训练**：训练回归奖励模型 \(R_\phi^{\text{CF}}\)，最小化MSE损失。
- **步骤3：PPO优化**：初始化 \(\pi_{\text{SFT}}\)，对随机样本生成响应，用奖励模型打分，优化PPO损失：
  \[
  L_{\text{PPO}}(\theta) = -\mathbb{E}_{x \sim D_{\text{CF}}} \mathbb{E}_{y \sim \pi_{\theta}^{\text{RL}}(x)} \left[ R_\phi^{\text{CF}}(x,y) - \beta \log \frac{\pi_{\theta}^{\text{RL}}(y|x)}{\pi_{\text{SFT}}(y|x)} \right]
  \]
- **共享反射器**：所有智能体共用同一反射器，输入中包含角色信息以生成个性化反射。

## 3. 实验设计

### 3.1 数据集与场景
| 数据集 | 领域 | 任务描述 |
|--------|------|----------|
| HotPotQA | 多跳问答 | 需要多步检索推理 |
| GSM8K | 数学 | 小学数学应用题 |
| Checkmate in One Move | 国际象棋 | 给定棋局找出一步杀 |
| ALFWorld（附录C） | 具身环境 | 交互式任务 |

### 3.2 基准方法
- **CoT**：链式思维推理（数学、象棋）
- **ReAct**：推理+行动（问答）
- **Reflexion (GPT-3.5 / LongChat)**：多智能体版本，使用GPT-3.5或LongChat作为反射器，无微调
- **Retroformer (Multi)**：为每个智能体独立微调反射器（单智能体方法扩展）
- **COPPER**：本文方法

### 3.3 评估指标
- 精确匹配准确率（Exact Match Accuracy）
- 奖励函数：HotPotQA用F1分数，其余用精确匹配分数。

## 4. 资源与算力

- **硬件**：4张 NVIDIA A800-80G GPU（实验在四卡上完成）
- **模型**：演员模型使用 GPT-3.5 (gpt-3.5-turbo)；反射器基础模型为 LongChat-7b-16k（另实验 Llama-3-8b-16k）；奖励模型使用 GPT-2
- **训练细节**：
  - LoRA 高效微调
  - SFT：epoch {1,2,3,4}，batch size {64,128,256}，学习率 {1e-4,2e-4,3e-4,5e-4}（网格搜索验证集100例）
  - PPO：学习率 {1e-5,2e-5,3e-5,5e-5}
  - 奖励模型：学习率5e-5，epoch 3，batch size 16
- **未明确**：训练总时长（文中未给出具体小时数，仅说明在四张A800上运行）

## 5. 实验数量与充分性

- **主要结果**（图3）：三个数据集上对比5个基线，5次试验（trials）后的成功率曲线。
- **消融实验**（图4）：
  - 去除反事实奖励（w/o CF）
  - 去除PPO（w/o PPO）
  - 与原始 Reflexion (LongChat) 对比
- **推广性实验**（图5）：将COPPER（基于GPT-3.5训练）直接用于GPT-4演员模型。
- **反事实奖励通用性**（图6）：将反事实奖励用于SFT筛选正例（CF SFT vs 普通SFT）。
- **共享反射器效果**（图7）：对比共享反射器与独立反射器（非共享）在SFT和PPO下的表现。
- **角色信息必要性**（图8）：去除角色信息（no-profile setting）对比。
- **不同基座反射器**（图9）：使用Llama-3作为基础反射器微调（GSM8K）。
- **额外实验**：ALFWorld（附录C）、部分信息设置（附录E）、案例研究（附录F）。
- **公平性**：测试阶段温度设为0以保证可重复性；评估100个随机样本（遵循前人做法如Retroformer、Reflexion）。实验覆盖多种任务和多智能体协作范式（师生式、辩论式），消融和变体分析充分。

## 6. 主要结论与发现

1. **反射机制显著提升协作性能**：多智能体反射框架本身（使用GPT-3.5或LongChat）即可在初始成功率基础上大幅提升（HotPotQA +15.9%~22.7%）。
2. **COPPER效果最佳**：相比所有基线，COPPER在5次试验后达到最高成功率：
   - HotPotQA：提升31.8%
   - GSM8K：提升18.5%
   - Checkmate in One Move：提升86.4%
3. **反事实奖励和PPO必不可少**：消融实验显示，去除其中任一部分均导致性能下降。
4. **共享反射器优于独立反射器**：共享反射器能利用更多训练数据，产生更好反射效果。
5. **强泛化能力**：在GPT-3.5上训练的COPPER可直接应用于GPT-4演员模型，性能接近GPT-4自反射。
6. **反事实奖励适用于其他微调方法**：用于SFT筛选正例时也优于普通SFT。
7. **角色信息重要**：去除角色信息后性能下降，COPPER在无角色设置下仍优于其他无角色基线。

## 7. 优点

- **方法创新**：首次将反事实奖励引入多智能体反射优化，有效缓解信用分配问题；共享反射器设计既保持个性化又降低资源消耗。
- **实验全面**：覆盖问答、数学、象棋、具身环境（ALFWorld）等多个领域，进行消融、泛化、基座模型替换等丰富实验。
- **实用性**：不需要微调演员模型（使用冻结GPT-3.5/4），仅微调小型反射器，保持通用能力。
- **泛化性强**：训练好的反射器可直接用于不同能力（GPT-4）的演员模型，无需重新训练。
- **代码开源**：提供匿名代码仓库，实验可复现。

## 8. 不足与局限

- **数据效率**：构建反事实奖励需要额外执行一次交互（去除单个智能体反射后重跑），数据收集成本较高。论文提及需要更高效的数据收集方法。
- **长时记忆限制**：当前使用滑动窗口（最大容量），未来可扩展为向量嵌入等更先进结构。
- **测试规模**：评估样本量仅为100（受计算资源限制，类似前作），统计稳定性有待更大规模验证。
- **仅针对特定协作范式**：实验涵盖师生式和辩论式，但未在更多复杂动态协作场景（如社会模拟）中验证。
- **基座模型依赖**：反射器基于LongChat/Llama-3等开源模型微调，可能不适用于所有闭源API场景。
- **未报告误差棒**：因使用商业API成本高，未重复多次实验报告方差，但遵循该领域常见做法。

（完）

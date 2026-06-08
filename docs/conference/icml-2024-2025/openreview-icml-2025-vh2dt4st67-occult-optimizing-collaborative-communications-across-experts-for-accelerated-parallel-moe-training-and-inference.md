---
title: "Occult: Optimizing Collaborative Communications across Experts for Accelerated Parallel MoE Training and Inference"
title_zh: Occult：优化专家间协作通信以加速并行MoE训练与推理
authors: "Shuqing Luo, Pingzhi Li, Jie Peng, Yang Zhao, Yu Cao, Yu Cheng, Tianlong Chen"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=vh2Dt4sT67"
tags: ["query:eca"]
score: 6.0
evidence: 优化分布式MoE训练中的协作通信
tldr: "混合专家模型（MoE）中的全连接通信开销占总运行时间40%以上，严重阻碍分布式扩展。本文定义“协作通信”概念并创新系统级和算法级优化：利用专家共激活模式减少通信量。实验表明在大规模训练中显著降低延迟，加速比接近理论最优。该工作为分布式机器学习中的通信优化提供了新思路，但与移动或边缘代理无直接关联。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 843, \"height\": 695, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 831, \"height\": 597, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 826, \"height\": 273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1755, \"height\": 359, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1681, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 622, \"height\": 212, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 622, \"height\": 235, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1667, \"height\": 340, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1761, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 853, \"height\": 657, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1758, \"height\": 397, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1760, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 841, \"height\": 703, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vh2dt4st67/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1758, \"height\": 433, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 846, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 851, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1773, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1772, \"height\": 1092, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 1094, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vh2dt4st67/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1773, \"height\": 1094, \"label\": \"Table\"}]"
motivation: MoE中全连接通信开销极大，影响分布式训练的可扩展性。
method: 定义协作通信，提出系统与算法级创新以减少专家间通信成本。
result: 在大规模训练中显著降低通信延迟，加速比接近理论最优。
conclusion: 所提方法有效提升了MoE分布式训练的效率和可扩展性。
---

## Abstract
Mixture-of-experts (MoE) architectures could achieve impressive computational efficiency with expert parallelism, which relies heavily on all-to-all communication across devices. Unfortunately, such communication overhead typically constitutes a significant portion of the total runtime, hampering the scalability of distributed training and inference for modern MoE models (consuming over 40% runtime in large-scale training). In this paper, we first define $\textit{collaborative communication}$ to illustrate this intrinsic limitation, and then propose system- and algorithm-level innovations to reduce communication costs. Specifically, given a pair of experts co-activated by one token, we call them as $\textit{collaborated}$, which comprises $2$ cases as $\textit{intra-}$ and $\textit{inter-collaboration}$, depending on whether they are kept on the same device. Our pilot investigations reveal that augmenting the proportion of intra-collaboration can accelerate expert parallel at scale. It motivates us to strategically $\underline{\texttt{o}}$ptimize $\underline{\texttt{c}}$ollaborative $\underline{\texttt{c}}$omm$\underline{\texttt{u}}$nication for acce$\underline{\texttt{l}}$era$\underline{\texttt{t}}$ed MoE training and inference, dubbed $\textbf{\texttt{Occult}}$. Our designs are capable of $\underline{either}$ delivering exact results with reduced communication cost, $\underline{or}$ controllably minimizing the cost with collaboration pruning, materialized by modified fine-tuning. Comprehensive experiments on various MoE-LLMs demonstrate that $\texttt{Occult}$ can be faster than popular state-of-the-art inference or training frameworks (over 50% speed up across multiple tasks and models) with comparable or superior quality compared to the standard fine-tuning. Codes will be available upon acceptance.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
混合专家模型（MoE）通过专家并行（expert parallelism）实现高效计算扩展，但该技术依赖设备间的全连接通信（all-to-all communication）。在大规模训练中，这种通信开销通常占总运行时长的 **40% 以上**，成为分布式训练和推理的可扩展性瓶颈。论文首先定义了“协作通信”（collaborative communication）这一概念，指出每个token激活的专家对（称为“协作”专家）有两种情况：位于同一设备（**内部协作**）或不同设备（**外部协作**）。增强内部协作比例能有效加速专家并行。基于此，作者提出系统-算法协同设计方案 **Occult**，旨在优化协作通信以加速MoE训练与推理。

## 2. 方法论
### 核心思想
- 将MoE的全连接通信问题重新表述为**协作通信优化**问题：最大化内部协作（减少通信复制），最小化外部协作。
- 提出**CT（Communication Complexity）**度量指标，表示每个token的平均复制次数，与运行时强线性相关（见表1）。理论上最优CT下界为 \(\lceil k \cdot N_d / N_e \rceil\)。

### 关键技术细节
1. **稀疏矩阵乘法（SMM）内核**：设计双向重索引矩阵（BRIM）数据结构，统一管理三种张量状态（ORI原始、SFD简化、EPD扩展），实现高效的Dispatch、Combine和专家计算。BRIM提供散射（Scattering）和合并（Merging）两种函数，分别对应状态转换。

2. **专家放置重调度**：利用配置数据集的协作频率图 \(P\)，通过类似最远点采样的聚类算法（Algorithm 1）将专家均匀分配到 \(N_d\) 个设备，最大化内部协作。无需修改模型即可降低约20%的CT。

3. **协作剪枝（Collaboration Pruning）**：通过算法级修改路由策略，将每个token的top-k专家选择限制在预定义的 \(N_d\) 个设备范围内，超出范围的专家被替代。提供两种剪枝准则：
   - **基于路由分数**：按分数排序，只从目标设备范围内选择专家。
   - **基于专家相似性**：利用配置数据集的logits余弦相似度构建相似性表 \(T\)，替换为最相似的合法专家。

两种剪枝均可通过微调（fine-tuning）恢复模型质量。

## 3. 实验设计
### 数据集/场景
- **微调数据集**：Alpaca。
- **评测基准**：6个主流NLP任务：Winogrande、WSC、PIQA、RACE、MathQA、RTE。另有完整23个基准（附录B）包括MMLU、HellaSwag、BoolQ、COQA等。
- **任务类型**：预填充（Prefilling，长序列推理）、解码（Decoding，并发生成）、训练（微调）。

### Benchmark与对比方法
- **推理框架**：vLLM、HuggingFace。
- **训练框架**：PyTorch FSDP、DeepSpeed。
- **MoE库**：Tutel、MegaBlocks（含块稀疏矩阵乘法和分组GeMM）。
- **消融设置**：无剪枝（仅重调度）、1 GPU剪枝、2 GPU剪枝；路由分数剪枝 vs 相似性剪枝。

### 模型
- OLMoE-1B-7B（8个专家，top-2）
- Qwen1.5-MoE-A2.7B（4个专家，top-2）
- DeepSeek-MoE（6个专家，top-2）

## 4. 资源与算力
文中明确说明：
- **硬件**：单节点，NVIDIA A6000 GPU（48GB HBM），通过PCIe连接。
- **软件**：BFloat16参数和激活，Float32原子加操作。
- **未明确说明**训练时长（例如微调步数或总时间），但提到了训练实验评估了平均每步延迟（1k迭代），序列长度512 tokens。未提及具体使用的GPU数量在不同实验中的变化（如4/8/16 GPU实验）。

## 5. 实验数量与充分性
### 实验规模
- **性能对比**：对三种MoE模型，分别在预填充、解码、训练三个任务上进行延迟对比，涵盖不同batch size。每个任务均与Tutel、MegaBlocks、vLLM、FSDP、DeepSpeed等对比。
- **剪枝效果评估**：23个NLP基准（附录表3-5），分别测试无剪枝、1/2设备剪枝（路由分数和相似性两种），与原始模型和标准SFT对比。
- **消融实验**：CT与运行时相关性（表1）、专家放置重调度效果、不同设备数剪枝效果（图7）、不同GPU数扩展性（图12）。
- **可视化分析**：专家协作模式变化（图8）。

### 充分性与公平性
- 实验覆盖了主流MoE架构和常见任务，对比方法为当前流行框架，实验条件一致（相同GPU、batch size、序列长度等）。但**未包含**与最新MoE优化方案（如Janus、Hexa-MoE）的直接对比，也未在更大规模集群（如数十GPU）上验证可扩展性。此外，所有实验仅在一个节点内（PCIe连接）进行，未涉及跨节点网络（如InfiniBand）。

## 6. 主要结论与发现
1. **CT与运行时强线性相关**，可作为通信预算的有效度量。
2. **专家放置重调度**无需修改模型即可降低约20%的CT和运行时。
3. **协作剪枝**（尤其是相似性剪枝）在2设备约束下**保持甚至提升模型质量**，同时显著加速（1.5×以上）。
4. Occult在预填充、解码、训练中均优于Tutel、MegaBlocks、vLLM等基准，**支持更大batch size**（内存效率更高）。
5. Occult可扩展到更多GPU（8/16路专家并行），且延迟增长趋势稳定。

## 7. 优点
- **创新视角**：将通信问题重新定义为协作通信，并引入CT指标，直观且可优化。
- **系统-算法协同设计**：同时提供“无精度损失”的放置重调度和“可控精度损失”的剪枝方案，灵活性高。
- **高效实现**：BRIM数据结构和稀疏矩阵乘法内核专为减少内存访问和加速all-to-all设计。
- **实验充分**：覆盖三种前沿MoE模型、多种任务，与主流框架对比，效果一致优越。
- **兼容性**：Occult与现有框架正交，可集成使用。

## 8. 不足与局限
- **实验环境局限**：所有实验仅在单节点PCIe连接GPU上进行，未评估跨节点网络（如RDMA）下的性能，实际大规模部署可能有所不同。
- **对比方法覆盖不足**：未与最新MoE优化库（如Janus、Hexa-MoE）或算法（如Pre-gated MoE）直接比较。
- **资源需求未详细报告**：未说明微调总耗时或显存消耗细节，仅给出每步延迟。
- **剪枝质量依赖配置数据**：相似性表和放置重调度均需额外配置数据集，可能引入数据偏差。
- **载荷均衡未解决**：文中提到负载均衡问题仍待研究，剪枝可能加剧专家负载不均。
- **可扩展性验证有限**：最多仅测试16 GPU，未验证更大规模（如64 GPU+）下的通信优化效果。

（完）

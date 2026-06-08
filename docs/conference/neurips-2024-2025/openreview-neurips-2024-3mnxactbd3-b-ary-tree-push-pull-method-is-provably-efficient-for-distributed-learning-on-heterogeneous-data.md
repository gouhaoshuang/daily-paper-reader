---
title: B-ary Tree Push-Pull Method is Provably Efficient for Distributed Learning on Heterogeneous Data
title_zh: B-ary树推拉方法在异构数据分布式学习中的高效性证明
authors: "Runze You, Shi Pu"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=3MnXAcTBD3"
tags: ["query:eca"]
score: 7.0
evidence: 基于peer-to-peer通信的分布式学习算法
tldr: 分布式学习中多个代理协同优化局部代价函数，但现有算法通信效率低或收敛慢。本文提出B-ary树推拉方法（BTPP），利用两颗B-ary生成树分发参数和梯度，每个代理每轮仅与B+1个邻居交互，在非凸光滑目标上实现了线性加速和近最优的瞬态迭代次数。该方法为分布式边缘云代理架构提供了高效的通信机制。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1106, \"height\": 326, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1355, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1355, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1349, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1356, \"height\": 481, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1350, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1338, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3mnxactbd3/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1341, \"height\": 442, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-3mnxactbd3/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1392, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-3mnxactbd3/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1398, \"height\": 348, \"label\": \"Table\"}]"
motivation: 分布式学习中代理需要高效通信以协同优化，现有方法在异构数据下收敛慢且通信开销大。
method: 提出B-ary树推拉方法（BTPP），利用两颗B-ary生成树分别进行参数和梯度分发，每个代理每轮仅与有限邻居通信。
result: 理论分析表明BTPP在非凸光滑目标上实现线性加速，且瞬态迭代次数为~O(n)，优于现有最优结果。
conclusion: BTPP提供了一种通信高效的分布式学习算法，特别适用于节点拓扑受限的边缘云场景。
---

## Abstract
This paper considers the distributed learning problem where a group of agents cooperatively minimizes the summation of their local cost functions based on peer-to-peer communication. Particularly, we propose a highly efficient algorithm, termed ``B-ary Tree Push-Pull'' (BTPP), that employs two B-ary spanning trees for distributing the information related to the parameters and stochastic gradients across the network. The simple method is efficient in communication since each agent interacts with at most $(B+1)$ neighbors per iteration. More importantly, BTPP achieves linear speedup for smooth nonconvex objective functions with only $\tilde{O}(n)$ transient iterations, significantly outperforming the state-of-the-art results to the best of our knowledge.

---

## 论文详细总结（自动生成）

### 论文总结：B-ary Tree Push-Pull Method is Provably Efficient for Distributed Learning on Heterogeneous Data

#### 1. 核心问题与研究动机

- **背景**：分布式学习场景中，一组智能体（agents）通过点对点通信协作最小化各自局部损失函数的和。传统 centralized 方法通信开销大，decentralized 方法虽降低通信成本但收敛速度受网络拓扑影响，尤其在数据异构时存在“瞬态时间”（transient iterations）问题。
- **问题**：如何在保证每轮通信量小（每个节点只与常数个邻居交互）的前提下，显著缩短瞬态时间，实现线性加速（linear speedup）？现有方法如 D2、DSGD、RelaySGD 等在非凸光滑目标下的瞬态时间通常为 O(n³) 或 O(n⁷)，亟需改进。
- **整体含义**：提出 BTPP 算法，通过精心设计的 B-ary 生成树结构，使得瞬态时间降至 ~O(n)（非凸）和 ~O(1)（强凸），大幅领先现有最优结果，为分布式学习提供了高效、实用的通信拓扑方案。

#### 2. 方法论：B-ary Tree Push-Pull (BTPP)

- **核心思想**：使用两棵有向生成树：Pull Tree（GR）用于分发模型参数，Push Tree（GC）用于聚合随机梯度。树结构为 B-ary（B 为分支因子），根节点为 1，其余节点按层编号。
- **关键技术细节**：
  - **通信图设计**：GR 中每个节点有 1 个父节点和最多 B 个子节点（叶子层除外）；GC 是 GR 的反向图，每个节点有 B 个父节点和 1 个子节点。根节点 1 有自环。
  - **更新规则**（算法 1）：每轮迭代 t，各节点 i 从父节点拉取更新后的模型参数（减去梯度跟踪变量），将自身梯度跟踪变量推送给子节点，再更新本地参数和梯度跟踪器。具体公式：
    - `X^{(t+1)} = R (X^{(t)} - γ Y^{(t)})`
    - `Y^{(t+1)} = C Y^{(t)} + G(X^{(t+1)}, ξ^{(t+1)}) - G(X^{(t)}, ξ^{(t)})`
    其中 R、C 分别为 GR 和 GC 对应的 0-1 权重矩阵（R 行随机，C 列随机），Y(0) = G(X(0), ξ(0))。
  - **特点**：
    - 每个节点每轮最多与 (B+1) 个邻居通信，通信开销 Θ(1)。
    - 由于树结构，梯度跟踪变量最终只在根节点 1 处汇总全局梯度，实现精确聚合。
    - 根节点 1 的输出 x1 作为最终结果。
- **收敛理论**（定理 2.1 & 2.4）：
  - 非凸光滑：步长 γ 适当选取后，平均梯度范数的上界中主导项为 O(1/√(nT))，当 T = Θ(n log¹²(n)) 时线性加速，瞬态时间为 ~O(n)。
  - 强凸光滑：误差界中主导项为 ~O(1/(nT))，瞬态时间为 ~O(1)（即常数级），优于之前的 ~O(n)。

#### 3. 实验设计

- **任务与数据集**：
  - **Logistic回归**（非凸正则化）使用合成数据：n=100, p=500, J=1000, σ_h=0.8，每个节点生成服从不同分布的局部数据。
  - **深度学习**：CNN 在 MNIST（手写数字分类）上训练，batch size=8, 24 个 agent；VGG13 在 CIFAR10 上训练，n=8, batch size=16。均采用异构数据划分（按标签排序后分割）。
- **对比方法**：DSGD-FullyConnected（集中式SGD）、DSGD (Ring)、D2 (Ring)、Hypercube、Static Exp.、OD-EquiDyn、RelaySGD、Base-(k+1)、DSGD-CECA 等。BTPP 分别取 B=2 及不同 B 进行比较。
- **评价指标**：梯度范数（logistic 回归）、训练损失和测试准确率（深度学习）；还对比了实时运行时间（wall-clock time）。
- **公平性**：所有算法初始步长相同（除 BTPP 使用 γ/n 调整，因其梯度跟踪累加 n 倍梯度）。步长每 100 轮衰减 60%。

#### 4. 资源与算力

- 实验在配备 **8 张 Nvidia RTX 3090 GPU** 的服务器上运行。
- 深度学习任务（MNIST CNN）进行了 13,000 轮迭代，并测量了实际运行时间。
- 未明确说明总训练时长或单个实验的 GPU 小时数，但提供了实时性能曲线。

#### 5. 实验数量与充分性

- **实验数量**：共包含 3 个主要实验场景（Logistic 合成数据、MNIST CNN、CIFAR10 VGG13），每个场景下对比了多个基线方法（约 6-8 种），并做了 BTPP 不同分支因子 B 的消融实验。
- **充分性**：实验覆盖了传统机器学习（浅层模型）和深度学习（CNN、VGG）任务，涉及合成数据和真实数据，异构数据设置合理。但仅使用 MNIST 和 CIFAR10 两个数据集，未在更大规模数据集（如 ImageNet）或更复杂的架构（如 Transformer）上验证。
- **客观公平性**：所有基线步长一致（除 BTPP 需缩放），但未报告多次实验的统计误差条形图（仅声称重复了部分实验取平均）。由于分布式训练随机种子影响，缺乏 error bars 可能使结论不完整。

#### 6. 主要结论与发现

- BTPP 在保持每轮通信量 Θ(1) 的前提下，实现了非凸光滑目标下的 ~O(n) 瞬态时间，强凸下 ~O(1)，显著优于现有方法（通常为 O(n³) 甚至更高）。
- 理论证明与实验验证一致：BTPP 收敛速度接近集中式 SGD，且调整 B 可平衡通信与收敛。
- 在实时运行时间上，BTPP 也优于其他 Θ(1) 度方法，尤其适合小规模节点数（B=2 常最佳）。

#### 7. 优点

- **通信效率与收敛速率的优化平衡**：通过 B-ary 树结构，每个节点仅与常数个邻居通信，同时实现接近最优的瞬态时间。
- **理论分析的深刻性**：严格证明了非凸和强凸两种场景下的收敛上界，并揭示了瞬态时间与树直径 d = ⌊log_B n⌋ 的关系。
- **算法简洁易实现**：R、C 矩阵仅为 0/1 矩阵，更新规则简单，易于部署。
- **全面的实验验证**：涵盖不同类型任务和多种基线，且提供了代码开源，可复现性强。

#### 8. 不足与局限

- **实验覆盖有限**：仅在 MNIST 和 CIFAR10 两个较小数据集上测试，未在更大规模数据集（如 ImageNet）或现代大模型上验证，结果泛化性存疑。
- **缺乏统计误差度量**：未提供多次运行的标准差或置信区间，单次曲线可能受随机性影响。
- **对节点规模的讨论不足**：BTPP 在 n 较大时（如数千节点）的性能未实验验证，虽然理论支持，但实际通信与同步开销（特别是树深度增加）可能带来问题。
- **未考虑异步或故障容忍**：论文仅讨论同步更新，未涉及实际系统中的异步、掉线等挑战。
- **数据异构程度的控制仅通过一个参数σ_h**：实验固定了一个异构场景，未系统分析不同异构水平下的性能差异。

（完）

---
title: "You Get What You Give: Reciprocally Fair Federated Learning"
title_zh: 你付出即你所获：互惠公平的联邦学习
authors: "Aniket Murhekar, Jiaxin Song, Parnian Shahkar, Bhaskar Ray Chaudhury, Ruta Mehta"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ZdmMDz33Io"
tags: ["query:eca"]
score: 6.0
evidence: 互惠公平的联邦学习协作
tldr: "联邦学习中，智能体可能搭便车导致不公平和低效。本文设计了M^{Shap}支付机制，在温和条件下达到纳什均衡，实现互惠公平：每个智能体的收益等于其对协作的贡献。实验表明该机制能促进数据共享，提高整体效率和公平性。"
source: ICML-2025-Accepted
selection_source: conference_retrieval
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zdmmdz33io/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1743, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zdmmdz33io/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1557, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zdmmdz33io/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1589, \"height\": 246, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zdmmdz33io/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1555, \"height\": 247, \"label\": \"Table\"}]"
motivation: 联邦学习中存在搭便车行为，导致数据共享不足和公平性下降。
method: 基于Shapley值设计预算平衡的支付机制，激励智能体真实贡献。
result: 机制在多个数据集上减少了搭便车，提高了模型准确性和参与方满意度。
conclusion: 互惠公平机制为联邦学习中的协作激励提供了有效解决方案。
---

## Abstract
Federated learning (FL) is a popular collaborative learning paradigm, whereby agents with individual datasets can jointly train an ML model. 
While higher data sharing improves model accuracy and leads to higher payoffs, it also raises costs associated with data acquisition or loss of privacy, causing agents to be strategic about their data contribution. 
This leads to undesirable behavior at a Nash equilibrium (NE) such as *free-riding*, resulting in sub-optimal fairness, data sharing, and welfare.
To address this, we design $\mathcal{M}^{Shap}$, a budget-balanced payment mechanism for FL, that admits Nash equilibria under mild conditions, and achieves *reciprocal fairness*: where each agent's payoff equals her contribution to the collaboration, as measured by the Shapley share. 
In addition to fairness, we show that the NE under $\mathcal{M}^{Shap}$ has desirable guarantees in terms of accuracy, welfare, and total data collected.
We validate our theoretical results through experiments, demonstrating that $\mathcal{M}^{Shap}$ outperforms baselines in terms of fairness and efficiency.

---

## 论文详细总结（自动生成）

# 论文中文详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：在联邦学习（Federated Learning, FL）中，多个智能体（agent）联合训练一个机器学习模型。尽管数据共享能提升模型精度和收益，但也会带来数据采集成本、计算开销和隐私泄露等代价，导致智能体策略性地减少数据贡献。这种策略行为在纳什均衡（Nash Equilibrium, NE）下会产生**搭便车（free-riding）** 问题，进而造成**不公平**（收益与贡献不成比例）、**数据共享不足**以及**整体福利次优**等不良后果。
- **核心挑战**：如何设计一种激励机制，既能**激励智能体真实贡献数据**，又能在稳定解（如NE）上实现**公平性**（互惠性）和**高效性**（整体数据量、准确率、福利接近最优）。
- **现有工作局限**：此前的工作（如Karimireddy et al., 2022; Murhekar et al., 2023）分别关注数据量最大化或福利最大化，但都**不满足互惠公平性**（例如，迫使高贡献智能体仅获得较少收益）。本文首次将**互惠公平性**（Reciprocal Fairness）作为核心设计目标。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

### 2.1 核心思想
- 定义一个**互惠公平性（Reciprocity）** 度量：在NE下，每个智能体从机制中获得的收益（支付后）与其对协作总收益的贡献（用Shapley值衡量）之比的最小值。一个机制若实现**完全互惠（Reciprocity = 1）**，则每个智能体的收益正好等于其贡献。
- 设计一个**预算平衡（Budget-Balanced）** 的支付机制 $\mathcal{M}^{Shap}$：智能体i的支付 $p_i(s) = \phi_i^A(s) - a_i(s)$，其中 $\phi_i^A(s)$ 是i对总体精度的Shapley值，$a_i(s)$ 是i从联合模型获得的精度。即：若贡献超过自身收益则获得补贴，反之则被征税。

### 2.2 关键技术细节
- **Shapley值计算**：对于样本向量s，总体收益 $A(s) = \sum_i a_i(s)$。第i个智能体的Shapley值为：
  $$
  \phi_i^A(s) = \frac{1}{n} \sum_{X \subseteq N\setminus\{i\}} \binom{n-1}{|X|}^{-1} \left[ A(s[X\cup\{i\}]) - A(s[X]) \right]
  $$
- **NE的存在性**：在精度函数凹、成本函数凸的假设下，证明 $\mathcal{M}^{Shap}$ 的NE存在（通过Kakutani不动点定理）。
- **随机最佳响应动力学（Stochastic Best-Response Dynamics）**：每轮随机选择k个智能体，按梯度方向更新数据贡献量，收敛到近似NE。证明在强凹和梯度有界条件下，迭代次数 $T = O(\log(1/\varepsilon))$。
- **成本无关性**：$\mathcal{M}^{Shap}$ 不需要知道智能体的私有成本函数，仅依赖精度函数，避免了成本验证问题。

### 2.3 算法流程（文字说明）
1. 服务器发布机制，指定支付方案。
2. 智能体观测机制，各自选择数据贡献量 $s_i$。
3. 服务器收集数据后训练模型，计算每个智能体的Shapley值，并按照 $p_i = \phi_i^A - a_i$ 进行支付（正支付为补贴，负支付为征税）。
4. 智能体更新自己的效用 $u_i(s) = a_i(s) - c_i(s_i) + p_i(s)$。
5. 通过随机最佳响应动力学迭代，直至收敛到NE。

## 3. 实验设计：使用了哪些数据集/场景，对比了哪些方法

- **数据集**：共5个数据集，涵盖不同领域和规模：
  - **图像分类**：MNIST、FashionMNIST、CIFAR-10。
  - **医疗保健**：Lumpy Skin Disease dataset（兽医传染病预测）。
  - **合成数据**：二元分类 + 二次回归（10个输入变量）。

- **场景设置**：
  - 图像数据：30个智能体，各智能体拥有**非独立同分布（Non-IID）** 数据（按角度旋转：10°、90°、180°，每组10个智能体）。
  - 医疗和合成数据：2个智能体，数据标签分布不对称（70%正例 vs 30%负例）。

- **基准方法（Baselines）**：
  - **M0**：无支付的基准机制（即原始FL）。
  - **MBG**：Murhekar et al. (2023) 提出的福利最大化机制（基于成本补偿）。

- **评价指标**：
  - 平均准确率（Avg Accuracy）
  - 数据共享比例（Data Share）
  - 数据增益（Data Gain）：相比于M0最好NE的总数据量的比值。
  - 准确率增益（Accuracy Gain）：相比于M0最好NE的总准确率比值。
  - 互惠性（Reciprocity）：机制NE下所有智能体 $ (a_i + p_i)/\phi_i^A$ 的最小值。

- **实验方式**：
  - 对每个数据集重复3次实验，报告平均值和标准差。
  - 对于30个智能体的实验，Shapley值使用Monte Carlo采样（⌊n log n⌋ = 102个排列）近似。
  - 对于2个智能体的实验，直接计算精确Shapley值。

## 4. 资源与算力

- 论文在**“系统配置”**小节明确说明：实验运行在**伊利诺伊大学校园集群（Illinois Campus Cluster）**，配置为**1个节点**，包含**16个CPU核心**，**Fedora@9.4操作系统**，以及**1张A100 GPU**。
- 未提供具体训练时长（如小时数或轮次时间），但提到每轮使用1000次最佳响应动力学迭代，训练100个epoch用于拟合精度函数。

## 5. 实验数量与充分性

- **实验数量**：总计5个数据集 × 3种机制 × 3次重复 = 15组主实验结果。此外还报告了**标准差**以展示稳定性。
- **充分性判断**：
  - **充分**：覆盖了图像、医疗、合成三类任务，且包含Non-IID和数据不平衡等实际场景。
  - **公平性**：对比了最相关的两个baseline（无支付和福利最大化），且使用相同实验设置。
  - **补充实验**：在附录中提供了3个主要图像数据集的详细标准差表格（表2-4），证明Shapley近似采样的稳定性。
  - **消融/分析**：缺少对$\mathcal{M}^{Shap}$在不同超参数（如步长、采样数k）下的敏感性分析，是一个小局限。

## 6. 论文的主要结论与发现

- **公平性**：$\mathcal{M}^{Shap}$ 在所有实验中均实现**完全互惠（Reciprocity=1.0）**，而M0和MBG的互惠性显著低于1（例如MNIST上M0为0.61，MBG为0.70）。
- **效率提升**：
  - **数据增益**：$\mathcal{M}^{Shap}$ 相比M0大幅提升数据共享量（MNIST: 9.51×, FashionMNIST: 13.43×, CIFAR-10: 3.89×, 合成: 31.18×）。
  - **准确率增益**：在多数数据集上略高于baseline（1.02×~1.11×），在合成数据上高达1.36×。
  - **福利**：满足**帕累托最优**性质：任何帕累托优于$\mathcal{M}^{Shap}$ NE的数据共享方案都会导致更低的总福利。
- **理论下界**：在标准化精度函数 $a(s)=1-\alpha(\|s\|_1+1)^{-\beta}$ 和线性成本下，推导出数据增益下界 $\Omega(n^{1/(\beta+1)})$（至少 $\sqrt{n}$），准确率增益下界也随n增大而提高。
- **个体理性**：$\mathcal{M}^{Shap}$ 满足个体理性（UI≥0），保证参与不会使智能体效用为负。
- **实用协议**：设计了分布式FL协议 **FedBR-Shap**，仅依赖梯度信息，无需共享原始数据，且无需假设精度函数的闭式形式，在实际训练中可动态调整数据贡献并分阶段进行支付。

## 7. 优点：方法或实验设计上的亮点

- **方法论亮点**：
  - **成本无关性**：无需知道智能体的私有成本函数，避免了昂贵的成本验证。
  - **完全互惠与预算平衡**：在预算平衡约束下实现了理论上最强的公平性（Reciprocity=1）。
  - **NE的质量保证**：不仅公平，还证明NE具有高效性（帕累托最优性）和可计算性（随机最佳响应动力学收敛）。
  - **理论下界**：给出了数据增益和准确率增益随智能体数量增加的严格下界，理论基石坚实。

- **实验设计亮点**：
  - **多种真实数据集**：涵盖图像、医疗、合成，验证泛化性。
  - **Non-IID和数据不平衡**：模拟实际FL中的异质性。
  - **对比两个相关baseline**：无支付和福利最大化机制，凸显了$\mathcal{M}^{Shap}$在公平性上的绝对优势。
  - **标准差报告与重复实验**：增强了结果可靠性。
  - **FedBR-Shap协议**：提供了实际可部署的分布式实现，克服了以往工作依赖闭式精度函数的限制。

## 8. 不足与局限

- **实验覆盖**：
  - 仅在一个小规模集群（1张A100）上实验，未进行大规模跨GPU/跨节点实验。
  - 图像任务仅使用30个智能体，未测试更大规模（如100+）的场景。
- **适用场景限制**：
  - 方法特别适合**跨孤联邦学习（cross-silo FL）**，其中智能体数量适中（如几十个），因为Shapley值计算复杂度随n呈指数增长（虽然采用了蒙特卡洛近似，但仅采样102个排列，在大规模场景下可能不够精确）。
- **理论假设限制**：
  - 要求精度函数凹、成本函数凸，虽然许多典型模型满足，但并非所有实际场景都严格满足（如某些深度学习损失函数可能非凸）。
  - 强凹性假设（定理4.4、4.5）进一步限制了适用范围。
- **偏差风险**：
  - 实验中的智能体成本 $\gamma_i$ 是随机设置的，未在更大范围或真实成本分布下验证。
  - 精度函数拟合基于预训练的轻量FL，可能无法完美反映真实精度增长曲线。
- **计算开销**：在每个迭代中计算所有智能体的Shapley值需要额外训练 $\mathcal{O}(2^n)$ 个模型（通过蒙特卡洛简化但仍有⌊n log n⌋次评估），对于实时性要求高的场景可能负担较大。
- **未完全解决的trade-off**：论文提到进一步研究在 $r<1$ 时可能获得更高数据增益，但未给出具体折衷方案。

（完）

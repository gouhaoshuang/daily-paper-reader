---
title: "LBI-FL: Low-Bit Integerized Federated Learning with Temporally Dynamic Bit-Width Allocation"
title_zh: LBI-FL：具有时变比特宽度分配的低比特整数化联邦学习
authors: "Li Ding, Hao Zhang, Wenrui Dai, Chenglin Li, Weijia Lu, ZHIFEI YANG, xiaodong Zhang, Xiaofeng Ma, Junni Zou, Hongkai Xiong"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=li59703WbA"
tags: ["query:eca"]
score: 4.0
evidence: 联邦学习用于边缘协作，使用强化学习代理进行比特分配
tldr: 为了解决联邦学习中通信与计算的双重瓶颈，本文提出LBI-FL框架，将模型权重、激活和梯度量化至低于INT8精度，并利用强化学习代理沿训练轨迹动态分配比特宽度。实验表明，该方法在显著降低通信和计算开销的同时，保持了模型精度，为边缘云协同场景下的高效训练提供了可行方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-li59703wba/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 776, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-li59703wba/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 890, \"height\": 286, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-li59703wba/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 859, \"height\": 350, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-li59703wba/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 855, \"height\": 454, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-li59703wba/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1105, \"height\": 536, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 730, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 880, \"height\": 841, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 880, \"height\": 692, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 830, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 864, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 875, \"height\": 690, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 826, \"height\": 393, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 832, \"height\": 393, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 879, \"height\": 683, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-li59703wba/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1221, \"height\": 723, \"label\": \"Table\"}]"
motivation: 联邦学习面临通信瓶颈和客户端计算限制，现有量化方法无法同时降低上下行通信和计算负担。
method: 提出LBI-FL框架，将权重、激活和梯度量化至低于INT8精度，并通过强化学习代理动态分配时变比特宽度。
result: 显著降低通信和计算成本，同时保持模型精度。
conclusion: 首次实现低比特整数化联邦学习，为边缘设备协作训练提供高效方案。
---

## Abstract
Federated learning (FL) is greatly challenged by the communication bottleneck and computation limitation on clients. Existing methods based on quantization for FL cannot simultaneously reduce the uplink and downlink communication cost and mitigate the computation burden on clients. To address this problem, in this paper, we propose the first low-bit integerized federated learning (LBI-FL) framework that quantizes the weights, activations, and gradients to lower than INT8 precision to evidently reduce the communication and computational costs. Specifically, we achieve dynamical temporal bit-width allocation for weights, activations, and gradients along the training trajectory via reinforcement learning. An agent is trained to determine bit-width allocation by comprehensively considering the states like current bit-width, training stage, and quantization loss as the state. The agent efficiently trained on small-scale datasets can be well generalized to train varying network architectures on non-independent and identically distributed datasets. Furthermore, we demonstrated in theory that federated learning with gradient quantization achieves an equivalent convergence rate to FedAvg. The proposed LBI-FL can  reduce the communication costs by 8 times compared to full-precision FL. Extensive experiments show that the proposed LBI-FL achieves a reduction of more than 50\% BitOPs per client on average for FL with less than 2\% accuracy loss compared to low-bit training with INT8 precision.

---

## 论文详细总结（自动生成）

# LBI-FL: 低比特整数化联邦学习详细总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：联邦学习（FL）面临严重的通信瓶颈与客户端计算限制。现有基于量化的方法（如梯度量化）仅能降低上行通信成本，无法同时减少下行通信（仍需下载全精度模型）和减轻客户端计算负担。低比特训练（量化权重、激活和梯度）可以同时解决这两个问题，但现有低比特训练方法在精度低于INT8（如INT4）时易导致模型崩溃。
- **整体含义**：本文首次提出低比特整数化联邦学习（LBI-FL）框架，通过将权重、激活和梯度均量化至低于INT8的精度（INT4/INT6混合），并利用强化学习动态调整各阶段的比特宽度，在保持模型精度的前提下显著降低通信和计算开销。该工作为边缘设备协作训练提供了新的高效方案。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：沿训练轨迹动态分配比特宽度，利用强化学习智能体（RL agent）根据当前训练状态（包括训练阶段、当前比特宽度、量化损失、上次更改时间等）决定是否将每个组件的比特宽度从INT4增加至INT6或INT8（仅允许增加，不允许降低）。智能体在小型数据集上预训练，然后泛化到其他模型和数据集。
- **关键技术细节**：
  - **量化方案**：对权重和激活使用最近舍入（nearest rounding），对梯度使用随机舍入（stochastic rounding）以减少偏差。采用对称量化（权重、激活）和非对称量化（梯度）。
  - **状态空间**：包含时间步（训练进度）、当前比特宽度（权重/激活/梯度）、量化损失（公式5）、上次更改时间。
  - **动作空间**：四种动作：不变；增加权重比特宽度（+2）；增加激活比特宽度（+2）；增加梯度比特宽度（+2）。仅允许从INT4→INT6→INT8的单向增加。
  - **奖励函数**：由量化指数（基于BitOPs压缩比）、准确率指数（与全INT8参考准确率比较）和时间步三者乘积构成，公式(6)(7)(8)。超参数θ和δ调节权重。
  - **算法流程**（Algorithm 1）：初始化比特宽度为INT4；每轮训练后客户端上传量化后的低比特权重；服务器聚合后下发（再量化）；每Itv个epoch智能体决定是否调整每个客户端的比特宽度。
  - **行为克隆（Behavior Cloning）**：收集教师样本（根据先验知识：梯度量化需早期升位、激活量化需后期升位、权重保持INT4），通过KL散度约束智能体策略接近教师，加速训练。
  - **收敛性分析**：在假设梯度量化噪声均值为零且方差有界下，理论证明了梯度量化的联邦学习收敛速率与FedAvg相同（O(1/√T)）。

## 3. 实验设计

- **数据集**：CIFAR-10, CIFAR-100。
- **模型**：LeNet, ResNet-18/50/101, MobileNetV2, ViT-S。
- **基准方法**：
  - 全精度FP32训练（FP32）
  - 全INT4训练（UI4，使用Zhu et al. 2020方法）
  - 全INT8训练（UI8，使用Zhu et al. 2020方法）
  - 随机比特选择（Random）
- **对比指标**：Top-1准确率（Acc）、BitOPs减少比例（RR）、通信成本减少比例。
- **数据分布**：iid和non-iid（Dirichlet分布参数0.25/0.5）。
- **训练设置**：LeNet 2000轮，100个客户端，10%参与；其余模型200轮，10个客户端，全部参与；本地更新epoch为2或5；学习率衰减1.0或0.998。
- **智能体训练**：在CIFAR-10的10%子集上训练ResNet-20 100轮，收集200个episode。

## 4. 资源与算力

- 文中说明：实验在**单个NVIDIA 3090 GPU**上完成。
- 未提供训练总时长或具体GPU小时数，仅提及智能体网络仅1.92K参数，每次决策需1.97G BitOPs，每5轮决策一次，计算开销远小于网络训练。其他模型训练时长未明确给出。

## 5. 实验数量与充分性

- **实验组数**：约20+组主要实验（表2-9），包括：
  - 表2、3：在CIFAR-10和CIFAR-100上对5种模型（LeNet、ResNet-18/50、ViT-S、MobileNetV2）对比FP32/UI4/UI8和LBI-FL。
  - 表4：收敛速度比较（达到目标准确率所需轮数）。
  - 表5：与随机选择的对比。
  - 表6：non-iid下效果（Dirichlet=0.25/0.5）。
  - 表7、8、9：消融实验（本地更新轮数、学习率衰减、初始化种子）。
  - 附录表10：更全面的消融（不同数据分布和超参数组合）。
  - 更多可视化（图2、5：比特宽度变化过程、量化损失变化）。
- **充分性评价**：
  - 覆盖了iid和non-iid场景，多种模型架构（CNN和Transformer），多种位宽策略对比，消融实验充分。
  - 但缺乏跨更大规模数据集（如ImageNet）的验证，且未与其他FL量化方法（如QSGD, SignSGD, 误差反馈方法）做直接对比，仅与固定位宽（UI4, UI8）和全精度比较。
  - 实验客观合理，结果一致支持结论。

## 6. 论文的主要结论与发现

- LBI-FL在**通信成本**方面：由于权重保持INT4，通信量降至全精度的1/8（减少87.5%），相比INT8减少50%。
- **BitOPs**方面：平均减少超过50%（例如ResNet-18上减少54.06%，ViT-S上减少49.51%）。
- **精度损失**：与INT8训练相比，大多数情况下精度损失小于1.5%（CIFAR-10/100），最高不超过2%。
- **收敛速度**：介于INT4和INT8之间，略慢于INT8但可接受。
- **泛化性**：在小数据集上训练的智能体能成功泛化到不同模型和更大数据集（如CIFAR-100）。
- **理论贡献**：证明了梯度量化的联邦学习与FedAvg具有相同的收敛速率O(1/√T)。

## 7. 优点

- **同时降低上行/下行通信和计算成本**：解决了现有方法仅降低单方向通信的局限。
- **动态比特分配**：通过RL自适应地调整不同训练阶段的位宽，避免早期过早使用高精度或晚期低精度导致的性能损失，优于固定位宽。
- **轻量级智能体**：仅1.92K参数，额外开销极小，且能跨模型/数据泛化。
- **行为克隆加速训练**：利用先验知识收集教师样本，加快RL收敛，降低采样需求。
- **理论保证**：证明了收敛速率等价于标准FedAvg，增强了可信度。

## 8. 不足与局限

- **实验规模有限**：仅使用CIFAR-10/100（小规模图像数据集），未在ImageNet、医学图像、文本等更大/更复杂数据集上验证。泛化性有待进一步检验。
- **基线对比不全**：未与更先进的FL压缩方法（如QSGD、SignSGD with error feedback、分层量化、稀疏化）作对比；仅与固定位宽训练比较。
- **仅支持bit-width单向增加（INT4→INT6→INT8）**：无法根据训练情况降低位宽（如从INT6回到INT4），可能错过更优的压缩策略。
- **奖励函数依赖全INT8参考准确率**：该参考准确率需前期预计算，增加了部署复杂度（尤其在non-iid下，全局参考可能不准）。
- **Non-iid实验不充分**：仅测试了Dirichlet=0.25/0.5两种情况，未探索极端非独立同分布场景（如高度倾斜分布），也未提供与其他FL量化方法在non-iid下的对比。
- **计算度量**：使用BitOPs作为计算开销指标，未在真实硬件上测量延迟或功耗，实际加速效果需进一步验证。

（完）

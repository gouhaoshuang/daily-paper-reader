---
title: Federated Ensemble-Directed Offline Reinforcement Learning
title_zh: 联邦集成导向的离线强化学习
authors: "Desik Rengarajan, Nitin Ragothaman, Dileep Kalathil, Srinivas Shakkottai"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=ypaqE8UwsC"
tags: ["query:eca"]
score: 7.0
evidence: 分布式学习智能体协作学习策略
tldr: 针对联邦离线强化学习中数据异构和小样本问题，提出FEDORA算法，通过集成学习汇集各客户端知识。在多个环境下，FEDORA显著优于朴素联邦强化学习方法，为分布式协同学习提供了有效方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 504, \"height\": 317, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1424, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1406, \"height\": 542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1375, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 575, \"height\": 331, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 274, \"height\": 277, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1190, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1303, \"height\": 483, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1306, \"height\": 626, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1445, \"height\": 869, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 575, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 507, \"height\": 354, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 436, \"height\": 357, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 365, \"height\": 325, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 358, \"height\": 314, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-ypaqe8uwsc/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 560, \"height\": 430, \"label\": \"Figure\"}]"
motivation: 联邦离线强化学习中各客户端数据量小且策略不同，直接结合效果差。
method: 提出FEDORA算法，使用集成方法蒸馏各客户端知识。
result: FEDORA在多个任务上大幅超越基线方法。
conclusion: 分布式离线强化学习可通过集成学习高效协同。
---

## Abstract
We consider the problem of federated offline reinforcement learning (RL), a scenario under which distributed learning agents must collaboratively learn a high-quality control policy only using small pre-collected datasets generated according to different unknown behavior policies. Na\"{i}vely combining a standard offline RL approach with a standard federated learning approach to solve this problem can lead to poorly performing policies.  In response, we develop the Federated Ensemble-Directed Offline Reinforcement Learning  Algorithm (FEDORA), which distills the collective wisdom of the clients using an ensemble learning approach.  We develop the FEDORA codebase to utilize distributed compute resources on a federated learning platform. We show that FEDORA significantly outperforms other approaches, including offline RL over the combined data pool, in various complex continuous control environments and real-world datasets. Finally, we demonstrate the performance of FEDORA in the real-world on a mobile robot. We provide our code and a video of our experiments at \url{https://github.com/DesikRengarajan/FEDORA}.

---

## 论文详细总结（自动生成）

# 论文总结：Federated Ensemble-Directed Offline Reinforcement Learning (FEDORA)

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：在联邦学习场景下进行离线强化学习。分布式客户端（智能体）各自拥有少量、由不同未知行为策略生成的离线数据集，且无法共享数据。目标是协作学习一个高质量的控制策略。
- **核心问题**：直接套用标准离线RL（如TD3-BC）和标准联邦聚合（如FedAvg）会导致性能严重下降。论文识别出三个根本挑战：
  - **集成异质性**：客户端策略质量差异大，简单平均会丧失集体智慧。
  - **悲观值计算**：离线RL的悲观估计会压制在本地数据中少见但在其他客户端数据中常见的高价值动作。
  - **数据异质性**：多轮本地更新会导致模型漂移，偏离全局最优。
- **整体含义**：首次系统性地提出并解决联邦离线RL的上述挑战，设计了一个集成导向的算法FEDORA，能够在保护隐私的前提下有效利用分布式异质数据。

## 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：采用**集成学习**方式，通过**最大熵加权**聚合客户端的策略和评论家，提取集体智慧；同时对评论家进行**乐观化**处理，对策略进行**近端正则化**，并**衰减低质量本地数据的影响**。
- **关键技术细节**：
  - **策略联邦（Ensemble-Directed Policy Aggregation）**：使用软最大权重（softmax weight）聚合各客户端策略，权重由客户端策略的本地性能（通过评论家评估）和数据集大小共同决定，并加入熵正则项以防止权重集中。
    \[
    w_i^t = \frac{e^{\beta J_i^t |D_i|}}{\sum_j e^{\beta J_j^t |D_j|}}, \quad \pi_{\text{fed}}^{t+1} = \sum_i w_i^t \pi_i^t
    \]
  - **乐观评论家（Federated Optimism for Critic）**：联邦评论家也采用同样的加权聚合。在本地评论家更新时，目标值取本地评论家与联邦评论家输出的最大值，以鼓励乐观估计。
    \[
    \tilde{Q}_i^{(t,k)}(s,a) = \max\left(Q_i^{(t,k)}(s,a), Q_{\text{fed}}^t(s,a)\right)
    \]
  - **近端策略更新（Proximal Policy Update）**：本地策略更新时，损失函数包含TD3-BC的本地损失（动作与本地数据行为克隆）加上与联邦策略的均方误差正则项，以缓解数据异质性造成的漂移。
    \[
    L_{\text{actor}}(\pi) = L_{\text{local}}(\pi) + \mathbb{E}_{(s,a)\sim D_i}[(\pi(s) - \pi_{\text{fed}}^t(s))^2]
    \]
  - **本地数据影响衰减（Decay of Local Data）**：比较联邦策略在本地数据上的性能与更新后本地策略的性能，若联邦策略更好，则减小本地损失项的系数δ，从而降低低质量本地数据的干扰。
- **算法流程**（文字说明）：
  - 服务器初始化联邦策略和评论家。
  - 每轮通信：选部分客户端，发送联邦策略和评论家。
  - 客户端进行K步本地更新：更新评论家时采用乐观目标值；更新策略时采用近端损失；之后根据性能比较衰减本地损失权重。
  - 服务器收集各客户端的策略和评论家，按加权平均更新联邦模型（权重基于客户端性能熵加权）。

## 3. 实验设计

- **数据集与环境**：
  - **模拟环境**：MuJoCo（Hopper、HalfCheetah、Walker2D），使用D4RL数据集中的expert和medium等级数据。
  - **大规模随机环境**：CityLearn（城市能源管理），使用NeoRL数据集。
  - **真实机器人**：TurtleBot3，在真实物理世界中执行避障导航任务，使用四种不同水平的行为策略收集数据。
- **基准方法**：
  - Fed-A（仅联邦策略，评论家本地）、Fed-AC（联邦策略和评论家）、Fed-AC-Prox（加近端项）、HDAFL（异构数据感知联邦学习）、Centralized（合并所有数据集中训练TD3-BC）、以及数据重平衡版TD3-BC等。
- **实验设置**：
  - 模拟：50个客户端（25个expert、25个medium），各5000条数据，每轮随机选20个客户端，进行1000轮通信，4个随机种子。
  - CityLearn：10个客户端，150轮。
  - 真实机器人：20个客户端，100轮。

## 4. 资源与算力

- **明确指出**：每个MuJoCo实验约需7小时，运行在单机上（AMD Ryzen Threadripper 3960X 24核CPU + 2块NVIDIA 2080Ti GPU）。使用Flower框架可在分布式环境中大幅缩短时间。未提供总的实验运行次数或总计算量，但可推测大量实验（不同环境、消融、超参数扫描等）消耗了显著算力。

## 5. 实验数量与充分性

- **实验覆盖**：三种MuJoCo环境 + CityLearn + 真实机器人，涵盖了连续控制、大规模随机环境、真实部署。
- **消融研究**：
  - 逐步添加组件（加权策略、乐观评论家、近端项、衰减）展示效果提升。
  - 移除每个组件显示性能下降。
  - 超参数扫描（温度β、衰减系数δ）。
  - 分析客户端权重与衰减随训练变化趋势。
  - 变化本地训练轮数、参与客户端比例、expert客户端比例。
  - 可变数据集大小、多种行为策略混合、不同离线RL基线（CQL、IQL）比较等。
- **充分性评价**：实验设计系统，覆盖主要因素，统计使用4个随机种子并给出均值与标准差，结果可靠且具有可重复性。相比直接基线方法显著优越，充分证明了FEDORA的有效性和鲁棒性。

## 6. 论文的主要结论与发现

- FEDORA在所有测试环境中均显著优于其他联邦方法，也优于集中式训练（合并数据），特别是在客户端数据高度异质时。
- 乐观评论家与加权联邦是提升性能最关键的两个组件；近端项和衰减机制进一步稳定和提升性能。
- FEDORA对参与客户端比例、本地训练轮数、数据集大小等变化均表现出稳健性，即使在只有20% expert客户端时也能取得良好效果。
- 在真实TurtleBot上，只有FEDORA能成功完成避障导航任务，验证了算法的实际可用性。

## 7. 优点

- **问题定义清晰**：首次系统分析联邦离线RL的三个核心挑战，并针对性设计解决方案。
- **方法创新**：结合最大熵加权与乐观评论家，既保留离线RL的保守性（通过近端项）又鼓励探索高价值动作（通过乐观目标），平衡巧妙。
- **实验全面**：涵盖模拟到真实、不同数据集、多种异质性场景，消融实验详实，代码开源，可复现性强。
- **实用价值高**：适用于数据隐私敏感、通信有限的分布式RL应用，如机器人协作、能源管理等。

## 8. 不足与局限

- **假设限制**：假设所有客户端共享相同的MDP（转移和奖励模型），仅行为策略不同。实际中客户端可能具有不同的环境动力学或奖励函数，论文未考虑此场景。
- **未处理个性化**：联邦学习有时需个性化模型，FEDORA只产生一个全局策略，不包含客户端特定适配。
- **计算与通信成本**：虽然能降低通信轮次，但客户端需进行多次本地更新，且服务器需聚合策略和评论家两个模型，成本较单纯策略联邦高。
- **真实实验规模较小**：TurtleBot场景仅20个客户端、100轮，样本量较小，可能无法完全反映复杂现实条件。
- **理论保证缺失**：论文未给出收敛性或有限样本分析，仅靠经验验证。

（完）

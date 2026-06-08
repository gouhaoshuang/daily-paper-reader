---
title: Multi-Agent Coordination via Multi-Level Communication
title_zh: 通过多级通信实现多智能体协调
authors: "Ziluo Ding, Zeyuan Liu, Zhirui Fang, Kefan Su, Liwen Zhu, Zongqing Lu"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=3l2HnZXNou"
tags: ["query:eca"]
score: 8.0
evidence: 多智能体通过多级通信协调
tldr: 针对多智能体协调中循环依赖问题，提出顺序通信协议SeqComm。通过协商阶段确定决策优先级，再顺序通信，解决了同时决策冲突。实验表明该方法在部分可观测随机环境中显著提升了协调性能。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 500, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1376, \"height\": 420, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 660, \"height\": 723, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1471, \"height\": 1106, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1353, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 549, \"height\": 332, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1470, \"height\": 1105, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1164, \"height\": 968, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-3l2hnzxnou/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1471, \"height\": 735, \"label\": \"Figure\"}]"
motivation: 多智能体系统中存在由于循环依赖导致的协调困难。
method: 提出异步多级通信方案，分为协商和启动两阶段。
result: 在多个基准任务上，SeqComm优于现有通信方法。
conclusion: 异步顺序通信能有效解决多智能体协调难题。
---

## Abstract
The partial observability and stochasticity in multi-agent settings can be mitigated by accessing more information about others via communication. However, the coordination problem still exists since agents cannot communicate actual actions with each other at the same time due to the circular dependencies. In this paper, we propose a novel multi-level communication scheme, Sequential Communication (SeqComm). SeqComm treats agents asynchronously (the upper-level agents make decisions before the lower-level ones) and has two communication phases. In the negotiation phase, agents determine the priority of decision-making by communicating hidden states of observations and comparing the value of intention, which is obtained by modeling the environment dynamics. In the launching phase, the upper-level agents take the lead in making decisions and then communicate their actions with the lower-level agents. Theoretically, we prove the policies learned by SeqComm are guaranteed to improve monotonically and converge. Empirically, we show that SeqComm outperforms existing methods in a variety of cooperative multi-agent tasks.

---

## 论文详细总结（自动生成）

## 论文总结：Multi-Agent Coordination via Multi-Level Communication

### 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：在多智能体强化学习（MARL）中，由于部分可观测性和随机性，智能体之间需要通信来获取更多信息，但传统同步决策方式会导致循环依赖（circular dependencies），即智能体无法同时获得彼此的真实动作，从而引发协调失败（如次优联合动作选择）。
- **研究背景**：现有通信方法主要关注传递观测或历史轨迹的消息，但无法传递真实动作；而通过世界模型预测未来轨迹的方法又因循环依赖导致预测不准确。协调问题需要一种机制来打破同等优势动作选择中的“平局”，使智能体能够明确知道其他智能体将要采取的动作。
- **整体含义**：该论文提出一种多级异步通信方案，通过引入决策优先级顺序，让高层智能体先做决策，低层智能体在获知高层真实动作后再做决策，从而自然解决循环依赖，实现显式协调。

### 2. 方法论：核心思想、关键技术细节、算法流程

- **核心思想**：将同步决策改为异步顺序决策，每个时间步为智能体动态分配决策优先级（order），高优先级智能体做出动作后，将其真实动作通过通信传递给低优先级智能体，低优先级智能体以此条件化其策略。决策优先级通过“意图（intention）”价值比较来确定。
- **关键技术细节**：
  - **两阶段通信**：
    - **协商阶段（Negotiation Phase）**：
      - 智能体首先互相通信隐藏状态（观测编码）。
      - 每个智能体基于世界模型和自身策略，以自己为第一个决策者，随机采样多个可能的后续顺序序列，预测未来H步轨迹（意图），并通过critic计算每个轨迹的返回值，平均得到意图值。
      - 所有智能体通信自己的意图值，选择意图值最高的智能体作为第一优先级；然后固定该智能体，对剩余智能体重复相同过程，直到确定所有智能体的顺序。
    - **启动阶段（Launching Phase）**：
      - 按照协商确定的顺序，高优先级智能体先依据观测和已收到的上层动作做出真实决策，并将动作通信给低优先级智能体；低优先级智能体在收到所有高层动作后，再做出自己的决策。所有智能体最终同时执行动作。
  - **世界模型**：用于预测下一时刻观测和奖励，使用注意力机制处理联合隐藏状态和动作，训练方式为回归（MSE损失）。
  - **策略与价值网络**：基于MAPPO（PPO算法），策略网络和critic网络均使用注意力模块处理自身观测与接收到的消息（隐藏状态和上层动作）。
  - **局部通信版本**：当智能体只能与附近智能体通信时，简化协商过程，仅根据局部隐藏状态计算意图值，并与邻域内智能体比较，划分局部上下级，仅一次通信确定局部顺序。
- **算法流程（文字说明）**：
  1. 每个智能体编码当前观测得到隐藏状态，并广播给所有其他智能体。
  2. 每个智能体利用世界模型和策略，以自己为第一决策者，随机采样多种后续顺序，预测H步未来轨迹，用critic评估其价值，平均得到意图值。
  3. 所有智能体通信意图值，比较后选出最大值对应的智能体作为第一优先级；固定该智能体后，对剩余智能体重复步骤2-3，直至全部顺序确定。
  4. 根据确定顺序，高优先级智能体依次做出真实动作，并将动作传递给低优先级智能体；低优先级智能体在收到所有高层动作后做出自己的动作。
  5. 所有智能体同时执行动作，环境反馈下一状态和奖励。
  6. 同时训练策略网络、价值网络与世界模型（使用收集的经验）。

### 3. 实验设计

- **数据集/场景**：StarCraft Multi-Agent Challenge v2 (SMACv2) 中的9个地图（protoss 5v5, 10v10, 10v11; terran 5v5, 10v10, 10v11; zerg 5v5, 10v10, 10v11）。对观测做了修改：将视野范围从9缩小到3，且友军信息不可见，增加部分可观测性难度。
- **基准（Benchmark）**：SMACv2是一个常用的合作MARL测试环境，具有随机性和部分可观测性。
- **对比方法**：
  - 无通信方法：MAPPO。
  - 通信方法：TarMAC（两轮通信）、SeqComm的完整版本和局部通信版本。
  - 消融实验额外对比：随机顺序（Random）、不通信动作（No action）、不同通信范围（1,3,9）、不同网络机制（MLP替代注意力）、额外对比MAIC和CommFormer。

### 4. 资源与算力

论文在附录D.4中提到：模型在一张GeForce GTX 1050 Ti和Intel Core i9-9900K CPU @ 3.60GHz上训练。未详细说明每个实验的具体训练时长或GPU数量（仅说明使用单GPU），但指出训练是在上述硬件上完成的。

### 5. 实验数量与充分性

- **实验数量**：涵盖9种不同地图的完整实验（主实验Figure 4），以及针对通信范围、决策优先级、网络机制的多组消融实验（Figure 5, 6, 7），另外在附录中补充了与MAIC和CommFormer的对比（Figure 8）。总计超过12组不同的实验设置。
- **充分性与客观性**：
  - 每组实验报告了5个随机种子的均值和标准差，提供了误差线。
  - 超参数经过调整，基线方法也进行了调优。
  - 消融实验设计合理，逐一验证了决策优先级、通信范围、世界模型/意图机制的作用。
  - 实验较为充分，但仅在SMACv2这一种环境上进行测试，没有在其他基准（如MPE、Hanabi等）上验证，泛化性有待进一步证明。

### 6. 主要结论与发现

- SeqComm在SMACv2全部9个地图上均优于无通信方法MAPPO和通信方法TarMAC，尤其在部分可观测性强的困难场景中优势明显。
- 决策优先级（顺序）对收敛最优性有重要影响：固定优先级（如B→A）容易陷入局部最优，而动态选择优先级（如Learned）或基于意图的方法（SeqComm）可以获得更好的性能。
- 消融实验表明：基于意图确定优先级比随机顺序效果更好；随机顺序甚至可能破坏协调；通信范围越大性能越好（权衡开销与收益）。
- 世界模型误差会在一定程度上影响顺序选优，但通过理论分析保证了在模型误差可控范围内的单调改进。

### 7. 优点

- **创新性**：首次提出在MARL中显式使用异步顺序决策与多级通信相结合，解决循环依赖问题。
- **理论保障**：证明了在异步顺序决策下联合策略的单调改进和收敛性，并给出了世界模型误差下的性能边界。
- **实验设计全面**：包含了主实验、多组消融实验（优先级、通信范围、网络结构、额外基线），结果有统计意义。
- **局部通信版本**：考虑了实际通信限制，提供了适用性更广的变体，降低了假设强度。

### 8. 不足与局限

- **环境单一**：所有实验仅在SMACv2中进行，未在其他合作MARL基准（如MPE、LBF、Hanabi）上验证，泛化性存疑。
- **算力开销**：协商阶段需要多次预测未来轨迹（H=20, F=2），世界模型训练和意图计算增加了计算成本，论文未报告具体训练时间和推理延迟。
- **假设限制**：完整版本假设全局广播通信，在某些场景下不现实；局部版本虽降低假设，但仍需周围智能体可通信。
- **偏差风险**：世界模型训练误差可能影响优先级判定的可靠性，当模型误差过大时，意图价值可能不准确。
- **消融对比稍显不足**：对于优先级确定的替代方案（如学习一个独立的顺序网络），仅在简单矩阵游戏中学了Learned策略，在SMACv2中只与随机顺序比较，未与更复杂的顺序学习方法对比。

（完）

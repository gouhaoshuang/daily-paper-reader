---
title: Autonomous Agents for Collaborative Task under Information Asymmetry
title_zh: 信息非对称下的自主协作智能体
authors: "Wei Liu, Chenxi Wang, YiFei Wang, Zihao Xie, Rennai Qiu, Yufan Dang, Zhuoyun Du, Weize Chen, Cheng Yang, Chen Qian"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=mp6OWpDIJC"
tags: ["query:eca"]
score: 8.0
evidence: 应对信息非对称的协作多智能体系统
tldr: 为解决多智能体协作中的信息非对称问题，本文提出iAgents范式，通过镜像人类社交网络让智能体主动交换各自人类用户所需信息。实验证明该方法能有效完成传统方法无法处理的跨用户协作任务，为隐私保护下的协作智能体提供了新思路。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1345, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1408, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 449, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1306, \"height\": 470, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1174, \"height\": 545, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 981, \"height\": 867, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-mp6owpdijc/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 584, \"height\": 579, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1204, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1040, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1456, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 739, \"height\": 753, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1494, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1334, \"height\": 273, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-mp6owpdijc/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1363, \"height\": 1900, \"label\": \"Table\"}]"
motivation: 现有多智能体系统假设信息共享，无法处理每个智能体仅知悉其用户信息的场景。
method: 构建镜像人类社交网络的智能体网络，实现信息主动交换以完成任务。
result: 在多人协作基准上准确率和完成度显著提升。
conclusion: 主动信息交换机制是解决信息非对称协作的关键。
---

## Abstract
Large Language Model Multi-Agent Systems (LLM-MAS) have greatly progressed in solving complex tasks. It communicates among agents within the system to collaboratively solve tasks, under the premise of shared information. However, when agents' collaborations are leveraged to perform multi-person tasks, a new challenge arises due to information asymmetry, since each agent can only access the information of its human user. Previous MAS struggle to complete tasks under this condition. To address this, we propose a new MAS paradigm termed iAgents, which denotes Informative Multi-Agent Systems. In iAgents, the human social network is mirrored in the agent network, where agents proactively exchange human information necessary for task resolution, thereby overcoming information asymmetry. iAgents employs a novel agent reasoning mechanism, InfoNav, to navigate agents' communication towards effective information exchange. Together with InfoNav, iAgents organizes human information in a mixed memory to provide agents with accurate and comprehensive information for exchange. Additionally, we introduce InformativeBench, the first benchmark tailored for evaluating LLM agents' task-solving ability under information asymmetry. Experimental results show that iAgents can collaborate within a social network of 140 individuals and 588 relationships, autonomously communicate over 30 turns, and retrieve information from nearly 70,000 messages to complete tasks within 3 minutes.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：现有多智能体系统（MAS）通常假设所有智能体共享信息，但在真实多人协作场景中，每个智能体仅能访问其对应人类用户的私人信息，导致**信息不对称**。之前的MAS（如ChatDev、MetaGPT）无法处理该场景，因为（1）人类信息敏感且私有，不能简单集中共享；（2）信息动态变化，无法通过角色扮演提示在预训练中记忆。
- **整体含义**：本文首次将研究视角从整体系统转向个体，提出**iAgents**范式，通过镜像人类社交网络，让智能体代表各自用户主动交换必要信息，从而克服信息不对称。这为**隐私保护下的协作智能体**提供了新思路，有望提升人类社会的生产力。

## 2. 论文提出的方法论

### 核心思想
- 构建一个**与人类社交网络镜像的智能体网络**，每个智能体只能看到其用户的信息，但可以通过主动通信从其他智能体处获取缺失信息。
- 采用**InfoNav（信息导航）**机制引导通信方向，并用**混合记忆（Mixed Memory）**组织人类信息以支持精准检索。

### 关键技术细节
1. **InfoNav机制**：
   - 智能体在每次发言前生成一个**计划（Plan）**，列出回答问题所需的所有推理依据（rationales），标记为“已知”或“未知”。
   - 通信过程中，智能体根据收到的信息更新计划中的状态（未知→已知），直到所有必需信息被收集。
   - 最后双方进行**共识推理（Consensus Reasoning）**，统一收集到的理由并消除矛盾，输出答案。
   - 公式表示：
     - 计划生成：\( P(r_u^1, ..., r_u^m) = Prompt(Q) \)
     - 通信中更新：\( P(r_k) = Think_A(Obs_A) \)
     - 最终答案：\( Ans = Reasoning(Q, R) \)，其中 \( R = Consensus(P_1(R_1), P_2(R_2)) \)
   - InfoNav比传统CoT/ToT更强调**导航通信和信息交换**，而非仅生成计划。

2. **混合记忆机制**：
   - **清晰记忆（Clear Memory）**：以结构化格式存储原始信息，支持精确检索（如SQL查询），但严格匹配导致难以获取上下文。
   - **模糊记忆（Fuzzy Memory）**：存储对话摘要文本，通过embedding进行近似最近邻搜索（ANN），提供语义级检索和丰富上下文。
   - 两者结合：智能体根据观察动态调整查询参数（如上下文窗口、消息数、关键词数等），实现跨会话信息提取。

3. **递归通信**：智能体可发起新的子通信会话（如A向B询问，B再向C询问），从而在更大社交网络内扩散信息。

### 算法流程（文字说明）
1. 人类用户唤醒各自智能体，每个智能体仅拥有其用户的信息。
2. 智能体使用InfoNav生成初始计划，标记未知理由。
3. 智能体交替发言：观察当前通信历史和计划状态 → 思考（更新计划、决定查询什么信息） → 行动（从人类记忆检索信息、生成下一句发言）。
4. 当双方计划中所有理由均为“已知”时，进行共识推理，输出答案。

## 3. 实验设计

### 数据集与Benchmark
- 作者提出了**InformativeBench**，首个针对信息不对称下协作任务的多智能体基准，包含两大类、五个数据集：
  - **Needle-Oriented（针状查找）**：
    - **Needle in the Persona (NP)**：基于SPC对话数据集，向两个用户的个性中插入共同/相反信息（“针”），智能体需找出该信息。
    - **FriendsTV**：基于《老友记》第一季剧本重构社交网络（140节点、588关系），将两个FriendsQA问题合并为新问题，需结合剧情信息回答。
  - **Reasoning-Oriented（推理导向）**：
    - **Schedule**：为多人分配日程，智能体需协作解决算法问题：Easy（计算两人日程冲突数）、Medium（找出最长的活动）、Hard（找出所有人的共同空闲时间段）。算法自动验证答案。

- 各数据集规模：NP 100个QA，Schedule各30个，FriendsTV 222个QA。FriendsTV需要外存，其余在内存即可。

### 对比方法
- 论文未与其他多智能体系统直接对比，而是将**iAgents自身作为完整模型**，并做消融实验。
  - 消融组件：去掉InfoNav（w/o InfoNav）、去掉递归通信（w/o Recursive Comm）、去掉模糊记忆（w/o Fuzzy Memory）、去掉清晰记忆（w/o Clear Memory）。
- 后端LLM对比：GPT-4、GPT-3.5、Claude Sonnet、Gemini 1.0（均作为iAgents的智能体骨干）。
- 额外分析：先验干扰（匿名化角色名）、隐私保护（要求模糊表达）的影响。

### 实验设置
- 最大通信轮数：10轮。
- LLM温度：0.2。
- 模糊记忆用GPT-4总结，OpenAI text-embedding-3-small做embedding。
- 指标：NP、ScheduleEasy、FriendsTV用准确率；ScheduleMedium用F1；ScheduleHard用IoU。

## 4. 资源与算力

- 文中未明确报告使用的GPU型号、数量或训练时长。
- 实验基于**API调用**（GPT-4、GPT-3.5等），无模型训练过程。
- 成本方面：每个任务平均消耗约**30,000 tokens**输入（用于处理人类信息）。作者认为这是挑战，但随着长上下文模型的发展可缓解。
- 未提及具体计算资源（如A100、V100等）。

## 5. 实验数量与充分性

- **主要实验**：表1报告了4种LLM在5个数据集上的结果，共4×5=20组结果。
- **消融实验**：表2列出了5组消融（w/o InfoNav在NP和Schedule上的部分，w/o Recursive Comm和w/o Memory在FriendsTV上的部分），共约10组左右。
- **行为分析**：表3分析InfoNav行为（#理由数、解决比例等），图5分析记忆参数调整行为。
- **额外实验**：隐私与先验干扰各1组（FriendsTV上），共2组。
- **充分性评价**：
  - **优点**：覆盖了不同难度、不同规模、不同信息类型的任务，消融实验验证了各组件的贡献，行为分析提供了机理理解。
  - **不足**：
    - **缺乏与其他方法对比**：实验仅对比了不同LLM作为iAgents骨干，未与现有MAS（如ChatDev、MetaGPT）或其他基线（如直接让LLM对话）比较，因为作者认为“Previous MAS struggle”，但直接展示差距更具说服力。
    - **数据集规模有限**：Schedule只有30个题目，NP 100个，FriendsTV 222个，统计显著性可能受限。
    - **未报告误差线或多次运行**：所有结果可能仅一次运行，缺乏方差分析。
    - **隐私实验仅调整输出**，未调整输入访问权限，可能未能充分测试隐私保护能力。

## 6. 论文的主要结论与发现

1. **信息不对称是阻碍多智能体协作的重要挑战**，现有方法无法解决。
2. **iAgents能有效解决该问题**：在140人、588关系的社交网络中，自主通信30轮、检索近7万条消息，3分钟内完成任务。GPT-4在多数数据集上准确率超50%，但最硬任务仅22.8%。
3. **InfoNav是关键**：消融后性能下降15%~26%，尤其在需要复杂推理的Schedule数据集上。
4. **混合记忆在信息规模大时更重要**：FriendsTV中去除记忆导致准确率下降2.38%~6.34%。
5. **递归通信提升显著**（12.7%），表明主动扩散信息的重要性。
6. **先验干扰和隐私保护会降低性能**（分别降3.17%和4.76%），提示未来需平衡。
7. **小模型（GPT-3.5、Claude、Gemini）表现较差**，说明任务对模型推理能力要求高。

## 7. 优点

- **问题新颖且重要**：首次系统提出并解决多智能体系统中的信息不对称问题，切合隐私和分布式场景。
- **方法创新**：
  - InfoNav将对话状态跟踪和计划融合，显式管理信息流，比隐式推理更可靠。
  - 混合记忆结合精确检索和语义检索，适应不同信息粒度。
  - 递归通信机制支持信息在社交网络中扩散，实现可扩展协作。
- **基准贡献**：InformativeBench是首个针对信息不对称的协作基准，包含多种任务类型，可动态生成，避免过拟合。
- **实验设计全面**：覆盖不同难度、网络规模、记忆需求，进行了组件消融和行为分析。
- **现实意义强**：考虑隐私、先验干扰等真实世界问题，并进行了初步探索。

## 8. 不足与局限

- **方法局限性**：
  - **隐私保护不彻底**：仅从输出端限制模糊表达，未从输入端控制访问权限。更严格的隐私保护（如边缘部署小模型）尚未实现。
  - **网络建模简单**：仅基于用户相关性发起通信，未利用过往协作历史或网络拓扑来优化效率。
  - **成本较高**：每个任务约3万tokens输入，大规模部署下成本可观。
  - **人类仍需介入**：部分场景需用户验证和调整策略，无法全自动。
- **实验局限**：
  - **缺乏公平基线**：未与任何现有MAS系统或简单基线（如直接让两个LLM对话）对比，无法量化iAgents相对于现有技术的提升幅度。
  - **数据集规模偏小**：Schedule只有30个样本，统计误差可能较大；FriendsTV虽有222个，但仅为单一电视剧故事，泛化性存疑。
  - **未报告多次运行结果**：性能可能因随机性波动，无误差线则难以判断稳定性。
  - **消融实验不够完整**：如在Schedule数据集上未包含混合记忆消融（因为信息量小），在NP上未包含递归通信消融，限制了跨数据集对比。
- **潜在偏差**：
  - 使用GPT-4进行模糊记忆摘要和答案评估可能存在自偏好偏差。
  - FriendsTV数据集来自公开电视剧，LLM预训练中可能已记忆剧情，导致先验干扰实验结论需谨慎。
- **应用限制**：当前方法依赖LLM API，延迟和成本在实时多人协作中可能成为瓶颈；边缘部署小模型效果差（Gemini仅28%准确率）。

（完）

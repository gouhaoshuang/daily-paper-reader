---
title: "C-World: A Computer Use Agent Environment Creator"
title_zh: C-World：计算机使用智能体环境创建器
authors: "Ziqiao Xi, Shuang Liang, Qi Liu, Jiaqing Zhang, Letian Peng, Fang Nan, Meshal Nayim, Tianhui Zhang, Rishika Mundada, Lianhui Qin, Biwei Huang, Kun Zhou"
date: 2026-07-01
pdf: "https://aclanthology.org/2026.acl-long.2001.pdf"
tags: ["query:mobile-agent"]
score: 4.0
evidence: 为LLM智能体构建训练环境的系统，可支持移动智能体环境生成
tldr: 论文提出C-World，一个能让用户按需构建智能体环境的系统。它定义了完整环境所需的四个组件：包含5571个统一格式工具的动作空间、能合成长期工作流的任务分布引擎、注入真实故障与扰动的状态控制器，以及可验证度量与LLM评判结合的奖励信号。该系统可创建多样化环境，为智能体提供大规模持续学习支撑。该环境创建能力可扩展到移动应用场景。
source: ACL-2026-Long
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2001/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 718, \"height\": 659, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2001/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1653, \"height\": 651, \"label\": \"Figure\"}, {\"url\": \"assets/figures/acl-2026-long/anthology-2026acl-long2001/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 843, \"height\": 352, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1604, \"height\": 629, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1397, \"height\": 488, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 789, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 754, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 809, \"height\": 488, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1657, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 803, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 557, \"height\": 253, \"label\": \"Table\"}, {\"url\": \"assets/tables/acl-2026-long/anthology-2026acl-long2001/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 728, \"height\": 251, \"label\": \"Table\"}]"
motivation: 构建大规模多样化智能体训练环境成本过高，阻碍智能体学习与部署。
method: 提出C-World环境创建系统，以动作空间、任务分布、状态控制器和奖励信号四要素按需生成环境。
result: 能够低成本构建覆盖204个应用的多样化长期任务环境。
conclusion: 为智能体环境构建提供通用工具，对移动智能体的训练与评估有潜在价值。
---

## Abstract
To close the gap between LLM-based agents and humans in planning and reasoning, agents need large-scale, diverse environments for continuous learning—yet building such environments is itself prohibitively expensive. We present C-World, an environment creation system that enables users to build agent environments on demand. We define a complete agent environment through four components: an Action Space of 5,571 format-unified tools across 204 common applications, a Task Distribution engine that synthesizes long-horizon workflows with wild constraints, a Transition Function implemented as a state controller that injects realistic failures and perturbations, and a Reward Signal combining verifiable metrics with LLM-based judgment. C-World operates in two modes: a realistic mode grounded in live API execution, and a synthesized mode powered by the World Engine, which approximates tool behavior without live service access, enabling scalable environment creation—including environments for domains and tools that do not yet exist in the real world. Evaluation of nine state-of-the-art LLMs reveals that planning ability is uniformly strong but execution remains the bottleneck, and that constraint following—not tool invocation—is the dominant failure mode. The World Engine achieves Spearman 𝜌 = 0.883 ranking correlation with real execution, and fine-tuning on just 1,170 C-World trajectories outperforms baselines trained on 119k samples, demonstrating C-World’s dual value as a rigorous evaluation environment and a scalable data engine. Our code and data are available at https://ziqiao-git.github.io/C-World/.

---

## 论文详细总结（自动生成）

# C-World: 计算机使用智能体环境创建器 —— 详细中文总结

## 1. 核心问题与整体含义

- **研究动机**：尽管LLM在单轮函数调用和模式合规基准上已接近饱和性能，但在真实世界复杂任务中，智能体与人类之间的规划与推理能力仍存在显著差距。人类通过在日常生活中不断接触多样化、开放式的挑战来建立这些能力，而智能体缺乏同样广度和密度的学习经验来源。
- **核心瓶颈**：构建大规模、多样化的智能体训练环境本身就是一项极其昂贵的工作。现有智能体环境大多为窄域人工设计，工具覆盖面有限、设置简化、任务集静态不可演化，无法支撑智能体持续学习所需的环境规模和多样性。
- **关键洞察**：论文提出从“构建固定基准”转向“构建环境创建系统”——给定种子任务、工具和评估标准，系统能自动生长和演化出日益多样化的复杂环境，让用户按需创建所需环境，而无需每次从头开始。
- **整体含义**：C-World既是一个严格的评估环境，也是一个可扩展的数据引擎，为缩小LLM智能体与人类在规划和推理上的差距提供了基础设施支撑。

## 2. 方法论：核心思想与关键技术细节

C-World将智能体环境定义为四个必要组件：

- **动作空间（Action Space，A）**：
  - 从Smithery平台策展了来自276个MCP服务器的5,571个工具，覆盖204个生产级应用（如Gmail、GitHub）。
  - 通过三阶段验证管线确保工具可用性：认证可用性、成功调用验证和可用响应过滤。
  - 使用BGE-M3嵌入工具文档并存入FAISS索引，提供`search_tools(query, k)`的轻量级MCP服务，支持开放世界场景下的按需工具发现。

- **任务分布（Task Distribution，T）**：
  - 采用工具候选采样策略：随机采样1-3个种子工具，通过检索索引召回相关的更大工具集，再按服务器/应用分组进行轮询采样，防止单服务主导，促进跨应用工作流。
  - 合成任务时使用迭代的“检查-然后-修改”循环：从LLM生成的初始任务草稿出发，每轮从工具覆盖率和约束质量两个维度评估，若未达标则生成针对性反馈并重合成。
  - 通过模糊重写（将工具名抽象为意图级描述）、仅暴露检索接口、要求任务分解等策略防止检索捷径。

- **转换函数（Transition Function，F）**：
  - 实现为状态控制器（State Controller），即位于智能体与工具执行后端之间的轻量级Python中间件。
  - 三类干预：工具级控制（注入超时、限流、临时不可用）、状态级控制（延迟或损坏结果、会话超时）、约束级控制（中途引入或改变任务约束）。

- **奖励信号（Reward Signal，R）**：
  - 可验证奖励：模式合规、顺序约束、信息多样性等确定性检查。
  - 基于Judge的奖励：三个前沿模型（GPT-4o、GPT-5.1、DeepSeek-V3.2）多数投票，评分任务完整性、接地性、格式合规和权衡质量。

- **双模式设计**：
  - 真实模式：通过实时API调用与真实服务交互，产生完全真实的执行轨迹，适合高保真评估。
  - 合成模式（World Engine）：按功能类别（邮件、日历、代码托管等）构建类别级卡片，编码共享响应模式、字段结构和常见失败模式，结合工具模式与会话级执行日志生成现实响应，无需实时API访问。甚至可为尚不存在的领域和工具合成全新环境。

- **智能体框架**：采用Planner-Actor分解，两者由同一LLM实例化。Planner在执行前将任务分解为子目标图，执行中与Actor轨迹对比并纠正反馈；Actor遵循ReAct范式逐步执行。

## 3. 实验设计

- **评估基准与环境规模**：
  - C-World环境本身：204个应用、276个服务器、5,571个工具，平均每任务28.5轮交互。
  - 对比基准（表1）：BFCL v4、ToolBench、AgentBench、ToolEyes、StableToolBench、MCPEval、LiveMCPBench、MCP-Universe、MCP-Bench、Toolathlon、ToolAce、Toucan等12个相关系统，在应用数、工具数、轮数、环境级合成、通配约束、状态控制器、模糊指令等维度上进行对比。

- **主评估（表2）**：对9个代表性LLM进行评估——前沿闭源模型（gpt-5.2、gemini-3-pro-preview、claude-opus-4.5、grok-4）、流行开源模型（deepseek-v3.2、glm-4.6v、qwen3-235b-a22b、gpt-oss-120b）、成本优化基线（gpt-4o-mini）。指标涵盖质量（完整性、接地性）、鲁棒性（恢复率、灵活性）、约束遵循（格式）和规划（工具调用数、目标分解）。

- **消融/对比分析**：
  - 表3：首轮动态vs长期结果的对比，作为Planner-Actor分解的消融。
  - 表4：World Engine合成执行模式下的模型性能，与真实API执行排名计算Spearman相关性。
  - 表5：C-World轨迹微调（Qwen2.5-7B、Qwen3-8B）与Toucan（119k样本）、ToolACE（11.3k样本）在BFCL和MCP-Universe上的对比。
  - 表7：按干扰类型分解的恢复率/灵活性。
  - 表9：人类对齐测量（N=40个查询，人类-人类一致性ρ=0.773）。

- **数据来源**：50个种子任务场景，C-World微调数据1,170条轨迹。

## 4. 资源与算力

- 论文正文及附录**未明确提及**使用的GPU型号、数量或训练时长。
- 从上下文可推断：微调实验使用了Qwen2.5-7B-Instruct和Qwen3-8B两个7B/8B规模模型，训练数据量为1.2k-119k条轨迹，计算量应在单卡或少量GPU即可完成的范围内，但具体硬件配置未披露。
- 评估涉及9个模型（含多个大规模模型）的推断调用，World Engine使用gemini-3.1-flash-lite-preview作为合成引擎，具体API调用成本和计算资源未说明。

## 5. 实验数量与充分性

**实验组数**：
- 1组主排行榜实验（9个模型 × 50个任务）
- 1组首轮vs长期对比分析（9个模型）
- 1组World Engine合成环境评估（9个模型）
- 1组人类对齐测量（N=40，涉及3个Judge模型）
- 1组特征分析（5个维度 × 代表性模型）
- 1组训练数据效率对比（2个骨干模型 × 3个数据源）
- 1组干扰类型分解分析（5个模型 × 3类干预）
- 1组小模型补充实验（4个≤32B模型）

**充分性评估**：
- **优点**：实验设计层次丰富，覆盖了评估、消融、人类对齐、数据效率等多个维度。特别是表3的Planner-Actor消融设计精巧；表7的按干扰类型分解展现了细粒度的行为差异；人类对齐测量增强了评判可信度。
- **客观性考量**：交叉家族多数投票机制设计合理，论文明确论证了不存在OpenAI家族偏倚；干扰注入的公平性保证（每模型接受相同的“逆境预算”）体现了严谨性。
- **局限性**：仅50个合成场景无法穷尽工具-服务器-约束的组合空间；表3中提到的“Rank Shift”仅基于单一基准，稳定性未验证；人类对齐仅在40个查询上进行，样本量偏小。

## 6. 主要结论与发现

**评估发现**：
- 所有LLM规划能力普遍较强，但执行能力显著落后，是造成任务成功率差距的主因（目标分解得分普遍7.7-8.6，但完成度差异巨大）。
- 约束遵循而非工具调用是各模型的主要失败模式。
- DeepSeek-v3.2鲁棒性最佳（恢复率90.6%、灵活性72.4%），甚至超越专有模型，且以最少步骤保持高质量。
- 更高的工具调用量不意味着更高成功率——gpt-4o-mini调用量最高（51.71次）但质量最低，陷入低效“循环陷阱”。
- 首轮表现好不代表长期稳定：gpt-5.2首轮得分最高但最终排名下降5位；而gemini-3-pro和glm-4.6v虽起步平庸但长期反超。

**训练发现**：
- 仅用1,170条C-World轨迹微调的模型在BFCL上达到30.05%准确率，超过用119k样本训练的基线，验证了极致的样本效率。
- World Engine与真实执行的排名相关性达Spearman ρ=0.883，说明合成环境可以可靠替代实时API用于轨迹生成和模型评估。

## 7. 优点

- **四要素环境定义框架**：将环境明确定义为动作空间、任务分布、转换函数和奖励信号，概念清晰、具有通用性和可扩展性。
- **大规模真实工具集**：5,571个经过三阶段验证的工具本身就是一项重要的工程贡献，远超现有基准的工具覆盖度。
- **双模式设计**：真实模式保证高保真评估，合成模式（World Engine）支持无实时API依赖的大规模环境生成，两模式互补覆盖完整开发周期。
- **状态控制器设计精巧**：三类干预（工具级、状态级、约束级）系统化覆盖了真实世界中的各种扰动类型，且通过“逆境预算”保证公平性。
- **数据效率优势显著**：1,170条轨迹打败119k条轨迹，极好地验证了环境生成质量和轨迹“认知密集度”的重要性。
- **人类对齐验证**：LLM-Judge与人类排名相关性（ρ≈0.73-0.76）接近人类-人类一致性上限（ρ=0.773），证明评估方案可信。
- **开放实践**：代码和数据公开，支持社区复现和扩展。

## 8. 不足与局限

- **评估场景数量有限**：论文仅合成50个场景，无法覆盖工具-服务器-约束组合空间的多样性。虽然表5的结果实证支持跨分布迁移，但稀有领域或不太常见的约束组合下的性能仍可能偏离排行榜。
- **小模型分析不足**：主分析聚焦前沿和大型开源模型，论文明确承认在10B以下参数规模中识别出的行为模式（如规划-执行差距）可能表现不同。附录H的小模型实验仅报告总体分数，未深入分析各维度表现。
- **训练数据选取策略可能引入选择性偏差**：仅从“有效首轮动作”中提取训练样本（1,170条），这一策略虽然高效，但也意味着模型未从错误恢复、长期规划调整等过程中学习，可能限制了习得能力的完整性。
- **World Engine的普适性有待验证**：仅在一个生成引擎（gemini-3.1-flash-lite-preview）和50个任务上验证了排名保真度，不同引擎、不同领域的合成质量差异未见分析。
- **人类对齐样本量较小**：仅40个查询的人类标注，虽然相关性接近人类上限，但置信区间较宽，更充分的人类评估有待扩展。
- **硬件资源透明度不足**：未披露训练和评估的具体算力配置，复现成本难以预估。
- **真实模式依赖第三方API**：评估结果的稳定性和可重复性受限于Smithery等第三方服务的可用性和政策变化。

（完）

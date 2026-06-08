---
title: "InfantAgent-Next: A Multimodal Generalist Agent for Automated Computer Interaction"
title_zh: InfantAgent-Next：面向自动化计算机交互的多模态通用智能体
authors: "Bin Lei, Weitai Kang, Zijian Zhang, Winson Chen, Xi Xie, Shan Zuo, Mimi Xie, Ali Payani, Mingyi Hong, Yan Yan, Caiwen Ding"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=NKcwN347H7"
tags: ["query:eca"]
score: 6.0
evidence: 模块化多智能体架构
tldr: 现有通用代理要么围绕单一模型构建复杂流程，要么仅提供模块化工作流，缺乏灵活协作。InfantAgent-Next提出高度模块化架构，融合工具型代理和纯视觉代理，不同模型以逐步方式协作解决解耦任务。在OSWorld、GAIA、SWE-Bench等基准上验证了其通用性和协作效果，为端云协同中的多智能体协作提供了可迁移的设计。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-nkcwn347h7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1373, \"height\": 643, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nkcwn347h7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1352, \"height\": 1176, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nkcwn347h7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1452, \"height\": 364, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nkcwn347h7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 915, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-nkcwn347h7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1362, \"height\": 1309, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1440, \"height\": 435, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1450, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1454, \"height\": 860, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1459, \"height\": 826, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1438, \"height\": 389, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1445, \"height\": 245, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1452, \"height\": 114, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-nkcwn347h7/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1466, \"height\": 176, \"label\": \"Table\"}]"
motivation: 现有通用代理缺乏灵活的模块间协作，难以处理多样化的计算机交互任务。
method: 提出高度模块化架构，集成工具代理与纯视觉代理，通过逐步协作求解解耦任务。
result: "在OSWorld、GAIA等基准上取得约7.27%的准确率，优于同类通用代理。"
conclusion: 模块化多智能体协作能有效提升通用代理的任务覆盖能力。
---

## Abstract
This paper introduces \textsc{InfantAgent-Next}, a generalist agent capable of interacting with computers in a multimodal manner, encompassing text, images, audio, and video.
Unlike existing approaches that either build intricate workflows around a single large model or only provide workflow modularity, our agent integrates tool-based and pure vision agents within a highly modular architecture, enabling different models to collaboratively solve decoupled tasks in a step-by-step manner. 
Our generality is demonstrated by our ability to evaluate not only pure vision-based real-world benchmarks (i.e., OSWorld), but also more general or tool-intensive benchmarks (e.g., GAIA and SWE-Bench).
Specifically,
we
achieve a $\mathbf{7.27\\%}$ accuracy gain over Claude-Computer-Use on OSWorld.  
Codes and evaluation scripts are included in the supplementary material and will be released as open-source.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容生成的结构化、深入、客观的中文总结。

# 论文总结：InfantAgent-Next

## 1. 核心问题与整体含义（研究动机与背景）

- **背景**：自动化AI智能体在数字时代至关重要，需通过多模态（文本、图像、音频、视频）理解用户意图，并转化为精确的界面操作。
- **问题**：现有方法分为两类，但都有明显局限：
    1.  **工具型智能体**（如OpenHands、AutoGPT）：依赖单一模型决定何时使用工具，需要为每个桌面场景手动定义和集成工具，缺乏通用性且脆弱。
    2.  **纯视觉智能体**（如UI-TARS、Aguvis）：依赖vLLM通过GUI控制计算机，虽适用范围广，但在可简单调用工具的任务（如文档编辑、代码操作）上准确率低。
    3.  **单一高级模型**（如Claude-3.7-Sonnet）虽能分解复杂问题，但在精确执行（如GUI点击坐标定位、正确的行号选择）上频繁失败。
- **核心挑战**：如何同时实现高任务级准确率和广泛通用性，需要一种融合工具型与纯视觉范式的混合智能体范式。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：提出高度模块化架构，将智能体的工作流、工具选择和工具执行进行细粒度模块化，每个子任务路由给最合适的专业模型（推理模型、视觉定位模型、音频分析模型等），并将各模型输出无缝合并到统一对话上下文中，实现真正的多模态交互。

- **关键技术细节**：
    - **架构**（图2）：
        1.  **参数配置**：用户可为工作流模型（规划、工具选择、执行）和工具模型（图像、音频、视频）分配不同模型。
        2.  **智能体初始化**：为每个模型分配特定角色和提示模板，打包成统一多模态工具包，并初始化内存缓存。
        3.  **智能体工作流**：循环迭代，每轮包括：规划（Planner）生成任务 → 工具选择（Tool Selector）从工具集中选择最合适的工具 → 执行（Executor）调用工具并收集反馈，直到任务完成。
    - **内存管理**：将每次模型输出用特殊标签（`<thought>`, `<task>`, `<toolkit>`, `<execute_bash>`等）结构化存储。在不同阶段（规划、工具选择、执行）提取并重建相应对话历史，避免无关信息干扰。
    - **工具集**：定义了7个工具包（文件读取、文件搜索、文件编辑、网页浏览、计算机使用、代码执行、高级工具），每个工具包带有使用示例。工具选择时动态选择相关子集，降低推理开销和选择难度。
    - **鼠标点击改进（算法1）**：迭代区域裁剪。先截全屏，进行n次迭代：每次将当前区域和元素描述输入视觉定位模型得到坐标，然后以该坐标为中心裁剪更小区域。最后在最终小区域上执行点击。通过逐步缩小搜索区域提高定位精度。
    - **文件编辑改进（算法2）**：采用四参数格式（文件路径、起始行号s和结束行号e、替换内容）。首先验证行边界是否匹配预期内容；若不匹配，则采用备用策略：模糊匹配（`Fuzzify`）预期内容，通过`FindBestMatch`找到最佳区间，更新请求后最多重试`MAX_ITER`次。

## 3. 实验设计：数据集、基准、对比方法

- **视觉能力（OSWorld）**：
    - **基准**：OSWorld（369个开放式桌面任务，覆盖网页浏览、文件操作、代码编辑等）。
    - **对比方法**：UI-TARS、OpenAI CUA、Claude Computer Use、Agent S2、AGUVIS、Aria-UI、OS-Atlas、SeeClick、Qwen2.5-VL等。
    - **设置**：Claude-3.7-Sonnet用于推理，UI-TARS-1.5-7B用于视觉定位，`max_steps=50`。
- **逻辑推理能力（SWE-Bench）**：
    - **基准**：SWE-Bench-Lite（300个GitHub Issue）和SWE-Bench-Verified（500个案例，采样50个评估）。
    - **对比方法**：SWE-agent、OpenHands、AutoCodeRover、Agentless、CodeStory Midwit Agent、Amazon Q Developer Agent等。
    - **设置**：SWE-Bench-Lite使用GPT-4o；SWE-Bench-Verified使用Claude-3.7-Sonnet；DeepSeek-V3-0324作为专用文件编辑模型。
- **通用任务（GAIA）**：
    - **基准**：GAIA验证集（分三级难度，需推理、多模态理解、网页导航、工具使用）。
    - **对比方法**：Langfun Agent、Trase Agent、OWL、TapeAgents、Open Deep Research等（根据官方排行榜）。
    - **设置**：Claude-3.7-Sonnet（推理执行）、Deepseek-V3-0324（工具选择）、gpt-4o-audio-preview（音频处理）、UI-TARS-1.5-7B（视觉理解）。
- **视觉定位消融（ScreenSpot-Pro）**：
    - **基准**：ScreenSpot-Pro（1581张高分辨率专业截图，5个行业23个应用，3个操作系统）。
    - **设置**：2×A100 80G GPU。消融裁剪区域宽度、高度、宽高比以及迭代次数（0-4次）。
- **文件编辑评估（SWE-Bench-Verified子集）**：
    - **基准**：从SWE-Bench-Verified按仓库类别随机抽样10%的任务。
    - **指标**：RepairSuccessRate (RSR) = 修复数/失败数；OverallRepairRate (ORR) = 修复数/总数。
    - **设置**：评估每个任务的解决方案，分类统计成功修复、未修复的错误类型（行号偏移、内容不匹配、语法错误等）。

## 4. 资源与算力

- **视觉定位实验**：明确提到使用2×A100 80G GPU进行ScreenSpot-Pro消融实验。
- **其他实验**：论文未明确给出训练或推理所用GPU型号/数量/时长，但提及使用了VMware虚拟机（OSWorld）、以及多个商业API模型（Claude、GPT-4o等）。可推断实验主要依赖API调用，本地仅需少量GPU加载视觉定位模型（如UI-TARS-1.5-7B）。

## 5. 实验数量与充分性

- **实验组数**：
    - 主要基准：OSWorld（1组）、SWE-Bench-Lite（1组）、SWE-Bench-Verified（1组）、GAIA（1组）。
    - 消融实验：
        - 视觉定位：在ScreenSpot-Pro上从4个维度（宽度、高度、宽高比、迭代次数）进行了消融，共计约4×3=12组不同设置（图3）。
        - 文件编辑：在SWE-Bench-Verified子集上进行了错误类型统计和修复率分析（1组），报告了RSR和ORR。
- **充分性与公平性**：
    - 视觉实验对比了多个开源和闭源SOTA方法，且设置`max_steps=50`与部分基线一致，公平性较好。
    - 逻辑推理任务完全关闭GUI工具，专注代码能力，对比基线包括多个专业代码智能体。
    - 通用任务使用官方排行榜数据比较，设置相对公平。
    - 消融实验系统全面，覆盖了算法关键超参数的影响。
    - 总体充分，但未报告多次运行的标准差（除图3有误差棒外）。另外，SWE-Bench-Verified仅采样50个案例，可能存在抽样偏差。

## 6. 主要结论与发现

- **主要结论**：InfantAgent-Next通过模块化架构融合工具型和纯视觉智能体，在三大类基准上均达到或接近SOTA水平，证明了混合范式的有效性。
- **具体发现**：
    1.  **OSWorld**：以35.3%准确率（50步）超过Claude Computer Use（26.0%，50步）7.27个百分点，仅次于UI-TARS-72B（38.0%）。
    2.  **SWE-Bench-Verified**：66%准确率，与OpenHands（68%）接近，优于多家闭源产品（如Amazon Q Developer Agent 54%）。
    3.  **GAIA**：56.97%平均分，在开源智能体中排名第二（仅次于OWL 58.18%），且在Level 2任务上取得SOTA（62.79%）。
    4.  **视觉定位消融**：迭代裁剪区域的最优设置为迭代3次（准确率51.36%），迭代2次是性能与推理成本的较好折中（49.53%）。裁剪区域的高度调整效果最好。
    5.  **文件编辑**：总体成功率90.4%（166/184个正确命令中），RSR为84.3%，ORR为51.4%。能有效修复行号偏移（30%）、内容不匹配（13%）和语法错误（6%）。

## 7. 优点

- **方法亮点**：
    - 高度模块化设计，支持多种模型协同工作，避免单一模型瓶颈。
    - 创新的迭代区域裁剪算法，显著提升GUI点击定位精度。
    - 稳健的文件编辑算法，结合行号验证和模糊匹配回退机制，修复率高。
    - 动态工具选择，降低推理开销，增强可伸缩性。
- **实验亮点**：
    - 覆盖多类型基准（视觉操作、代码工程、通用问答），全面评估通用性。
    - 与多个最新开源和闭源SOTA进行公平对比。
    - 对关键算法（迭代裁剪、文件编辑）进行了详尽的消融分析和错误分析。

## 8. 不足与局限

- **实验覆盖**：
    - SWE-Bench-Verified仅采样50例，可能不足以代表全量500例的性能，存在抽样偏差。
    - ScreenSpot-Pro消融可能未覆盖所有超参数组合，且未在更大模型（如UI-TARS-72B）上验证迭代裁剪效果。
    - 未在更多样化的真实UI场景（如移动端、复杂设计软件）上测试。
- **偏差风险**：
    - 实验高度依赖特定商业模型（Claude、GPT-4o），结果可能随模型更新而改变，且无法完全复现（闭源API）。
    - 视觉定位模型仅用了UI-TARS-1.5-7B，未尝试其他定位模型。
- **应用限制**：
    - 模块化架构引入多余组件（如内存提取、动态工具选择），可能增加系统复杂度和延迟。
    - 论文未讨论低资源环境（如无高性能GPU、无法调用商业API）下的适用性。
    - 文件编辑算法假设文件是文本且能模糊匹配，对于二进制文件或高度混淆的代码可能失效。
    - 安全性方面：虽然使用隔离VM，但若工具执行有误仍可能导致系统状态损坏或数据泄露（如恶意文件操作）。
- **其他**：
    - 论文未提供多次运行的统计置信区间（除ScreenSpot-Pro消融外）。
    - 缺少与HumanAgent（人类表现）的对比，难以衡量实际提升上限。

（完）

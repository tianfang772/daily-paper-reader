---
title: New Neural Controller Generalises Modular Control Across Lower-Limb Tasks Using Internal Models
title_zh: 基于内部模型的新型神经控制器在下肢任务中实现了模块化控制的泛化
authors: "Munoz, D., Holland, D., Severini, G."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.1101/2023.12.04.569887v7.full.pdf"
tags: ["query:q2"]
score: 9.0
evidence: 用于下肢运动任务和步态控制的内部模型
tldr: 本研究针对现有步态控制器生理基础薄弱且行为单一的问题，提出了一种基于内部模型的模块化神经控制器（IMMC）。该控制器模拟中脑运动区激活不同的内部模型，通过组织功能性肌肉协同网络，实现了在单次模拟中完成起立、行走、后退及停止等多种下肢运动任务的平滑切换。实验结果显示，该控制器的生物力学表现与肌肉激活模式与实验观测一致，为解释复杂运动行为的产生机制提供了新视角。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-001.webp\", \"caption\": \"Figure 1. Scheme of IMMC, showing its hierarchy, from top to bottom: Control layer, Planner layer, Synergistic layer, and Motoneuron layer. MLR: mesencephalic locomotor region, IM: Internal Model, S1: first synergy, Sn: n-th synergy, MPExt/Flex: extensor/flexor motor pools, F: sensory feedback, MTUExt/Flex: extensor/flexor musculotendon unit.\", \"page\": 2, \"index\": 1, \"width\": 471, \"height\": 379}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-002.webp\", \"caption\": \"Figure 2. Instantaneous anterior/posterior speed of Head-Arms-Torso (HAT) for: (A) Stand-To-Walk (t = 5 s) and Walk-To-Stand (t = 10 s) transitions with a gait speed of 0.8 ms-1. (B) Stand-To-Backward Walk (t = 5 s) and Backward Walk-To-Stand (t = 10 s). (C) Speed transitions for forward gait at 0.8, 0.9, 1.2, 1.3, 1.5, 1.6, and 1.8 ms-1.\", \"page\": 2, \"index\": 2, \"width\": 450, \"height\": 650}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-003.webp\", \"caption\": \"Figure 6. Principles of the legged mechanics. The figure presents the five principles of legged mechanics. The synergies implemented in the IMMC are based on these principles.\", \"page\": 6, \"index\": 3, \"width\": 468, \"height\": 435}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-004.webp\", \"caption\": \"Figure 5. Comparison between simulated and experimental biomechanics and muscular activation for backward walking. (A) Experimental and simulated angular positions for hips, knees, and ankles at 1.3 ms-1. Green: simulated data, grey: experimental data. Upward direction: flexion, downward direction: extension. (B) GRF across the gait cycle at 1.3 ms-1. Experimental and simulated GRF. Yellow: simulated data, grey: experimental data. (C) Muscle activation patterns along the gait cycle at 1.3 ms-1. Orange: simulated data, grey: experimental data. Experimental data for HAM was not present in the referenced dataset. Experimental angular positions, GRF, and muscle trajectories taken from [28]. Blue vertical dotted line: experimental foot-off (76 %), black vertical dotted line: simulation foot-off (77 %).\", \"page\": 4, \"index\": 4, \"width\": 483, \"height\": 710}]"
motivation: 现有的神经控制模型难以在单一模拟中实现多种运动任务的平滑切换，且缺乏足够的生理学依据。
method: 提出一种基于内部模型的模块化控制器，利用简化的中脑运动区模型激活特定任务的肌肉协同网络。
result: 成功模拟了从站立到行走、后退及再次站立的转换，并能通过调节少量控制信号实现步态速度的灵活变换。
conclusion: 该模块化架构为产生异质性运动行为提供了一种具有生理合理性的计算机制。
---

## 摘要
神经控制的计算模型是评估运动控制原理的有力工具，而这些原理在传统的实验设置中无法直接测试。目前的步态控制器在生理基础方面存在困难，且只能复制一小部分离散行为。目标：在此我们提出了一种新型神经控制器，即基于内部模型的模块化控制器（Internal Model-based Modular Controller），它可以在单次模拟中实现多种下肢运动任务之间的切换。该架构包含一个中脑运动区（Mesencephalic Locomotor Region）的简化模型，用于激活不同的内部模型。这些内部模型将功能性肌肉协同作用组织成特定任务的网络，从而产生跨多块肌肉的协调活动。结果：该控制器实现了“站立-行走-站立”以及“站立-倒走-站立”的转换，并通过调节少量控制信号在模拟中调制步态速度。观察到的模拟生物力学和肌肉激活模式与实验观察结果基本一致。结论：我们的结果表明，所提出的模块化架构为产生异质运动行为提供了一种合理的机制。

## Abstract
Computational models of neural control are a powerful tool for evaluating principles of motor control that cannot be tested directly in conventional experimental settings. Current gait controllers struggle with physiological grounding and can replicate a small set of discrete behaviours. Objective: here we propose a new neural controller, the Internal Model-based Modular Controller, that can transition between multiple lower-limb motor tasks within a single simulation. The architecture comprises a simplified model of the Mesencephalic Locomotor Region, which activates different internal models. These internal models organise functional muscle synergies into task-specific networks that generate coordinated activity across multiple muscles. Results: the controller performs Stand-To-Walk-To-Stand and Stand-To-Backward Walking-To-Stand transitions and modulates gait speed within a simulation by adjusting a few control signals. The observed simulated biomechanics and muscle activation patterns are generally consistent with experimental observations. Conclusions: Our results show that the proposed modular architecture represents a plausible mechanism for producing heterogeneous motor behaviours.

---

## 论文详细总结（自动生成）

这是一份关于论文《New Neural Controller Generalises Modular Control Across Lower-Limb Tasks Using Internal Models》的结构化深入总结：

### 1. 核心问题与整体含义（研究动机和背景）
论文的核心问题在于：**如何构建一个既具有生理合理性，又能在单一模拟框架内实现多种下肢运动任务平滑切换的神经控制器。**

现有的步态控制器（如纯反射模型或中央模式发生器 CPG 模型）存在以下局限：
*   **任务单一性**：通常只能模拟单一的行走任务，难以处理从站立到行走、倒走或速度切换的动态转换。
*   **生理基础薄弱**：往往忽略了高级神经中枢（如中脑运动区 MLR）和内部模型（Internal Models）在协调肌肉协同作用中的作用。
*   **控制维度高**：缺乏模块化结构，导致在处理复杂任务时控制参数过多，缺乏泛化能力。

### 2. 论文提出的方法论：IMMC 架构
研究者提出了一种**基于内部模型的模块化控制器（Internal Model-based Modular Controller, IMMC）**，其核心思想是模拟生物神经系统的分层控制机制。

*   **四层分层架构**：
    1.  **控制层 (Control Layer)**：模拟中脑运动区（MLR），负责根据目标任务（如前行、倒走）发送激活信号。
    2.  **规划层 (Planner Layer)**：包含多个**内部模型 (IMs)**。每个 IM 对应特定任务，负责将高级指令转化为对肌肉协同作用的组织模式。
    3.  **协同层 (Synergistic Layer)**：包含 6 个功能性肌肉协同模块（S1-S6），如“支撑重力”、“踝关节推离”、“摆动腿部”等。这些模块是跨任务共享的“运动原语”。
    4.  **运动神经元层 (Motoneuron Layer)**：整合协同层输出与脊髓反射信号，最终驱动肌肉骨骼模型。
*   **关键技术细节**：
    *   **功能协同设计**：基于腿部力学原理（如 Compliant-leg-behaviour），将复杂的肌肉活动简化为 6 个功能模块。
    *   **参数优化**：使用**协方差矩阵自适应进化策略 (CMA-ES)** 算法，分六个阶段对 176 个控制器参数进行顺序优化，确保模型在不同任务下的稳定性。

### 3. 实验设计
*   **测试场景**：
    1.  **STWTS (站立-行走-站立)**：模拟从静止开始行走，达到稳定速度后再停止。
    2.  **STBWTS (站立-倒走-站立)**：测试控制器在相反运动方向上的泛化能力。
    3.  **速度转换**：在 0.8 m/s 到 1.8 m/s 范围内进行 7 种不同速度的步态模拟。
*   **Benchmark（基准）**：
    *   使用 Zych 等人（2021）和 Fukuchi 等人（2018）提供的**人类实验数据集**，包括关节角度（髋、膝、踝）、地面反作用力（GRF）以及 9 块主要下肢肌肉的肌电信号（EMG）。
*   **对比指标**：计算模拟轨迹与实验数据之间的**互相关系数 (r)** 和**时间滞后 (Δ)**。

### 4. 资源与算力
*   **算力说明**：论文**未明确指出**使用的具体硬件（如 GPU/CPU 型号及数量）。
*   **训练细节**：提到了优化过程。每个优化阶段最大迭代次数为 600 次，每代包含 5 个父代和 40 个后代。由于涉及复杂的肌肉骨骼动力学模拟和进化算法，预计需要中等规模的 CPU 集群算力支持。

### 5. 实验数量与充分性
*   **实验规模**：研究涵盖了前向行走、后向行走、站立平衡以及 7 种速度梯度的模拟。
*   **充分性评价**：
    *   **充分性高**：实验不仅关注稳态步态，更重点分析了任务间的**过渡态**，这在同类研究中较为少见。
    *   **客观性**：通过与公开的人类实验数据集进行定量对比（r 值大多超过 0.8），证明了模型的有效性。
    *   **消融/对比**：虽然没有传统的消融实验，但通过“前向”与“后向”行走共享协同模块的对比，验证了模块化架构的泛化价值。

### 6. 主要结论与发现
*   **多任务泛化**：IMMC 仅需调节极少数控制信号（如 IM 的激活权重），即可在单次模拟中实现站立、前行和倒走的无缝切换。
*   **生物力学一致性**：模拟产生的关节运动学和地面反作用力与人类实验数据高度吻合（r > 0.9）。
*   **代谢成本合理**：在 1.3 m/s（人类偏好速度）时，模拟的代谢运输成本（3.5 J/kg/m）与实验观测值接近。
*   **协同共享**：证明了前向和后向行走可以共享同一套底层肌肉协同模块，区别仅在于内部模型对这些模块的组织方式。

### 7. 优点
*   **高度模块化**：将复杂的神经控制简化为可解释的四层架构，降低了控制维度。
*   **任务灵活性**：突破了以往控制器只能运行单一任务的限制，实现了动态任务切换。
*   **生理可解释性**：模型组件（MLR, IM, Synergies）均有神经生理学对应关系，可用于研究病理性运动（如中风后的协同改变）。

### 8. 不足与局限
*   **模型简化**：生物力学模型较为简单（平面模型），缺乏躯干肌肉和前庭反射（Vestibular reflexes），这导致某些肌肉（如股直肌 RF、胫骨前肌 TA）的激活模式与实验数据存在偏差。
*   **踝关节异常**：在倒走模拟中，踝关节出现了过度跖屈，这反映了简化模型在处理复杂接触力学时的局限。
*   **参数依赖**：虽然参数量已减少，但仍需通过复杂的 CMA-ES 算法进行多阶段优化，参数的物理意义与生物学真实值的对应关系仍需进一步验证。

（完）

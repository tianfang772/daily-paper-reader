---
title: New Neural Controller Generalises Modular Control Across Lower-Limb Tasks Using Internal Models
title_zh: 新型神经控制器利用内部模型在下肢任务中实现模块化控制的泛化
authors: "Munoz, D., Holland, D., Severini, G."
date: 2026-07-10
pdf: "https://www.biorxiv.org/content/10.1101/2023.12.04.569887v7.full.pdf"
tags: ["query:q4"]
score: 6.0
evidence: 用于下肢任务控制的内部模型
tldr: 本研究针对现有步态控制器生理基础薄弱且难以处理多种连续动作的问题，提出了一种基于内部模型的模块化神经控制器（IMMC）。该架构模拟中脑步态区（MLR）激活不同的内部模型，通过功能性肌肉协同网络生成协调的肌肉活动。实验证明，该控制器能在单一模拟中实现站立、行走及后退等多种任务的平滑切换与速度调节，其生物力学特征与实验观察一致，为理解人类异质性运动行为提供了生理学解释。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-001.webp\", \"caption\": \"Figure 1. Scheme of IMMC, showing its hierarchy, from top to bottom: Control layer, Planner layer, Synergistic layer, and Motoneuron layer. MLR: mesencephalic locomotor region, IM: Internal Model, S1: first synergy, Sn: n-th synergy, MPExt/Flex: extensor/flexor motor pools, F: sensory feedback, MTUExt/Flex: extensor/flexor musculotendon unit.\", \"page\": 2, \"index\": 1, \"width\": 471, \"height\": 379}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-002.webp\", \"caption\": \"Figure 2. Instantaneous anterior/posterior speed of Head-Arms-Torso (HAT) for: (A) Stand-To-Walk (t = 5 s) and Walk-To-Stand (t = 10 s) transitions with a gait speed of 0.8 ms-1. (B) Stand-To-Backward Walk (t = 5 s) and Backward Walk-To-Stand (t = 10 s). (C) Speed transitions for forward gait at 0.8, 0.9, 1.2, 1.3, 1.5, 1.6, and 1.8 ms-1.\", \"page\": 2, \"index\": 2, \"width\": 450, \"height\": 650}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-003.webp\", \"caption\": \"Figure 6. Principles of the legged mechanics. The figure presents the five principles of legged mechanics. The synergies implemented in the IMMC are based on these principles.\", \"page\": 6, \"index\": 3, \"width\": 468, \"height\": 435}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-1101-2023-12-04-569887-v7/fig-004.webp\", \"caption\": \"Figure 5. Comparison between simulated and experimental biomechanics and muscular activation for backward walking. (A) Experimental and simulated angular positions for hips, knees, and ankles at 1.3 ms-1. Green: simulated data, grey: experimental data. Upward direction: flexion, downward direction: extension. (B) GRF across the gait cycle at 1.3 ms-1. Experimental and simulated GRF. Yellow: simulated data, grey: experimental data. (C) Muscle activation patterns along the gait cycle at 1.3 ms-1. Orange: simulated data, grey: experimental data. Experimental data for HAM was not present in the referenced dataset. Experimental angular positions, GRF, and muscle trajectories taken from [28]. Blue vertical dotted line: experimental foot-off (76 %), black vertical dotted line: simulation foot-off (77 %).\", \"page\": 4, \"index\": 4, \"width\": 483, \"height\": 710}]"
motivation: 现有的步态控制器缺乏生理学依据，且难以在单一模拟中实现多种运动行为之间的灵活切换。
method: 提出一种基于内部模型的模块化控制器，利用模拟中脑步态区激活特定任务的肌肉协同网络。
result: 控制器成功实现了站立、行走、后退等任务间的平滑转换及速度调节，且模拟数据与实验观测相符。
conclusion: 该模块化架构为产生复杂的异质性运动行为提供了一种具有生理合理性的神经控制机制。
---

## 摘要
神经控制的计算模型是评估运动控制原理的有力工具，而这些原理在传统的实验设置中无法直接测试。目前的步态控制器在生理基础方面存在困难，且只能复制一小部分离散行为。目标：在此，我们提出了一种新型神经控制器——基于内部模型的模块化控制器（Internal Model-based Modular Controller），它可以在单次模拟中实现多种下肢运动任务之间的转换。该架构包含一个简化的中脑步行区（Mesencephalic Locomotor Region）模型，用于激活不同的内部模型。这些内部模型将功能性肌肉协同作用组织成特定任务的网络，从而在多块肌肉之间产生协调活动。结果：该控制器能够执行“站立-行走-站立”以及“站立-倒走-站立”的转换，并通过调整少量控制信号在模拟中调节步态速度。观察到的模拟生物力学和肌肉激活模式与实验观察结果基本一致。结论：我们的结果表明，所提出的模块化架构代表了产生异质运动行为的一种合理机制。影响声明：本研究提出了一种模块化神经控制器，该控制器利用内部模型和功能性肌肉协同作用，在单一模拟框架内重现了异质的腿部运动行为。

## Abstract
Computational models of neural control are a powerful tool for evaluating principles of motor control that cannot be tested directly in conventional experimental settings. Current gait controllers struggle with physiological grounding and can replicate a small set of discrete behaviours.

Objectivehere we propose a new neural controller, the Internal Model-based Modular Controller, that can transition between multiple lower-limb motor tasks within a single simulation. The architecture comprises a simplified model of the Mesencephalic Locomotor Region, which activates different internal models. These internal models organise functional muscle synergies into task-specific networks that generate coordinated activity across multiple muscles.

Resultsthe controller performs Stand-To-Walk-To-Stand and Stand-To-Backward Walking-To-Stand transitions and modulates gait speed within a simulation by adjusting a few control signals. The observed simulated biomechanics and muscle activation patterns are generally consistent with experimental observations.

ConclusionsOur results show that the proposed modular architecture represents a plausible mechanism for producing heterogeneous motor behaviours.

IMPACT STATEMENTThis study presents a modular neural controller, which employs internal models and functional muscle synergies to reproduce heterogeneous legged behaviours within a single simulation framework.
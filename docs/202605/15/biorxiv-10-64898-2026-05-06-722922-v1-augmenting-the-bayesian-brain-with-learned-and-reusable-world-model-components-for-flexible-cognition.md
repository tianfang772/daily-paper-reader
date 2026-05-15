---
title: Augmenting the Bayesian Brain with learned and reusable world-model components for flexible cognition
title_zh: 利用已学习且可重用的世界模型组件增强贝叶斯大脑以实现灵活认知
authors: "Findling, C., Lee, J. K., Bakermans, J. J. W., Pouget, A., Wyart, V."
date: 2026-05-08
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.06.722922v1.full.pdf"
tags: ["query:q1"]
score: 6.0
evidence: 作为世界模型组件的模块化神经状态空间模型
tldr: 该研究针对贝叶斯大脑假设中生成模型结构固定且推理计算繁重的局限，提出了模块化神经状态空间模型。该框架通过可学习且可重用的世界模型组件取代预设规则，支持在不同任务间灵活组合，实现了零样本泛化。实验证实人类行为符合该模型的预测，为理解灵活认知的计算原理提供了新视角。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有的贝叶斯大脑模型受限于预设的特定任务结构和高复杂度的迭代推理，难以应对灵活多变的认知需求。
method: 提出一种模块化神经状态空间模型，利用可学习的世界模型组件和摊销神经更新来实现推理的重用与组合。
result: 该模型能够通过重新组合组件实现零样本泛化，且其预测的推理参数相关性在人类行为实验中得到了证实。
conclusion: 模块化且可重用的世界模型组件是实现灵活认知的一种关键计算机制。
---

## 摘要
贝叶斯大脑假说认为认知依赖于世界的内部生成模型，然而现有的实现仍受限于预先指定的、特定于任务的生成结构以及计算量巨大的迭代推理方案。在此，我们引入模块化神经状态空间模型作为贝叶斯大脑的一种可扩展实现，利用已学习的世界模型组件和摊销神经更新取代了固定的生成结构和预先指定的推理规则。该框架保留了通过隐藏原因解释观测值的核心承诺，同时使推理过程变得可学习且可重用，而非预先指定且特定于任务。这些模型的模块化实现允许已学习的组件在具有相似潜在动力学但表面不同的任务之间进行无缝重组和堆叠。这种计算重用支持零样本泛化，并预测了任务间推理参数的选择性相关性。我们在人类行为中证实了这些关键预测，从而将已学习且可重用的世界模型组件确定为灵活认知的一种候选计算原理。

## Abstract
The Bayesian Brain hypothesis assumes that cognition relies on internal generative models of the world, yet existing implementations remain constrained by pre-specified, task-specific generative structures and computationally heavy iterative inference schemes. Here, we introduce modular neural state-space models as a scalable realization of the Bayesian Brain, replacing fixed generative structures and pre-specified inference rules with learned world-model components and amortized neural updates. This framework preserves the core commitment to explaining observations through hidden causes while making inference learned and reusable rather than pre-specified and task-specific. Our modular implementation of these models affords learned components to be seamlessly recombined and stacked across superficially different tasks that share similar latent dynamics. Such computational reuse supports zero-shot generalization and predicts selective correlations of inference parameters between tasks. We confirm these key predictions in human behavior, identifying learned and reusable world-model components as a candidate computational principle for flexible cognition.
> 声明：本项目是 [huggingface/diffusion-models-class](https://github.com/huggingface/diffusion-models-class) 的中文翻译版。
>
> [English Version (英文原版)](https://github.com/huggingface/diffusion-models-class/blob/main/README.md)
---
# 扩散模型课程

欢迎来到扩散模型课程！

本课程由 Hugging Face 团队的专家们携手打造，旨在：

- 讲解这些模型背后的理论知识。
- 通过使用 `diffusers` 库以及其他 Hugging Face 生态系统中的工具（如 `transformers` 和 `accelerate`），将理论付诸实践。

## 课程内容

### Unit 1: 扩散模型基础

- **01_introduction_to_diffusers.ipynb**: 介绍扩散模型的基本概念和 `diffusers` 库的核心组件。你将训练一个简单的扩散模型来生成蝴蝶图像，并学习如何使用 scheduler 向数据添加噪声、创建并训练 UNet 模型，以及将各个部分组合成一个可运行的 pipeline。

- **02_diffusion_models_from_scratch.ipynb**: 从零开始实现一个简化版的扩散模型，深入理解其工作原理。本笔记将讨论破坏过程（向数据逐步注入噪声）、UNet 的概念及其实现、扩散模型训练以及采样理论，并与 `diffusers` 库中的 DDPM 实现进行比较。

### Unit 2: 扩散模型进阶技术

- **01_finetuning_and_guidance.ipynb**: 介绍两种调整已有扩散模型的方法：微调（在新数据上重新训练现有模型）和引导（在推断阶段对生成过程进行引导）。你将学习如何编写采样循环、使用新的调度器更快地生成样本，以及通过附加损失函数来引导采样过程。

- **02_class_conditioned_diffusion_model_example.ipynb**: 演示如何构建类别条件扩散模型。在这个示例中，你将在 MNIST 数据集上训练一个模型，使其能够根据指定的数字类别生成相应的图像。

### Unit 3: Stable Diffusion 模型

- **01_stable_diffusion_introduction.ipynb**: 介绍如何利用现有的 Stable Diffusion pipeline 来生成和修改图像，并了解管线中的关键组件。内容包括使用 `StableDiffusionPipeline` 根据文本生成图像、探索 pipeline 中的核心组件（VAE、tokenizer、text encoder、UNet 和不同的 scheduler），以及使用 Img2Img、修复（Inpainting）和 Depth2Img 等高级编辑功能。

- **02_dreambooth.ipynb**: 介绍 DreamBooth 技术，这是一种强大的个性化微调方法，允许你使用少量（3-5张）特定主体的图像来训练 Stable Diffusion 模型，使其能够在各种场景和姿势中生成该主体的新图像。本笔记本将指导你如何使用 `diffusers` 库实现 DreamBooth 微调，包括准备训练数据、设置训练参数、以及如何在微调过程中保留模型的先验知识。

- **03_stable_diffusion_deep_dive.ipynb**: 深入剖析 Stable Diffusion 模型的内部工作原理。本笔记本将拆解 Stable Diffusion pipeline 的简洁接口，详细解释其背后的代码实现，逐一检视不同组件（如 VAE、UNet、文本编码器等）的职责与作用，帮助你理解整个生成过程，并学习如何根据需求自定义和调整模型行为。
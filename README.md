# Mini-LLM

Mini-LLM 是一个基于 PyTorch 从零实现的 0.1B 参数自回归语言模型项目。

本项目复现了现代大语言模型的核心结构与训练流程，包括模型架构实现、分词器训练、预训练、指令微调以及强化学习对齐，并在阅读理解与因果推理任务上进行评测。

## 模型结构

- Transformer Decoder-only 架构
- 12 层，Hidden Size 768
- 约 0.1B 参数
- 支持 RoPE 位置编码、RMSNorm、GQA 注意力机制
- 可选 FlashAttention 加速

## 训练流程

1. 训练 15k 词表 BPE Tokenizer  
2. 自回归语言模型预训练  
3. 指令微调（SFT）  
4. 基于 GRPO 的强化学习对齐  

## 评测任务

- CLUE C3（阅读理解）
- XCOPA（因果推理）

## 环境

- Python 3.10
- PyTorch 2.x

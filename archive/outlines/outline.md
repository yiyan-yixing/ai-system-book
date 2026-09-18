# 《AI System 原理 —— 从一个 Token，到一个 AI System》目录

> 本页为对外版目录。完整写作大纲（含素材索引、写作进度与内部约定）为内部文档，不公开。

## 序章 · 第 0 节

0. 从一个模型，到一个 AI System（序章）

## 上篇 · 零件：从一个 Token，到一个模型

### 第一章 · Token 与向量

1. Token：你和模型之间唯一的通货
2. Embedding：从一个数字到一个向量

### 第二章 · 神经网络在学什么

3. 神经网络学到了什么：哪些参数是白养的
4. Loss / 反向传播：错怎么摊回每个参数
5. 优化器与归一化：RMSNorm、残差、学习率

### 第三章 · Transformer：一个架构改变一切

6. Transformer 为什么改变 AI：从 RNN 到 attention
7. Attention 在算什么：Q·K、softmax、O(n²)
8. Self-Attention 与上下文：最贵的那块地
9. Multi-Head：为什么一个头不够
10. 位置编码：模型怎么知道谁在谁前面
11. FFN：参数的大头在哪里
12. 一层 Transformer 全解

### 第四章 · 稀疏与高效：让大模型跑得动

13. MoE 稀疏化：参数多、算得少
14. KV cache 与高效注意力：上下文为什么贵
15. 量化：4-bit 之后还剩多少

### 第五章 · 预训练：模型怎么学

16. 预训练在训练什么：下一个 token 预测
17. Scaling Law 与数据：词表大小为何影响能力

### 第六章 · 后训练与对齐

18. SFT：指令微调为何有效
19. RLHF / RLVR：从人工偏好到可验证奖励
20. DPO 与蒸馏：把大模型压进小模型

### 第七章 · 本地训练：亲手造一个

21. 从零写一个小 GPT
22. 小规模 scaling 实验

## 下篇 · 系统：从一个模型，到一个 AI System

### 第八章 · Small Model

23. Small Model：小模型不是缩水的大模型

### 第九章 · Model Pool / Router

24. Model Pool：为什么一个模型不够
25. Router：把对的活派给对的模型

### 第十章 · Context

26. Context：系统里最贵的那块地

### 第十一章 · Knowledge / Graph · Memory

27. 组织记忆：从文件夹到图谱

### 第十二章 · Agent

28. Agent：一个模型不够，一个 agent 也不够
29. 多 agent 协作：从"一个"到"一群"

### 第十三章 · Harness

30. Harness：agent 跑一半崩了怎么办

### 第十四章 · Evaluation 与闭环

31. Evaluation / Gate：没有闸门等于没有系统
32. 闭环 / 反馈：同一个坑摔两次

### 第十五章 · AI System

33. AI System：零件拼成系统的样子

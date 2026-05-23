# Karpathy Skill 实战：Andrej Karpathy AI 实战技巧集

> Andrej Karpathy 总结的 AI 实战技巧集，覆盖提示工程、模型微调、从零构建神经网络等动手经验。

---

## 👤 人物背景

**Andrej Karpathy** —— 前 Tesla AI 总监、OpenAI 联合创始人、斯坦福大学博士，深度学习领域最具影响力的教育家之一。他倡导"Zero to Hero"（从零到英雄）的教学哲学，强调通过手写代码而非调用高级 API 来真正理解神经网络。

---

## 🎯 核心实战领域

### 1. 从零构建神经网络

Karpathy 认为理解神经网络最好的方式是抛开 PyTorch/TensorFlow，仅用 NumPy 从头实现：

- **手写多层感知机（MLP）**：手动定义 `forward` 和 `backward`
- **直面底层机制**：权重初始化、矩阵乘法、反向传播链式法则
- **教学案例**：手写数字识别，观察梯度消失/爆炸现象
- **代表项目**：`minGPT`（300 行 PyTorch 实现 GPT 训练）、`nanoGPT`

> **核心观点**："代码即文档"——通过编写极简但完整的代码揭示复杂算法本质。

### 2. 大语言模型微调

#### 预训练 → 监督微调 → RLHF 三阶段
| 阶段 | 类比教科书 | 核心目标 |
|------|-----------|---------|
| **预训练** | 背景知识阅读 | 积累广泛知识，对互联网数据进行有损压缩 |
| **监督微调（SFT）** | 示范性例题 | 学习高质量输出格式与应答礼仪 |
| **RLHF** | 练习题 | 通过试错-反馈循环优化，目前仍是新兴领域 |

#### 轻量级微调：LoRA
- **核心思想**：冻结主干网络，仅在注意力 Q/V 投影矩阵注入低秩分解参数
- **优势**：显存占用大幅降低，单张消费级显卡可微调 7B+ 模型
- **避免灾难性遗忘**：保留预训练知识的同时适配特定领域

### 3. 提示工程策略

Karpathy 在微软 Build 2023 演讲 "State of GPT" 中系统阐述：

- **Few-Shot Learning**：提供少量高质量示例引导模型模仿特定语气
- **Chain of Thought（思维链）**：给模型更多标记/思考时间，展示推理过程
- **结构化模板**：将创作嵌入模板（先生成大纲→确认→分段扩写）
- **人机回环（Human-in-the-loop）**：将生成初稿视为素材而非成品

### 4. 模型可解释性与调试

- **梯度热力图**：定位输入中哪些 token 对预测贡献最大
- **干预实验**：遮蔽部分输入或固定中间层激活，验证逻辑鲁棒性
- **监控生成过程**：监测熵值和概率分布，发现重复循环或逻辑崩塌

---

## 📦 代表项目

| 项目 | GitHub | 说明 |
|------|--------|------|
| **minGPT** | github.com/karpathy/minGPT | 300 行 GPT 训练库 |
| **nanoGPT** | github.com/karpathy/nanoGPT | 可复现 GPT-2 的训练 |
| **llm.c** | github.com/karpathy/llm.c | 纯 C/CUDA 实现 LLM 训练 |
| **micrograd** | github.com/karpathy/micrograd | 极简自动微分引擎 |

---

## 📺 核心学习资源

| 资源 | 链接 | 内容 |
|------|------|------|
| State of GPT 演讲 | [Build 2023](https://build.microsoft.com/en-US/sessions/db3f4859-cd30-4445-a0cd-553c3304f8e2) | 标记化、预训练、微调、RLHF 全流程 |
| Let's build GPT from scratch | YouTube | 手写 Transformer 教育视频 |
| LLM 训练比喻 | [Twitter/X](https://x.com/karpathy/status/1885026028428681698) | 预训练=SFT=RLHF = 教科书三种信息类型 |

---

## 🛠️ 快速开始清单

```markdown
[ ] 观看 "State of GPT" 演讲，理解 LLM 训练全貌
[ ] 克隆 nanoGPT，在单 GPU 上跑通训练
[ ] 用 LoRA 在消费级显卡上微调一个 7B 模型
[ ] 手写一个 micrograd，理解反向传播
[ ] 实践 Few-Shot + Chain of Thought 提示策略
```

---

## 💡 核心金句

> "LLM 是对互联网数据的有损压缩。"  
> "强大的成功标准让 LLM 能够独立循环。弱的标准（'让它工作'）需要持续的澄清。"  
> "教育与训练 LLM 之间的相似性：都需要背景知识、示范例题和大量练习题。"

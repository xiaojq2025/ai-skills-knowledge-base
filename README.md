# AI 实战资源知识库

> 本仓库系统整理了 AI 开发、UI/UX 设计、知识管理与工程提效领域的核心资源，涵盖官方链接、核心概念、使用教程与最佳实践。

---

## 📚 资源总览

### AI 编程与工程

| 资源名称 | 核心定位 |
|---------|---------|
| [Karpathy Skill 实战](./docs/karpathy-skill-guide.md) | Andrej Karpathy 总结的 AI 实战技巧集 |
| [Andrej Karpathy Skill 框架](./docs/andrej-karpathy-skills.md) | 四条行为约束让 AI 编程更靠谱 |
| [Superpowers（超级能力）](./docs/superpowers.md) | 结构化 AI 工作流，理解→规划→验证→执行 |
| [Skill Creator（技能创建器）](./docs/skill-creator.md) | Codex 内置技能工厂，封装重复流程 |
| [全自动 YOLO](./docs/auto-yolo.md) | 端到端自动化 AI 任务链 |

### UI/UX 设计

| 资源名称 | 核心定位 |
|---------|---------|
| [UI-UX-Pro-Max 教程](./docs/ui-ux-pro-max.md) | AI 驱动的专业级 UI/UX 设计智能体 |
| [Awesome DESIGN.md 介绍](./docs/awesome-design-md.md) | 用 Markdown 写设计规格说明 |

### AI 模型与工具

| 资源名称 | 核心定位 |
|---------|---------|
| [Hugging Face 项目介绍](./docs/hugging-face-ecosystem.md) | Transformers、Diffusers 等核心生态 |
| [CLAUDE.md 单文件封神](./docs/claude-md-guide.md) | 通过系统提示文件拉满 Claude 能力 |

### 知识管理

| 资源名称 | 核心定位 |
|---------|---------|
| [Obsidian 知识库套装](./docs/obsidian-knowledge-base.md) | 预配置插件、主题与工作流的开箱即用包 |
| [Obsidian 知识管理软件](./docs/obsidian-software.md) | 本地优先、双向链接的笔记与知识库 |

### 垂直搜索

| 资源名称 | 核心定位 |
|---------|---------|
| [AnySearch（垂直搜索）](./docs/anysearch.md) | 统一 API 聚合金融、法律、学术等垂直数据 |

---

## 💼 AI 办公实战（新增）

> 专为办公人员设计的 AI 提效指南，覆盖写作、沟通、数据分析、会议等核心场景。

### 场景指南

| 文档 | 适用场景 |
|------|---------|
| [AI 办公总览](./docs/ai-office/ai-office-overview.md) | 快速了解 AI 办公能做什么 |
| [提示工程实战](./docs/ai-office/prompt-engineering.md) | 办公场景 Prompt 设计方法论 |
| [AI 辅助邮件撰写](./docs/ai-office/email-writing.md) | 商务邮件、通知、催办、道歉信 |
| [AI 会议纪要](./docs/ai-office/meeting-minutes.md) | 从录音到结构化纪要+待办 |
| [AI 数据分析](./docs/ai-office/data-analysis.md) | Excel/CSV 分析、图表、报告 |
| [文案与报告撰写](./docs/ai-office/writing-workflow.md) | 周报、方案、总结、述职 |

### Prompt 模板库

| 文档 | 内容 |
|------|------|
| [Prompt 模板库](./docs/prompts/templates.md) | 邮件、文档、数据分析、沟通、创意类即开即用模板 |

---

## 🛠️ 项目 Skill 清单

本项目已配置的 Kimi CLI 自定义 Skill：

| Skill | 触发方式 | 功能 |
|-------|---------|------|
| **结构化开发流程** | 自动 / 显式引用 | Brainstorm→Plan→Execute→Review 工程化工作流 |
| **AI实战资源导航** | `/resources` | 13个核心资源快速索引与分类查询 |
| **邮件助手** | `/email` | 商务邮件、通知、催办函生成 |
| **会议助手** | `/meeting` | 纪要整理、待办提取、会议通知 |
| **报告撰写助手** | `/report` | 周报、方案、总结、述职报告 |

---

## 🚀 快速导航

### AI 编程提效
1. **想规范 AI 编码行为？** → [andrej-karpathy-skills](./docs/andrej-karpathy-skills.md)（6万+ Star，一个 CLAUDE.md 文件解决 80% 常见问题）
2. **想建立完整工程流程？** → [superpowers](./docs/superpowers.md)（20万+ Star，Brainstorm→Plan→TDD→Review）
3. **想封装自定义工作流？** → [skill-creator](./docs/skill-creator.md)（Codex/Claude Code 技能工厂）

### 设计与前端
1. **想快速生成专业 UI？** → [ui-ux-pro-max](./docs/ui-ux-pro-max.md)（161 条行业规则 + 67 种风格）
2. **想让 AI 读懂设计规范？** → [awesome-design-md](./docs/awesome-design-md.md)（58 个顶级品牌的 DESIGN.md）

### 知识管理
1. **想搭建个人知识库？** → [obsidian-knowledge-base](./docs/obsidian-knowledge-base.md)（开箱即用套装）
2. **想了解 Obsidian 原理？** → [obsidian-software](./docs/obsidian-software.md)（双向链接与图谱思维）

---

## 📂 仓库结构

```
.
├── README.md                 # 本文件：资源总览与导航
├── docs/                     # 各资源详细文档
│   ├── karpathy-skill-guide.md
│   ├── andrej-karpathy-skills.md
│   ├── superpowers.md
│   ├── skill-creator.md
│   ├── auto-yolo.md
│   ├── hugging-face-ecosystem.md
│   ├── claude-md-guide.md
│   ├── ui-ux-pro-max.md
│   ├── awesome-design-md.md
│   ├── obsidian-knowledge-base.md
│   ├── obsidian-software.md
│   └── anysearch.md
└── assets/                   # 图片、截图等静态资源
```

---

## ⭐ 推荐组合

### 组合一：AI 编码终极套件
```bash
# 1. 行为规范
andrej-karpathy-skills + CLAUDE.md

# 2. 工程流程
superpowers (brainstorm → plan → tdd → review)

# 3. 设计规范
ui-ux-pro-max / awesome-design-md

# 4. 垂直搜索
AnySearch (填补通用搜索盲区)
```

### 组合二：全栈知识管理
```bash
# 1. 知识库底座
Obsidian + 开箱即用套装

# 2. AI 辅助处理
Claude Code + Karpathy Skills

# 3. 设计文档
Awesome DESIGN.md
```

---

## 📅 维护说明

- 所有资源链接截至 2026-05-23 已验证可用
- 每个文档包含：简介、核心要点、官方链接、快速开始、最佳实践
- 欢迎通过 Issue 补充新资源或更新过期信息

---

*本知识库采用 MIT 协议开源，数据整理自公开网络资源，仅供学习参考。*

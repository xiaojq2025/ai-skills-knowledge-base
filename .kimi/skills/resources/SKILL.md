---
name: AI实战资源导航
description: |
  项目知识库的资源导航中心。当用户需要查看所有资源、查找特定资源、
  或输入 /resources 时自动触发。提供13个核心AI/设计/知识管理资源的
  快速索引，包括官方链接、核心要点和推荐学习顺序。
trigger: /resources
---

# AI 实战资源导航

## 🚀 快速使用

输入以下关键词查看特定资源详情：
- `/resources` — 查看全部资源总览
- `/resources 编程` — 筛选编程类资源
- `/resources 设计` — 筛选设计类资源
- `/resources 知识管理` — 筛选知识管理类资源

---

## 📚 全部 13 个核心资源

### 🔧 AI 编程（4个）

#### 1. Karpathy Skill 实战
- **定位**：Andrej Karpathy 总结的 AI 实战技巧集
- **覆盖**：提示工程、模型微调、从零构建神经网络
- **核心项目**：minGPT、nanoGPT、llm.c
- **文档**：`docs/karpathy-skill-guide.md`

#### 2. Andrej Karpathy Skill 框架
- **定位**：四条 AI 行为约束，让编程更靠谱
- **核心**：Think → Simplicity → Surgical → Goal-Driven
- **GitHub**：forrestchang/andrej-karpathy-skills（6万+ Star）
- **文档**：`docs/andrej-karpathy-skills.md`

#### 3. Superpowers（超级能力）
- **定位**：结构化 AI 工作流
- **流程**：Brainstorm → Plan → Execute → TDD → Review
- **GitHub**：obra/superpowers（20万+ Star）
- **状态**：✅ 已创建为项目 Skill

#### 4. Skill Creator（技能创建器）
- **定位**：封装重复流程为自定义 Skill
- **核心**：SKILL.md 格式 + 渐进式披露
- **适用**：Codex / Claude Code / Kimi CLI
- **文档**：`docs/skill-creator.md`

---

### 🎨 UI/UX 设计（2个）

#### 5. UI-UX-Pro-Max 教程
- **定位**：AI 驱动的专业级 UI/UX 设计智能体
- **覆盖**：161条行业规则 + 67种风格 + 15种技术栈
- **集成**：Figma MCP、Pixso、Cursor
- **文档**：`docs/ui-ux-pro-max.md`

#### 6. Awesome DESIGN.md 介绍
- **定位**：AI 能读懂的设计规格说明
- **覆盖**：66+ 顶级品牌设计系统（Linear、Vercel、Stripe）
- **格式**：纯 Markdown，9个核心模块
- **文档**：`docs/awesome-design-md.md`

---

### 🤖 AI 模型与工具（3个）

#### 7. Hugging Face 项目介绍
- **定位**：开源 AI 生态概览
- **核心库**：Transformers、Diffusers、Datasets、Accelerate
- **规模**：30万+模型、5万+数据集
- **文档**：`docs/hugging-face-ecosystem.md`

#### 8. CLAUDE.md 单文件封神
- **定位**：系统提示工程指南
- **核心**：项目级 AI 行为宪法
- **分层**：核心指令 + 工具定义 + 用户上下文 + 系统上下文
- **文档**：`docs/claude-md-guide.md`

#### 9. 全自动 YOLO
- **定位**：端到端自动化 AI 任务链
- **诠释**：YOLO自动训练 / AI内容生产 / ML Agent工作流
- **代表**：auto-ml-agent、AutoAgent
- **文档**：`docs/auto-yolo.md`

---

### 🧠 知识管理（2个）

#### 10. Obsidian 知识库套装
- **定位**：预配置的开箱即用 Obsidian 包
- **覆盖**：插件推荐、主题配置、文件夹结构、同步方案
- **文档**：`docs/obsidian-knowledge-base.md`

#### 11. Obsidian 知识管理软件
- **定位**：本地优先的第二大脑
- **核心**：双向链接 + 知识图谱 + Markdown原生
- **对比**：vs Notion / vs Evernote
- **文档**：`docs/obsidian-software.md`

---

### 🔍 搜索与基础设施（1个）

#### 12. AnySearch（垂直搜索）
- **定位**：AI 时代的搜索基础设施
- **覆盖**：23+垂直领域（金融、法律、学术、代码）
- **输出**：结构化 Markdown，Agent直接消费
- **文档**：`docs/anysearch.md`

---

## 🎯 推荐学习路径

### 入门组合（Week 1-2）
```
Karpathy Skill 框架 → CLAUDE.md → Superpowers → Skill Creator
```

### 进阶组合（Week 3-4）
```
Awesome DESIGN.md → AnySearch → Obsidian知识库
```

### 完整工作流
```
需求输入 → Superpowers(规划) → Karpathy原则(编码) 
  → DESIGN.md(设计) → AnySearch(检索) → Obsidian(沉淀)
```

---

## 📂 项目文件结构

```
skill/
├── README.md                 ← 资源总览
├── AGENTS.md                 ← 项目行为规范
├── docs/                     ← 详细文档
│   ├── karpathy-skill-guide.md
│   ├── andrej-karpathy-skills.md
│   ├── superpowers.md
│   ├── skill-creator.md
│   ├── ui-ux-pro-max.md
│   ├── awesome-design-md.md
│   ├── hugging-face-ecosystem.md
│   ├── claude-md-guide.md
│   ├── auto-yolo.md
│   ├── obsidian-knowledge-base.md
│   ├── obsidian-software.md
│   ├── anysearch.md
│   └── learning-path.md      ← 4周学习路线
└── .kimi/skills/
    ├── superpowers-zh/SKILL.md   ← 结构化开发流程
    └── resources/SKILL.md        ← 本导航文件
```

---

## 🔗 外部资源速查

| 资源 | 地址 |
|------|------|
| andrej-karpathy-skills | github.com/forrestchang/andrej-karpathy-skills |
| superpowers | github.com/obra/superpowers |
| awesome-design-md | github.com/VoltAgent/awesome-design-md |
| ui-ux-pro-max | github.com/nextlevelbuilder/ui-ux-pro-max-skill |
| Hugging Face | huggingface.co |
| Obsidian | obsidian.md |
| AnySearch | github.com/anysearch-ai |

---

> **使用提示**：需要深入了解某个资源时，直接说"打开 docs/xxx.md"或"学习 XXX"。

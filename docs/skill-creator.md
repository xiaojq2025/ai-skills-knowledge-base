# Skill Creator（技能创建器）：Codex 内置技能工厂

> Codex 内置技能工厂，把重复流程封装为一键调用的自定义 Skill，告别重复粘贴提示词。

---

## 📖 什么是 Skill？

**Skill** 是一个文件夹，里面装着：
- **指令文档（SKILL.md）**：告诉 AI 什么时候用、具体怎么做
- **参考资料**：API 文档、工作流指南
- **可执行脚本**：Python/Bash 自动化脚本
- **模板资产**：PPT 模板、字体、样板代码

**本质**：AI 的**能力插件**——插上去就多一项专长；拔掉，AI 还是通用助手。

---

## 🏗️ Skill 的最小形态

一个 Skill 最少只需要 **一个 SKILL.md 文件**：

```markdown
---
name: 代码审查
description: 执行深度代码审查并提供改进建议。当用户请求 review、检查代码质量或发现潜在问题时使用。
trigger: /review
---

# 代码审查技能

## 审查标准
1. 代码可读性
2. 性能问题
3. 安全隐患
4. 最佳实践遵循情况
5. 测试覆盖度

## 输出格式
- 问题列表（按严重程度排序）
- 改进建议
- 代码评分（1-10）
```

### 两段式结构

| 部分 | 名称 | 作用 | 加载时机 |
|------|------|------|---------|
| **上半** | Frontmatter（YAML） | 告诉 AI "什么时候用我" | 每次对话开始时扫描 |
| **下半** | Body（Markdown） | 告诉 AI "具体怎么做" | 技能被触发后才加载 |

**关键规则**：
- `description` 是**唯一触发机制**——必须写清楚何时使用
- `name` + `description` 是唯一必需字段
- Body 内容在触发前**不会加载**，不占用上下文窗口

---

## 📂 Skill 文件结构

```
skill-name/
├── SKILL.md            # 核心定义文件（必需）
├── references/         # 参考资料（API 文档、指南）
│   └── api_reference.md
├── scripts/            # 可执行脚本（Python/Bash）
│   └── helper.py
└── assets/             # 模板资产（字体、图标、样板代码）
    └── template.pptx
```

### 资源类型说明

| 目录 | 用途 | 示例 |
|------|------|------|
| `scripts/` | 执行特定操作的可执行代码 | PDF 处理、数据转换 |
| `references/` | 加载到上下文中提供信息 | API 文档、架构说明 |
| `assets/` | 用于 AI 生成的输出中 | 模板、字体、图标 |

---

## 🚀 创建自定义 Skill（三步法）

### 步骤 1：创建目录
```bash
# 全局技能（所有项目可用）
mkdir -p ~/.codex/skills/生成测试

# 或项目级技能（仅限当前项目）
mkdir -p .codex/skills/生成测试
```

### 步骤 2：编写 SKILL.md
```markdown
---
name: 生成测试
description: 为代码生成单元测试。当用户请求测试、test、unit test 时使用。
trigger: 测试
---

# 生成测试技能

## 步骤
1. 分析现有代码的功能
2. 识别需要测试的边界情况
3. 选择合适的测试框架
4. 生成测试用例

## 测试标准
- 覆盖率包括正常情况、边界情况和错误情况
- 每个测试用例独立，不依赖执行顺序
- 使用清晰的测试函数命名
```

### 步骤 3：使用 Skill
```bash
# 触发方式 1：匹配 trigger 关键词
"帮我为这个函数生成测试"

# 触发方式 2：显式调用
"/review 检查这段代码"
```

---

## 📦 安装位置（按作用域）

| 作用域 | 路径 | 适用场景 |
|--------|------|---------|
| **企业级** | 托管设置 | 组织所有用户 |
| **个人级** | `~/.claude/skills/<name>/SKILL.md` | 你的所有项目 |
| **项目级** | `.claude/skills/<name>/SKILL.md` | 仅限此项目（通过 git 共享） |
| **插件级** | `<plugin>/skills/<name>/SKILL.md` | 启用插件的地方 |

**最佳实践**：项目技能通过 git 共享，队友拉取代码自动获得，无需额外安装。

---

## 🧠 Skill 设计哲学

### 何时创建 Skill？
> "当你发现自己在重复解释上下文时，就构建 Skill。如果你三次粘贴了相同的检查清单，它就应该成为一个 Skill。"

### 好的 Skill 标准
1. **教 AI 怎么干活**，而不是某个框架/语言的教程
2. 有**明确的步骤、检查清单、示例**
3. AI 加载后能**直接执行**，不需要额外推理
4. **保持专注**：一个 Skill 解决一个稳定、可复用的问题

### 渐进式披露
- Frontmatter 先入场：让 AI 判断"是否相关"
- Body 后入场：触发后才加载详细指令
- 避免把 200 行指导规则一股脑塞进每次对话

---

## 🆚 不同平台的 Skill 格式

| 平台 | 文件路径 | 格式特点 |
|------|---------|---------|
| **Codex CLI** | `.codex/skills/*/skill.md` | YAML frontmatter + Markdown |
| **Claude Code** | `.claude/skills/*/SKILL.md` | 同上，支持 allowed-tools 约束 |
| **OpenClaw** | `skills/*/SKILL.md` | 工作区级自动发现 |
| **Windsurf** | `.windsurf/skills/*/SKILL.md` | 项目级 skills 目录 |
| **Gemini CLI** | `.gemini/skills/*/SKILL.md` | 兼容 Claude Code 格式 |

---

## 🔗 相关资源

| 资源 | 说明 |
|------|------|
| [Superpowers](./superpowers.md) | 包含 "writing-skills" meta-skill，教你创建新 skill |
| [andrej-karpathy-skills](./andrej-karpathy-skills.md) | 最经典的 Skill 实践案例 |
| [Open Skills 规范](https://agentskills.io) | 跨平台 Skill 标准 |
| Anthropic 官方文档 | support.claude.com（如何创建自定义技能） |

---

## 💡 核心金句

> "Skill 的本质是 AI 的能力插件——插上去，AI 就多了一项专长。"
> 
> "描述字段决定一切。Claude 使用 LLM 推理将你的请求与描述进行匹配。在描述上投入的时间应该多于技能内容本身。"

# CLAUDE.md 单文件封神：系统提示工程指南

> 通过精心编写 CLAUDE.md 系统提示文件，把 Claude Code 的能力在单次对话中拉到极致。这是 Anthropic 官方推荐的项目级配置机制。

---

## 📖 什么是 CLAUDE.md？

`CLAUDE.md` 是放在**项目根目录**的 Markdown 文件，Claude Code 在每次对话开始时自动读取并注入系统提示上下文。它相当于项目的"AI 宪法"，告诉 Claude：

- 项目的技术栈与架构
- 编码规范与风格指南
- 常用的命令和工作流
- 行为约束（如 Karpathy 四原则）

---

## 🏗️ 系统提示的分层架构

Claude Code 的系统提示采用**动态构建 + 分层设计**：

```
优先级（从高到低）：
1. --append-system-prompt（用户追加，最高优先级）
2. --system-prompt（用户自定义，完全替换）
3. CLAUDE.md（项目级配置）
4. 默认系统提示（Claude Code 内置）
```

### 构建流程（简化）
```typescript
async function fetchSystemPromptParts(config) {
  const parts = []
  parts.push(getCoreInstructions())          // 1. 核心指令
  parts.push(getToolDefinitions(config.tools)) // 2. 工具定义
  
  const userContext = await getUserContext()
  if (userContext.claudeMd) {
    parts.push(formatClaudeMd(userContext.claudeMd))  // 3. 用户上下文
  }
  
  const systemContext = await getSystemContext()
  if (systemContext.gitStatus) {
    parts.push(formatGitStatus(systemContext.gitStatus)) // 4. 系统上下文
  }
  
  return parts.join('\n\n')
}
```

---

## ✍️ CLAUDE.md 编写最佳实践

### 1. 保持简洁（建议 2000 字以内）
- 系统提示越长，token 消耗越大
- 核心信息前置，细节可引用外部文件

### 2. 结构化组织
```markdown
# 项目概述
- 技术栈：React + TypeScript + Tailwind
- 架构：Monorepo (Turborepo)

# 编码规范
- 使用函数组件 + Hooks
- 类型定义优先于 any
- 错误处理使用 Result 模式

# 常用命令
- 启动开发：pnpm dev
- 运行测试：pnpm test
- 构建：pnpm build

# 行为约束（可选）
- Think Before Coding
- Simplicity First
- Surgical Changes
- Goal-Driven Execution
```

### 3. 缓存优化
- Claude API 支持**提示缓存（Prompt Caching）**
- 稳定内容（核心指令、工具定义）前置，可跨请求缓存
- 动态内容（git 状态、CLAUDE.md）后置

---

## 🚀 高阶用法

### 与 Karpathy Skills 结合
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/forrestchang/andrej-karpathy-skills/main/CLAUDE.md
```
直接在项目里落地四条行为约束。

### 多文件拆分
当项目复杂时，可在 `.claude/` 目录下拆分：
```
.claude/
├── CLAUDE.md          # 主配置
├── frontend.md        # 前端规范
├── backend.md         # 后端规范
└── testing.md         # 测试策略
```

### 与 DESIGN.md 协同
```
项目根目录/
├── CLAUDE.md          # 告诉 AI "怎么构建"
├── DESIGN.md          # 告诉 AI "长什么样"
└── AGENTS.md          # 告诉 AI "项目背景"
```

---

## 📊 效果对比

| 场景 | 无 CLAUDE.md | 有 CLAUDE.md |
|------|-------------|--------------|
| **代码风格** | 每轮可能不一致 | 严格遵循项目规范 |
| **技术栈** | 可能选错框架/库 | 明确限定技术选型 |
| **命令执行** | 需要反复确认 | 直接执行预定义命令 |
| **上下文理解** | 从零开始推断 | 预设架构与约束 |

---

## 🔗 相关资源

| 资源 | 说明 |
|------|------|
| [andrej-karpathy-skills](./andrej-karpathy-skills.md) | 最经典的 CLAUDE.md 实践 |
| [Claude Code 官方文档](https://docs.anthropic.com) | 系统提示与技能官方指南 |
| [awesome-design-md](./awesome-design-md.md) | 与 DESIGN.md 配合实现设计-代码一致 |

---

## 🛠️ 快速开始

```bash
# 1. 在项目根目录创建 CLAUDE.md
touch CLAUDE.md

# 2. 写入项目核心信息（技术栈、规范、常用命令）

# 3. 测试：向 Claude 提出一个简单任务，观察是否遵循规范

# 4. 迭代优化，根据实际使用效果调整内容
```

---

## 💡 核心洞察

> "系统提示是 AI 的'宪法'——它定义了 AI 的角色、能力和边界。"
> 
> "一个好的系统提示能让 Claude 更准确地理解任务、更合理地使用工具、更安全地执行操作。"

# Superpowers（超级能力）：结构化 AI 工作流

> GitHub 20 万星的结构化 AI 工作流，强制模型"理解→规划→验证→执行"，省 token 又提效。由 Jesse Vincent（obra）打造的开源可组合技能框架。

---

## 🔥 项目概况

| 指标 | 数据 |
|------|------|
| **GitHub Star** | 198,000+（截至 2026-05） |
| **核心 Skills** | 20+ 个结构化技能 |
| **作者** | Jesse Vincent（obra） |
| **仓库** | [github.com/obra/superpowers](https://github.com/obra/superpowers) |
| **中文增强版** | [github.com/jnMetaCode/superpowers-zh](https://github.com/jnMetaCode/superpowers-zh) |

---

## 🎯 核心理念

**Process over Prompt（流程大于提示词）**

不是让你手动写一堆长 Prompt，而是把资深工程师的思考和执行习惯，直接"编译"进 AI 的大脑。

**解决的问题**：
- "Vibe Coding"（凭感觉 coding）越到后面越乱
- Bug 一堆、需求漂移、代码难以维护
- AI 缺少工程纪律，像"自信的初级开发者"

---

## 🏗️ 核心技能与完整工作流

### 推荐完整流程
```
Brainstorm（头脑风暴）
    ↓
Write Plan（编写实施计划）
    ↓
Execute Plan（执行计划）
    ↓ 自动触发 TDD + Review
TDD（测试驱动开发）
    ↓
Code Review（代码审查）
    ↓
人工最终确认
```

### 14 个核心 Skills 详解

| Skill | 用途 | 触发方式 |
|-------|------|---------|
| **brainstorming** | 需求分析 → 设计规格，不写代码先想清楚 | `/brainstorm` |
| **writing-plans** | 把规格拆成可执行的实施步骤 | 自动 |
| **executing-plans** | 按计划逐步实施，每步验证 | 自动 |
| **test-driven-development** | 严格 TDD：先写测试，再写代码 | 自动 |
| **systematic-debugging** | 四阶段调试：定位→分析→假设→修复 | 手动/自动 |
| **requesting-code-review** | 派遣审查 agent 检查代码质量 | 自动 |
| **receiving-code-review** | 技术严谨地处理审查反馈 | 自动 |
| **verification-before-completion** | 证据先行——声称完成前必须跑验证 | 自动 |
| **dispatching-parallel-agents** | 多任务并发执行 | 手动 |
| **subagent-driven-development** | 每个任务一个 agent，两轮审查 | 手动 |
| **using-git-worktrees** | 隔离式特性开发 | 手动 |
| **finishing-a-development-branch** | 合并/PR/保留/丢弃四选一 | 手动 |
| **writing-skills** | 创建新 skill 的方法论 | 手动 |
| **using-superpowers** | 元技能：如何调用和优先使用 skills | 自动 |

---

## ⚙️ 关键机制

### 1. 子代理（Sub-agent）机制
- 不同子任务使用**独立上下文窗口**，避免 token 污染
- 自动管理 **git worktree** 隔离环境，安全实验
- 并行处理多个特性，互不干扰

### 2. TDD 强制循环
```
红：编写测试 → 测试失败
绿：实现功能 → 测试通过
重构：优化代码 → 测试仍通过
```

### 3. Prompt Cache 继承
Fork 子 Agent 继承父级的 prompt cache，对于大型代码库边际成本极低，使得"并行研究"策略在经济上可行。

---

## 🚀 安装方式

### Claude Code
```bash
# 添加市场
/plugin marketplace add obra/superpowers

# 安装
/plugin install superpowers
```

### 中文增强版（superpowers-zh）
```bash
# 一条命令自动识别工具并安装
npx superpowers-zh

# 或显式指定工具
npx superpowers-zh --tool cursor
```

支持 18 款工具：Claude Code / Cursor / Windsurf / Codex / Gemini CLI / Trae / VS Code / Aider 等。

---

## 🆚 与其他工作流对比

| 维度 | 原生 Claude Code | + Superpowers |
|------|-----------------|---------------|
| **需求澄清** | 容易理解偏差 | Brainstorm 强制交互式澄清 |
| **代码规划** | 边写边想 | 必须先写 Plan 再执行 |
| **测试覆盖** | 经常遗漏 | TDD 强制先写测试 |
| **代码审查** | 无 | 自动派遣 Review Agent |
| **并行开发** | 单线程 | Sub-agent 多任务并发 |
| **返工率** | 较高 | 减少 70%+ |

---

## 💡 实际案例

**开发 Web 功能时的变化**：
- **前期**：需求澄清更彻底，不再中途改方向
- **中期**：代码结构清晰，测试覆盖率高
- **后期**：Bug 少，可读性好，迭代成本大幅降低

> "一个典型小项目，从 0 到 1 的时间可能没缩短太多，但返工时间减少 70%+，最终交付质量接近人工中高级水平。"

---

## ⚠️ 注意事项

1. **小脚本/一次性任务**：可能觉得 overkill，流程较重
2. **学习曲线**：第一次用建议严格跟着流程走
3. **Token 消耗**：复杂任务会多一些，但质量回报远超消耗
4. **持续更新**：插件非常活跃，建议定期 `/plugin update`

---

## 🔗 相关资源

| 资源 | 说明 |
|------|------|
| 英文原版 | github.com/obra/superpowers |
| 中文增强版 | github.com/jnMetaCode/superpowers-zh |
| 关联项目 | agency-agents-zh（211 个 AI 专家角色库） |
| | ai-coding-guide（66 个 Claude Code 技巧） |

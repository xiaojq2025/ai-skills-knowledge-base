# Andrej Karpathy Skills：给 AI 编程加四条行为约束

> GitHub 上 Karpathy 相关的技能仓库，一个 70 行的 CLAUDE.md 文件，一周内暴涨数万 Star，直接把 LLM 编码常见通病转成可执行的行为准则。

---

## 🔥 项目概况

| 指标 | 数据 |
|------|------|
| **GitHub Star** | 60,000+（截至 2026-05） |
| **核心文件** | `CLAUDE.md`（约 70 行） |
| **作者** | Forrest Chang（基于 Karpathy 观察） |
| **仓库** | [github.com/forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills) |

---

## 🎯 起源故事

2026 年 1 月，Andrej Karpathy 发了一条推特，吐槽 AI 写代码时的通病：

> "模型会替你做错误假设，然后沿着假设一路往下跑。它们不管理困惑，不寻求澄清，不呈现不一致，不展示权衡取舍，该反对的时候不反对。"
> 
> "它们真的喜欢把简单问题搞复杂，膨胀抽象层，不清理死代码……100 行能搞定的事非要写 1000 行。"
> 
> "它们还会顺手改掉并不理解的旁边代码，即使与任务无关。"

开发者 Forrest Chang 把这些观察变成了**四条行为约束**，写进一个 `CLAUDE.md` 文件。

---

## 📜 四大核心原则

### 1. Think Before Coding（先思考后编码）

**解决**：错误假设、隐藏困惑、缺失权衡

**要求**：
- 明确陈述所有假设
- 有歧义时，不要默默选一个
- 呈现多种解释和权衡取舍
- 有困惑时停下来问，而不是猜

**反面教材**：
```
用户：帮我添加用户验证
❌ AI 默默假设需要 OAuth，实现完整流程，还加了密码强度检测
✅ AI：需要确认验证方式（邮箱/手机/第三方）、安全级别、额外功能
```

### 2. Simplicity First（简洁优先）

**解决**：过度设计、膨胀抽象

**要求**：
- 不要加没被要求的功能
- 不要为一次性代码抽象一层
- 不要为"灵活性"提前做配置
- 200 行能写成 50 行，就继续收

**检验标准**：删除 50% 代码，功能还能正常工作吗？如果能，删掉那 50%。

### 3. Surgical Changes（精准修改）

**解决**：顺手改无关代码、引入副作用

**要求**：
- 只修改必须修改的部分
- 匹配现有代码风格
- 不要"改进"相邻代码或注释
- 每一行修改都能追溯到用户要求

**Diff 检验**：每一行修改都能说出"这是为了 XXX 要求"。

### 4. Goal-Driven Execution（目标驱动执行）

**解决**：模糊指令、缺乏验证标准

**要求**：
- 将任务转换为可验证的目标
- 先写测试定义成功标准
- 独立循环直到所有测试通过
- 用多步骤格式：目标 → 验证 → 下一步

**精髓**：
> "不要告诉 AI 该做什么，给它成功标准然后看它发挥。"

---

## 🚀 三种使用方式

### 方式一：Claude Code 插件（推荐）
```bash
/plugin marketplace add forrestchang/andrej-karpathy-skills
/plugin install andrej-karpathy-skills@karpathy-skills
```

### 方式二：手动复制 CLAUDE.md（通用）
```bash
curl -o CLAUDE.md https://raw.githubusercontent.com/forrestchang/andrej-karpathy-skills/main/CLAUDE.md
```

### 方式三：添加到全局配置
```bash
git clone https://github.com/forrestchang/andrej-karpathy-skills.git /tmp/karpathy-skills
cat /tmp/karpathy-skills/CLAUDE.md >> ~/.claude/CLAUDE.md
```

### Cursor 用户
仓库已内置 Cursor 适配：
```bash
cp /tmp/karpathy-skills/.cursor/rules/karpathy-guidelines.mdc .cursor/rules/
```

---

## ✅ 效果验证清单

```markdown
[ ] Diff 中不必要的变更更少——只出现请求的变更
[ ] 因过度复杂而重写的次数更少——代码第一次就保持简洁
[ ] 澄清问题出现在实现之前——而不是出错之后
[ ] 干净、最小的 PR——没有顺手的重构或"改进"
```

---

## 🧠 设计哲学

这不是要束缚 AI，而是让 AI 的行为更**透明、可控、可预测**。核心洞察：

| 对比维度 | 传统最佳实践 | Karpathy 指南 |
|---------|------------|--------------|
| **目标** | 人类程序员 | LLM 编程助手 |
| **重点** | 代码质量 | 行为透明度 |
| **形式** | 文档/规范 | 可执行指令 |
| **验证** | Code Review | AI 自律 |

> **"好的代码是简单地解决今天问题的代码，而不是提前解决明天问题的代码。"**

# UI-UX-Pro-Max 教程：AI 驱动的专业级 UI/UX 设计

> 一套聚焦 UI/UX 设计提效的嵌入式 AI 设计智能体，将专业设计知识库注入 AI 编程助手，自动生成符合行业规范的高质量界面代码。

---

## 🎯 核心定位

**ui-ux-pro-max** 不是一个普通的设计插件，而是一个 **AI Skill（技能包）**。它将专业 UI/UX 知识库直接注入你日常使用的 AI 编程助手（如 Cursor、Copilot、Claude Code），实现：

- 自动场景识别与模板匹配
- 设计系统生成（配色、字体、间距、组件）
- 代码生成与优化（React + Tailwind 等）
- 设计还原度保障

---

## 🏗️ 核心能力

### 1. 场景识别引擎
通过 `search.py` 自动匹配最佳设计模板：

- **Internal Monitoring Dashboard** → `slate-900` 背景 + `amber-400` 强调色
- **Fintech 风格** → 紧凑表格 + 状态标签 + 数据可视化
- **SaaS 后台** → Bento Grid + 卡片分区

### 2. 多技术栈支持
| 技术栈 | 适配版本 | 配套资源 |
|--------|---------|---------|
| React + Tailwind | 通用 | 组件代码、主题配置、页面模板 |
| Vue 3 | 通用 | SFC 组件、组合式 API 示例 |
| Jetpack Compose | 1.4+ (API 21+) | Kotlin 组件、Material 3 主题 |
| SwiftUI | iOS 15+ | View 组件、状态管理示例 |

### 3. AI 工具集成
- **Figma**：通过 MCP 插件实时同步设计稿，AI 直接生成对应代码
- **Pixso**：配合 Trae AI IDE，完成从 UI 设计到前端代码的完整工作流
- **Cursor**：输入 `/ui-ux-pro-max` 触发设计智能体

---

## 📋 实战流程示例

**需求**：用 React + Tailwind 重做异常列表和数据分析页，深色主题，Fintech 风格

**步骤**：
1. 在 Cursor 中输入：`/ui-ux-pro-max 重设计「接口哨兵」的异常列表和数据分析页，深色主题，Fintech 风格`
2. AI 自动执行：
   - 场景识别 → 匹配 "Internal Monitoring Dashboard"
   - 生成配色方案、字体层级、布局网格
   - 设计异常列表页（行高 48px、状态标签、筛选区、空态）
   - 设计数据分析页（折线图、4 个核心指标卡片、高频 Case 表格）
   - 代码生成与优化（clsx 管理动态类名、提取公共组件）

---

## ⚙️ 高级配置

### 自定义设计系统
在项目根目录创建 `.uipro/custom.yaml`：

```yaml
brandColor: "#6366f1"  # 自定义主色
fontPrimary: "Manrope"
spacingUnit: 8         # 8px 基准网格
```

### 批量重设计
```bash
uipro batch --pages "src/pages/dashboard,src/pages/users"
```

---

## 🔗 官方资源

| 资源 | 链接 |
|------|------|
| GitHub 仓库 | github.com/nextlevelbuilder/ui-ux-pro-max-skill |
| 官方文档 | ui-ux-pro-max-skill.nextlevelbuilder.io |
| 开源协议 | MIT |
| 社区 | Discord（500+ 开发者） |

---

## 🆚 与 Awesome DESIGN.md 的对比

| 维度 | UI-UX-Pro-Max | Awesome DESIGN.md |
|------|--------------|-------------------|
| **定位** | 智能推理生成设计系统 | 静态提取真实网站设计规范 |
| **使用方式** | 自然语言触发 / CLI 命令 | 复制 DESIGN.md 文件到项目 |
| **定制化** | 智能推理生成定制方案 | 选择现有网站风格 |
| **反模式检测** | ✅ 有（如"银行不要用紫色渐变"） | ❌ 无 |
| **技术栈** | 15 种（React, Vue, SwiftUI 等） | 通用（不限定） |

---

## 🛠️ 快速安装（Claude Code）

```bash
# 添加到插件市场
claude plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill

# 安装插件
claude plugin install ui-ux-pro-max@ui-ux-pro-max-skill

# 验证
claude plugin list
# 应显示：ui-ux-pro-max (enabled)
```

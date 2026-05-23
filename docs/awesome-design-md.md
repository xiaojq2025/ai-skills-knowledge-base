# Awesome DESIGN.md 介绍：AI 能读懂的设计规格

> Awesome 系列的设计文档资源，教你用 Markdown 写出清晰、高效的设计规格说明，让 AI Coding Agent 直接生成风格一致的 UI。

---

## 📖 什么是 DESIGN.md？

**DESIGN.md** 由 Google Stitch 提出，是一个**纯文本的设计系统文档**。与 Figma 导出或 JSON 配置不同，它采用 Markdown 格式——LLM 最擅长读取的格式。

**核心分工**：
- `AGENTS.md` → 告诉 AI **"怎么构建"** 项目
- `DESIGN.md` → 告诉 AI 项目 **"应该长什么样"**

---

## 🏗️ DESIGN.md 的 9 个核心部分

每个文件遵循 Stitch 格式标准：

1. **视觉主题和氛围** —— 情绪、密度、设计哲学
2. **色彩调色板和角色** —— 语义名称 + 十六进制值 + 功能角色
3. **排版规则** —— 字体族、完整层级表
4. **组件样式** —— 按钮、卡片、输入框、导航及其状态
5. **布局原则** —— 间距尺度、网格、留白哲学
6. **深度和层次** —— 阴影系统、表面层级
7. **该做和不该做** —— 设计护栏和反模式
8. **响应式行为** —— 断点、触摸目标、折叠策略
9. **AI 助手提示指南** —— 快速色彩参考、即用提示词

---

## 🌟 Awesome DESIGN.md 项目

| 指标 | 数据 |
|------|------|
| **GitHub Star** | 46,000+ |
| **支持品牌** | 66+ 个顶级网站 |
| **仓库** | [github.com/VoltAgent/awesome-design-md](https://github.com/VoltAgent/awesome-design-md) |
| **许可证** | MIT |

### 包含品牌示例
- **开发者工具**：Vercel、Linear、Stripe、Supabase、Notion、Claude、Cursor、Warp
- **科技巨头**：Apple、Google、Microsoft
- **设计系统**：Material Design、Ant Design

每个品牌包含：
```
brand-name/
├── DESIGN.md          # 设计规范
├── preview.html       # 亮色主题预览
└── preview-dark.html  # 深色主题预览
```

---

## 🚀 使用方法

### 步骤一：复制 DESIGN.md
```bash
# 克隆仓库
git clone https://github.com/VoltAgent/awesome-design-md.git

# 复制你想要的品牌风格到项目根目录
cp awesome-design-md/design-md/linear.app/DESIGN.md ./DESIGN.md
```

### 步骤二：让 AI 按风格生成
```
用户：基于项目根目录的 DESIGN.md，为我生成一个设置页面
AI：读取 DESIGN.md → 理解 Linear 风格 → 生成像素级匹配的设置页
```

### 效果
> "把 DESIGN.md 放在 Cursor 项目根目录，Claude 立刻开始尊重我的品牌 token。终于，AI 不再自己发明 Tailwind 样式了。"

---

## 🛠️ 自动生成工具：HyperDesign

不想手动写？用 **HyperDesign** 自动提取：

1. 输入任意网站 URL
2. 16 秒输出颜色、字体、间距规范
3. 9 秒生成结构化 DESIGN.md

**特点**：
- 不是简单取色器，而是分析设计语言
- 能判断风格气质（"克制的、学术的、借鉴印刷传统的"）
- 每个字号对应的行高字重都列得清清楚楚

---

## 🆚 与其他方案对比

| 对比项 | Awesome DESIGN.md | Figma Tokens | design-tokens |
|--------|------------------|--------------|---------------|
| **格式** | Markdown 纯文本 | 二进制/同步 | JSON/YAML |
| **AI 友好度** | ⭐⭐⭐ 直接读取 | ⭐ 需 API/插件 | ⭐⭐ 需解析器 |
| **使用门槛** | 极低（复制文件） | 高（需 Figma） | 中（需构建流程）|
| **品牌覆盖** | 66+ 顶级品牌 | 需自己定义 | 需自己定义 |
| **维护成本** | 低（更新 MD 即可）| 中 | 高 |

---

## 💡 最佳实践

1. **与 CLAUDE.md 配合使用**：AGENTS.md（构建方式）+ DESIGN.md（视觉风格）
2. **选择最接近目标的品牌**：不要混搭多个品牌的风格
3. **在 custom.yaml 中覆盖**：基于提取的规范，微调为自己的品牌色
4. **定期更新**：网站改版后需手动更新 DESIGN.md

---

## 🔗 资源链接

| 资源 | 地址 |
|------|------|
| Awesome DESIGN.md | github.com/VoltAgent/awesome-design-md |
| HyperDesign 工具 | github.com/hyperbrowserai/hyperbrowser-app-examples |
| Google Stitch | 参考 Stitch 设计规范格式 |

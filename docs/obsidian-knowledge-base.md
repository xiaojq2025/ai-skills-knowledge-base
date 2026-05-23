# Obsidian 知识库套装：开箱即用包

> 预配置了插件、主题和工作流的 Obsidian 开箱即用包，帮助你快速搭建个人知识库（第二大脑）。

---

## 📦 什么是 Obsidian 知识库套装？

Obsidian 虽然功能强大，但**从零配置学习曲线较陡**。社区开发者整理了各种**开箱即用库（Starter Kits / Templates）**，预装了：

- 精选第三方插件
- 优化过的主题与 CSS
- 结构化文件夹体系
- 预定义的工作流模板

---

## 🌟 主流开箱即用库推荐

### 1. PARA 模板库
- **定位**：基于 Tiago Forte PARA 方法论的轻量知识管理
- **特点**：简洁设计，开箱即用
- **使用方法**：
  1. 下载模板库并解压
  2. 用 Obsidian 打开目录
  3. 信任并启用第三方插件
  4. 激活 Components 插件，关掉主页，重新打开即可

### 2. Math-And-English-Library
- **定位**：考研数学 + 英语笔记完整模板
- **特点**：20W+ 字数，含高等数学、线性代数、英语语法/阅读/作文
- **插件**：Excalidraw（思维导图）、Easy Typing（打字优化）
- **主题**：AnuPpuccin（黑色基础色）
- **地址**：WandD2277/Math-And-English-Library

### 3. 飞书 × Obsidian 自动化工作流
- **定位**：打通本地知识图谱与团队协同
- **特点**：基于 OpenClaw 原生 second-brain 插件
- **流程**：采集 → 整理 → 存储 → 复用 全闭环

---

## 🔧 必装插件清单（知识库向）

### 白板与可视化
| 插件 | 功能 |
|------|------|
| **advanced-canvas** | 最好的白板增强 |
| **obsidian-mindmap-nextgen** | Markmap 思维导图预览 |
| **obsidian-enhancing-mindmap** | 绘制思维导图、大纲、白板 |

### 视图与项目管理
| 插件 | 功能 |
|------|------|
| **obsidian-projects** | 多视图项目管理（表格/看板/日历/画廊） |
| **workspaces-plus** | 快速管理不同工作区布局 |
| **dataview** | 将笔记作为数据库查询 |

### 学习与记忆
| 插件 | 功能 |
|------|------|
| **obsidian-spaced-repetition** | 利用遗忘曲线间隔重复复习 |
| **obsidian-language-learner** | 辅助英语学习（查词、生词） |

### 同步与备份
| 插件 | 功能 |
|------|------|
| **Remotely Save** | 跨设备同步（支持 WebDAV/OneDrive/S3） |

---

## 🎨 推荐主题

| 主题 | 特点 | 配置要点 |
|------|------|---------|
| **AnuPpuccin** | 高度可定制，支持 Style Settings | 安装 Style Settings 插件后细调 |
| **Minimal** | 极简专注，阅读体验佳 | 配合 Minimal Theme Settings |
| **Things** | 精致优雅，macOS 风格 | 直接启用即可 |

---

## 📂 推荐文件夹结构

```
My-Vault/
├── 00-Inbox/           # 收件箱，临时存放
├── 01-Projects/        # 当前进行中的项目
├── 02-Areas/           # 持续维护的领域
├── 03-Resources/       # 参考素材与笔记
├── 04-Archive/         # 归档内容
├── Templates/          # 笔记模板
├── Attachments/        # 图片、附件
└── Daily/              # 日记/日志
```

---

## 🚀 快速搭建步骤

```markdown
[ ] 1. 下载 Obsidian 客户端（obsidian.md）
[ ] 2. 创建新 Vault（本地文件夹）
[ ] 3. 关闭安全模式：设置 → 第三方插件 → 关闭安全模式
[ ] 4. 浏览社区插件市场，安装必装插件
[ ] 5. 选择主题：设置 → 外观 → 管理 → 安装社区主题
[ ] 6. 建立 PARA 或自定义文件夹结构
[ ] 7. 创建常用 Templates（日记、会议记录、读书笔记）
[ ] 8. 配置 Remotely Save 实现跨设备同步（可选）
[ ] 9. 开始使用 [[双向链接]] 建立知识网络
```

---

## 💡 最佳实践

1. **收件箱习惯**：所有新内容先丢进 Inbox，定期整理
2. **原子化笔记**：一条笔记一个核心概念，便于链接
3. **标签与链接并用**：标签做粗分类，`[[链接]]` 做精确关联
4. **定期回顾图谱**：通过 Graph View 发现隐藏的知识联系
5. **AI 辅助处理**：结合 AI 工具提取文章核心要点，再写入 Obsidian

---
theme: seriph
background: https://cover.sli.dev
title: AI时代的文档格式
info: |
  ## Markdown的扩展语法和生态介绍
  探索AI时代下Markdown的发展和生态系统

class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# AI 时代的文档格式<br>Markdown 扩展语法和生态介绍

探索 AI 时代下 Markdown 的发展和生态系统

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  点击或按空格键继续 <carbon:arrow-right />
</div>

<!--
这是幻灯片的首页，介绍主题为"AI时代的文档格式——Markdown的扩展语法和生态介绍"
-->

---

# 目录

Contents

<Toc columns="2" maxDepth="1"/>

---
layout: section
___

# Markdown 简介与历史

Introduction to Markdown

---

# Markdown 简介与历史

Introduction to Markdown

## 什么是 Markdown？

::v-clicks

- **轻量级标记语言** - 易读易写的纯文本格式
- **易于转换** - 可转换为有效的 XHTML 或 HTML 文档
- **专注内容** - 让作者专注于写作而非格式

::

---

# Markdown 简介与历史

Introduction to Markdown

## 历史发展

- 2004 年由 John Gruber 创建
- 设计目标是尽可能易读、易写
- 受到 Markdown 启发的众多变种和扩展

<Note>
Markdown 的设计目标是让普通人也能轻松进行格式化写作
</Note>

---

# AI 时代对文档格式的新需求

New Requirements in the AI Era

## AI 驱动的文档处理

- **语义理解** - AI 需要更好地理解文档结构和内容
- **自动化生成** - AI 能够自动生成结构化文档
- **智能交互** - 文档不仅是静态内容，还能与用户互动

---

# AI 时代对文档格式的新需求

New Requirements in the AI Era

## 协作与分享需求

- **实时协作** - 多人同时编辑和评论
- **跨平台兼容** - 在不同设备和系统间无缝切换
- **版本控制** - 清晰的变更历史和回溯能力

---

# AI 时代对文档格式的新需求

New Requirements in the AI Era

## 可扩展性要求

- **自定义语法** - 满足特定领域需求
- **插件生态** - 丰富的扩展功能
- **工具链整合** - 与开发工具和流程深度集成

---

## layout: section

# Markdown 扩展语法

Markdown Extended Syntax

---

## 常见扩展语法

### 表格 (Tables)

用于展示结构化数据，比传统文档中的表格更易维护和版本控制

```markdown
| 姓名 | 年龄 | 职业   |
| ---- | ---- | ------ |
| 张三 | 25   | 工程师 |
| 李四 | 30   | 设计师 |
```

| 姓名 | 年龄 | 职业   |
| ---- | ---- | ------ |
| 张三 | 25   | 工程师 |
| 李四 | 30   | 设计师 |

### 任务列表 (Task Lists)

用于创建待办事项清单，支持勾选状态，非常适合项目管理和进度跟踪

```markdown
- [x] 完成项目规划
- [ ] 编写技术文档
- [ ] 进行代码审查
```

- [x] 完成项目规划
- [ ] 编写技术文档
- [ ] 进行代码审查

### 代码块增强 (Fenced Code Blocks)

支持语法高亮和行号显示，对技术文档尤为重要

````markdown
```javascript {all|2|1-6|9|all}
function highlightMe() {
  console.log("这段代码会被高亮显示");
  return "支持行号和特定行高亮";
}
```
````

```javascript {all|2|1-6|9|all}
function highlightMe() {
  console.log("这段代码会被高亮显示");
  return "支持行号和特定行高亮";
}
```

### 数学公式 (Mathematical Formulas)

使用 LaTeX 语法，支持行内公式和块级公式，适合学术和科研文档

```markdown
行内公式: $E = mc^2$

块级公式:

$$
\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \frac{i}{\hbar}\hat{H}\Psi(\mathbf{r},t)
$$
```

### 图表支持 (Diagrams)

使用 Mermaid 等工具，可直接在 Markdown 中创建流程图、时序图等

流程图示例：

````markdown
```mermaid
graph LR
  A[Hard edge] --> B(Round edge)
  B --> C{Decision}
  C --> D[Result one]
  C --> E[Result two]
```
````

```mermaid
graph LR
  A[Hard edge] --> B(Round edge)
  B --> C{Decision}
  C --> D[Result one]
  C --> E[Result two]
```

时序图示例：

```mermaid
sequenceDiagram
  participant A as 用户
  participant B as 系统
  A->>B: 登录请求
  B->>A: 登录成功
```

类图示例：

```mermaid
classDiagram
  Animal <|-- Duck
  Animal <|-- Fish
  Animal: +int age
  Animal: +String gender
  Animal: +isMammal()
  class Duck{
    +String beakColor
    +swim()
    +quack()
  }
  class Fish{
    -int sizeInFeet
    -canEat()
  }
```

饼图示例：

```mermaid
pie title 销售分布
  "产品A" : 42.86
  "产品B" : 57.14
```

状态图示例：

```mermaid
stateDiagram-v2
  [*] --> Still
  Still --> [*]
  Still --> Moving
  Moving --> Still
  Moving --> Crash
  Crash --> [*]
```

### 脚注 (Footnotes)

为文档添加注释和引用，提高内容的可信度和完整性

```markdown
这是一个带有脚注的句子[^1]

[^1]: 这是脚注的内容
```

<br>

## AI 增强功能

### 元数据支持 (Front Matter)

为 AI 处理提供上下文信息，便于内容分类和检索

```markdown
---
title: 文档标题
author: 作者姓名
tags: [标签1, 标签2]
date: 2023-01-01
---
```

### 注释和标签 (Comments and Tags)

便于内容分类和检索，提高文档的可管理性

```markdown
<!-- 这是一个注释，不会在最终文档中显示 -->

# 标题 {#custom-id .class-name}
```

### 引用和链接 (References and Links)

建立知识网络，便于 AI 理解文档间的关系

```markdown
这是一个[内部链接](#章节标题)和[外部链接](https://example.com)

> 这是一个引用块，常用于引用他人观点
```

---

# Markdown 生态系统

# Markdown Ecosystem

<br>

## 编辑器工具

- **Typora** - 所见即所得 Markdown 编辑器
- **Obsidian** - 知识管理和笔记应用
- **Mark Text** - 开源 Markdown 编辑器
- **Zettlr** - 学术写作专用编辑器

### VS Code 及其 Markdown 扩展

- **Markdown All in One** - 提供快捷键、自动预览、目录生成等功能
- **Markdown Preview Enhanced** - 增强的 Markdown 预览功能，支持数学公式、图表等
- **Markdownlint** - Markdown 语法检查和规范工具
- **Markdown Table Formatter** - 表格自动格式化
- **Markdown Emoji** - 支持 Emoji 表情符号
- **Markdown PDF** - 将 Markdown 文档导出为 PDF 格式
- **Paste Image** - 方便在 Markdown 中插入图片
- **Auto-Open Markdown Preview** - 自动打开 Markdown 预览窗口

<br>

## 替代 Office 套件的工具

### 替代 Word 的文档工具

- **Markdown** - 专注于内容创作的纯文本格式
- **Typora/Obsidian** - 提供所见即所得的编辑体验
- **HackMD/CodiMD** - 在线协作 Markdown 编辑器

### 替代 Excel 的表格和数据工具

- **CSV/TSV 文件** - 简单的纯文本表格格式
- **Markdown 表格** - 内联表格语法
- **Jupyter Notebook** - 数据科学和分析环境
- **Airtable** - 结合数据库和电子表格功能

### 替代 PowerPoint 的演示工具

- **Slidev** - 我们正在使用的演示文稿工具
- **Marp** - Markdown 转换为幻灯片
- **Reveal.js** - HTML 演示框架，支持 Markdown
- **Remark.js** - 简单的 Markdown 幻灯片工具

<br>

## 转换和发布工具

- **Pandoc** - 万能文档转换器
- **Hugo** - 静态网站生成器
- **Jekyll** - 博客感知静态网站生成器
- **Slidev** - 我们正在使用的演示文稿工具

<br>

## 协作和版本控制

- **Git** - 版本控制系统的完美搭档
- **GitHub/GitLab** - 在线协作平台
- **Notion** - 集成文档和项目管理

---

# 实际应用案例

# Real-world Applications

<br>

## 技术文档

- **API 文档** - 使用 Markdown 编写，自动生成
- **开发手册** - 团队内部知识库
- **开源项目** - README 和 Wiki

<br>

## 学术和教育

- **课程材料** - 教案、讲义、作业
- **学术论文** - 配合工具链实现公式和引用
- **在线教育** - MOOC 平台内容

<br>

## 商业应用

- **产品文档** - 用户手册、帮助文档
- **内容营销** - 博客、白皮书、案例研究
- **内部沟通** - Wiki、会议记录

---

# 未来展望

# Future Perspectives

<br>

## AI 与 Markdown 的深度融合

- **智能写作助手** - 根据上下文提供语法建议
- **自动格式化** - 根据内容类型自动应用样式
- **语义增强** - 自动添加元数据和标签

<br>

## 新兴技术整合

- **WebAssembly** - 更强大的本地处理能力
- **区块链** - 文档确权和溯源
- **AR/VR** - 沉浸式文档体验

<br>

## 标准化和互操作性

- **统一扩展语法** - 减少碎片化
- **跨平台兼容** - 更好的互操作性
- **生态系统整合** - 工具链无缝衔接

---

# 总结

# Conclusion

<br>

## Markdown 的核心优势

- **简洁易用** - 专注于内容创作
- **广泛支持** - 几乎所有平台都支持
- **易于扩展** - 丰富的生态系统

<br>

## AI 时代的机遇

- **智能化处理** - 更好的语义理解和生成
- **自动化工具** - 提高创作效率
- **协作增强** - 更好的团队协作体验

<br>

## 展望

Markdown 作为轻量级标记语言，在 AI 时代将继续发挥重要作用，其简单性和可扩展性使其成为理想的文档格式选择。

---

# 谢谢！

# Thank You!

<br>

## 有任何问题吗？

### Questions & Discussion

<br>
<br>

<!-- <div class="flex">
  <div class="mx-auto">
    <logos-markdown text="xl" class="opacity-50 m-2" />
    <logos-ai text="xl" class="opacity-50 m-2" />
    <logos-open-source text="xl" class="opacity-50 m-2" />
  </div>
</div> -->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

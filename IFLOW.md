# 项目概述

这是一个基于 [Slidev](https://github.com/slidevjs/slidev) 构建的演示文稿项目，主题为"AI时代的文档格式——Markdown的扩展语法和生态介绍"。该项目使用 Markdown 语法编写幻灯片内容，并利用 Slidev 提供的特性（如主题、布局、组件等）来创建专业的演示文稿。

## 主要技术

- **Slidev**: 用于创建演示文稿的工具。
- **Markdown**: 用于编写幻灯片内容的标记语言。
- **Vue.js**: Slidev 基于 Vue.js 构建，允许在幻灯片中使用 Vue 组件。
- **Yarn**: 项目的包管理器。

## 项目结构

- `slides.md`: 主要的幻灯片内容文件，包含了所有幻灯片的内容和元数据。
- `components/`: 包含自定义 Vue 组件的目录，如 `Cols.vue` 和 `Note.vue`。
- `public/`: 静态资源目录，如图片等。
- `snippets/`: 可能包含代码片段或其他文本内容。
- `package.json`: 项目配置文件，定义了依赖项和脚本命令。
- `README.md`: 项目说明文件，提供了基本的使用指导。

# 构建和运行

## 安装依赖

```bash
yarn install
```

## 开发模式

启动开发服务器并打开浏览器：

```bash
yarn dev
```

## 构建静态站点

将演示文稿构建为静态站点：

```bash
yarn build
```

## 导出为 PDF

将演示文稿导出为 PDF 文件：

```bash
yarn export
```

# 开发约定

## 幻灯片编写

- 幻灯片内容主要在 `slides.md` 文件中编写。
- 使用 Markdown 语法和 Slidev 的扩展语法来定义幻灯片的布局、样式和内容。
- 可以使用 Vue 组件来增强幻灯片的功能和表现力。

## 代码风格

- 使用 Prettier 来格式化 Markdown 文件，特别是 `slides.md`。
- 配置了 `prettier-plugin-slidev` 插件来更好地支持 Slidev 的语法。

## 自定义组件

- 在 `components/` 目录中可以创建和使用自定义 Vue 组件。
- 这些组件可以在 `slides.md` 中通过标签直接使用。
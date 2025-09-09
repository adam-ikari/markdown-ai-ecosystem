# AI 时代的文档格式 - Markdown 生态介绍

这是一个基于 [Slidev](https://github.com/slidevjs/slidev) 构建的演示文稿项目，主题为"AI时代的文档格式——Markdown的扩展语法和生态介绍"。该项目使用 Markdown 语法编写幻灯片内容，并利用 Slidev 提供的特性（如主题、布局、组件等）来创建专业的演示文稿。

## 快速开始

要启动幻灯片演示：

- 安装依赖: `yarn install`
- 启动开发模式: `yarn dev`
- 访问地址: <http://localhost:3030>

编辑 [slides.md](./slides.md) 文件以查看更改。

## 项目结构

- `slides.md`: 主要的幻灯片内容文件，包含了所有幻灯片的内容和元数据。
- `components/`: 包含自定义 Vue 组件的目录，如 `Cols.vue` 和 `Note.vue`。
- `public/`: 静态资源目录，如图片等。
- `IFLOW.md`: 项目详细信息和开发指南。

## 构建和导出

- 构建静态站点: `yarn build`
- 导出为 PDF: `yarn export`

## 更多信息

- 了解 Slidev 的更多功能，请查看 [官方文档](https://sli.dev/)。
- 项目的详细开发信息请参阅 [IFLOW.md](./IFLOW.md)。
# Project Guidelines

## 项目概述

这是「知更鸟SKill」个人知识站点，基于 **Docsify v4** 构建，通过 GitHub Pages 部署。纯静态站点，无构建步骤，无 package.json。

- 仓库：https://github.com/wlunan/idocs
- 站点名：知更鸟SKill
- 主题：Vue (CDN docsify@4)

## 架构

```
README.md           ← 仓库说明（GitHub 展示用）
docs/
├── index.html          Docsify 入口 + 配置（window.$docsify）
├── _sidebar.md         手动维护的导航栏（部分使用 autoSidebar 自动生成）
├── _coverpage.md       封面页
├── README.md           首页内容（Docsify 站点首页）
├── media/              静态资源（图片等）
├── 博客/               博客文章
├── 介绍/               站点介绍
└── 资源/               资源分享
```

## 关键约定

- **纯 Markdown 内容**：所有页面都是 `.md` 文件，Docsify 在浏览器端渲染
- **无构建/部署命令**：推送到 GitHub 即自动部署（GitHub Pages），没有 `npm run build`
- **中文内容**：所有文章和 UI 文本使用中文
- **文件名可含中文**：目录和文件名使用中文，如 `博客/站点搭建.md`
- **侧栏管理**：`_sidebar.md` 中部分条目被注释（`<!-- -->`），新增页面需同步更新侧栏或依赖 autoSidebar
- **Docsify 插件**：已启用 sidebar-collapse（可折叠侧栏）和全文搜索

## 编辑注意事项

- 修改 `docs/index.html` 中的 `window.$docsify` 对象来调整 Docsify 配置
- 新增页面后检查 `docs/_sidebar.md` 是否需要手动添加链接
- 图片放入 `docs/media/` 目录，用相对路径引用：`media/xxx.png`
- 不需要 `npm install` 或任何依赖安装——直接编辑 Markdown 文件即可预览
- 本地预览：使用 `docsify serve docs`（需全局安装 docsify-cli）或直接打开 `docs/index.html`

## 文件格式

- Markdown 文件遵循 Docsify 语法（标准 Markdown + Docsify 扩展）
- `_coverpage.md` 使用 HTML 标签（`<img>`）和 Markdown 链接混合
- `index.html` 中的 JS 注释使用中文，记录配置项用途

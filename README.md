# 🏡 知更鸟SKill

个人知识站点 —— 博客、资源分享与碎碎念。

🔗 **站点地址**：https://wlunan.github.io/idocs

## 项目结构

```
docs/           ← Docsify 站点源文件
├── index.html      Docsify 入口 + 配置
├── _sidebar.md     导航侧栏
├── _coverpage.md   封面页
├── README.md       首页内容
├── media/          静态资源（图片等）
├── 博客/           博客文章
├── 介绍/           站点介绍
└── 资源/           资源分享
```

## 本地预览

```bash
# 方式一：docsify-cli
# 全局安装 docsify-cli
npm i -g docsify-cli

cd docs
docsify serve docs

# 方式二：直接打开
# 用浏览器打开 docs/index.html
```

## 使用指南

### 新建博客文章

1. 在 `docs/博客/` 下新建 `.md` 文件，例如 `docs/博客/读书笔记.md`
2. 编写内容：

```markdown
# 读书笔记

## 正文标题

这里是正文内容...
```

3. 如需在侧栏显示，编辑 `docs/_sidebar.md` 添加链接：
   ```markdown
   - [博客](博客/)
     - [读书笔记](./博客/读书笔记.md)
   ```
   > 未手动添加也无妨，autoSidebar 会自动生成

### 添加资源

编辑 `docs/资源/README.md`，按分类追加：

```markdown
### 工具

- [工具名](https://example.com) — 一句话描述
```

### 添加图片

将图片放入 `docs/media/`，在 Markdown 中用相对路径引用：

```markdown
![描述](media/xxx.png)
```

## 部署

站点基于 [Docsify](https://docsify.js.org/) 构建，纯静态，无需构建步骤。推送到 `main` 分支后通过 GitHub Pages / Cloudflare Pages 自动部署。

## 技术栈

- [Docsify v4](https://docsify.js.org/) — 客户端 Markdown 渲染
- Vue 主题 + sidebar-collapse 插件
- 全文搜索插件
- 无 Node.js 依赖，无 package.json，纯 Markdown 内容管理

## 相关链接
- v4文档：https://docsify.js.org/#/zh-cn/
- v5文档：https://preview.docsifyjs.org/#/zh-cn/
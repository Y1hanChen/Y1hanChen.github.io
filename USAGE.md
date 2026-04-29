# 使用指南

## 快速开始

你的个人学术主页已经创建完成！这是一个基于 Jekyll 的静态网站，参考了 al-folio 的设计风格。

## 下一步操作

### 1. 更新个人信息

编辑 [_config.yml](_config.yml)，填写你的社交媒体账号：

```yaml
# Social links
github_username: your-github-username        # 你的 GitHub 用户名
scholar_userid: your-google-scholar-id       # Google Scholar ID
linkedin_username: your-linkedin-username    # LinkedIn 用户名
```

### 2. 添加个人照片

将你的照片放在 `assets/img/profile.jpg`。建议使用：
- 尺寸：至少 400x400 像素
- 格式：JPG 或 PNG
- 专业的个人照片

### 3. 添加更多论文

在 `_publications/` 目录下创建新的 Markdown 文件，格式如下：

```markdown
---
title: "论文标题"
authors: "作者列表"
venue: "会议/期刊名称"
year: 2026
status: "Accepted/Published/Under Review"
pdf: "PDF链接"
code: "代码仓库链接"
arxiv: "arXiv链接"
abstract: "摘要"
---

详细描述（可选）
```

### 4. 写博客文章

在 `_posts/` 目录下创建新文件，命名格式：`YYYY-MM-DD-title.md`

```markdown
---
layout: post
title: "文章标题"
date: 2026-04-29
categories: research nlp
---

文章内容...
```

### 5. 本地预览

```bash
cd personal-website

# 安装依赖（首次运行）
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

### 6. 部署到 GitHub Pages

详细步骤请查看 [DEPLOY.md](DEPLOY.md)

简要步骤：
1. 在 GitHub 创建仓库（建议命名为 `username.github.io`）
2. 推送代码到仓库
3. 在仓库设置中启用 GitHub Pages
4. 等待自动部署完成

## 项目结构

```
personal-website/
├── _config.yml              # 网站配置
├── index.md                 # 主页
├── _layouts/                # 页面布局模板
│   ├── default.html
│   ├── page.html
│   └── post.html
├── _includes/               # 可复用组件
│   ├── header.html
│   └── footer.html
├── _posts/                  # 博客文章
│   └── 2026-04-29-welcome.md
├── _publications/           # 论文列表
│   └── coconuts-acl2026.md
├── pages/                   # 其他页面
│   ├── publications.md
│   └── blog.md
├── assets/                  # 静态资源
│   ├── css/
│   │   └── main.css        # 主样式文件
│   ├── js/
│   └── img/
│       └── profile.jpg     # 个人照片（需要添加）
├── .github/
│   └── workflows/
│       └── jekyll.yml      # GitHub Actions 配置
├── Gemfile                  # Ruby 依赖
├── README.md               # 项目说明
└── DEPLOY.md               # 部署指南
```

## 自定义样式

如果你想修改网站的外观，编辑 [assets/css/main.css](assets/css/main.css)。

主要的 CSS 变量：
```css
:root {
  --primary-color: #2c3e50;      /* 主色调 */
  --secondary-color: #3498db;    /* 强调色 */
  --text-color: #333;            /* 文字颜色 */
  --link-color: #0366d6;         /* 链接颜色 */
}
```

## 功能特性

✅ 响应式设计，支持移动端
✅ 个人简介和照片展示
✅ 教育背景和研究经历
✅ 论文出版物列表
✅ 博客功能
✅ 社交媒体链接
✅ SEO 优化
✅ GitHub Pages 自动部署

## 需要帮助？

- Jekyll 文档：https://jekyllrb.com/docs/
- GitHub Pages 文档：https://docs.github.com/en/pages
- al-folio 主题参考：https://github.com/alshedivat/al-folio

## 许可

你可以自由使用和修改这个模板。

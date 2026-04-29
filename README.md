# Yihan Chen - Personal Website

学术个人主页，基于 Jekyll 构建，部署在 GitHub Pages。

## 本地开发

1. 安装依赖：
```bash
bundle install
```

2. 启动本地服务器：
```bash
bundle exec jekyll serve
```

3. 访问 http://localhost:4000

## 部署到 GitHub Pages

1. 创建 GitHub 仓库（建议命名为 `username.github.io`）
2. 推送代码到仓库
3. 在仓库设置中启用 GitHub Pages
4. 选择 `main` 分支作为源

## 自定义

- 编辑 `_config.yml` 修改网站配置
- 在 `assets/img/` 添加个人照片
- 在 `_posts/` 添加博客文章
- 在 `_publications/` 添加论文信息

## 目录结构

```
├── _config.yml          # 网站配置
├── index.md             # 主页
├── _layouts/            # 页面布局
├── _includes/           # 可复用组件
├── _posts/              # 博客文章
├── _publications/       # 论文列表
├── assets/              # 静态资源
│   ├── css/            # 样式文件
│   ├── js/             # JavaScript
│   └── img/            # 图片
└── pages/              # 其他页面
```

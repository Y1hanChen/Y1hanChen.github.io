# 部署指南

## 快速开始

### 1. 准备工作

确保你已经安装了以下工具：
- Git
- Ruby (>= 2.7)
- Bundler

### 2. 本地预览

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

### 3. 部署到 GitHub Pages

#### 方法一：使用 GitHub Actions（推荐）

1. 在 GitHub 上创建新仓库，建议命名为 `username.github.io`
2. 将代码推送到仓库：
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```
3. 在仓库设置中：
   - 进入 Settings > Pages
   - Source 选择 "GitHub Actions"
4. 等待 Actions 自动构建和部署
5. 访问 `https://username.github.io`

#### 方法二：直接部署

1. 创建仓库并推送代码
2. 在仓库设置中：
   - 进入 Settings > Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 "main" 和 "/ (root)"
3. 等待几分钟后访问你的网站

### 4. 自定义域名（可选）

1. 在域名提供商处添加 DNS 记录：
   ```
   A    @    185.199.108.153
   A    @    185.199.109.153
   A    @    185.199.110.153
   A    @    185.199.111.153
   ```
2. 在仓库根目录创建 `CNAME` 文件，内容为你的域名
3. 在 GitHub Pages 设置中添加自定义域名

## 自定义内容

### 修改个人信息

编辑 `_config.yml` 文件，更新以下字段：
- `title`: 你的名字
- `email`: 你的邮箱
- `author`: 个人信息
- `github_username`: GitHub 用户名
- `scholar_userid`: Google Scholar ID
- `linkedin_username`: LinkedIn 用户名

### 添加个人照片

将你的照片放在 `assets/img/profile.jpg`

### 添加论文

在 `_publications/` 目录下创建新的 Markdown 文件，参考 `coconuts-acl2026.md` 的格式。

### 写博客

在 `_posts/` 目录下创建新文件，命名格式：`YYYY-MM-DD-title.md`

## 常见问题

### 本地预览时出现依赖错误

```bash
bundle update
bundle install
```

### GitHub Pages 构建失败

检查 Actions 标签页的错误日志，通常是依赖版本问题。

### 样式没有正确加载

确保 `_config.yml` 中的 `baseurl` 和 `url` 配置正确。

## 更多资源

- [Jekyll 文档](https://jekyllrb.com/docs/)
- [GitHub Pages 文档](https://docs.github.com/en/pages)
- [al-folio 主题](https://github.com/alshedivat/al-folio)

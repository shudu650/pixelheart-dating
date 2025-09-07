# GitHub Pages 部署指南

## 步骤 1: 创建 GitHub 仓库

1. 登录到 [GitHub](https://github.com)
2. 点击右上角的 "+" 按钮，选择 "New repository"
3. 输入仓库名称，例如 `pixel-love-blog`
4. 确保仓库是 Public（GitHub Pages 免费版需要公开仓库）
5. 不要初始化 README、.gitignore 或 license（我们已经创建了这些文件）
6. 点击 "Create repository"

## 步骤 2: 上传代码到 GitHub

在项目目录中运行以下命令：

```bash
# 初始化 Git 仓库（如果还没有初始化）
git init

# 添加所有文件
git add .

# 提交代码
git commit -m "Initial commit: Pixel Love dating blog"

# 添加远程仓库（替换为你的 GitHub 用户名和仓库名）
git remote add origin https://github.com/YOUR_USERNAME/pixel-love-blog.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

## 步骤 3: 启用 GitHub Pages

1. 在 GitHub 仓库页面，点击 "Settings" 标签
2. 在左侧菜单中找到 "Pages"
3. 在 "Source" 部分，选择 "Deploy from a branch"
4. 选择 "main" 分支和 "/ (root)" 文件夹
5. 点击 "Save"

## 步骤 4: 访问你的网站

几分钟后，你的网站将在以下地址可用：
```
https://YOUR_USERNAME.github.io/pixel-love-blog/
```

## 自定义域名（可选）

如果你有自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 在文件中写入你的域名，例如：`www.pixellove.com`
3. 在你的域名提供商处设置 DNS 记录指向 GitHub Pages

## 更新网站

要更新网站内容，只需：

1. 修改本地文件
2. 提交并推送更改：
   ```bash
   git add .
   git commit -m "Update content"
   git push
   ```
3. GitHub Pages 会自动更新你的网站

## 故障排除

- 如果网站没有立即显示，请等待几分钟
- 检查 GitHub Pages 设置是否正确
- 确保 `index.html` 文件在仓库根目录
- 查看仓库的 Actions 标签页检查部署状态

---

🎉 恭喜！你的像素风约会博客现在已经在线了！
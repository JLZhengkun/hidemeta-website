# 🚀 GitHub Pages 部署指令

## ✅ 已完成的准备工作

- ✓ Git 仓库已初始化
- ✓ 所有文件已提交到 `main` 分支
- ✓ 共提交 4 个文件,700 行代码

## 📋 下一步操作指南

### 步骤 1: 创建 GitHub 仓库

请访问 GitHub 并创建一个新的仓库:

1. 访问: https://github.com/new
2. **仓库名称**: `hidemeta-privacy` (推荐名称)
3. **可见性**: ✅ **Public** (必须设置为公开,GitHub Pages 免费版仅支持公开仓库)
4. **其他选项**: 
   - ❌ 不要勾选 "Add a README file"
   - ❌ 不要添加 .gitignore
   - ❌ 不要选择 license
5. 点击 **"Create repository"**

### 步骤 2: 推送代码到 GitHub

创建仓库后,GitHub 会显示推送指令。请在终端执行以下命令:

```bash
# 进入隐私政策目录
cd /Users/zhengkun/Documents/app/HideMeta/privacy-policy

# 添加远程仓库 (请替换 YOUR_USERNAME 为您的 GitHub 用户名)
git remote add origin https://github.com/YOUR_USERNAME/hidemeta-privacy.git

# 推送到 GitHub
git push -u origin main
```

> **提示**: 如果需要身份验证,请使用 GitHub Personal Access Token 或 SSH 密钥。

### 步骤 3: 启用 GitHub Pages

代码推送成功后:

1. 在 GitHub 仓库页面,点击 **Settings** (设置)
2. 在左侧菜单找到 **Pages**
3. 在 **Source** (来源) 部分:
   - **Branch**: 选择 `main`
   - **Folder**: 选择 `/ (root)`
4. 点击 **Save** (保存)

### 步骤 4: 获取隐私政策 URL

等待 1-2 分钟后,GitHub Pages 会显示您的网站 URL:

```
https://YOUR_USERNAME.github.io/hidemeta-privacy/
```

这就是您需要在 App Store Connect 中填写的隐私政策 URL！

### 步骤 5: 验证部署

在浏览器中访问您的 URL,确认:
- ✓ 页面能正常加载
- ✓ 中英文切换功能正常
- ✓ 在手机和电脑上显示正常

## 🎯 App Store Connect 配置

1. 登录 [App Store Connect](https://appstoreconnect.apple.com)
2. 选择 **HideMeta** 应用
3. 进入 **App 信息**
4. 找到 **隐私政策 URL** 字段
5. 填入: `https://YOUR_USERNAME.github.io/hidemeta-privacy/`
6. 保存

---

## 🆘 需要帮助？

**常见问题:**

1. **推送时要求身份验证**
   - 使用 GitHub Personal Access Token
   - 或配置 SSH 密钥

2. **GitHub Pages 显示 404**
   - 等待 2-5 分钟让 GitHub 构建页面
   - 确保仓库是 Public (公开)
   - 检查 Settings > Pages 设置是否正确

3. **页面无法显示**
   - 确认分支是 `main` 且文件夹是 `/`
   - 检查 `index.html` 文件确实存在于根目录

---

**准备好了吗？请告诉我您的 GitHub 用户名(或完整仓库 URL),我可以帮您生成准确的命令！**

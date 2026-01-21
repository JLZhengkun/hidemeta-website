# HideMeta 隐私政策 - GitHub Pages 部署指南

本目录包含 HideMeta 应用的隐私政策文档，可以部署到 GitHub Pages 上。

## 📁 文件说明

- `index.html` - 中英文双语隐私政策静态页面（推荐用于 GitHub Pages）
- `privacy-policy-zh.md` - 中文版 Markdown 格式
- `privacy-policy-en.md` - 英文版 Markdown 格式
- `README.md` - 本部署指南

## 🚀 部署到 GitHub Pages

### 方法一：使用现有仓库（推荐）

如果您已经有 GitHub 仓库（例如存放 HideMeta 代码的仓库）：

#### 步骤 1: 创建 GitHub 仓库（如果还没有）

```bash
# 进入隐私政策目录
cd /Users/zhengkun/Documents/app/HideMeta/privacy-policy

# 初始化 Git 仓库（如果还没有）
git init

# 添加所有文件
git add .

# 提交
git commit -m "Add HideMeta privacy policy"

# 关联远程仓库（替换 YOUR_USERNAME 为您的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/hidemeta-privacy.git

# 推送到 GitHub
git push -u origin main
```

#### 步骤 2: 启用 GitHub Pages

1. 访问您的 GitHub 仓库页面
2. 点击 **Settings**（设置）
3. 在左侧菜单找到 **Pages**
4. 在 **Source** 下选择：
   - Branch: `main`
   - Folder: `/ (root)` 或 `/privacy-policy`（取决于您的文件位置）
5. 点击 **Save**

#### 步骤 3: 获取隐私政策 URL

几分钟后，您的隐私政策将可以通过以下 URL 访问：

```
https://YOUR_USERNAME.github.io/hidemeta-privacy/
```

或者，如果文件在子目录：

```
https://YOUR_USERNAME.github.io/REPO_NAME/privacy-policy/
```

### 方法二：使用独立仓库

创建一个专门用于隐私政策的仓库：

```bash
# 创建新目录
mkdir hidemeta-privacy-policy
cd hidemeta-privacy-policy

# 复制隐私政策文件
cp /Users/zhengkun/Documents/app/HideMeta/privacy-policy/index.html .
cp /Users/zhengkun/Documents/app/HideMeta/privacy-policy/*.md .

# 初始化 Git
git init
git add .
git commit -m "Initial commit: HideMeta privacy policy"

# 创建 GitHub 仓库后推送
git remote add origin https://github.com/YOUR_USERNAME/hidemeta-privacy-policy.git
git branch -M main
git push -u origin main
```

然后按照上面的步骤 2 和 3 启用 GitHub Pages。

## 🌐 自定义域名（可选）

如果您有自己的域名，可以设置自定义域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 在文件中写入您的域名，例如：`privacy.hidemeta.com`
3. 在您的域名 DNS 设置中添加 CNAME 记录指向：`YOUR_USERNAME.github.io`

## 📝 在 App Store Connect 中使用

部署完成后，您可以在 App Store Connect 中填写隐私政策 URL：

1. 登录 [App Store Connect](https://appstoreconnect.apple.com)
2. 选择您的应用（HideMeta）
3. 进入 **App 信息**
4. 找到 **隐私政策 URL** 字段
5. 填入您的 GitHub Pages URL，例如：
   ```
   https://YOUR_USERNAME.github.io/hidemeta-privacy/
   ```

## ✅ 验证部署

部署完成后，请验证：

- ✓ URL 可以正常访问
- ✓ 中英文切换功能正常
- ✓ 页面在移动设备和桌面设备上显示正常
- ✓ 深色模式/浅色模式自动适配

## 🔄 更新隐私政策

如需更新隐私政策：

1. 修改 `index.html` 或 Markdown 文件
2. 更新 "最后更新日期"
3. 提交并推送到 GitHub：
   ```bash
   git add .
   git commit -m "Update privacy policy"
   git push
   ```

GitHub Pages 会自动重新部署，通常在几分钟内生效。

## 🎨 自定义样式

`index.html` 使用了现代化的设计，包括：
- 响应式布局
- 深色/浅色模式自动适配
- 平滑的语言切换动画
- 移动设备优化

您可以根据需要修改 `<style>` 标签中的 CSS。

## 📞 技术支持

如果遇到问题，请检查：
- GitHub Pages 是否已启用
- 分支和文件路径设置是否正确
- 仓库是否设置为 Public（公开）

---

**提示**：如果您使用的是 GitHub 免费账户，请确保仓库设置为 **Public**（公开），因为 GitHub Pages 仅支持公开仓库的免费托管。

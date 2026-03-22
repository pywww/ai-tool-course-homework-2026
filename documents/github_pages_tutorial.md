# GitHub Pages 个人网页创建详细教程

## 📖 目录
- [什么是 GitHub Pages](#什么是-github-pages)
- [第一步：创建仓库](#第一步创建仓库)
- [第二步：创建你的第一个网页](#第二步创建你的第一个网页)
- [第三步：开启 GitHub Pages 服务](#第三步开启-github-pages-服务)
- [第四步：访问你的网页](#第四步访问你的网页)
- [进阶：如何更新网页](#进阶如何更新网页)
- [更多创意玩法](#更多创意玩法)
- [常见问题解答](#常见问题解答)

---

## 什么是 GitHub Pages

GitHub Pages 是 GitHub 提供的**免费静态网页托管服务**。你可以用它来：
- 📝 创建个人博客
- 🎨 展示个人作品
- 📚 分享学习笔记
- 🖼️ 制作项目介绍页面
- 等等...

它的优点：
- ✅ 完全免费
- ✅ 全球访问速度快
- ✅ 操作简单
- ✅ 支持自定义域名
- ✅ 集成GitHub版本控制

---

## 第一步：创建仓库

### 1.1 登录 GitHub
打开浏览器，访问 [https://github.com](https://github.com) 并登录你的账号。

### 1.2 新建仓库
1. 点击右上角的 **"+"** 图标
2. 选择 **"New repository"**

### 1.3 填写仓库信息（非常重要！）

| 项目 | 填写内容 | 说明 |
|------|---------|------|
| Repository name | `你的用户名.github.io` | **必须**这样命名！ |
| Description | （可选）我的个人网页 | 简单描述一下 |
| Public/Private | Public | 必须选择公开 |
| Initialize with a README | ✅ 勾选 | 使用Readme文件初始化 |

**示例**：
如果你的 GitHub 用户名是 `zhangsan`，那么仓库名就必须是 `zhangsan.github.io`

### 1.4 创建仓库
点击 **"Create repository"** 按钮。

**✅ 成功标准**：
你现在有了一个名为 `你的用户名.github.io` 的仓库！

---

## 第二步：创建你的第一个网页

### 2.1 进入仓库
点击你刚创建的仓库，进入仓库主页。

### 2.2 新建文件
1. 点击仓库页面上的 **"Add file"** → **"Create new file"**
2. 在"Name your file..."输入框中输入：`index.html`
   - 注意：文件名必须是 `index.html`，这是主页的默认文件名

### 2.3 编写网页代码

在文件内容区域，复制并粘贴以下代码（你可以根据自己的喜好修改）：

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>我的个人网页</title>
    <style>
        body {
            font-family: "Microsoft YaHei", "微软雅黑", sans-serif;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }
        .container {
            background-color: white;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.2);
            overflow: hidden;
        }
        .header {
            text-align: center;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px 20px;
        }
        .header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        .header p {
            margin-top: 10px;
            font-size: 1.2em;
            opacity: 0.9;
        }
        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid white;
            margin-bottom: 15px;
            background-color: #ddd;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }
        .content {
            padding: 30px;
        }
        .section {
            margin-bottom: 30px;
        }
        .section h2 {
            color: #667eea;
            border-bottom: 2px solid #667eea;
            padding-bottom: 10px;
            margin-top: 0;
        }
        .info-list {
            list-style: none;
            padding: 0;
        }
        .info-list li {
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        .info-list li:last-child {
            border-bottom: none;
        }
        .tag {
            display: inline-block;
            background-color: #667eea;
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            margin: 5px;
            font-size: 0.9em;
        }
        .footer {
            text-align: center;
            padding: 20px;
            background-color: #f8f9fa;
            color: #666;
        }
        .social-links a {
            display: inline-block;
            margin: 10px;
            color: #667eea;
            text-decoration: none;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="avatar">👤</div>
            <h1>欢迎来到我的个人网页！</h1>
            <p>这是我用 GitHub Pages 创建的第一个网页 🎉</p>
        </div>
        
        <div class="content">
            <div class="section">
                <h2>👋 关于我</h2>
                <ul class="info-list">
                    <li><strong>姓名：</strong>你的姓名</li>
                    <li><strong>学号：</strong>你的学号</li>
                    <li><strong>专业：</strong>你的专业</li>
                    <li><strong>学校：</strong>你的学校</li>
                </ul>
            </div>
            
            <div class="section">
                <h2>🌟 我的兴趣</h2>
                <div>
                    <span class="tag">人工智能</span>
                    <span class="tag">编程开发</span>
                    <span class="tag">阅读写作</span>
                    <span class="tag">音乐电影</span>
                    <span class="tag">旅行摄影</span>
                </div>
            </div>
            
            <div class="section">
                <h2>📚 学习目标</h2>
                <ul class="info-list">
                    <li>✅ 掌握 Git 和 GitHub 的使用</li>
                    <li>✅ 学习 AI 工具的应用</li>
                    <li>✅ 完成一个有趣的项目</li>
                    <li>⬜ 更多目标等你来添加...</li>
                </ul>
            </div>
            
            <div class="section">
                <h2>📧 联系方式</h2>
                <div class="social-links">
                    <a href="mailto:你的邮箱@example.com">📧 邮箱</a>
                    <a href="https://github.com/你的用户名">🔗 GitHub</a>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <p>&copy; 2024 我的个人网页 | Made with ❤️ using GitHub Pages</p>
        </div>
    </div>
</body>
</html>
```

### 2.4 自定义你的网页

修改代码中的以下部分，替换为你自己的信息：

| 需要修改的地方 | 示例 |
|--------------|------|
| `你的姓名` | 张三 |
| `你的学号` | 2023001 |
| `你的专业` | 人工智能 |
| `你的学校` | XX大学 |
| `你的邮箱@example.com` | zhangsan@example.com |
| `你的用户名` | zhangsan |

你还可以：
- 修改兴趣标签（`<span class="tag">...</span>`）
- 修改学习目标
- 修改页面颜色（在 `<style>` 部分）

### 2.5 提交文件
1. 在页面底部的"Commit message"中输入：`创建个人主页`
2. 点击 **"Commit new file"** 按钮

---

## 第三步：开启 GitHub Pages 服务

### 3.1 进入设置页面
1. 在仓库页面，点击顶部的 **"Settings"** 选项卡
2. 在左侧菜单中找到并点击 **"Pages"**

### 3.2 配置 Pages 服务
填写以下信息：

| 配置项 | 选择/填写 |
|--------|----------|
| Source | Deploy from a branch |
| Branch | `main`（或 `master`） |
| Folder | `/ (root)` |

### 3.3 保存设置
点击 **"Save"** 按钮。

### 3.4 等待部署
页面会显示"Your site is ready to be published"，首次部署通常需要等待 5-10 分钟。

**✅ 成功标准**：
页面显示"Your site is live at https://你的用户名.github.io"，并且提供了访问地址！

---

## 第四步：访问你的网页

### 4.1 获取访问地址
在 GitHub Pages 设置页面，你会看到你的网页地址：

```
https://你的用户名.github.io
```

**示例**：
```
https://zhangsan.github.io
```

### 4.2 访问网页
在浏览器中输入这个地址，你就能看到你的个人网页了！

**注意**：有时候可能需要等待 5-10 分钟才能正常访问，这是正常的，请耐心等待。

---

## 进阶：如何更新网页

### 方法一：在 GitHub 网页上直接编辑（适合小修改）

1. 进入你的仓库
2. 点击要修改的文件（比如 `index.html`）
3. 点击编辑图标（铅笔形状 ✏️）
4. 修改内容
5. 在底部填写提交信息，比如"更新个人信息"
6. 点击 **"Commit changes"**

### 方法二：使用 Git 在本地编辑（推荐，适合大修改）

#### 1. 克隆仓库到本地
打开 Git Bash 或终端，执行：
```bash
git clone https://github.com/你的用户名/你的用户名.github.io.git
```

#### 2. 进入仓库目录
```bash
cd 你的用户名.github.io
```

#### 3. 修改文件
用你喜欢的编辑器（如 VS Code、记事本等）打开并修改 `index.html` 文件。

#### 4. 提交并推送
```bash
git add .
git commit -m "更新网页内容"
git push origin main
```

完成！等待几分钟，你的网页就会自动更新了！

---

## 更多创意玩法

### 🎨 玩法一：添加图片

1. 在仓库中创建一个文件夹，命名为 `images`
2. 上传你的照片或图片到这个文件夹
3. 在 HTML 中引用图片：

```html
<img src="images/你的照片.jpg" alt="我的照片" style="width: 200px; border-radius: 10px;">
```

### 📄 玩法二：创建多个页面

1. 创建新文件 `about.html`（关于我页面）
2. 创建新文件 `blog.html`（博客页面）
3. 在主页添加导航链接：

```html
<div style="text-align: center; margin: 20px 0;">
    <a href="index.html" style="margin: 0 10px;">首页</a>
    <a href="about.html" style="margin: 0 10px;">关于我</a>
    <a href="blog.html" style="margin: 0 10px;">博客</a>
</div>
```

### 🎭 玩法三：使用现成模板

1. 在网上搜索 "HTML5 website template" 或 "免费网页模板"
2. 下载你喜欢的模板
3. 将模板文件上传到你的仓库
4. 修改模板内容为你自己的信息

推荐模板网站：
- [Free CSS](https://www.free-css.com/)
- [Templated](https://templated.co/)
- [HTML5 UP](https://html5up.net/)

### 💡 玩法四：添加更多功能

- 添加访客计数器
- 添加音乐播放器
- 添加留言板
- 添加社交媒体链接
- 等等...

---

## 常见问题解答

### Q: 我的网页访问显示 404 Not Found，怎么办？

**A:** 请检查以下几点：
1. 仓库名称是否正确？必须是 `你的用户名.github.io`
2. 是否已经开启了 GitHub Pages 服务？
3. 是否有 `index.html` 文件？
4. 等待 5-10 分钟再试，有时候部署需要时间
5. 检查浏览器是否需要清除缓存（按 Ctrl+F5 强制刷新）

### Q: 网页更新后，为什么看到的还是旧内容？

**A:** 这是浏览器缓存的问题，尝试：
1. 按 `Ctrl + F5` 强制刷新页面
2. 或者清除浏览器缓存后再访问
3. 等待几分钟让 GitHub Pages 重新部署

### Q: 可以绑定自己的域名吗？

**A:** 可以！在 GitHub Pages 设置页面可以添加自定义域名。你需要：
1. 拥有一个域名
2. 在域名 DNS 解析中添加 CNAME 记录指向 `你的用户名.github.io`
3. 在 GitHub Pages 设置中填写你的域名

### Q: GitHub Pages 支持动态网页吗（比如 PHP、Python）？

**A:** 不支持。GitHub Pages 只支持静态网页（HTML、CSS、JavaScript）。

### Q: 仓库必须公开吗？

**A:** 是的，GitHub Pages 要求仓库必须是公开的。

### Q: 可以删除网页重新开始吗？

**A:** 可以！你可以：
1. 删除仓库中的所有文件，重新上传
2. 或者直接删除仓库，重新创建一个

### Q: 还有其他问题怎么办？

**A:** 
1. 查看 [GitHub Pages 官方文档](https://docs.github.com/cn/pages)
2. 询问老师和同学
3. 在网上搜索相关问题

---

## 🎉 恭喜你！

你已经成功创建了自己的个人网页！继续探索，让它变得更酷吧！

有任何问题，随时查看本教程或寻求帮助。祝你玩得开心！✨

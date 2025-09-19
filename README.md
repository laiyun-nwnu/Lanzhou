# 兰州地名学习网站

这是一个用于国际中文教学的兰州地名学习网站，包含交互式地名网络图和汉字学习功能。

## 项目结构

```
.
├── index.html          # 主页 - 地名网络展示
├── place.html          # 地名详情页
├── character.html     # 汉字学习页
├── static/            # 静态资源
│   ├── place_data.json              # 地名数据
│   ├── place_network_top100.json    # 地名网络数据
│   └── character_detail.json        # 汉字详情数据
├── templates/         # 模板和音频文件
│   └── fayindata/
│       └── *.mp3      # 汉字发音音频
└── README.md         # 项目说明
```

## GitHub Pages 部署指南

### 第一步：创建GitHub仓库
1. 登录GitHub账号
2. 点击右上角"+" → "New repository"
3. 输入仓库名称（如：lanzhou-place-names）
4. 选择公开(Public)
5. 点击"Create repository"

### 第二步：上传文件到GitHub
1. 在本地打开终端，进入项目目录：
   ```bash
   # 直接导航到项目目录
   cd /Users/laiyun/codebuddy/Lanzhou
   
   # 确认已进入正确目录（应该看到index.html等文件）
   ls
   ```

2. 初始化Git仓库：
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Lanzhou place names website"
   ```

3. 连接到GitHub仓库：
   ```bash
   git remote add origin https://github.com/你的用户名/仓库名.git
   git branch -M main
   git push -u origin main
   ```

   如果遇到权限问题，可能需要配置Git：
   ```bash
   # 设置用户名和邮箱（只需要第一次使用Git时配置）
   git config --global user.name "你的名字"
   git config --global user.email "你的邮箱"
   
   # 如果push时要求登录，可以使用个人访问令牌
   # 或者在GitHub设置中启用SSH密钥
   ```

   如果遇到Git命令问题，可以尝试以下替代方案：

   **方案一：使用GitHub Desktop（图形界面）**
   1. 下载安装 GitHub Desktop
   2. 拖拽当前项目文件夹（/Users/laiyun/codebuddy/Lanzhou）到GitHub Desktop
   3. 点击"Publish repository"

   **方案二：使用网页上传**
   1. 在GitHub仓库页面点击"Add file" → "Upload files"
   2. 拖拽所有文件到网页界面
   3. 点击"Commit changes"

   **方案三：使用Homebrew安装新版Git**
   ```bash
   # 安装Homebrew（如果尚未安装）
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   
   # 安装新版Git
   brew install git
   ```

### 第三步：启用GitHub Pages
**重要：GitHub仓库必须设置为公开（Public）才能使用GitHub Pages**

1. 进入GitHub仓库页面
2. 点击"Settings" → "Pages"
3. 在"Build and deployment"部分：
   - Source: 选择"Deploy from a branch"
   - Branch: 选择"main"分支和"/ (root)"文件夹
4. 点击"Save"

如果看不到Pages选项，请检查：
- 仓库是否为公开（Public）状态
- 如果使用免费账户，私有仓库无法使用GitHub Pages
- 考虑升级到GitHub Pro或使用其他部署平台

### 第四步：访问网站
等待几分钟后，您的网站将在以下地址可用：
```
https://你的用户名.github.io/仓库名/
```

**重要：URL格式说明**
- 正确格式：`https://用户名.github.io/仓库名/`
- 错误格式：`https://用户名.github.io/仓库名/子文件夹/`

如果您的仓库名为 `Lanzhou`，正确地址应为：
```
https://laiyun-nwnu.github.io/Lanzhou/
```

如果仍然遇到404错误，请检查：
1. 仓库是否为公开（Public）状态
2. GitHub Pages是否已成功启用
3. 等待几分钟让GitHub完成部署

## 功能特点

- 🗺️ 交互式地名网络图可视化
- 📍 地名详情页面展示
- 🔤 HSK分级汉字学习
- 🔊 汉字发音音频支持
- 📱 响应式设计，支持移动设备

## 技术栈

- HTML5 + CSS3
- Bootstrap 5 响应式框架
- ECharts 数据可视化
- JavaScript ES6+

## 本地开发

要在本地运行此网站，可以使用Python内置服务器：

```bash
# Python 3
python -m http.server 8000

# 或者使用PHP
php -S localhost:8000
```

然后在浏览器中访问 http://localhost:8000
# Hexo Theme Apple

<p align="center">
  <strong>一个受 Apple 设计语言启发的简洁优雅的 Hexo 主题</strong>
</p>

<p align="center">
  A clean and elegant Hexo theme inspired by Apple's design language
</p>

## ✨ 特性 Features

- 🎨 **Apple 风格设计** - 采用 Apple 官网的设计语言和美学
- 📱 **完全响应式** - 完美适配桌面、平板和手机设备
- 🎯 **卡片式布局** - 首页采用现代化的网格卡片布局
- ⚡ **性能优化** - 轻量级，快速加载
- 🌈 **优雅动画** - 流畅的过渡动画和交互效果
- 🎭 **毛玻璃效果** - 导航栏采用 Apple 标志性的磨砂玻璃效果
- 🔍 **SEO 友好** - 优化的 HTML 结构和语义化标签
- 🌐 **国际化支持** - 内置中英文语言包
- 📝 **优秀的阅读体验** - 精心调整的排版和字体

## 📦 安装 Installation

### 方法 1: Git Clone（推荐）

在您的 Hexo 站点目录下执行：

```bash
cd your-hexo-site
git clone https://github.com/yourusername/hexo-theme-apple.git themes/apple
```

### 方法 2: 下载压缩包

1. 从 [Releases](https://github.com/yourusername/hexo-theme-apple/releases) 下载最新版本
2. 解压到 `themes/apple` 目录

## ⚙️ 配置 Configuration

### 1. 启用主题

编辑站点根目录的 `_config.yml`：

```yaml
theme: apple
```

### 2. 创建主题配置文件

Hexo 5.0+ 支持独立的主题配置文件：

```bash
cp themes/apple/_config.yml _config.apple.yml
```

### 3. 配置导航菜单

编辑 `_config.apple.yml`：

```yaml
menu:
  Home: /
  Archives: /archives
  About: /about
  Categories: /categories
  Tags: /tags
```

### 4. 清理缓存并启动

```bash
hexo clean
hexo server
```

访问 `http://localhost:4000` 查看效果！

## 🎨 主题配置 Theme Settings

### 导航菜单

```yaml
menu:
  Home: /
  Archives: /archives
  About: /about
  Categories: /categories
  Tags: /tags
```

### 社交链接

```yaml
social:
  GitHub: https://github.com/yourusername
  Twitter: https://twitter.com/yourusername
  Email: mailto:your@email.com
```

### 文章设置

```yaml
post:
  show_meta: true        # 显示文章元信息
  show_tags: true        # 显示标签
  show_categories: true  # 显示分类
  show_updated: false    # 显示更新时间
```

### 外观设置

```yaml
appearance:
  dark_mode: false      # 暗黑模式（计划中）
  back_to_top: true     # 返回顶部按钮
```

### 归档设置

```yaml
archive:
  posts_per_page: 20    # 每页文章数
```

## 🛠️ 开发 Development

### 文件结构

```
hexo-theme-apple/
├── layout/              # 模板文件
│   ├── layout.ejs      # 主布局（头部、底部）
│   ├── index.ejs       # 首页（卡片网格）
│   ├── post.ejs        # 文章详情页
│   ├── page.ejs        # 独立页面
│   └── archive.ejs     # 归档页
├── source/             # 静态资源
│   ├── css/
│   │   └── style.css   # 主样式表
│   └── js/
│       └── script.js   # 主脚本
├── languages/          # 国际化
│   ├── en.yml         # 英文
│   └── zh-CN.yml      # 简体中文
├── scripts/            # Hexo 脚本
├── _config.yml        # 主题配置
├── package.json       # NPM 包信息
└── README.md          # 说明文档
```

### 自定义样式

主题使用 CSS 变量，方便自定义颜色：

```css
:root {
    --primary-color: #0071e3;      /* 主色调 */
    --text-color: #1d1d1f;         /* 文字颜色 */
    --secondary-text: #86868b;     /* 次要文字 */
    --background: #ffffff;         /* 背景色 */
    --card-background: #fbfbfd;    /* 卡片背景 */
}
```

编辑 `source/css/style.css` 修改这些变量即可改变主题颜色。

### 本地开发

1. 修改模板文件后需要重启 `hexo server`
2. 修改 CSS/JS 文件后刷新浏览器即可
3. 使用 `hexo clean` 清理缓存

### 主要特性说明

#### 卡片式布局
- 首页采用 CSS Grid 布局
- 响应式网格，自动适配不同屏幕
- 悬停动画效果

#### 磨砂玻璃效果
- 使用 `backdrop-filter` 实现
- 导航栏支持滚动时的模糊效果

#### 动画效果
- 卡片入场动画（fadeInUp）
- 顺序延迟动画
- 流畅的过渡效果

## 📸 预览 Preview

访问示例站点查看效果：[Demo](#)

主要页面：
- **首页**: 卡片式网格布局，展示文章列表
- **文章页**: 优雅的阅读体验，大标题，舒适的行距
- **归档页**: 按时间线组织的文章列表

## 🤝 贡献 Contributing

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📝 待办事项 TODO

- [ ] 深色模式支持
- [ ] 文章封面图片支持
- [ ] 搜索功能
- [ ] 评论系统集成
- [ ] 更多配色方案
- [ ] 目录（TOC）支持

## 📄 许可证 License

[MIT License](LICENSE)

版权所有 (c) 2026

## 💝 致谢 Credits

- 设计灵感来自 [Apple Inc.](https://www.apple.com)
- 基于 [Hexo](https://hexo.io) 博客框架
- 字体使用 Apple 的 SF Pro Display

## 📮 联系方式 Contact

如有问题或建议，欢迎：
- 提交 [Issue](https://github.com/yourusername/hexo-theme-apple/issues)
- 发送邮件至 your@email.com

---

<p align="center">
  如果这个主题对您有帮助，请给个 ⭐️ Star 支持一下！
</p>

<p align="center">
  Made with ❤️ by Your Name
</p>

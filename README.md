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
- 📅 **按月份分组** - 首页文章按月份分组，时间线清晰
- 🎯 **横向滚动布局** - 每月文章横向滚动展示，现代化交互
- 🖱️ **智能自动滚动** - 鼠标移至边缘自动滚动，流畅体验
- ⚡ **性能优化** - 轻量级，快速加载
- 🌈 **优雅动画** - 流畅的过渡动画和交互效果
- 🎭 **毛玻璃效果** - 导航栏采用 Apple 标志性的磨砂玻璃效果
- 🎛️ **高度可定制** - CSS 变量控制所有视觉参数
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

主题使用 CSS 变量，方便自定义颜色和布局参数。编辑 `source/css/style.css` 中的 `:root` 部分：

#### 颜色变量

```css
:root {
    --primary-color: #0071e3;      /* 主色调（链接、按钮等） */
    --text-color: #1d1d1f;         /* 主要文字颜色 */
    --secondary-text: #86868b;     /* 次要文字颜色（日期、摘要等） */
    --background: #ffffff;         /* 页面背景色 */
    --card-background: #fbfbfd;    /* 卡片背景色 */
    --border-color: #d2d2d7;       /* 边框颜色 */
}
```

#### 卡片尺寸参数（v2.1 新增）

```css
/* 卡片尺寸参数 - 可自定义 */
--card-width: 280px;           /* 卡片宽度 */
--card-height: auto;            /* 卡片高度（auto 为自动） */
--card-padding: 2.5rem 2rem;    /* 卡片内边距（上下 左右） */
--card-gap: 2.5rem;             /* 卡片之间的间距 */
--card-border-radius: 28px;     /* 卡片圆角大小 */
```

#### 悬停效果参数（v2.1 新增）

```css
/* 悬停效果参数 - 可自定义 */
--card-hover-lift: -8px;        /* 悬停时上浮距离（负值向上，正值向下） */
--card-hover-scale: 1.02;       /* 悬停时缩放比例（1.0 = 不缩放） */
```

#### 自定义示例

想要更大的卡片和更明显的悬停效果？

```css
:root {
    --card-width: 350px;           /* 更宽的卡片 */
    --card-hover-lift: -12px;      /* 更高的上浮 */
    --card-hover-scale: 1.05;      /* 更明显的放大 */
    --card-border-radius: 32px;    /* 更圆润的边角 */
}
```

想要紧凑的布局？

```css
:root {
    --card-width: 240px;           /* 更窄的卡片 */
    --card-gap: 1.5rem;            /* 更小的间距 */
    --card-padding: 2rem 1.5rem;   /* 更小的内边距 */
}
```

### 本地开发

1. 修改模板文件后需要重启 `hexo server`
2. 修改 CSS/JS 文件后刷新浏览器即可
3. 使用 `hexo clean` 清理缓存

### 主要特性说明

#### 按月份分组的横向滚动布局（v2.1）
- 首页文章按月份自动分组（如"2024年02月"）
- 每个月份的文章在独立的横向滚动容器中
- 支持鼠标拖动、滚轮滚动
- 智能边缘检测：鼠标移至右侧 80px 区域自动向右滚动
- 流畅的 scroll-snap 对齐效果
- 移动端完美适配，触摸滑动流畅

#### 卡片式布局
- 使用 Flexbox 实现横向滚动
- 响应式设计，自动适配不同屏幕
- 增强的悬停动画效果（上浮 + 缩放 + 阴影）
- 所有参数可通过 CSS 变量自定义

#### 磨砂玻璃效果
- 使用 `backdrop-filter` 实现
- 导航栏支持滚动时的模糊效果

#### 动画效果
- 卡片入场动画（fadeInUp）
- 顺序延迟动画
- 流畅的过渡效果
- 使用 `requestAnimationFrame` 实现的自动滚动

## 📸 预览 Preview

访问示例站点查看效果：[Demo](#)

主要页面：
- **首页**: 按月份分组的横向滚动布局，时间线清晰
- **文章页**: 优雅的阅读体验，大标题，舒适的行距
- **归档页**: 按时间线组织的文章列表

### 首页特性
- 文章按月份自动分组
- 每月文章横向滚动展示
- 鼠标移至边缘自动滚动
- 悬停卡片时上浮并放大
- 移动端触摸滑动流畅

## 🔄 更新日志 Changelog

### v2.1.0 (2026-02-08)
- ✨ 新增按月份分组的横向滚动布局
- ✨ 新增智能边缘自动滚动功能
- ✨ 新增 CSS 变量控制卡片尺寸和悬停效果
- 🎨 增强卡片悬停动画（上浮 + 缩放）
- 🎨 优化阴影效果，更有层次感
- 📱 改进移动端横向滚动体验
- 📝 完善文档，添加自定义参数说明

### v2.0.0 (2026-02-08)
- 🎨 优化圆角设计，提升视觉美感
- 增加卡片圆角至 28px
- 更新各组件圆角，整体更加柔和

### v1.0.0 (2026-02-08)
- 🎉 首次发布
- Apple 风格设计
- 响应式布局
- 卡片式首页

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

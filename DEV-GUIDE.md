# Hexo Theme Apple - 开发指南

## 快速开始

### 1. 在 Hexo 站点中使用此主题

将此主题复制到你的 Hexo 站点的 `themes/` 目录下：

```bash
cd your-hexo-site/themes
git clone [your-repo-url] apple
```

然后在站点的 `_config.yml` 中设置：

```yaml
theme: apple
```

### 2. 本地开发

在主题目录下工作时，你可以：

#### 实时预览

在 Hexo 站点根目录运行：

```bash
hexo clean
hexo server
```

访问 `http://localhost:4000` 预览主题效果。

#### 修改样式

编辑 `source/css/style.css` 文件，保存后刷新浏览器即可看到效果。

#### 修改模板

编辑 `layout/` 目录下的 `.ejs` 文件，需要重启 hexo server 才能看到效果。

### 3. 主题配置

复制主题的 `_config.yml` 到 Hexo 站点根目录并重命名为 `_config.apple.yml`：

```bash
cp themes/apple/_config.yml _config.apple.yml
```

然后编辑 `_config.apple.yml` 进行自定义配置。

### 4. 测试内容

创建一些测试文章：

```bash
hexo new post "Test Post 1"
hexo new post "Test Post 2"
hexo new page "about"
```

### 5. 版本控制

建议使用 Git 管理主题开发：

```bash
git init
git add .
git commit -m "Initial theme setup"
```

### 6. 自动化工作流

你可以创建一个简单的脚本来自动化开发流程：

**Windows (dev.bat):**
```batch
@echo off
hexo clean
hexo generate
hexo server
```

**Linux/Mac (dev.sh):**
```bash
#!/bin/bash
hexo clean
hexo generate
hexo server
```

## 目录结构说明

```
hexo-theme-apple/
├── layout/              # 模板文件
│   ├── layout.ejs      # 主布局（包含 header、footer）
│   ├── index.ejs       # 首页模板
│   ├── post.ejs        # 文章页模板
│   ├── page.ejs        # 独立页面模板
│   └── archive.ejs     # 归档页模板
├── source/             # 静态资源
│   ├── css/           # 样式文件
│   │   └── style.css  # 主样式表
│   └── js/            # JavaScript 文件
│       └── script.js  # 主脚本
├── languages/          # 国际化语言文件
├── scripts/            # Hexo 脚本
├── _config.yml        # 主题配置文件
├── package.json       # NPM 包配置
└── README.md          # 说明文档
```

## 开发技巧

### 1. 实时刷新

使用 `hexo server` 时，CSS 和 JS 文件的修改会实时生效，但模板文件（.ejs）的修改需要重启服务器。

### 2. 调试模板

在模板中使用以下代码输出调试信息：

```ejs
<%- JSON.stringify(page, null, 2) %>
```

### 3. 样式开发

主题使用 CSS 变量，你可以在 `style.css` 的 `:root` 中修改颜色方案：

```css
:root {
    --primary-color: #007aff;
    --text-color: #1d1d1f;
    /* ... */
}
```

### 4. 添加新页面模板

1. 在 `layout/` 目录创建新的 `.ejs` 文件
2. 使用时在 Front-matter 中指定：

```yaml
---
title: My Page
layout: your-template-name
---
```

## 发布前检查清单

- [ ] 测试所有页面类型（首页、文章、归档、独立页面）
- [ ] 检查响应式布局（手机、平板、桌面）
- [ ] 验证导航链接
- [ ] 测试分页功能
- [ ] 检查代码高亮
- [ ] 验证图片显示
- [ ] 测试社交链接
- [ ] 更新 README.md
- [ ] 更新 package.json 版本号
- [ ] 创建 Git tag

## 常见问题

### 样式不生效

1. 运行 `hexo clean` 清除缓存
2. 检查 CSS 文件路径
3. 确认浏览器已刷新

### 模板修改不生效

1. 重启 `hexo server`
2. 清除缓存：`hexo clean`
3. 检查模板语法错误

### 需要更多帮助？

参考 Hexo 官方文档：https://hexo.io/zh-cn/docs/

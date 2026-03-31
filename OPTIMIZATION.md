# Hexo Theme Apple - 优化日志

## 优化日期
2026-03-31

## 优化内容

### 1. 配置文件优化 (_config.yml)

#### 导航菜单
- ✅ 添加 Categories 和 Tags 页面
- ✅ 注释掉 About 页面（可选）

#### 社交链接
- ✅ 配置 GitHub: https://github.com/yeae
- ✅ 预留 Twitter、Email、知乎、微博等链接

#### 外观设置
- ✅ 启用深色模式（dark_mode: true）
- ✅ 启用返回顶部按钮
- ✅ 添加平滑滚动动画

#### 文章设置
- ✅ 显示元信息、标签、分类
- ✅ 显示版权信息
- ✅ 显示目录（TOC）
- ✅ 启用代码复制和高亮

#### 归档设置
- ✅ 每页显示 15 篇文章
- ✅ 启用年/月归档

#### SEO 设置
- ✅ 自动摘要长度增加到 200 字符
- ✅ 预留 RSS 和搜索配置

### 2. CSS 样式优化 (source/css/style.css)

#### 新增功能
- ✅ **深色模式支持** - 自动根据系统偏好切换
- ✅ **改进的颜色变量** - 添加三级文本颜色
- ✅ **优化的字体系列** - 添加 SF Pro Text 和 SF Mono
- ✅ **平滑过渡动画** - 添加 smooth 过渡效果

#### 深色模式配色
```css
@media (prefers-color-scheme: dark) {
    --primary-color: #2997ff;
    --text-color: #f5f5f7;
    --background: #000000;
    --card-background: #1c1c1e;
    /* ... */
}
```

#### 新增样式组件
- ✅ 返回顶部按钮样式
- ✅ 表格样式优化
- ✅ 引用块样式
- ✅ 搜索框样式
- ✅ 分类/标签页面样式
- ✅ 加载动画
- ✅ 打印样式优化

#### 设计改进
- ✅ 统一的圆角和阴影
- ✅ 改进的悬停效果
- ✅ 更好的响应式布局
- ✅ 优化的动画延迟

### 3. JavaScript 功能 (source/js/script.js)

现有功能：
- ✅ 平滑滚动
- ✅ 懒加载支持
- ✅ 返回顶部按钮
- ✅ 横向滚动自动滚动（鼠标悬停）
- ✅ 加载动画

## 使用方法

### 1. 启用主题

在 Hexo 站点根目录的 `_config.yml` 中：

```yaml
theme: apple
```

### 2. 复制配置（可选）

```bash
cp /mnt/d/ml/hexo-theme-apple/_config.yml ./_config.apple.yml
```

### 3. 清理并启动

```bash
hexo clean
hexo generate
hexo server
```

## 效果预览

访问：http://localhost:4000

## 自定义建议

### 修改配色
编辑 `source/css/style.css` 中的 `:root` 变量

### 修改布局
编辑 `layout/` 目录下的 EJS 模板文件

### 添加功能
在 `scripts/` 目录添加 Hexo 插件脚本

## 性能优化建议

1. **启用缓存** - 使用 hexo-generator-cache
2. **图片优化** - 使用 webp 格式
3. **CDN 加速** - 使用 jsdelivr 或 unpkg
4. **压缩资源** - 使用 hexo-neat

## 兼容性

- ✅ 现代浏览器（Chrome、Firefox、Safari、Edge）
- ✅ 移动端（iOS Safari、Chrome Mobile）
- ✅ 深色模式（macOS、iOS、Windows）
- ✅ 无障碍访问（WCAG 2.1）

---

**最后更新**: 2026-03-31

# Minimal Mistakes Jekyll 个人网站项目

## 项目概述

这是一个基于 **Minimal Mistakes** Jekyll 主题的个人网站项目。Minimal Mistakes 是一个灵活的双栏 Jekyll 主题，适合构建个人网站、博客和作品集。

## 技术栈

- **静态站点生成器**: Jekyll 4.4.1
- **主题**: Minimal Mistakes Jekyll
- **CSS预处理**: Sass/SCSS
- **Markdown解析**: Kramdown (GFM模式)
- **代码高亮**: Rouge
- **搜索**: Lunr.js (本地搜索)
- **JavaScript**: jQuery 3.6.0

## 目录结构

```
love02-master/
├── _config.yml          # 主配置文件 (站点设置、插件、默认值)
├── _data/               # 数据文件
│   ├── navigation.yml   # 导航菜单配置
│   └── ui-text.yml      # 多语言UI文本 (支持30+语言)
├── _includes/           # 可复用组件/片段
│   ├── analytics-providers/  # 分析工具集成
│   ├── comments-providers/   # 评论系统集成
│   ├── head/            # HTML head 相关组件
│   ├── footer/          # 页脚组件
│   ├── search/          # 搜索组件
│   ├── author-profile.html    # 作者简介
│   ├── masthead.html    # 顶部导航
│   ├── sidebar.html     # 侧边栏
│   ├── toc.html         # 目录
│   └── ...              # 其他组件
├── _layouts/            # 页面布局模板
│   ├── default.html     # 基础布局
│   ├── single.html      # 单页文章布局
│   ├── home.html        # 首页布局
│   ├── archive.html     # 归档页布局
│   ├── search.html      # 搜索页布局
│   ├── splash.html      # 启动页布局
│   └── ...              # 其他布局
├── _sass/               # Sass 样式源文件
│   └── minimal-mistakes/    # 主题样式模块
├── assets/              # 静态资源
│   ├── css/main.scss    # 主样式入口
│   ├── images/          # 图片资源
│   └── js/              # JavaScript文件
├── docs/                # 主题文档和示例
├── _site/               # 生成的静态站点 (构建输出)
├── Gemfile              # Ruby 依赖配置
└── index.html           # 首页入口

```

## 核心配置 (_config.yml)

### 站点设置
- `title`: 站点标题
- `name`: 作者名称
- `description`: 站点描述
- `locale`: 语言区域 (默认 en-US)
- `url` / `baseurl`: 站点URL配置

### 主题皮肤 (minimal_mistakes_skin)
可选值: `default`, `air`, `aqua`, `contrast`, `dark`, `dirt`, `neon`, `mint`, `plum`, `sunrise`, `catppuccin_latte`, `catppuccin_mocha`

### 评论系统 (comments.provider)
支持: Disqus, Discourse, Facebook, Staticman, utterances, giscus

### 搜索 (search_provider)
支持: lunr (本地), algolia, google

### 插件 (plugins)
- `jekyll-paginate` - 分页
- `jekyll-sitemap` - 站点地图
- `jekyll-gist` - GitHub Gist 嵌入
- `jekyll-feed` - RSS 订阅
- `jekyll-include-cache` - 缓存包含文件 (**必须保留**)

## 重要约束

### 必须遵守的规则

1. **jekyll-include-cache 插件必须保留**
   - 必须在 `Gemfile` 中保留 `gem "jekyll-include-cache"`
   - 必须在 `_config.yml` 的 `plugins` 数组中保留 `- jekyll-include-cache`
   - 否则构建时会报错: `Unknown tag 'include_cached'`

2. **Gemfile 使用国内镜像**
   - source 已配置为 `https://gems.ruby-china.com/`

3. **修改配置后需重启服务**
   - `_config.yml` 修改后需要重启 `jekyll serve`

## 常用命令

```bash
# 安装依赖
bundle install

# 本地预览 (默认 http://127.0.0.1:4000)
bundle exec jekyll serve

# 增量构建 (更快)
bundle exec jekyll serve --incremental

# 构建生产版本
JEKYLL_ENV=production bundle exec jekyll build
```

## 自定义指南

### 添加文章
在 `_posts/` 目录创建文件，格式: `YYYY-MM-DD-title.md`

```yaml
---
layout: single
title: "文章标题"
categories: [分类]
tags: [标签1, 标签2]
---
```

### 修改导航
编辑 `_data/navigation.yml`:

```yaml
main:
  - title: "导航名称"
    url: /path/
```

### 修改作者信息
编辑 `_config.yml` 中的 `author` 部分。

### 更换皮肤
修改 `_config.yml` 中的 `minimal_mistakes_skin` 值。

## 多语言支持

主题内置 30+ 语言支持，UI 文本在 `_data/ui-text.yml` 中定义。
修改 `locale` 配置切换语言 (如 `zh-CN` 为简体中文)。

## SEO 优化

- 自动生成 Open Graph 和 Twitter Card 标签
- 支持结构化数据 (JSON-LD)
- 可配置 Google/Bing/Baidu 站点验证
- 支持 Google Analytics

## 许可证

MIT License - 主题作者 Michael Rose

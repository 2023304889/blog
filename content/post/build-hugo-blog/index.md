---
title: "用 Hugo 搭建个人博客的完整步骤"
slug: "build-hugo-blog"
description: "从零开始，用 Hugo + Stack 主题搭建一个现代卡片式个人技术博客。"
date: 2026-10-15
tags: ["Hugo", "博客", "教程"]
categories: ["编程实践"]
comments: true
draft: false
---

## 什么是 Hugo

[Hugo](https://gohugo.io) 是一个用 Go 编写的静态站点生成器，以**构建速度快**、**安装简单**、**原生支持 Markdown** 而著称。非常适合个人博客、技术文档、作品集等场景。

## 搭建步骤

### 1. 安装 Hugo

下载对应系统的 Hugo 二进制（推荐 extended 版本），解压即可使用：

```bash
hugo version
```

### 2. 创建站点

```bash
hugo new site blog
```

### 3. 安装主题

以卡片式风格的 [Stack](https://github.com/CaiJimmy/hugo-theme-stack) 主题为例，把主题放到 `themes/hugo-theme-stack` 目录。

### 4. 编写配置

在 `hugo.toml` 中指定主题、标题、菜单等参数。

### 5. 写文章

```bash
hugo new post/我的第一篇文章/index.md
```

### 6. 本地预览与构建

```bash
# 本地预览（含草稿）
hugo server -D

# 构建静态文件到 public/
hugo
```

构建后，把 `public/` 目录部署到 GitHub Pages、Vercel、Netlify 或自己的服务器即可上线。

## 常用命令速查

| 命令 | 说明 |
| --- | --- |
| `hugo server -D` | 本地实时预览（含草稿） |
| `hugo` | 构建站点到 `public/` |
| `hugo new post/xxx/index.md` | 新建文章 |
| `hugo --minify` | 构建并压缩产物 |

## 小结

Hugo 上手简单、速度极快，配合 Stack 这样的成熟主题，几分钟就能搭建出一个美观的个人博客。希望这篇教程对你有帮助。

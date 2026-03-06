---
title: Hugo 快速入门指南
date: 2024-03-04
description: 学习如何使用 Hugo 和 Stack 主题快速搭建个人博客。
categories:
  - 技术
tags:
  - Hugo
  - 博客
  - 教程
image: "/images/posts/hugo-quickstart-cover.jpg"
---

# Hugo 快速入门指南

Hugo 是一个用 Go 语言编写的静态网站生成器，以其极快的构建速度而闻名。本文将介绍如何使用 Hugo 和 Stack 主���快速搭建个人博客。

## 为什么选择 Hugo？

- **速度快**：构建速度以毫秒计，即使有数千篇文章也能瞬间完成
- **易于使用**：简单的命令行界面，易于学习
- **灵活强大**：支持自定义主题和插件
- **SEO 友好**：生成的是纯静态 HTML，对搜索引擎友好
- **免费部署**：可以免费部署到 GitHub Pages

## 安装 Hugo

### Windows

最简单的方式是使用 Chocolatey：

```powershell
choco install hugo-extended
```

或者从 [GitHub Releases](https://github.com/gohugoio/hugo/releases) 下载二进制文件。

### macOS

使用 Homebrew：

```bash
brew install hugo
```

### Linux

使用包管理器或从源代码编译。

## 创建新站点

```bash
hugo new site my-blog
cd my-blog
```

## 安装主题

以 Stack 主题为例：

```bash
git init
git submodule add https://github.com/CaiJimmy/hugo-theme-stack.git themes/stack
```

## 配置站点

编辑 `hugo.toml`：

```toml
baseURL = "https://yourusername.github.io/my-blog/"
languageCode = "zh-cn"
title = "My Blog"
theme = "stack"
paginate = 10
```

## 创建文章

```bash
hugo new posts/my-first-post.md
```

然后编辑生成的 Markdown 文件。

## 本地预览

```bash
hugo server -D
```

然后在浏览器中访问 `http://localhost:1313`。

## 构建站点

```bash
hugo
```

生成的静态文件会在 `public` 目录中。

## 部署到 GitHub Pages

1. 创建一个 GitHub 仓库，命名为 `yourusername.github.io`
2. 将 `public` 目录的内容推送到仓库
3. 启用 GitHub Pages

## 总结

Hugo 是一个强大而易用的静态网站生成器，非常适合搭建个人博客。结合 Stack 主题，你可以快速拥有一个美观、功能完整的博客。

祝你使用愉快！

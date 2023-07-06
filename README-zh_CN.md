# JuiceBar
[English](https://github.com/hotjuicew/hugo-juicebar/tree/master/README.md) | 简体中文

JuiceBar 是一个简洁、优雅的博客主题，由 [Hugo](https://gohugo.io) 强力驱动。

这个主题从 PapermMod 和 LoveIt 获得了很多灵感，感谢！

⭐Demo → [juicebar-demo.add1.dev](https://juicebar-demo.add1.dev)

---
## 预览
![](https://github.com/hotjuicew/hugo-JuiceBar/blob/master/images/screenshot.png)
## 特点

- 主题：根据您的系统偏好或用户选择，**黑/白主题**。
- 通过 Hugo 工具轻松修改主题
- 完全响应式
- 支持社交图标
- 一些美丽的 CSS 动画
- 易于使用的自扩展目录toc
- 自动突出显示代码
- 自定义脚本短代码
- 支持 [giscus](https://giscus.app/) 评论系统

## 如何开始

您可以将主题安装为克隆或子模块。

我建议使用后者。从您的 Hugo 站点根目录开始，键入以下内容：

```
$ git submodule add https://github.com/hotjuicew/hugo-JuiceBar.git themes/JuiceBar
```

现在，您可以通过更新子模块来获取以后对 hugo-JuiceBar 的更新：

```
$ git submodule update --remote themes/JuiceBar
```

## 如何配置

该主题不需要任何高级配置。只需复制以下配置文件。
`config.toml`
```toml
baseURL = 'http://example.org/' 
languageCode = 'en-us'
theme = "JuiceBar"
title = "your_blog_title"

[params]
author = "your_name"
description = "My site description"
authorImage = "/images/profile.jpg"
paginate = 5 
Title = "your_blog_title"
content = "I'm JuiceBar, nice to meet you(ˊ˘ˋ*)♡"
imageUrl = "/images/avatar.jpg"

# 添加新的社交图标
# 更多社交图标可以在JuiceBar\layouts\partials\svg.html中找到
[[params.social]]
name = "Github"
url = "https://github.com/hotjuicew"
[[params.social]]
name = "telegram"
url = "https://t.me/Hotjuice"
[[params.social]]
name = "twitter"
url = "https://twitter.com/hotjuicee"
[[params.social]]
name = "email"
url = "mailto:hotjuicew@outlook.com"
[[params.social]]
name = "instagram"
url = "your_url"
[[params.social]]
name = "mastodon"
url = "your_url"
[[params.social]]
name = "reddit"
url = "your_url"
[[params.social]]
name = "stackoverflow"
url = "your_url"

[taxonomies]
category = "categories"
tag = "tags"

# 添加新的导航链接
[[menu.main]]
name = "About"
url = "/about"
[[menu.main]]
name = "Blog"
url = "/post"
[[menu.main]]
name = "Categories"
url = "/categories"

# 如果使用giscus评论系统
#[params.giscus]
#repo = "ENTER REPO HERE"
#repoID = "ENTER REPO ID HERE"
#category = "ENTER CATEGORY NAME HERE"
#categoryID = "ENTER CATEGORY ID HERE"
#mapping = "og:title"
#reactionsEnabled = "1"
#emitMetadata = "0"
#inputPosition = "bottom"
#lang = "en"
#loading = "lazy"

#用于输出文档的设置（必须的）
[outputs]
home = ["HTML", "RSS", "JSON"]
```


注意：还有更多的配置选项。查看`exampleSite`中的`config.toml`。

安装后，请查看`themes/hugo-JuiceBar`内部的`exampleSite`文件夹。

要开始使用，请将`exampleSite`中的`config.toml`文件复制到 Hugo 网站的根目录：

```
$ cp themes/hugo-JuiceBar/exampleSite/config.toml。
```

现在编辑此文件并添加您自己的信息。请注意，有些字段可以省略。

我建议您使用主题的原型，因此现在删除您站点的`archetypes/default.md`。

最后，只需运行 `$ hugo new content/about.md` 创建你的 '关于' 页面，以及 `$ hugo new content/post/title.md` 创建你的第一篇博客文章。

---
title: "Hugo的文章头部参数"
date: 2025-05-26T16:04:18+08:00
lastmod: 2025-05-26T16:04:18+08:00
draft: true
keywords: []
description: ""
tags: []
categories: [hugo相关]
author: ""

# Uncomment to pin article to front page
# weight: 1
# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: false
autoCollapseToc: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: false

# Uncomment to add to the homepage's dropdown menu; weight = order of article
# menu:
#   main:
#     parent: "docs"
#     weight: 1
---

<!--more-->

Hugo 文章头部参数（Front Matter）说明表格：

| 参数名        | 含义说明                                             |
| ------------- | ---------------------------------------------------- |
| `title`       | 文章标题，在页面中显示为主标题。                     |
| `date`        | 创建日期，用于排序或显示发布时间（格式为 ISO8601）。 |
| `lastmod`     | 最后修改时间，用于显示文章更新日期。                 |
| `draft`       | 是否为草稿（`true` 表示草稿，发布时不会生成）。      |
| `keywords`    | 页面关键词，通常用于 SEO 优化（数组形式）。          |
| `description` | 页面描述，用于 SEO 元标签和摘要信息。                |
| `tags`        | 标签，用于分类文章主题，支持多个标签。               |
| `categories`  | 分类，可用于更高层次的内容组织。                     |
| `author`      | 作者名，通常显示在文章中或用于元信息。               |



| 可选设置           | 含义说明                                         |
| ------------------ | ------------------------------------------------ |
| `weight`           | 权重，数值越小越靠前；可以用来将文章置顶或排序。 |
| `comment`          | 是否开启评论功能（`false` 表示关闭）。           |
| `toc`              | 是否显示目录（Table of Contents）。              |
| `autoCollapseToc`  | 是否自动折叠目录（适用于多级目录）。             |
| `contentCopyright` | 是否使用自定义版权信息（可以为字符串或布尔值）。 |
| `reward`           | 是否启用打赏功能（一般用于博客）。               |
| `mathjax`          | 是否启用 MathJax（用于渲染数学公式）。           |



| 菜单相关（注释状态） | 含义说明                                     |
| -------------------- | -------------------------------------------- |
| `menu`               | 将文章加入 Hugo 的菜单系统，例如主页导航栏。 |
| `parent`             | 菜单中的父项名称（如果是子菜单）。           |
| `weight`（菜单）     | 菜单排序权重，数字越小越靠前。               |



如果你想让文章发布，记得将 `draft: true` 改为 `draft: false`。是否显示目录和评论也取决于你主题的支持情况。需要我帮你配置自动目录或 SEO 吗？



##### You said:

tags，categories都是用于分类吗？有什么不同？



###### ChatGPT said:

是的，`tags` 和 `categories` 都是用于对内容进行分类，但它们的**用途和层次**有所不同：

| 项目       | `tags`（标签）                 | `categories`（分类）             |
| ---------- | ------------------------------ | -------------------------------- |
| 中文含义   | 标签                           | 分类                             |
| 用途定位   | 细粒度的主题或关键词标记       | 粗粒度的主题分组                 |
| 数量       | 一个文章可有多个标签           | 通常建议一个或少数几个分类       |
| 是否可重复 | 可高度复用（如“AI”、“工具”）   | 一般用来表达文章归属的主要板块   |
| 结构层级   | 无层级结构（扁平）             | 可呈现层级结构（父分类-子分类）  |
| 用例       | 描述文章的具体内容或关键词     | 表示文章所属的主要栏目           |
| 页面作用   | 用于生成关键词聚合页，方便搜索 | 用于构建站点结构、导航或分类列表 |



### 举个例子：

你有一篇文章标题为《推荐10个建站AI工具》：

- `categories`:

  ```
  yaml
  
  
  CopyEdit
  categories: ["网站建设"]
  ```

  表示这篇文章属于“网站建设”这一主类。

- `tags`:

  ```
  yaml
  
  
  CopyEdit
  tags: ["AI工具", "建站", "效率工具"]
  ```

  表示这篇文章涉及“AI 工具”、“建站”、“效率工具”等关键词，方便用户在相关标签页中查找。

------

### 建议用法（类比博客网站）：

- `categories` 像网站的主栏目（比如：编程 / 设计 / AI / 摄影）
- `tags` 像文章的标签云（比如：Python / 生成式AI / SEO / UI）

如你的网站内容偏向技术文档、博客或内容聚合类，合理区分这两个可以提升 SEO 和用户体验。

如需我帮你设计分类和标签结构，也可以告诉我你的网站主题内容。

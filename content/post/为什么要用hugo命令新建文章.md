---
title: "为什么要用hugo命令新建文章"
date: 2025-05-26T16:16:08+08:00
lastmod: 2025-05-26T16:16:08+08:00
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

你**不一定非得用 `hugo` 命令**来新建文章，**直接手动新建 `.md` 文件也是可以的**，只要你放对了路径、写好了前置参数（front matter）。

不过用 `hugo new` 命令有以下几个好处：

------

### ✅ 用 `hugo new` 命令的优点：

```
bash


CopyEdit
hugo new posts/my-new-post.md
```

1. **自动生成 front matter（前置参数）**：包括 title、date、draft 等字段，格式规范。
2. **自动放到正确的路径**：比如 `content/posts/` 下。
3. **避免忘记扩展名或格式问题**。
4. **配合 archetypes 模板更强大**：可以自定义不同类型文章的默认 front matter。

------

### ✅ 手动创建 `.md` 文件的做法：

你也可以手动在 `content/posts/` 目录下新建：

```
bash


CopyEdit
content/posts/my-manual-post.md
```

然后写好 front matter，例如：

```
markdownCopyEdit---
title: "手动创建的文章"
date: 2025-05-25T10:00:00+08:00
draft: true
---
内容开始……
```

只要位置和格式正确，Hugo 照样能识别。

------

### 🔧 总结建议：

| 方式            | 是否可行 | 推荐程度 | 适合人群                   |
| --------------- | -------- | -------- | -------------------------- |
| `hugo new` 命令 | ✅        | ⭐⭐⭐⭐     | 初学者、追求规范的写作流程 |
| 手动新建 `.md`  | ✅        | ⭐⭐⭐      | 熟悉 Hugo 文件结构的用户   |



------

需要我帮你写一个适合你博客的 `archetypes` 模板吗？可以让你每次 `hugo new` 自动带上你常用的 front matter。



##### You said:

hugo server 与 hugo server -D这两个命令有什么区别？



###### ChatGPT said:

这两个命令的区别在于是否**包含草稿（draft）文章**：

------

### ✅ `hugo server`

- **默认不包含草稿（draft: true）的文章**。
- 只会生成并预览那些 `draft: false` 或没有 `draft` 字段的文章。
- 适合用于发布前的最终预览。

------

### ✅ `hugo server -D`

- `-D` 是 `--buildDrafts` 的简写。
- **会包含所有设置了 `draft: true` 的草稿文章**。
- 适合开发、写作过程中的预览，即使文章还没正式发布。

------

### 📝 示例

假设你有这样一篇文章：

```
markdownCopyEdit---
title: "我的草稿文章"
date: 2025-05-25
draft: true
---
还在写的内容……
```

- `hugo server`：不会在页面中显示这篇文章。
- `hugo server -D`：会在页面中显示这篇文章。

------

### ✅ 实用建议：

| 命令             | 用途           | 是否显示草稿 |
| ---------------- | -------------- | ------------ |
| `hugo server`    | 最终发布前预览 | ❌ 不显示草稿 |
| `hugo server -D` | 开发写作时预览 | ✅ 显示草稿   |

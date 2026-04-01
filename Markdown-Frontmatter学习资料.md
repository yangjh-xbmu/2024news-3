# Markdown Frontmatter 5分钟入门指南

> Frontmatter 是 Markdown 文件顶部的元数据区块，用 `---` 包裹，让你的文档更智能、更有组织。

---

## 一、什么是 Frontmatter？（1分钟）

**Frontmatter**（前置元数据）位于 Markdown 文件的最顶部，用于存储文档的元信息，如标题、作者、日期、标签等。

它就像一本书的封面信息，告诉读者和管理系统：这篇文章是谁写的、什么时候写的、属于什么分类。

**常见应用场景：**
- 静态网站生成器（VitePress、VuePress、Jekyll、Hugo）
- 博客文章管理
- 笔记软件（Obsidian、Notion）
- 文档管理系统

---

## 二、基本语法（2分钟）

### 标准格式（YAML）

```markdown
---
title: 我的文章标题
author: 张三
date: 2024-01-15
tags: [markdown, 教程]
description: 这是一篇关于 Frontmatter 的入门教程
---

# 正文标题

这里是文章的正式内容...
```

### 语法规则

| 规则 | 说明 |
|------|------|
| 位置 | **必须**在文件最顶部，前面不能有任何内容 |
| 分隔符 | 使用三条短横线 `---` 作为开始和结束标记 |
| 格式 | 中间使用 YAML 语法（键值对） |
| 冒号后 | 必须有空格 `key: value` |

### 常用数据类型

```yaml
---
title: 字符串值          # 字符串
views: 100              # 数字
draft: false            # 布尔值（true/false）
tags: [a, b, c]         # 数组写法1
categories:             # 数组写法2
  - 技术
  - 教程
date: 2024-01-15        # 日期
---
```

---

## 三、实际应用示例（2分钟）

### 示例 1：博客文章

```markdown
---
title: "我的第一篇博客"
author: "张三"
date: 2024-01-20
categories: ["技术", "生活"]
tags: ["markdown", "入门"]
featured: true
reading_time: 5
---

# 我的第一篇博客

欢迎来到我的博客！
```

### 示例 2：VitePress 文档

```markdown
---
title: 配置指南
editLink: true
lastUpdated: true
layout: doc
sidebar: false
---

# 配置指南
```

### 示例 3：Obsidian 笔记

```markdown
---
title: 项目笔记
date: 2024-03-25
tags:
  - 工作
  - 项目A
aliases: [项目A笔记, 三月总结]
---

# 项目笔记
```

---

## 附：快速参考表

| 字段名 | 说明 | 示例 |
|--------|------|------|
| `title` | 文章标题 | `title: 我的文章` |
| `author` | 作者 | `author: 张三` |
| `date` | 日期 | `date: 2024-01-15` |
| `tags` | 标签数组 | `tags: [a, b]` 或 `- a` |
| `categories` | 分类 | `categories: 技术` |
| `draft` | 草稿标记 | `draft: false` |
| `description` | 描述 | `description: 简介...` |

**其他格式支持：**
- **TOML**：使用 `+++` 代替 `---`
- **JSON**：使用 `{ }` 包裹在花括号内

---

# 测试题

## 单选题（共5题）

### 第1题

Frontmatter 应该放在 Markdown 文件的什么位置？

A. 文件最底部
B. 文件最顶部
C. 正文中间任意位置
D. 标题之后

<details>
<summary>点击查看答案</summary>

**答案：B**

**解析：** Frontmatter 必须位于 Markdown 文件的最顶部，在任何其他内容之前，包括标题和正文。这是 Frontmatter 被正确识别的前提条件。

</details>

### 第2题

以下哪个是 Frontmatter 的标准分隔符？

A. `===`
B. `###`
C. `---`
D. `***`

<details>
<summary>点击查看答案</summary>

**答案：C**

**解析：** Frontmatter 使用三条短横线 `---` 作为开始和结束标记。这是最常用的 YAML 格式分隔符。

</details>

### 第3题

以下哪个是正确的 Frontmatter 语法？

A.
```yaml
---
title:我的文章
---
```

B.
```yaml
---
title: 我的文章
---
```

C.
```yaml
---
标题: 我的文章
---
```

D.
```yaml
title: 我的文章
```

<details>
<summary>点击查看答案</summary>

**答案：B**

**解析：** 正确的 Frontmatter 语法要求：1) 使用 `---` 作为开始和结束标记；2) 键名使用英文（如 `title` 而非 `标题`）；3) 冒号后面必须有一个空格。

</details>

### 第4题

以下哪个是合法的数组写法？

A. `tags: [markdown, tutorial]`
B. `tags: {markdown, tutorial}`
C. `tags: (markdown, tutorial)`
D. `tags: "markdown, tutorial"`

<details>
<summary>点击查看答案</summary>

**答案：A**

**解析：** 在 YAML 中，数组可以使用方括号 `[]` 表示，元素之间用逗号分隔。也可以使用 `-` 列表形式。方括号写法 `tags: [markdown, tutorial]` 是简洁的数组写法。

</details>

### 第5题

Frontmatter 主要用于什么目的？

A. 装饰文档
B. 存储文档元数据（如标题、作者、日期等）
C. 编写文档正文内容
D. 添加代码注释

<details>
<summary>点击查看答案</summary>

**答案：B**

**解析：** Frontmatter 的主要作用是存储文档的元数据（metadata），如标题、作者、日期、标签等。这些信息可以被静态网站生成器、博客系统、笔记软件等工具读取和使用，而不会影响文档的正文显示。

</details>

---

## 判断题（共5题）

### 第6题

Frontmatter 使用 `===` 作为分隔符。

<details>
<summary>点击查看答案</summary>

**答案：✗ 错误**

**解析：** Frontmatter 使用的是三条短横线 `---` 作为分隔符，而不是等号 `===`。`===` 不是标准的 Frontmatter 分隔符。

</details>

### 第7题

在 Frontmatter 中，`draft: true` 表示这篇文章是草稿。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

**解析：** `draft` 字段通常用于标记文章是否为草稿状态。设置为 `true` 时，许多静态网站生成器会跳过发布这篇文章；设置为 `false` 或省略时，文章会正常发布。

</details>

### 第8题

Frontmatter 中，键名和值之间的冒号后面可以没有空格。

<details>
<summary>点击查看答案</summary>

**答案：✗ 错误**

**解析：** 在 YAML 语法中，键值对的冒号后面**必须**有一个空格，例如 `title: 我的文章`。如果没有空格，会导致解析错误。

</details>

### 第9题

TOML 格式的 Frontmatter 可以使用 `+++` 作为分隔符。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

**解析：** TOML 格式的 Frontmatter 确实使用 `+++` 作为分隔符，这是 Hugo 等工具中常见的格式。也可以使用 `---toml` 标注 YAML 格式分隔符内的 TOML 内容。

</details>

### 第10题

Frontmatter 中定义的元数据可以在正文中通过变量引用。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

**解析：** 在许多静态网站生成器（如 VitePress、VuePress、Jekyll）中，Frontmatter 中定义的元数据可以通过变量在正文中引用。例如在 VitePress 中可以用 `{{ $frontmatter.title }}` 引用标题。

</details>

---

> 📚 **学习总结**
>
> - Frontmatter 是 Markdown 文件顶部的元数据区块
> - 使用 `---` 作为开始和结束标记
> - 支持 YAML、TOML、JSON 格式
> - 常用字段：title、author、date、tags、categories、draft
> - 广泛应用于静态网站生成器、博客、笔记软件

🎉 恭喜您完成了 Markdown Frontmatter 的5分钟学习！

# HTML 10分钟入门指南

> HTML（HyperText Markup Language，超文本标记语言）是构建网页的标准标记语言。它使用"标签"来描述网页的结构和内容。

---

## 一、HTML文档结构（2分钟）

每个HTML页面都有一个标准的基本结构：

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>页面标题</title>
</head>
<body>
    <!-- 页面可见内容写在这里 -->
    <h1>你好，世界！</h1>
    <p>这是我的第一个网页。</p>
</body>
</html>
```

### 核心概念解释

| 标签 | 含义 | 作用 |
|------|------|------|
| `<!DOCTYPE html>` | 文档类型声明 | 告诉浏览器这是一个HTML5文档 |
| `<html>` | 根元素 | 所有HTML内容的容器，`lang`属性指定语言 |
| `<head>` | 头部区域 | 包含元数据（字符编码、页面标题等），**不在页面显示** |
| `<body>` | 主体区域 | 包含页面**所有可见内容** |

---

## 二、常用基础标签（3分钟）

### 2.1 文本标签

```html
<!-- 标题标签：h1最大，h6最小 -->
<h1>一级标题</h1>
<h2>二级标题</h2>

<!-- 段落标签 -->
<p>这是一个段落文本。</p>

<!-- 换行标签（单标签，无闭合标签） -->
<p>第一行<br>第二行</p>

<!-- 强调标签 -->
<strong>加粗文本（重要）</strong>
<em>斜体文本（强调）</em>
```

### 2.2 链接与图片

```html
<!-- 超链接：href属性指定目标地址 -->
<a href="https://www.example.com">点击访问</a>

<!-- 打开新窗口 -->
<a href="https://www.example.com" target="_blank">新窗口打开</a>

<!-- 图片：src是图片地址，alt是替代文本（图片加载失败时显示） -->
<img src="photo.jpg" alt="风景照片" width="300">
```

### 2.3 列表

```html
<!-- 无序列表（ul = unordered list） -->
<ul>
    <li>苹果</li>
    <li>香蕉</li>
    <li>橙子</li>
</ul>

<!-- 有序列表（ol = ordered list） -->
<ol>
    <li>第一步</li>
    <li>第二步</li>
    <li>第三步</li>
</ol>
```

**实际效果：**

- 苹果
- 香蕉
- 橙子

1. 第一步
2. 第二步
3. 第三步

---

## 三、HTML5语义化标签（2分钟）

语义化标签让代码更具可读性，也利于搜索引擎优化（SEO）：

```html
<header>
    <!-- 页面或区块的头部，通常包含logo、导航等 -->
    <nav>
        <!-- 导航链接 -->
        <a href="/">首页</a>
        <a href="/about">关于</a>
    </nav>
</header>

<main>
    <!-- 页面主要内容（每个页面应只有一个） -->
    <article>
        <!-- 独立的文章内容 -->
        <h2>文章标题</h2>
        <p>文章内容...</p>
    </article>

    <aside>
        <!-- 侧边栏内容，如相关链接、广告 -->
    </aside>
</main>

<footer>
    <!-- 页面或区块的底部，通常包含版权信息 -->
    <p>© 2024 版权所有</p>
</footer>
```

### 为什么要用语义化标签？

1. **可读性**：代码结构清晰，易于维护
2. **SEO友好**：搜索引擎更容易理解页面内容
3. **可访问性**：屏幕阅读器能更好地为视障用户服务

---

## 四、表单元素（3分钟）

表单用于收集用户输入：

```html
<form action="/submit" method="POST">
    <!-- 文本输入 -->
    <label for="username">用户名：</label>
    <input type="text" id="username" name="username" placeholder="请输入用户名">

    <!-- 密码输入 -->
    <label for="password">密码：</label>
    <input type="password" id="password" name="password">

    <!-- 邮箱输入（带格式验证） -->
    <label for="email">邮箱：</label>
    <input type="email" id="email" name="email" required>

    <!-- 单选按钮 -->
    <p>性别：</p>
    <input type="radio" id="male" name="gender" value="male">
    <label for="male">男</label>
    <input type="radio" id="female" name="gender" value="female">
    <label for="female">女</label>

    <!-- 复选框 -->
    <p>爱好：</p>
    <input type="checkbox" id="reading" name="hobby" value="reading">
    <label for="reading">阅读</label>
    <input type="checkbox" id="sports" name="hobby" value="sports">
    <label for="sports">运动</label>

    <!-- 下拉选择 -->
    <label for="city">城市：</label>
    <select id="city" name="city">
        <option value="beijing">北京</option>
        <option value="shanghai">上海</option>
        <option value="guangzhou">广州</option>
    </select>

    <!-- 文本域 -->
    <label for="message">留言：</label>
    <textarea id="message" name="message" rows="4" cols="50"></textarea>

    <!-- 提交按钮 -->
    <button type="submit">提交</button>
</form>
```

### 常用input类型速查

| 类型 | 用途 | 示例 |
|------|------|------|
| `text` | 普通文本 | `<input type="text">` |
| `password` | 密码（显示为圆点） | `<input type="password">` |
| `email` | 邮箱（自动验证格式） | `<input type="email">` |
| `number` | 数字输入 | `<input type="number">` |
| `date` | 日期选择器 | `<input type="date">` |
| `checkbox` | 多选 | `<input type="checkbox">` |
| `radio` | 单选 | `<input type="radio">` |
| `file` | 文件上传 | `<input type="file">` |

---

## 附：快速参考表

### 最常用标签一览

| 功能 | 标签 | 示例 |
|------|------|------|
| 标题 | `<h1>` ~ `<h6>` | `<h1>主标题</h1>` |
| 段落 | `<p>` | `<p>一段文字</p>` |
| 链接 | `<a>` | `<a href="url">链接</a>` |
| 图片 | `<img>` | `<img src="pic.jpg" alt="描述">` |
| 容器 | `<div>` | `<div>内容块</div>` |
| 行内容器 | `<span>` | `<span>行内文字</span>` |
| 无序列表 | `<ul>`, `<li>` | `<ul><li>项</li></ul>` |
| 有序列表 | `<ol>`, `<li>` | `<ol><li>项</li></ol>` |
| 表格 | `<table>` | `<table><tr><td>单元格</td></tr></table>` |
| 输入框 | `<input>` | `<input type="text">` |
| 按钮 | `<button>` | `<button>点击</button>` |

### 全局属性（所有标签都可用）

| 属性 | 作用 | 示例 |
|------|------|------|
| `id` | 唯一标识符 | `<div id="header">` |
| `class` | 类名（可多个） | `<p class="intro highlight">` |
| `style` | 内联样式 | `<p style="color: red;">` |
| `title` | 鼠标悬停提示 | `<a title="点击查看详情">` |

---

# 测试题

## 单选题

### 第1题

HTML文档中，哪个标签用于定义页面的可见内容？

A. `<head>`
B. `<body>`
C. `<html>`
D. `<title>`

<details>
<summary>点击查看答案</summary>

**答案：B**

解析：`<body>` 标签包含页面的所有可见内容；`<head>` 包含元数据，不在页面显示；`<html>` 是整个文档的根元素；`<title>` 定义浏览器标签页上的标题。

</details>

### 第2题

以下哪个是正确的超链接写法？

A. `<a>https://example.com</a>`
B. `<a src="https://example.com">点击</a>`
C. `<a href="https://example.com">点击</a>`
D. `<a link="https://example.com">点击</a>`

<details>
<summary>点击查看答案</summary>

**答案：C**

解析：超链接使用 `href` 属性指定目标地址。`src` 是图片等资源的属性，`link` 不是有效的属性，直接写URL在标签内不会创建链接。

</details>

### 第3题

在HTML中，`alt` 属性的作用是什么？

A. 设置图片的对齐方式
B. 设置图片的替代文本，在图片无法显示时展示
C. 设置图片的标题提示
D. 设置图片的宽度和高度

<details>
<summary>点击查看答案</summary>

**答案：B**

解析：`alt`（alternative text）属性为图片提供替代文本描述，当图片加载失败或用户使用屏幕阅读器时显示。图片标题提示用 `title` 属性，宽高用 `width` 和 `height` 属性。

</details>

### 第4题

以下哪个是HTML5新增的语义化标签？

A. `<div>`
B. `<span>`
C. `<header>`
D. `<table>`

<details>
<summary>点击查看答案</summary>

**答案：C**

解析：`<header>`、`<nav>`、`<article>`、`<section>`、`<aside>`、`<footer>` 等都是HTML5新增的语义化标签。`<div>`、`<span>`、`<table>` 是HTML早期就有的标签。

</details>

### 第5题

创建单选按钮时，同一组选项的 `name` 属性应该如何设置？

A. 各不相同
B. 设置为相同值
C. 设置为"radio"
D. 不需要设置name属性

<details>
<summary>点击查看答案</summary>

**答案：B**

解析：同一组的单选按钮必须使用相同的 `name` 属性值，这样浏览器才能知道它们是互斥的选项，只能选其中一个。如果name不同，它们就不是同一组，可以同时选中多个。

</details>

## 判断题

### 第6题

`<br>` 标签是一个空元素（单标签），不需要闭合标签。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

解析：`<br>` 是换行标签，属于空元素（void element），它没有内容，也不需要闭合标签。类似的还有 `<img>`、`<input>`、`<hr>` 等。

</details>

### 第7题

HTML中，`<h1>` 标签的字体大小比 `<h6>` 小。

<details>
<summary>点击查看答案</summary>

**答案：✗ 错误**

解析：`<h1>` 是一级标题，字体最大、最重要；`<h6>` 是六级标题，字体最小。数字越小，标题级别越高，字体越大。

</details>

### 第8题

`<a>` 标签的 `target="_blank"` 属性可以让链接在新窗口或新标签页打开。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

解析：`target` 属性指定链接打开方式。`_blank` 表示新窗口/标签页；`_self`（默认）在当前窗口打开；`_parent` 在父框架打开；`_top` 在整个窗口打开。

</details>

### 第9题

HTML表单中，`type="checkbox"` 用于创建单选按钮，同一组只能选一个。

<details>
<summary>点击查看答案</summary>

**答案：✗ 错误**

解析：`type="checkbox"` 是复选框，可以多选；`type="radio"` 才是单选按钮，同一组（相同name）只能选择一个。

</details>

### 第10题

使用语义化标签（如 `<header>`、`<nav>`、`<article>` 等）有助于搜索引擎优化（SEO）和提高网页的可访问性。

<details>
<summary>点击查看答案</summary>

**答案：✓ 正确**

解析：语义化标签让搜索引擎更好地理解页面结构，提高SEO效果；同时也让屏幕阅读器等辅助技术能更好地为视障用户服务，提升可访问性。

</details>

---

## 学习资源推荐

- [MDN HTML 文档](https://developer.mozilla.org/zh-CN/docs/Web/HTML) - 最权威的Web文档
- [W3School HTML教程](https://www.w3school.com.cn/html/index.asp) - 适合入门的交互式教程
- [菜鸟教程 HTML](https://www.runoob.com/html/html5-intro.html) - 中文实例教程

---

*本教程生成时间：2026-03-25*

# HTML script 标签

## 学习契约

- 主题：HTML script 标签
- 目标：掌握概念
- 起点：0基础
- 时间：3分钟速通

## 核心知识点

### script 标签是什么

`<script>` 标签用于在 HTML 页面中嵌入或引用 JavaScript 脚本代码。

### 放置位置

可以放置在 `<head>` 或 `<body>` 中。

### 两种使用方式

1. **内联脚本**：直接在标签内编写 JavaScript 代码
2. **外部引用**：通过 `src` 属性引用外部 JS 文件

```html
<!-- 内联 -->
<script>
  console.log("Hello");
</script>

<!-- 外部引用 -->
<script src="app.js"></script>
```

### 当前代码状态

用户提供的代码中，`<script>` 标签内有换行和缩进，但没有任何 JavaScript 代码，属于空占位符状态，待后续填充脚本内容。

## 一句话总结

> `<script>` 标签是 HTML 页面中嵌入 JavaScript 代码的入口，可内联可外联。

## 学习记录

- 日期：2026-04-15
- 掌握要点：script 标签作用、放置位置、两种使用方式

该属性指定在何处显示链接的资源。 取值为标签（tab），窗口（window），或框架（iframe）等浏览上下文的名称或其他关键词。以下关键字具有特殊的意义:

- `_self`: 当前页面加载，即当前的响应到同一 HTML 4 frame（或 HTML5 浏览上下文）。此值是默认的，如果没有指定属性的话。
- `_blank`: 新窗口打开，即到一个新的未命名的 HTML4 窗口或 HTML5 浏览器上下文
- `_parent`: 加载响应到当前框架的 HTML4 父框架或当前的 HTML5 浏览上下文的父浏览上下文。如果没有 parent 框架或者浏览上下文，此选项的行为方式与 `_self` 相同。
- `_top`: IHTML4 中：加载的响应成完整的，原来的窗口，取消所有其它 frame。 HTML5 中：加载响应进入顶层浏览上下文（即，浏览上下文，它是当前的一个的祖先，并且没有 parent）。如果没有 parent 框架或者浏览上下文，此选项的行为方式相同\_self

> **注意：**使用target时，考虑添加 rel="noopener norefferrer" 以防止针对 window.opener API 的恶意行为。

## 参考文献

https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a
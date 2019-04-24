IIFE（ 立即调用函数表达式）是一个在定义时就会立即执行的  JavaScript 函数。

```Javascript
(function () {
    statements
})();
```

这是一个被称为 自执行匿名函数 的设计模式，主要包含两部分。第一部分是包围在 `圆括号运算符` `()` 里的一个匿名函数，这个匿名函数拥有独立的词法作用域。这不仅避免了外界访问此 IIFE 中的变量，而且又不会污染全局作用域。

第二部分再一次使用 `()` 创建了一个立即执行函数表达式，JavaScript 引擎到此将直接执行函数。

## 参考文献

https://developer.mozilla.org/zh-CN/docs/Glossary/%E7%AB%8B%E5%8D%B3%E6%89%A7%E8%A1%8C%E5%87%BD%E6%95%B0%E8%A1%A8%E8%BE%BE%E5%BC%8F
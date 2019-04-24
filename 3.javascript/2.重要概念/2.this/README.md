# this 的四种绑定规则

在 JavaScript 中，影响 this 指向的绑定规则有四种：

- 默认绑定
- 隐式绑定
- 显式绑定
- new 绑定

# 普通函数和箭头函数的区别

## 普通函数中的 this

1. this 总是代表它的直接调用者, 例如 obj.func ,那么 func 中的 this 就是 obj

2. 在默认情况(非严格模式下,未使用 'use strict'),没找到直接调用者,则 this 指的是 window

3. 在严格模式下,没有直接调用者的函数中的 this 是 undefined

4. 使用 call,apply,bind(ES5 新增)绑定的,this 指的是 绑定的对象

## 箭头函数中的 this

默认指向在定义它时,它所处的对象,而不是执行时的对象, 定义它的时候,可能环境是 window（即继承父级的 this）

## 参考文献

https://blog.csdn.net/xuexizhe88/article/details/79791143

https://juejin.im/post/596a28f6f265da6c360a2716

## HTML 语法节

语法非常简单。所有在元素上以`data-`开头的属性为数据属性。比如说你有一篇文章，而你又想要存储一些不需要显示在浏览器上的额外信息。请使用data属性：

```HTML
<article
  id="electriccars"
  data-columns="3"
  data-index-number="12314"
  data-parent="cars">
...
</article>
```

## JavaScript 访问

在外部使用JavaScript去访问这些属性的值同样非常简单。你可以使用`getAttribute()`配合它们完整的HTML名称去读取它们，但标准定义了一个更简单的方法：`DOMStringMap`你可以使用`dataset`读取到数据。

为了使用`dataset`对象去获取到数据属性，需要获取属性名中`data-`之后的部分(要注意的是破折号连接的名称需要改写为骆驼拼写法(如"index-number"转换为"indexNumber"))。

```JAVASCRIPT
var article = document.querySelector('#electriccars');.

article.dataset.columns // "3"
article.dataset.indexNumber // "12314"
article.dataset.parent // "cars"
```

## CSS 访问

注意，data设定为HTML属性，他们同样能被CSS访问。比如你可以通过generated content使用函数attr()来显示data-parent的内容：

```CSS
article::before {
  content: attr(data-parent);
}
```

你也同样可以在CSS中使用属性选择器根据data来改变样式：

```CSS
article[data-columns='3'] {
  width: 400px;
}
article[data-columns='4'] {
  width: 600px;
}
```

## 参考文献

https://developer.mozilla.org/zh-CN/docs/Web/Guide/HTML/Using_data_attributes
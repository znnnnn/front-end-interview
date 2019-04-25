这是一个历史遗留问题。

> 空白字符压缩（white space collapse）是西文排版的必然结果。SGML、TeX都是如此。不过对于不使用空格作为词分界的语言，比如东亚语言来说，就造成了问题。

我们知道造成「inline-block」元素空隙的本质是 HTML 中存在的空白符（whitespace）。

```CSS
ul{
  display:flex;
  flex-wrap:wrap;
```

用flex即可做到

## 参考文献

https://www.zhihu.com/question/21468450
HTML5 在引入新标签（见：[HTML5 新增标签及简介(全)](http://yanue.net/post-105.html "HTML5新增标签及简介(全)")）的同时，废弃了不少常见元素，大抵分为如下几类。

## 第一类：表现性元素

- basefont
- big
- center
- font
- s
- strike
- tt
- u

建议用语义正确的元素代替他们，并使用 CSS 来确保渲染后的效果

## 第二类：框架类元素

因框架有很多可用性及可访问性问题，HTML5 规范将以下元素移除。

- frame
- frameset
- noframes

但 html5 支持 iframe。

## 第三类:属性类

很多表现性的属性也被新规范移除，如下：

- align
- body 标签上的 link、vlink、alink、text 属性
- bgcolor
- height 和 width
- iframe 元素上的 scrolling 属性
- valign
- hspace 和 vspace
- table 标签上的 cellpadding、cellspacing 和 border 属性
- header 标签上的 profile 属性
- 链接标签 a 上的 target 属性
- img 和 iframe 元素的 longdesc 属性

## 第四类：其他

- abbr 取代 acronym（用于表示缩写）
- object 取代了 applet
- ul 取代了 dir

另附上直观的：[html5 元素周期表](http://demo.yanue.net/HTML5element/ "html5元素周期表")

## 参考文献

http://yanue.net/post-106.html
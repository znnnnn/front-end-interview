参考链接: [为何对有 display: table 的元素设置 margin 不起作用](https://link.jianshu.com?t=http://stackoverflow.com/questions/716442/css-cell-margin)

table 布局有两个特性：

- 同行等高
- 宽度自动调节

```HTML
<style type="text/css">
   .classtd {
        display:table-cell;
        padding:30px;
        border:1px solid #ccc;
    }
</style>
<div class="classtd">
   <p>大人。<br />
    其实我觉得大家别问元芳，元芳不是神人，<br />
    也不会武功，也许还是个智障，<br />
    我就不信我在这里黑元芳<br />
    他会突然飞檐走壁来到我身后<br />
    把我的头按在键盘上</p>
</div>
<div class="classtd">
    <p>我和左边等高</p>
</div>
```

![](//upload-images.jianshu.io/upload_images/1716779-d2966d91e5c64039.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/730/format/webp)

效果图

设置几个 div 的样式为`table-cell`，那么这几个 div 会被视作类似表单的同一行几个`td`, 有相同的高度，并且*无缝相接*。 并且！！！设置了`table-cell`后的元素，再设置`margin`是没有用的！！因为`margin`对 table 不起作用！！！

如果希望*有缝相接*，请务必按照如下结构

```HTML
<style type="css/text">
      .grandpa {
         display: table;
         border-collapse:separate;
         border-spacing:5px;
      }
      .father {
         display: table-row;
      }
      .classtd {
          display: table-cell;
          padding:10px;
          border:1px solid #ccc;
      }
</style>
<div class="grandpa">
    <div class="father">
          <div class="classtd">我是左边栏目</div>
          <div class="classtd">
              我是自适应的右边<br>
              哈哈哈<br>
          </div>
    </div>
</div>
```

那么得到的视图如下：

爷爷元素使用 separate 后的效果图.png

发现木有，使用 table 布局，可以轻松解决等高布局的问题。如果需要间距，则对爷爷元素使用`border-collapse:separate`和`border-spacing:10px;`便可以。

### 参考文献

https://www.jianshu.com/p/4f8dfcff5dbd

3.1、设置父元素 float 的值不为 none

```HTML
<div style="float:left">
    <ul style="float:left">
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
</div>
```

这个意思就是，既然儿子们都浮动了，那么老子也跟浮吧

3.2、设置父元素 overflow 的值不为 visible

```HTML
<div style="overflow:hidden">
    <ul style="float:left">
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
</div>
```

3.3、display 的值为 inline-block、table-cell、table-caption

```HTML
<div style="display:inline-block">
    <ul style="float:left">
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
</div>
```

用这个方法时注意 ie8 不支持 inline-block

3.4、position 的值为 absolute 或 fixed

```HTML
<div style="position:fixed">
    <ul style="float:left">
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
</div>
```

## 什么是闭包

```Javascript
function f1() {
  var n = 999;

  function f2() {
    alert(n);
  }

  return f2;
}

var result = f1();

result(); // 999
```

上面代码中的f2函数，就是闭包。

各种专业文献上的"闭包"（closure）定义非常抽象，很难看懂。我的理解是，闭包就是能够读取其他函数内部变量的函数。

由于在Javascript语言中，只有函数内部的子函数才能读取局部变量，因此可以把闭包简单理解成"定义在一个函数内部的函数"。

所以，在本质上，闭包就是将函数内部和函数外部连接起来的一座桥梁。

## 思考题

如果你能理解下面两段代码的运行结果，应该就算理解闭包的运行机制了。

代码片段一。

```JAVASCRIPT
　　var name = "The Window";

　　var object = {
　　　　name : "My Object",

　　　　getNameFunc : function(){
　　　　　　return function(){
　　　　　　　　return this.name;
　　　　　　};

　　　　}

　　};

　　alert(object.getNameFunc()());
```


代码片段二。

```JAVASCRIPT
　　var name = "The Window";

　　var object = {
　　　　name : "My Object",

　　　　getNameFunc : function(){
　　　　　　var that = this;
　　　　　　return function(){
　　　　　　　　return that.name;
　　　　　　};

　　　　}

　　};

　　alert(object.getNameFunc()());
```

## 参考文献

http://www.ruanyifeng.com/blog/2009/08/learning_javascript_closures.html
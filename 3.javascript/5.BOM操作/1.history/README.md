## 属性

- History.length `只读`
返回一个整数，该整数表示会话历史中元素的数目，包括当前加载的页。例如，在一个新的选项卡加载的一个页面中，这个属性返回1。

- History.scrollRestoration 
允许Web应用程序在历史导航上显式地设置默认滚动恢复行为。此属性可以是自动的（auto）或者手动的（manual）。

- History.state `只读`
返回一个表示历史堆栈顶部的状态的值。这是一种可以不必等待popstate 事件而查看状态而的方式。

## 方法

- History.back()
前往上一页, 用户可点击浏览器左上角的返回按钮模拟此方法. 等价于 history.go(-1).
Note: 当浏览器会话历史记录处于第一页时调用此方法没有效果，而且也不会报错。

- History.forward()
在浏览器历史记录里前往下一页，用户可点击浏览器左上角的前进按钮模拟此方法. 等价于 history.go(1).
Note: 当浏览器历史栈处于最顶端时( 当前页面处于最后一页时 )调用此方法没有效果也不报错。

- History.go()
通过当前页面的相对位置从浏览器历史记录( 会话记录 )加载页面。比如：参数为-1的时候为上一页，参数为1的时候为下一页. 当整数参数超出界限时( 译者注:原文为When integerDelta is out of bounds )，例如: 如果当前页为第一页，前面已经没有页面了，我传参的值为-1，那么这个方法没有任何效果也不会报错。调用没有参数的 go() 方法或者不是整数的参数时也没有效果。( 这点与支持字符串作为url参数的IE有点不同)。

- History.pushState()
按指定的名称和URL（如果提供该参数）将数据push进会话历史栈，数据被DOM进行不透明处理；你可以指定任何可以被序列化的javascript对象。注意到Firefox现在忽略了这个title参数，更多的信息，请看manipulating the browser history。

- History.replaceState()
按指定的数据，名称和URL(如果提供该参数)，更新历史栈上最新的入口。这个数据被DOM 进行了不透明处理。你可以指定任何可以被序列化的javascript对象。注意到Firefox现在忽略了这个title参数，更多的信息，请看manipulating the browser history。

当 deviceWidth 大于 750px 时，我们应该去访问的是 pc 版的页面，所以当 deviceWidth 大于 750px 时我们不应该再改变根元素的 font-size 值
完整的代码如下：

1. viewprot 宽度为移动设备的逻辑宽度：
  ```
 <meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no"/>
  ```
2. Js计算方式如下[以iphone6为基准]：
  ```
var deviceWidth = document.documentElement.clientWidth;
if(deviceWidth > 750) deviceWidth = 750;
document.documentElement.style.fontSize = deviceWidth / 7.5 + 'px';
  ```
# -
参考自：https://juejin.im/post/5bbdfccff265da0ae6775fed

# -
参考自：https://juejin.im/post/5bbdfccff265da0ae6775fed

最后，总结一下我在项目中使用的移动端适配方案：

将 viewport 宽度设置为移动设备逻辑宽度；
使用 js 根据不同分辨率的移动设备来设置根元素的 font-size 值，注意移动端与 pc 端的临界值；
在样式中字体使用 px 单位，而其它元素使用 rem 单位；
使用 sass 中的 function 来设置一个 px 与 rem 之间的转换函数；

viewprot 宽度为移动设备的逻辑宽度：

<meta name="viewport" content="width=device-width,initial-scale=1.0,maximum-scale=1.0,user-scalable=no"/>

Js计算方式如下[以iphone6为基准]：

var deviceWidth = document.documentElement.clientWidth;
if(deviceWidth > 750) deviceWidth = 750;
document.documentElement.style.fontSize = deviceWidth / 7.5 + 'px';

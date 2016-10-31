### 移动端统计 (from BiosSun)
[百度移动统计](http://tongji.baidu.com/data/mobile/brand)

### 页面描述
- 忽略将页面中的数字识别为电话号码
`<meta name="format-detection" content="telephone=no" />`
- 忽略Android平台中对邮箱地址的识别
`<meta name="format-detection" content="email=no" />`
- 当网站添加到主屏幕快速启动方式，可隐藏地址栏，仅针对ios的safari
`<meta name="apple-mobile-web-app-capable" content="yes" />
<!-- ios7.0版本以后，safari上已看不到效果 -->`
- 将网站添加到主屏幕快速启动方式，仅针对ios的safari顶端状态条的样式
`<meta name="apple-mobile-web-app-status-bar-style" content="black" />
<!-- 可选default、black、black-translucent -->`
[参考资料](http://www.cnblogs.com/PeunZhang/p/3407453.html)

><link rel="apple-touch-icon-precomposed" href="http://www.xxx.com/App_icon_114.png" />
><link rel="apple-touch-icon-precomposed" sizes="72x72" href="http://www.xxx.com/App_icon_72.png" />
><link rel="apple-touch-icon-precomposed" sizes="114x114" href="http://www.xxx.com/App_icon_114.png" />
这个属性是当用户把连接保存到手机桌面时使用的图标，如果不设置，则会用网页的截图。有了这，就可以让你的网页像APP一样存在手机里了

> <link rel="apple-touch-startup-image" href="/img/startup.png" />
这个是APP启动画面图片，用途和上面的类似，如果不设置，启动画面就是白屏，图片像素就是手机全屏的像素

### 阻止旋转屏幕时自动调整字体大小
> html, body, form, fieldset, p, div, h1, h2, h3, h4, h5, h6 {-webkit-text-size-adjust:none;}

### 模拟:hover伪类
因为iPhone并没有鼠标指针，所以没有hover事件。那么CSS :hover伪类就没用了。但是iPhone有Touch事件，onTouchStart 类似 onMouseOver，onTouchEnd 类似 onMouseOut。所以我们可以用它来模拟hover。使用Javascript：
`var myLinks = document.getElementsByTagName('a');
for(var i = 0; i < myLinks.length; i++){
　　myLinks[i].addEventListener(’touchstart’, function(){this.className = “hover”;}, false);
　　myLinks[i].addEventListener(’touchend’, function(){this.className = “”;}, false);
}`
然后用CSS增加hover效果：
`a:hover, a.hover { /* 你的hover效果 */ }`
这样设计一个链接，感觉可以更像按钮。并且，这个模拟可以用在任何元素上。

### placeholder--line-height
input 的placeholder会出现文本位置偏上的情况：PC端设置line-height等于height能够对齐，而移动端仍然是偏上，解决是设置line-height：normal，（stackoverflow也可查到这种解决办法）。

### 使用特殊链接：
如果你关闭自动识别后 ，又希望某些电话号码能够链接到 iPhone 的拨号功能 ，那么可以通过这样来声明电话链接 ,
`<a href="tel:12345654321">打电话给我</a>
<a href="sms:12345654321">发短信</a>`

### 自动大写与自动修正
- 要关闭这两项功能，可以通过autocapitalize 与autocorrect 这两个选项：
`<input type="text" autocapitalize="off" autocorrect="off" />`

### Web移动端Fixed布局的解决方案
[Web移动端Fixed布局的解决方案](http://efe.baidu.com/blog/mobile-fixed-layout/)


### 抽奖老虎机
[抽奖老虎机](http://perfey.github.io/laohuji/index.html)












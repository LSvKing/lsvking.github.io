---
title: CSS Hacks 和 问题解决
author: lsvking
type: post
date: 2008-02-23T13:41:13+00:00
url: /88
categories:
  - 前端
  - 技术

---
<p class="bold">
  &#160;
</p>

<p class="inner">
  这篇文章包括了8个非常有用的解决办法, 在进行css设计遇到问题时你就会用到它们.
</p>

&#160;

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;

## **目录**

  * 介绍 
  * 针对浏览器的选择器 
  * 让IE6支持PNG透明 
  * 移除超链接的虚线 
  * 给行内元素定义宽度 
  * 让固定宽度的页面居中 
  * 图片替换技术 
  * 最小宽度 
  * 隐藏水平滚动条 

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;

### **一. 介绍**

这篇文章包括了8个非常有用的解决办法, 在进行css设计遇到问题时你就会用到它们.

### **二. 针对浏览器的选择器**

这些选择器在你需要针对某款浏览器进行css设计时将非常有用.

IE6及其更低版本

* html {}

IE7及其更低版本

\*:first-child+html {} \* html {}

仅针对IE7

*:first-child+html {}

IE7和当代浏览器

html>body{}

仅当代浏览器(IE7不适用)

html>/**/body{}

Opera9及其更低版本

html:first-child {}

Safari

html[xmlns*=""] body:last-child {}

要使用这些选择器,请将它们放在样式之前. 例如:

#content-box {   
width: 300px;   
height: 150px;   
}   
* html   
#content-box {   
width: 250px;   
} /\* overrides the above style and changes the width to 250px in IE 6 and below \*/

### **三. 让IE6支持PNG透明**

一个IE6的Bug引起了大麻烦, 他不支持透明的PNG图片.

你需要使用一个css滤镜

*html #image-style {   
background-image: none;   
filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src="fil   
ename.png", sizingMethod="scale");   
}

### **四. 移除超链接的虚线(仅对FF有效)**

FireFox下,当你点击一个超链接时会在外围出现一个虚线轮廓. 这很容易解决, 只需要在标签样式中加入 outline:none .

a{   
outline: none;   
}

### **五. 给行内元素定义宽度**

如果你给一个行内元素定义宽度,那么它只是在IE6下有效. 所有的HTML元素要么是行内元素要么就好是块元素. 行内元素包括: <span>, <a>, <strong> 和 <em>. 块元素包括<div>, <p>, <h1>, <form>和<li> . 你不能定义行内元素的宽度, 为了解决这个问题你可以将行内元素转变为块元素.

span { width: 150px; display: block }

### **六. 让固定宽度的页面居中**

为了让页面在浏览器居中显示, 需要相对定位外层div, 然后把margin设置为auto.

#wrapper {   
margin: auto;   
position: relative;   
}

### **七. 图片替换技术**

用文字总比用图片做标题好一些. 文字对屏幕阅读机和SEO都是非常友好的.

HTML:

<h1><span>Main heading one</span></h1>

<a class="bodytag" href="http://www.yeeyan.com/articles/tag/CSS" target="_blank"><font color="#335533">CSS</font></a>:

h1 { background: url(heading-image.gif) no-repeat; }   
h1 span {   
position:absolute;   
text-indent: -5000px;   
}   
你可以看到我们对标题使用了标准的<h1>作为标签并且用css来将文本替换为图片. text-indent属性将文字推到了浏览器左边5000px处, 这样对于浏览者来说就看不见了.

关掉css,然后看看头部会是什么样子的.

### **八. 最小宽度**

IE6另外一个bug就是它不支持 min-width 属性. min-width又是相当有用的, 特别是对于弹性模板来说, 它们有一个100%的宽度,min-width 可以告诉浏览器何时就不要再压缩宽度了.

除IE6以外所有的浏览器你只需要一个 min-width: Xpx; 例如:

.container {   
min-width:300px;   
}

为了让他在IE6下工作, 我们需要一些额外的工作. 开始的时候我们需要创建两个div, 一个包含另一个:

<div class="container">   
<div class="holder">Content</div>   
</div>

然后你需要定义外层div的min-width属性

.container {   
min-width:300px;   
}

这时该是IE <a class="bodytag" href="http://www.yeeyan.com/articles/tag/hack" target="_blank"><font color="#335533">hack</font></a>大显身手的时候了. 你需要包含如下的代码:

* html .container {   
border-right: 300px solid #FFF;   
}   
* html .holder {   
display: inline-block;   
position: relative;   
margin-right: -300px;   
}

As the browser window is resized the outer div width reduces to suit until it shrinks to the border width, at which point it will not shrink any further. The holder div follows suit and also stops shrinking. The outer div border width becomes the minimum width of the inner div.

### **九. 隐藏水平滚动条**

为了避免出现水平滚动条, 在body里加入 overflow-x:hidden .

body { overflow-x: hidden; }

当你决定使用一个比浏览器窗口大的图片或者flash时, 这个技巧将非常有用.

&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8212;&#8211;

原作者: Chris Thomas <a href="http://www.solidstategroup.com/page/1592" target="_blank"><font color="#2e6ab1"> 原文</font></a>&#160; ![][1]&#160; 译者: [<font color="#2e6ab1">Rlog</font>][2]&#160; ![][1]

 [1]: http://www.yeeyan.com/img/div.gif
 [2]: http://www.yeeyan.com/space/show/10947
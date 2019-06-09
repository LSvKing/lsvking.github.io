---
title: FireFox左键无法使用迅雷？
author: lsvking
type: post
date: 2008-04-12T15:03:06+00:00
url: /205
categories:
  - 网络

---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 一直喜欢用迅雷下东西，虽然他有点“流氓”不过正是他的流氓才给我们带来了高速度的下载。

&nbsp;&nbsp;&nbsp;&nbsp; FireFox也支持迅雷，不过下东西时左键点击下载地址时，默认情况下会弹出，

[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="142" alt="image" src="http://www.lsvking.com/wp-content/uploads/2008/04/windowslivewriterfirefox-d2d7image-thumb1.png" width="447" border="0" />][1] 

此操作被浏览器拒绝！

请在浏览器地址栏输入“about:config”并回车

然后将[signed.applets.codebase\_principal\_support]设置为&#8217;true&#8217;

这是FF默认禁用了某个参数开启它就行，开启他的步骤：

1.在地址栏输入 “about:config”并回车

2.在“过滤器”栏输入 “princ” 就会过滤出这条控制，然后双击 默认值是&#8217;false&#8217;&nbsp; 双击后会变成&#8217;true&#8217;。

这样以后再用左键点击迅雷的下载就可以正常使用了

 [1]: http://www.lsvking.com/wp-content/uploads/2008/04/windowslivewriterfirefox-d2d7image-21.png
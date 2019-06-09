---
title: vagrant 打包box时候提示 “VM not created. Moving on…”
author: lsvking
type: post
date: 2014-11-13T09:48:10+00:00
url: /1134
categories:
  - 技术
tags:
  - vagrant

---
在使用vagrant 打包我本地的虚拟机的时候,提示 &#8220;VM not created. Moving on&#8230;&#8221;，折腾半天发现原来是名字大小写弄错了。。

<pre>vagrant package --base ubuntu --output ubuntu.box
ubuntu: VM not created. Moving on...
</pre>

[<img src="http://bcs.duapp.com/lsvking-wp//blog/201411//QQ图片201411131745041.jpg" alt="QQ图片20141113174504" width="449" height="191" class="alignnone size-full wp-image-1136" />][1]

名称要完全一样，大小写也要一样哦。折腾了半天，也是醉了。。

 [1]: http://bcs.duapp.com/lsvking-wp//blog/201411//QQ图片201411131745041.jpg
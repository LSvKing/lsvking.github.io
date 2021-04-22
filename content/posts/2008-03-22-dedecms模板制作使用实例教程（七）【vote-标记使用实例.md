---
title: DedeCMS模板制作使用实例教程（七）【Vote 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T19:29:03+00:00
url: /137
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Vote 标记】用于获取一组投票表单。   
其使用范围限于：封面模板。   
可先进入后台，按下面操作方法填写好调查内容：   
辅助插件&#8211;>投票模块&#8211;>增加一组投票   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Vote 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
我调试【Channel 标记】的具体代码如下：   
{dede:vote id=&#8217;2&#8242; lineheight=&#8217;22&#8217;   
tablewidth=&#8217;100%&#8217; titlebgcolor=&#8217;#EDEDE2&#8242;   
titlebackground=&#8221; tablebgcolor=&#8217;#FFFFFF&#8217;}   
{/dede:vote}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="166" alt="clip_image001" src="http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsvote-1114fclip-image001-thumb.gif" width="403" border="0" />][1]

 [1]: http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsvote-1114fclip-image001-2.gif
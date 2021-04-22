---
title: DedeCMS模板制作使用实例教程（三）【Channel 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T18:03:48+00:00
url: /125
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
</p> 

【Channel 标记】主要用于获取栏目列表，用法非常简单，主要是区分&#8220;type = top,sun/son,self &#8221;的所调用的对象就行了。   
说明：为了便于下面内容的理解，我将数据库中网站频道的截图如下：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="347" alt="clip_image001" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image001-thumb.gif" width="438" border="0" />][1]   
使用思路、步骤：   
一、明确使用范围   
我们在使用任何标记的过程中，都必须明确其使用的范围，否则可能无法正常调用该标签，【Channel 标记】的使用范围是：   
封面模板、列表模板、文档模板。   
二、通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Channel 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
调用方法一：   
我调试【Channel 标记】的具体代码如下：   
{dede:channel row=&#8217;3&#8242; type=&#8217;top&#8217;}   
<a href="[field:typelink/]">[field:typename/]</a>   
{/dede:channel}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="103" alt="clip_image002" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image002-thumb.gif" width="237" border="0" />][2]   
调用方法二：   
我调试【imglist标记】的具体代码如下：   
{dede:channel row=&#8217;3&#8242; type=&#8217;sun&#8217; typeid=&#8217;96&#8217;}   
<a href="[field:typelink/]">[field:typename/]</a>   
{/dede:channel}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="115" alt="clip_image003" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image003-thumb.gif" width="244" border="0" />][3]

 [1]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image001-2.gif
 [2]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image002-2.gif
 [3]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannel-fd47clip-image003-2.gif
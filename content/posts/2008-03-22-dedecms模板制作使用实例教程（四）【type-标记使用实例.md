---
title: DedeCMS模板制作使用实例教程（四）【Type 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T18:28:03+00:00
url: /130
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Type 标记】表示指定的单个栏目的链接，用法非常简单。   
说明：为了便于下面内容的理解，我将数据库中网站频道的截图如下：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="347" alt="clip_image001" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmstype-102f8clip-image001-thumb.gif" width="438" border="0" />][1]   
使用思路、步骤：   
一、明确使用范围   
我们在使用任何标记的过程中，都必须明确其使用的范围，否则可能无法正常调用该标签，【Type 标记】的使用范围是：   
封面模板、列表模板、文档模板。   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Type 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
我调试【Channel 标记】的具体代码如下：   
{dede:type typeid=&#8217;96&#8217;}{/dede:type}   
<br />   
<br />   
{dede:channel&#160; typeid=&#8217;96&#8217;}   
<a href='[field:typelink /]&#8217;>[field:typename/]</a>   
{/dede:channel}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="154" alt="clip_image002" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmstype-102f8clip-image002-thumb.gif" width="222" border="0" />][2]   
通过以上两行代码的对比，相信你的认识会更深刻。前者是生成单一的数据，后者通过数组生成一组的数据。

 [1]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmstype-102f8clip-image001-2.gif
 [2]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmstype-102f8clip-image002-2.gif
---
title: DedeCMS模板制作使用实例教程（二）【Field 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T17:54:06+00:00
url: /118
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Field 标记】在封面模板、列表模板、文档模板的使用频率很高，实用。主要用来获得到系统变量的值或者路径，用法很灵活。可以直接展示数据，如调用 position，得到栏目一 > 栏目二&#8221; 这样形式的链接；或者，调用templeturl得到/templets这样路径。   
使用思路、步骤：   
一、明确使用范围   
我们在使用【Field 标记】的过程中，必须明确其使用的范围，否则可能无法正常调用该标签，其使用范围是：   
封面模板（如index\_article.htm）、列表模板（如list\_article.htm）、文档模板（如article_article.htm）。   
&#160; index\_article.htm、list\_article.htm、article_article.htm等类似的模板文档都在templets\default\文件夹中。   
注意：   
&#160; 1、封面模板与列表模板是有区别的，但调用【Field 标记】可以相同；   
&#160; 2、封面模板有不同的类型，我们最常用的是文章模板（index\_article.htm），其它的还有图片模板（index\_image.htm），简 介模板（index\_info.htm），软件模板（index\_soft.htm）等等，这些模板调用【Field 标记】的道理都是一样的。   
二、通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的list\_default.htm和htmlist\_article.htm文件中的代码，全部掏空。放 入调用【Field 标记】的代码，再在管理后台进行操作，如下：HTML更新&#8211;>更新栏目HTML&#8211;>开始生成HTML。再在IE中访问网站的各栏封面和列 表，就可以得到返回的数据。   
用法一：   
这种用法，主要是从数据库获取相关的数据，特别是系统变量的数据。   
我调试【Arclist 标记】的具体代码如下：   
<font color="red">调用position标记,得到:栏目一 > 栏目二&#8221; 这样形式的链接：</font>{dede:field name=&#8217;position&#8217;/}<br/>   
<font color="red">插件路径：</font>{dede:field name=&#8217;phpurl&#8217;/}<br/>   
<font color="red">模板路径：</font>{dede:field name=&#8217;templeturl&#8217;/}<br/>   
<font color="red">版权信息：</font>{dede:field name=&#8217;powerby&#8217;/}<br/>   
<font color="red">主页路径：</font>{dede:field name=&#8217;indexurl&#8217;/}<br/>   
<font color="red">主页名称：</font>{dede:field name=&#8217;indexname&#8217;/}<br/>   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="231" alt="clip_image001" src="http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsfield-faffclip-image001-thumb.gif" width="389" border="0" />][1]   
请朋友们举一反三，增删属性和写入代码进行调试，加深印象。最好是对照官方的Dedecms文档进行调试，我这样做收获很大的。   
用法二：   
这一种用法比较灵活，作用也非常大，但必须有HTML知识才能运用的比较好，   
我调试【Arclist 标记】的具体代码如下：   
&#160; <link href="{dede:field name=&#8217;templeturl&#8217;/}/style/dede.css" rel="stylesheet" type="text/css" />   
注意：本页面的文字和链接都是经过dede.css处理的<br />   
<a href="http://bbs.dedecms.com/">织梦论坛</a> <br />   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="94" alt="clip_image002" src="http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsfield-faffclip-image002-thumb.gif" width="289" border="0" />][2]

 [1]: http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsfield-faffclip-image001-2.gif
 [2]: http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsfield-faffclip-image002-2.gif
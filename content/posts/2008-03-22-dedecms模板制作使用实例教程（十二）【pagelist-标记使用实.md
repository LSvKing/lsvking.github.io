---
title: DedeCMS模板制作使用实例教程（十二）【Pagelist 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T20:44:49+00:00
url: /154
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Pagelist 标记】表示分页页码列表   
适用范围：列表模板   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的list\_default.htm和htmlist\_article.htm文件中的代码，全部掏空。放 入调用【Pagelist 标记】的代码，再在管理后台进行操作，如下：HTML更新&#8211;>更新栏目HTML&#8211;>开始生成HTML。再在IE中访问网站的各栏封面和列 表，就可以得到返回的数据。   
我调试【Pagelist 标记】的具体代码如下：   
<ul>   
{dede:list col=&#8217;1&#8242; row=&#8217;3&#8242; titlelen=&#8217;20&#8217;   
infolen=&#8217;100&#8242; imgwidth=&#8217;120&#8242; imgheight=&#8217;80&#8217; pagesize=&#8217;3&#8242; typeid=&#8217;95&#8217;}   
<li>\[field:imglink/\] \[field:textlink/\] <font style="color:gray;">[field:info/]</font></li>   
{/dede:list}   
</ul>   
{dede:pagelist listsize=&#8217;3&#8242; listitem=&#8217;index pre pageno next end option&#8217;/}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="362" alt="clip_image001" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmspagelist-1230cclip-image001-thumb.gif" width="624" border="0" />][1]

 [1]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmspagelist-1230cclip-image001-2.gif
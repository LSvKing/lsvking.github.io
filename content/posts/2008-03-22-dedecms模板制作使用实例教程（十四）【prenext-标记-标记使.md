---
title: DedeCMS模板制作使用实例教程（十四）【Prenext 标记 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T21:08:15+00:00
url: /160
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Prenext 标记】表示获取文档&#8220;上一篇／下一篇&#8221;的链接列表。   
适用范围：仅文档模板。   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的article_article.htm文件中的代码，全部掏空。放入调用【Prenext 标记】的代码，再在管理后台进行操作，如下：HTML更新&#8211;>更新文档HTML&#8211;>开始生成HTML。再在IE中访问网站的各个文档，就 可以得到返回的数据。   
我调试【Pagelist 标记】的具体代码如下：   
<font color="red">文章标标题:</font>{dede:field name="title"/}<br />   
<font color="red">文章内容:</font>{dede:field name="body"/}<br />   
{dede:pagebreak/}<br />   
{dede:prenext/} <br />   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="307" alt="clip_image001" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmsprenext-1288aclip-image001-thumb.gif" width="621" border="0" />][1]

 [1]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmsprenext-1288aclip-image001-2.gif
---
title: DedeCMS模板制作使用实例教程（十五）【Pagetitle 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T21:13:29+00:00
url: /165
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Pagetitle 标记】   
功能说明：表示获取文档的分页标题   
适用范围：仅文档模板。   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的article_article.htm文件中的代码，全部掏空。放入调用【Pagetitle 标记】的代码，再在管理后台进行操作，如下：HTML更新&#8211;>更新文档HTML&#8211;>开始生成HTML。再在IE中访问网站的各个文档，就 可以得到返回的数据。   
我调试【Pagetitle 标记】的具体代码如下：   
<font color="red">文章标标题:</font>{dede:field name="title"/}<br />   
<font color="red">文章内容:</font>{dede:field name="body"/}<br />   
{dede:pagetitle style=&#8217;select&#8217;/}<br />   
{dede:prenext/} <br />   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="288" alt="clip_image001" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmspagetitle-129b0clip-image001-thumb.gif" width="502" border="0" />][1]   
注意：   
想要使用【Pagetitle 标记】的前提条件是，文章存在分页，而且要手动在需分的地方加上#p#副标题#e#，实现分页的。   
而且要将&#8220;#p#副标题#e#&#8221;，替换成相应的标题，如下图较所示。能得到到如上面的返回数据。   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="299" alt="clip_image002" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmspagetitle-129b0clip-image002-thumb.gif" width="358" border="0" />][2]

 [1]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmspagetitle-129b0clip-image001-2.gif
 [2]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmspagetitle-129b0clip-image002-2.gif
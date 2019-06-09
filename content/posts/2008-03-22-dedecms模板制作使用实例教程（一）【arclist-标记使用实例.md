---
title: DedeCMS模板制作使用实例教程（一）【Arclist 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T17:36:00+00:00
url: /109
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
从本文开始，我将根据我的学习心得写一系列的实例教程。通过实例说明DedeCMS标记的使用方法。本实例教程使用的版本是DedeCms 2007 V5.0版，在本地架设的php+mysql （APMServ）环境中测试。安装、架设等相关方法参阅寂寞天涯的整理：<http://bbs.dedecms.com/read.php?tid=33332>。以后一系列教程都是在这个环境中使用，不再重复。因测试需要数据，我已事先在数据库录入，就不理啰嗦，马上进入正题。   
现在先讲【Arclist 标记】。【Arclist 标记】是使用率很高，相当实用，所以我们使用都必须熟练掌握。它的详细使用说明在官方Dedecms文档中已经有严密的解释，见：<http://www.dedecms.com/archives/templethelp/help/index.htm>，我们在使用过程中可以随时查阅。   
使用思路、步骤：   
一、明确使用范围   
我们在使用任何标记的过程中，都必须明确其使用的范围，否则可能无法正常调用该标签，【Arclist 标记】的使用范围是：   
封面模板、列表模板、文档模板。   
即对应templets\default\文件夹下的   
index\_识别ID.htm模板、list\_识别ID.htm模板、article_识别ID.htm模板）   
二、通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Arclist 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
注意：其它文件保持不变，我不懂PHP，只能用这种方式调试，相信朋友们很容易上手的。   
我调试【Arclist 标记】的具体代码如下：   
{dede:arclist typeid=&#8221; row=&#8217;1&#8217;&#160; titlelen=&#8217;20&#8217; infolen=&#8221;   
imgwidth=&#8217;100&#8242; imgheight=&#8217;80&#8217;}   
<font color="red">文章ID:</font>[field:ID/] <br />   
<font color="red">文章标题:</font>[field:title/] <br />   
<font color="red">文章短标题:</font>[field:shorttitle/] <br />   
<font color="red">文章标题的文字链接:</font>[field:textlink/] <br />   
<font color="red">文章作者:</font>[field:writer/] <br />   
<font color="red">文章发表日期:</font>[field:stime/] <br />   
<font color="red">文章所属栏目的目录:</font>[field:typedir/] <br />   
<font color="red">文章所属栏目的名称:</font>[field:typename/] <br />   
<font color="red">文章所属栏目的文字链接:</font>[field:typelink/] <br />   
<font color="red">文章的图片链接:</font>[field:imglink/] <br />   
<font color="red">文章的缩略图:</font>[field:image/] <br />   
{/dede:arclist}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="476" alt="clip_image001" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsarclist-f6d4clip-image001-thumb.gif" width="500" border="0" />][1]   
文章篇幅所限，未能列出所有的属性和字段调用的方法。请朋友们举一反三，增删属性和写入代码进行调试，加深印象。最好是对照官方的Dedecms文档进行调试，我这样做收获很大的。   
三、【Arclist 标记】延伸出来的别名标记（实用又个性化，建议关注使用）   
为了使网页内容更具个性化，人性化，官方在【Arclist 标记】的基础上延伸出来一些别外标签，如：hotart、coolart、likeart、artlist、imglist、imginfolist、specart、autolist 。非常好！   
我调试【imglist标记】的具体代码如下：   
{dede:imglist typeid=&#8221; row=&#8217;2&#8242; col=&#8217;1&#8217;&#160; titlelen=&#8217;20&#8217; infolen=&#8221;   
imgwidth=&#8217;100&#8242; imgheight=&#8217;80&#8217;}   
[field:imglink/]&#160; [field:textlink/]<br />   
{/dede:imglist}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="287" alt="clip_image002" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsarclist-f6d4clip-image002-thumb.gif" width="392" border="0" />][2]   
如上例，其它的别名标记，朋友们可以举一反三，融会贯通！

 [1]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsarclist-f6d4clip-image001-2.gif
 [2]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsarclist-f6d4clip-image002-2.gif
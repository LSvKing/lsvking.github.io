---
title: DedeCMS模板制作使用实例教程（九）【Mynews 标记 使用实例】
author: lsvking
type: post
date: 2008-03-22T20:06:15+00:00
url: /145
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Mynews 标记】用于获取站内新闻。   
站内新闻有利于站长及时与会员沟通。   
使用思路、步骤：   
一、明确使用范围   
我们在使用任何标记的过程中，都必须明确其使用的范围，否则可能无法正常调用该标签，【Mynews 标记】的使用范围是：   
封面模板   
二、通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Mynews 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
我调试【Mynews 标记】的具体代码如下：   
{dede:mynews row=&#8217;2&#8242; titlelen=&#8217;30&#8217;}标题：[field:title/] <br />   
作者：[field:writer/] <br />   
时间：[field:senddate function="strftime(&#8216;%y-%m-%d %H:%M&#8217;,@me)"/] <br />   
内容：[field:body/] <br /><br /><br />   
{/dede:mynews}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="386" alt="clip_image001" src="http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsmynews-119fdclip-image001-thumb.gif" width="456" border="0" />][1]

 [1]: http://lsvking.github.iot/wp-content/uploads/2008/03/windowslivewriterdedecmsmynews-119fdclip-image001-2.gif
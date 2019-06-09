---
title: DedeCMS模板制作使用实例教程（八）【Flink 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T20:04:25+00:00
url: /142
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Flink 标记】用于获取友情链接。   
调用该标记后可以得到四种友情链接的形式。   
使用思路、步骤：   
一、明确使用范围   
我们在使用任何标记的过程中，都必须明确其使用的范围，否则可能无法正常调用该标签，【Flink 标记】的使用范围是：   
封面模板   
二、通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Flink 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
补充：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="379" alt="clip_image001" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsflink-11971clip-image001-thumb.gif" width="555" border="0" />][1]   
我调试【Flink 标记】的具体代码如下：   
全部用文字显示：{dede:flink type=&#8217;textall&#8217; row=&#8217;4&#8217;&#160; titlelen=&#8217;20&#8217;}{/dede:flink}<br />   
文字和图文混合排列：{dede:flink type=&#8217;textimage&#8217; row=&#8217;4&#8217;&#160; titlelen=&#8217;20&#8217;}{/dede:flink}<br />   
仅显示不带Logo的链接：{dede:flink type=&#8217;text&#8217; row=&#8217;4&#8217;&#160; titlelen=&#8217;20&#8217;}{/dede:flink}<br />   
仅显示带Logo的链接：{dede:flink type=&#8217;image&#8217; row=&#8217;4&#8217;&#160; titlelen=&#8217;20&#8217;}{/dede:flink}<br />   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="193" alt="clip_image003" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsflink-11971clip-image003-thumb.gif" width="624" border="0" />][2]

 [1]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsflink-11971clip-image001-2.gif
 [2]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsflink-11971clip-image003-2.gif
---
title: DedeCMS模板制作使用实例教程（十）【Channelartlist 标记 使用实例】
author: lsvking
type: post
date: 2008-03-22T20:38:28+00:00
url: /151
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
【Channelartlist 标记】用于获取当前频道的下级栏目的内容列表。该标记在封面模板（包括主页）中的经常被用到，具体用法见下面实例。   
除了宏标记外，channelArtlist 是唯一一个可以直接嵌套其它标记的标记，不过仅限于嵌套 {dede:type}{/dede:type} 和 {dede:arclist}{/dede:arclist} 两个标记。   
通过调试了解其使用方法   
我调试的方法是：   
将templets\default\文件夹下的index.html文件代码，全部掏空。放入调用【Channelartlist 标记】的代码，再在IE中访问网站主页index.php，就可以得到返回的数据。   
例1   
我调试【Channelartlist 标记】的具体代码如下：   
{dede:channelArtlist typeid="94" col="1"}   
<div style="width:500px;border:red solid 1px;float:left;">   
<div style="width:500px;background:#ccddee;">   
{dede:type}   
<a href="[field:typelink/]">[field:typename/]</a>   
{/dede:type}   
</div>   
<div style="width:500px;float:left;">   
<ul>   
{dede:arclist row="5"}   
<li><a href="[field:arcurl/]">[field:textlink/]</a></li>   
{/dede:arclist}   
</ul>   
</div>   
</div>   
{/dede:channelArtlist}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="345" alt="clip_image001" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannelartlist-1216eclip-image001-thumb.gif" width="555" border="0" />][1]   
注意：细心的朋友会发现，使用【Channelartlist 标记】时，需要你对div + css或者table的控制能力较强，否则在页面中很难控制它。请大家他细看下面例2，例1与例2代码上相差很小，但得到的布局却相差很大。仔细对比一下吧！   
例2   
我调试【Channelartlist 标记】的具体代码如下：   
{dede:channelArtlist typeid="94" col="1"}   
<div style="width:300px;border:red solid 1px;float:left;margin:5px;">   
<div style="width:300px;background:#ccddee;">   
{dede:type}   
<a href="[field:typelink/]">[field:typename/]</a>   
{/dede:type}   
</div>   
<div style="width:300px;float:left;">   
<ul>   
{dede:arclist row="5"}   
<li><a href="[field:arcurl/]">[field:textlink/]</a></li>   
{/dede:arclist}   
</ul>   
</div>   
</div>   
{/dede:channelArtlist}   
得到如下返回数据：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="256" alt="clip_image002" src="http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannelartlist-1216eclip-image002-thumb.gif" width="604" border="0" />][2]

 [1]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannelartlist-1216eclip-image001-2.gif
 [2]: http://lsvking.github.io/wp-content/uploads/2008/03/windowslivewriterdedecmschannelartlist-1216eclip-image002-2.gif
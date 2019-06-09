---
title: DedeCMS模板制作使用实例教程（六）【Mytag 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T19:20:13+00:00
url: /134
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
自定义宏标记【Mytag 标记】的作用：   
&#160; 可以将模板中多次出现的相同元素用一个自定义标记表示出来，从而达到，一次更改，全局更换的效果。辅助插件的广告管理也有相似的效果。

今天天涯来介绍下自定义宏标记的应用，大家可以进入后台，在&#8220;模板管理&#8221;-》&#8220;自定义宏标记&#8221;中查看到该选项。   
自定义宏标记的作用：   
可以将模板中多次出现的相同元素用一个自定义标记表示出来，从而达到，一次更改，全局更换的效果。辅助插件的广告管理也有相似的效果。   
适用范围：   
网页模板中多次出现的相同元素，例如：网站的导航条、网站的站点公告、网站的底部信息等，在我之前发布的几套模板中都运用到了自定义宏标记。   
自定义宏标记的调用办法：   
&#160; {dede:mytag name=&#8217;标记名称&#8217; ismake=&#8217;是否含板块代码（yes 或 no）&#8217; typeid=&#8217;栏目ID&#8217;/}   
1、name 标记名称，该项是必须的属性，以下 2、3是可选属性；   
2、ismake 默认是 no 表示设定的纯HTML代码， yes 表示含板块标记的代码；   
3、typeid 表示所属栏目的ID，默认为 0 ，表示所有栏目通用的显示内容，在列表和文档模板中，typeid默认是这个列表或文档本身的栏目ＩＤ。   
下面来通过一个实例进行说明：   
我有一个网站模板底部信息，其长度已经超出了系统可以设置的网站版权（cfg_powerby）的长度，但是我想实现一段代码，可以在不同模板（页面）中显示相同内容的效果。   
我们就可以使用自定义宏标记来实现这个效果   
如图进行设置：   
[<img style="border-right: 0px; border-top: 0px; border-left: 0px; border-bottom: 0px" height="450" alt="clip_image001" src="http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsmytag-10f34clip-image001-thumb.gif" width="599" border="0" />][1]   
然后我们回到模板制作的界面，将模板中的{dede:global name=&#8217;cfg_powerby&#8217;/}，替换为我们设置的自定义宏标记：   
{dede:mytag name=&#8217;footer&#8217;/},更新下，是不是已经变为我们设置的标记内容了啊。   
当然，自定义宏标记里面也可以加入dedecms的标记内容，适合当前栏目的显示内容，不过需要在调用代码中将ismake设为yes才可以，也可以通过设置typeid使自定义宏标记在特定栏目中显示。   
有人会问，我已经生成了很多页面了，现在想更改了一下自定义宏标记的内容，那岂不是要更改后重新再生成一遍，那样就不方便了。   
其实柏拉图早就考虑到这点，在自定义宏标记中可以使用javascript调用，这样以来，只要改变一次就可以实现全局改变的效果。   
具体操作：进入自定义标记管理，在相对应的标记管理项目中有JS调用这个选项，单击，dedecms自动生成调用该ID标记的js代码，例如< script src=&#8217;/plus/mytag_js.php?aid=1&#8242; language=&#8217;javascript&#8217;></script>   
我们将刚才的{dede:mytag name=&#8217;footer&#8217;/}用js替换掉，更新下，是不是还是原来的效果，我们再修改下标记的内容，怎么样？全局发生了变化。   
怎么样，自定义宏标记内容强大吧，相信他的引入会给你的模板制作带来更好的效果。

 [1]: http://lsvking.longshe.net/wp-content/uploads/2008/03/windowslivewriterdedecmsmytag-10f34clip-image001-2.gif
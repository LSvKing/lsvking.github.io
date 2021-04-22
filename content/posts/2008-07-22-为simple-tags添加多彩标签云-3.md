---
title: 为simple-tags添加多彩标签云
author: lsvking
type: post
date: 2008-07-22T13:00:18+00:00
url: /283
categories:
  - WordPress
  - 技术

---
<div id="Published By Juziyue:[4]1_A58B526FD28B4A2FB81A900DDB6B45F8_0A8DB854012046C1A14FD0BBC1385213">
  <div>
    此方法来<a href="http://blog.2i2j.com/2008/07/add-colorful-tags-cloud-for-simple-tags.html">自偶爱偶家</a>。
  </div>
  
  <div>
    言归正传， 首先我的修改是针对 simple tags 这个插件的， 其他的我就不说了， 你可以参照这里的方法自己研究。
  </div>
  
  <div>
    1、在simple-tags.client.php文件中查找该语句
  </div>
  
  <pre lang="html">function getColorByScale($scale_color, $min_color, $max_color)</pre>
  
  <div>
    2、注释掉上述函数中的以下语句（其实不注释掉也是无所谓的）
  </div>
  
  <pre lang="html">    $scale_color = $scale_color / 100;
$minr = hexdec(substr($min_color, 1, 2));
$ming = hexdec(substr($min_color, 3, 2));
$minb = hexdec(substr($min_color, 5, 2));
$maxr = hexdec(substr($max_color, 1, 2));
$maxg = hexdec(substr($max_color, 3, 2));
$maxb = hexdec(substr($max_color, 5, 2));
$r = dechex(intval((($maxr - $minr) * $scale_color) + $minr));
$g = dechex(intval((($maxg - $ming) * $scale_color) + $ming));
$b = dechex(intval((($maxb - $minb) * $scale_color) + $minb));</pre>
  
  <div>
    3、 在上述被注释掉的语句后增加如下语句（如果没有注释掉就必须加在后面， 否则无效）
  </div>
  
  <pre lang="html">//mod by hongfengye start
$r = dechex(rand(0,255));
$g = dechex(rand(0,196));
$b = dechex(rand(0,255));
//mod by hongfengye end</pre>
  
  <div>
    是的， 就是这么简单， 现在你应该就可以发现你的标签云(tags cloud)已经是彩色(colorful)的了。 效果图如下：
  </div>
  
  <div>
    <a href="0"><img src="http://lsvking.github.iot/wp-content/uploads/2008/07/a409af749acac6b825ab8cceb9b6998c4ce8cc0c1.png" alt="" width="207" height="357" /></a>
  </div>
</div>
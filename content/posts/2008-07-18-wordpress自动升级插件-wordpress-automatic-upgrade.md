---
title: WordPress自动升级插件 wordpress automatic upgrade
author: lsvking
type: post
date: 2008-07-18T13:44:56+00:00
url: /229
categories:
  - WordPress
  - 技术

---
&#160; 今天给博客升了下级，弄到2.6了，WP的升级实在麻烦，为此我找到了下面这款插件，作者网站好像在维护上不去了，我在这里把它发出来。

&#160; 将下载的文件传到插件目录下，启动插件，一直Next就差不多了，第一步他会备份数据库的，会给出个下载地址，大家最好下载到本地。我升级完后却怎么也登录不上后台了，想了一下清除了下Cookie就OK了。

他是从官方下载的版本安装的，大家安装完后，自己在去下中文包吧。

此插件是经过了如下几个步骤

  1. 1.备份数据库和文件到本地。 
  2. 2.从 <http://wordpress.org/latest.zip> 下载最新的补丁并解压。 
  3. 3.将你的站点设置为维护状态，主页被提示更新页暂时替换。 
  4. 4.锁定所有插件。 
  5. 5.后台更新 WordPress。 
  6. 6.在新窗口中显示更新后主页 
  7. 7.自动激活所有插件(按照 Keith 所说这一步应该可以实现，但是在我的 BLOG 上并没有完成，所有插件最后还是由我手动激活) 

个人角度来看，这款插件在很大程度上解决了因为 WordPress 版本更新的问题，而且最大限度的避免了数据和文件的丢失(其备份的过程和 WordPress Database Backup 插件基本类似)。由于使用 FTP 来进行更新操作，所以更新完成的速度也是很快的(我的BLOG更新大约前后用了不到一分钟)，基本不会因为更新而导致你的站点无法访问。

下载地址:[http://wordpress.org/extend/plugins/wordpress-automatic-upgrade/][1]

本站下载: 

<div class="wlWriterSmartContent" id="scid:8eb9d37f-1541-4f29-b6f4-1eea890d4876:387820d1-de5f-450f-8ced-dd5c5447f104" style="padding-right: 0px; display: inline; padding-left: 0px; padding-bottom: 0px; margin: 0px; padding-top: 0px">
  <p>
    <div>
      <a href="http://lsvking.cn/wp-content/uploads/2008/07/wordpress-automatic-upgrade12021.zip" target="_self">wordpress-automatic-upgrade.1.2.0.2.zip</a>
    </div>
  </p>
</div>

 [1]: http://wordpress.org/extend/plugins/wordpress-automatic-upgrade/ "http://wordpress.org/extend/plugins/wordpress-automatic-upgrade/"
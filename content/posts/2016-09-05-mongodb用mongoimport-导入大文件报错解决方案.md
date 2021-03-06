---
title: MongoDB用mongoimport 导入大文件报错解决方案
author: lsvking
type: post
date: 2016-09-05T15:41:13+00:00
url: /1152
categories:
  - 技术
tags:
  - Mongodb
description: 用Mongoexport 可以很方便的导出一个集合到Json格式 同时也可以用MongoImport 将数据导入进去,之前用的时候都没有导入太大的文件，大的数据迁移都是用的restore导入的。这次遇到一次数据迁移导出的json 文件大概有4.7G左右,再倒入的时候出现了问题
---
用Mongoexport 可以很方便的导出一个集合到Json格式 同时也可以用MongoImport 将数据导入进去,之前用的时候都没有导入太大的文件，大的数据迁移都是用的restore导入的。这次遇到一次数据迁移导出的json 文件大概有4.7G左右,再倒入的时候出现了问题

`mongoimport -h127.0.0.1 -d database -c indexs < indexs.dat`

却出现了如下的错误提示

<pre>2016-09-05T23:30:35.773+0800	connected to: 127.0.0.1
2016-09-05T23:30:37.653+0800	Failed: lost connection to server
2016-09-05T23:30:37.653+0800	imported 0 documents
</pre>

Mongo的错误提示也是醉了，这也忒不友好了, 完全是再猜,不过通过万能的大G还是搜到了解决方案,原来是因为Mongo对单次处理好像有大小限制（16m）好像是，所以大文件会出问题,这应该是个Bug mongoimport 默认会10000条 为一个批量导入数据，但实际上我的单条数据太大了,每51条数据就达到了16m 所以10000条导入一次肯定是不行的。幸好他有个参数 --batchSize 可以指定每次批量导入的条数 设置小一些就OK了。

`mongoimport -h127.0.0.1 -d database -c indexs < indexs.dat --batchSize 1`

这样你会看到他会分开执行导入任务

<pre>2016-09-05T23:12:48.622+0800	connected to: 127.0.0.1
2016-09-05T23:12:51.632+0800	d.indexs_value	42.6 MB
2016-09-05T23:12:54.626+0800	d.indexs_value	79.4 MB
2016-09-05T23:12:57.607+0800	d.indexs_value	115.9 MB
2016-09-05T23:13:00.618+0800	d.indexs_value	151.5 MB
</pre>
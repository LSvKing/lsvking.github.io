---
title: DedeCMS模板制作使用实例教程（五）【Autochannel 标记使用实例】
author: lsvking
type: post
date: 2008-03-22T19:16:50+00:00
url: /131
categories:
  - DEDECMS
  - 技术
tags:
  - 模版

---
{dede:autochannel partsort=&#8217;1&#8217;/}
  
{dede:channel typeid=&#8217;1&#8242;} [field:typename/] {/dede:channel}
  
{dede:autolist row=12 titlelen=38 orderby=pubdate partsort=&#8217;1&#8242;}
  
[field:textlink/] {/dede:autolist}

autochannel，autolist 是专门给懒人用的，partsort 的属性是表示排列顺序为某位置，它是栏目排列的位置，不是ID，这样的好处是，没有某个ID，只要有足够的栏目，也会显示内容，这个标记如果加了 typeid，则变成获取特定栏目的子栏目的这个排序位置的内容了
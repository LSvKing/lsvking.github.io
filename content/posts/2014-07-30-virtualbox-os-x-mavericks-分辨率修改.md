---
title: VirtualBox OS X Mavericks 分辨率修改
author: lsvking
type: post
date: 2014-07-30T10:16:11+00:00
url: /951
categories:
  - 技术
tags:
  - Mavericks
  - VirtualBox

---
需要开启EFI模式 然后在命令行下 VirtualBox目录 输入一下命令：

`VBoxManage setextradata "虚拟机名称" VBoxInternal2/EfiGopMode N`

其中 N 可以是 0,1,2,3,4,5 其中一个，分别代表 640&#215;480, 800&#215;600, 1024&#215;768, 1280&#215;1024, 1440&#215;900, 1920&#215;1200 几种分辨率
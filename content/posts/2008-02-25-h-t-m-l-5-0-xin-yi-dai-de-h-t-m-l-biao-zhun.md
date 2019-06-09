---
title: HTML 5.0 新一代的HTML标准~
author: lsvking
type: post
date: 2008-02-25T21:27:04+00:00
url: /95
categories:
  - 前端
  - 技术

---
      新千年以来，超文本标记语言（HTML）5 第一次向 HTML 中引入新的元素。新的结构元素包括 aside、figure 和section。新的内联元素包括time、meter和progress。新的内嵌元素有 video 和 audio。新的交互元素有 details、datagrid 和command
  
超文本标记语言（HTML）的开发到 1999 年 HTML 4 就停止了。万维网联盟（W3C）把重点转向将 HTML 的底层语法从标准通用标记语言（SGML）改为可扩展标记语言（XML），以及可缩放向量图型（SVG）、XForms 和 MathML 这些全新的标记语言。浏览器厂商则把精力放到选项卡和富站点摘要（RSS）阅读器这类浏览器特性上。Web 设计人员开始学习使用异步 JavaScript + XML（Ajax），在现有的框架下通过层叠样式表（CSS）和 JavaScript™ 语言建立自己的应用程序。但是在接下来的八年中，HTML 本身没有任何变化。

    最近，它又复活了。三家重要的浏览器厂商 — Apple、Opera 和 Mozilla Foundation — 成立了 Web Hypertext Application Technology Working Group（WhatWG）来开发传统 HTML 的新版本。最近，W3C 也注意到了这些活动，也启动了自己的新一代 HTML 项目，双方的成员有很多是相同的。这两个项目最终很可能合并。虽然很多细节还在争论之中，但下一版本 HTML 的大体轮廓已经清楚了。

     Web 开发人员从 1999 年就一直期待 HTML 的新版本（通常称为 HTML 5，但是也称为 Web Applications 1.0），现在它终于发布了。它保持了 HTML 原来的特色：没有名称空间或模式。元素不必结束。浏览器会宽容地对待错误。`<font face="Courier New">p</font>` 仍然是 `<font face="Courier New">p</font>`，`<font face="Courier New">table</font>` 仍然是 `<font face="Courier New">table</font>`。

     如果在 1999 年将一位 Web 开发人员冷冻起来，现在再解冻，那么他会遇到一些新的让人迷惑的元素。是的，他熟悉的元素（比如 `<font face="Courier New">div</font>`）仍然保留了；但是，HTML 现在还包含 `<font face="Courier New">section</font>`、`<font face="Courier New">header</font>`、`<font face="Courier New">footer</font>` 和 `<font face="Courier New">nav</font>` 等新元素。`<font face="Courier New">em</font>`、`<font face="Courier New">code</font>` 和 `<font face="Courier New">strong</font>` 仍然存在，但是增加了 `<font face="Courier New">meter</font>`、`<font face="Courier New">time</font>` 和 `<font face="Courier New">m</font>`。`<font face="Courier New">img</font>` 和 `<font face="Courier New">embed</font>` 仍然可用，但是还增加了 `<font face="Courier New">video</font>` 和 `<font face="Courier New">audio</font>`。但是，他仔细观察一下就会发现，这些元素实际上没什么区别。其中许多元素可能在 1999 年是开发人员需要而没有得到的。通过与他已经掌握的元素进行简单的类比，这些新元素都很容易理解。实际上，与 Ajax 或 CSS 相比，它们非常容易掌握。

     最后，当他打开 300MHz 的笔记本（运行的是 Windows 98，也是在 1999 年冷冻起来的）时，他可能对 Netscape 4 和 Windows® Internet Explorer® 5 中显示的新页面效果很吃惊。当然，这些老式浏览器不认识新元素，会完全忽略它们，但是页面仍然会显示，内容仍然是完整的。

      这并不是什么虚构的故事。HTML 5 的设计原则就是在不支持它的浏览器中能够平稳地退化。原因很简单：我们都是这样的 “原始人”。浏览器现在有选项卡、CSS 和 XmlHttpRequest，但是它们的 HTML 显示引擎仍然停留在 1999 年的水平。除了用户量大大增加之外，Web 其实在本质上没什么进步。HTML 5 考虑到了这一点。它目前为 Web 开发人员一些真正的好处，随着浏览器的缓慢升级，页面浏览者会逐渐享受到这些好处。
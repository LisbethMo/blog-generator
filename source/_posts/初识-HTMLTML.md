---
title: 初识 HTML
date: 2017-11-24 01:36:11
tags:
---
    刚开始接触 HTML，了解到 HTML 规范是由一个叫 W3C 的组织制定的。 
1、W3C 简介（摘自Wiki百科）
    - W3C 全称是万维网联盟（World Wide Web Consortium）
	- 历史：万维网联盟是由李爵士于1994年10月离开欧洲核子研究中心（
	  CERN）后成立的。
	- 标准：为了解决 Web 应用中不同平台、技术和开发者带来的不兼容
	  问题，W3C 制定了一系列标准并督促 Web 应用开发者和内容提供者
	  遵循这些标准。但是，W3C 制定的 Web 标准并非强制而只是推荐，
	  因此部分网站仍不能完全实现这些标准。
    在查询使用 HTML 文档的时候，又碰到了另一个网站，叫 MDN。
2、MDN 简介（摘自Wiki百科） 
    - MDN 的全称是 Mozilla Developer Network，是一个汇集众多Mozilla基
      金会产品和网络技术开发文档的免费网站。
    - 这个网站的文档非常的多，也很详细，很清楚明了，如果遇到前端的问题
      可以直接在Google搜索，然后看到MDN相关链接就进去。
    因为 HTML 是一门标记语言，所以我关注于它有哪些标签，于是就去查了
    W3C 网站的标准文档以及 MDN 的相关文档，发现除去那些已经被废弃，或
    者不被推荐使用的标签外，HTML 依旧有100多个标签需要学习。这是一个漫
    长的过程，简单地说几个。
3、HTML 的标签列表
    - 比如根元素的话就是<html>标签
    - 还有像<head>、<title>、<base>、<link>、之类存放文档元数据的标签
    - 又比如<body>、<article>、<section>、<nav> 之类的
    需要了解学习的标签很多，刚开始接触的时候，了解到有这么两个概念，一
    个叫空标签，一个叫可替换标签，于是我就想了解一下这两个到底是什么意思。
4、空元素（摘自 MDN）
    - 一个空元素（empty element）可能是 HTML、SVG，或者 MathML 里的一
      个不可能存在字节点的 element
    - 在HTML中，通常在一个空元素上使用一个闭标签是无效的
    - 在HTML 中有这些空元素：<area>、<base>、<br>、<col>、<colgroup>、
      <command>、<embed>、<hr>、<img>、<input>、<keygen>、<link>、
      <meta>、<param>、<source>、<track>、<wbr>
5、可替换元素（replaced element）
    - 可替换元素的展现不是由 CSS 来控制的，这些元素是一类外观和渲染都
      独立于 CSS 的外部对象。
    - 典型的可替换元素有<img>、<object>、<video>和表单元素，比如
      <textarea>、<input>.
    - 某些元素只在一些特殊情况下表现为可替换元素，例如<audio>和
      <canvas>
    - 通过 CSS content 属性来插入的对象，被称作匿名可替换元素
    - CSS 在某些情况下会对可替换元素做特殊处理，比如计算外编剧和一些
      auto值
    - 需要注意的是，一部分可替换元素，本身有尺寸和基线，会被像
      vertical-align之类的一些CSS属性用到
    初步接触 HTML 大概就了解到这些

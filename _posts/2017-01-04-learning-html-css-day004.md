---
layout: post
title: 小白学编程之HTML/CSS-Day004
date: 2017-1-04
categories: HTML/CSS
tags: [HTML,CSS]
---


小白学编程之HTML/CSS Day 004

![从此妈妈再也不用担心我不懂编程了](http://upload-images.jianshu.io/upload_images/147665-d809afbec1cf065a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 本期概览
这一篇是学习HTML/CSS的第四天，从这篇开始要学习Level 2 CSS，主要内容有
> 2.01 CSS是什么？
> 2.02 Selector是什么？
> 2.03 Selector书写语法规范
> 2.04 一个selector可定义多个属性
> 2.05 一个selector可包含多个标签

***

## 2.01 CSS是什么？
CSS 全称 Cascading Style Sheets，用来指定HTML的外表(appearance)。但是HTML里面有些类似于给一个房子搭主要架构(structure)，而CSS则是刷墙、贴墙纸决定这房子看起来(looks)是怎样的。

e.g.
![](http://upload-images.jianshu.io/upload_images/147665-8abc3610d9c21195.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 2.02 Selector是什么？
选中tags来创建一些东西，就叫做selector。
> Tags are selected by creating something called a selector.

## 2.03 Selector书写语法规范
Selector的书写语法规范(syntax)——按照以下格式来写selector。
![](http://upload-images.jianshu.io/upload_images/147665-892810548cc9b6c6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


例如最简单的selector写法如下，即不带`<>`的 `p` 。`text-decoration`是属性(property); `underline`是你赋予这个属性的值(value)。在下面的例子中，CSS语法翻译为白话文就是：给`p`标签里的文字加下划线。
![](http://upload-images.jianshu.io/upload_images/147665-12d138cdcf032934.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 2.04 一个selector可定义多个属性
一个selector可以定义多个属性(properties)，如下图所示，在`p` selector里不仅定义了文字装饰(text-decoration)要加下划线(underline)这个属性，还定义了文字颜色(color)这个属性为红色(red)。

![](http://upload-images.jianshu.io/upload_images/147665-e38556e4b0d0de20.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



## 2.05 一个selector可包含多个标签
Selectors会自动选择所有相同标签并应用定义的属性，下图中所有`li`标签内的文字都变成了红色。
![](http://upload-images.jianshu.io/upload_images/147665-94182d0d4814ffe5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

如果只想指定`ul`标签(parent tag)内的`li`内容为红色，要把parent tag 也写到selector里，如下图所示，这样只有`ul`里面列表的文字变成了红色，而`ol`里的列表没有改变。
![](http://upload-images.jianshu.io/upload_images/147665-1457f84a610fca3b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**贪多嚼不烂，练习练习再练习。**

***
# 下期预告
> - 基于动作和条件定义selector属性
> - pseudo-selectors
> - 在一个selector里加多个properites
> - selector、CSS什么的放在哪里
> - 扩展知识之Hexadecimal colors


欢迎来纠错，也欢迎提意见和任何问题~~~

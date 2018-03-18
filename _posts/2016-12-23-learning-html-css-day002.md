---
layout: post
title: 小白学编程之HTML/CSS-Day002
date: 2016-12-23
categories: HTML/CSS
tags: [HTML,CSS]
---

小白学编程之HTML/CSS Day 002


![从此妈妈再也不用担心我不懂编程了](http://upload-images.jianshu.io/upload_images/147665-d809afbec1cf065a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 上期回顾
在上一篇学习笔记中，主要学习了以下内容，可以翻阅[《小白学编程之HTML/CSS Day 001》](_posts/2016-12-21-learning-html-css-day-001.md) 查看具体内容
> 1.01 What is HTML | 什么是HTML
> 1.02 HTML tags | HTML 标签
> 1.03 `<h1>`tag | 标题标签
> 1.04 `<p>` tag | 自然段标签
> 1.05 `<ul>`和`<ol>` tag | 列表标签

上篇文章发出来以后有两点需要补充如下
1. 有人问需不需要Mac，答案windos和Mac都可以，事实上只要有个浏览器就OK了。
2. 上次我推荐在txt记事本或者[W3School的在线编辑器](http://www.w3school.com.cn/tiy/t.asp?f=html_basic)上进行HTML练习。有亲爱的读者朋友[yarving](http://www.jianshu.com/users/e3858c25553e/latest_articles)推荐可以在 [codeopen](http://codepen.io/#) 或者是 [jsfiddle](https://jsfiddle.net/) 上进行练习，看了一下，很酷的两个网站。我自己比较喜欢codeopen，因为界面酷炫，不像jsfiddle需要点击“Run”才能显示效果。还有很重要的一点，codeopen的code需要一个字符一个字符敲，而jsfiddle有自动补全功能，个人认为对于初学小白还是一个字一个字敲比较好。所以这篇文章里将使用codeopen进行效果演示。

[codeopen](http://codepen.io/#) 截图如下：


![codeopen截图](http://upload-images.jianshu.io/upload_images/147665-64de2b21b3d386b5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



[jsfiddle](https://jsfiddle.net/)截图如下


![jsfiddle截图](http://upload-images.jianshu.io/upload_images/147665-c80ecd1289d615c8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 本期概览
这一篇是学习HTML/CSS的第二天，主要内容有
> 1.06 Nesting tags| 标签的嵌套关系
> 1.07 `<body>` tag | 包含一切的<body>标签
> 1.08 `<head>` tag | `<head>` 标签
> 1.09 `<html>` tag | `<html>`　标签
> 1.10 DOCTYPE | 设置HTML版本


***
# 1.06 Nesting tags| 标签的嵌套关系
HTML标签有时候会包含另外的标签，在这种情况下，包含其他标签的标签叫做parent（爹和妈），被包含的标签叫做children（娃）。

像之前在使用列表标签时，`<li> </li> `被包含在`<ul> </ul>` （无序列表）或`<ol> </ol>` （有序列表），这时候`<ul> </ul>` 或`<ol> </ol>` 就被称为**parent**，`<li> </li>`就被称为**children**，如下图所示：


![6.nesting.png](http://upload-images.jianshu.io/upload_images/147665-fe0e79c5cd98a08a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




# 1.07  <body> tag | 包含一切的<body>标签
既然娃有爹妈，那么爹妈也有爹妈；在HTML里，所有能**通过网页显示（纯文字）内容**的标签都要被嵌套在`<body> </body>`标签里。

![7.bodytag.png](http://upload-images.jianshu.io/upload_images/147665-37dab937b9aee564.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



#  1.08 <head> tag | <head> 标签
既然任何网页显示的（文字）内容都需要放在`<body></body>`标签里。言外之意，就是`<body></body>`之外还有标签写的不是（纯文字）内容的显示，这就是`<head></head>`。

![8.headtag.png](http://upload-images.jianshu.io/upload_images/147665-bd75ab2d32bd104e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 1.09 <html> tag | <html>标签
HTML 当然少不了`<html></html>`标签，所有的HTML标签 都要放在`<html></html>`标签里面。

![9.htmltag.png](http://upload-images.jianshu.io/upload_images/147665-378a64044331bb6d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



# 1.11 DOCTYPE | 设置HTML版本
DOCTYPE 翻译为中文就是文件类型，这不是一个标签，所以不是成对出现，只有一个`<!DOCTYPE html>`，这个主要是用来指定HTML 版本。设定这个之后，浏览器可以知道如何更好的显示你的页面。

![10.doctype.png](http://upload-images.jianshu.io/upload_images/147665-05e85b46ec1fe297.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



扩展阅读之，如果还想知道更多 请前往 [`<!DOCTYPE>`声明](http://www.w3school.com.cn/tags/tag_doctype.asp)


**最后来总结一下**，
目前为止，学习了一份HTML文件包含四大类元素：DOCTYPE，`<html>`标签，`<head>`标签，`<body>`标签，每一类里面都需要填写不同的内容。层次结构如下图所示：

![summary.png](http://upload-images.jianshu.io/upload_images/147665-fcba4ec551152bb3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)





**贪多嚼不烂。建议一个字一个字敲，练习练习再练习。**

用目前学到的试着敲一个作品吧！下面是我的“黯然销魂虾”哟。

![sample销魂虾.png](http://upload-images.jianshu.io/upload_images/147665-1d636cf7ce395725.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


***

**_欢迎来纠错，也欢迎提意见和任何问题~~~_**

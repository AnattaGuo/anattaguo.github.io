---
layout: post
title: 小白学编程之HTML/CSS Day001
date: 2016-12-23
categories: HTML/CSS
tags: [HTML,CSS]
---

>版权声明
>本文无需授权即可转载
>转载时请务必注明作者及来源


![](http://upload-images.jianshu.io/upload_images/147665-cc55172095b634e6.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 写在前面的话
我本人是纯种文科生，纯度100％那种——中文系毕业。我对于编程就是纯种小白，纯度，也是100％那种。不过，我的口号是人不折腾枉少年。所以， Don't be afraid. Just Learn It.

这个系列是我的自学笔记，我是跟着code school上面一步一步学的，所以文中出现的一些例子是参照着教程重新敲的，当然也加入了自己现编的一些例子。

又因为这个教程是全英文，所以我会把每个专有名词的英文列出来，自己翻译为中文，由于我也不知道业内怎么叫，所以中文专有名词参考看就好。

秉承着**教是学的最好方法**的理念，所以每学完一个level，我尽量做笔记——也就是自己给自己写个教程，并尽量保持定期更新。

就酱，撸起袖子干吧。

# 本文概览
这一篇是学习HTML/CSS的第一天，主要内容有

> - 1.01 What is HTML | 什么是HTML
> - 1.02 HTML tags | HTML 标签
> - 1.03 `<h1>`tag | 标题标签
> - 1.04 `<p>` tag | 自然段标签
> - 1.05 `<ul>`和`<ol>` tag | 列表标签

# 1.01 What is HTML | 什么是HTML
## 1.01.1 HTML的定义及全称
HTML是一种网页语言，全称是**HyperText Markup Language**。翻译为中文就是：超文本标记语言。

## 1.01.2 HTML在哪里敲
一开始练习，HTML一般写在文本文件里，如windows下的txt记事本。

## 1.01.3 在哪里看HTML效果
在浏览器上看，如谷歌浏览器、IE浏览器、火狐浏览器等。

##1.01.4 怎么看效果
如果无特别申明，本文所有输入均是在txt记事本中进行，所有显示均是使用Chrome谷歌浏览器。

将txt记事本的后缀名`.txt`改成`.html`, 然后将html文件拖入到浏览器中即可查看效果。如果不想这么麻烦，可以使用W3School的在线编辑器：http://www.w3school.com.cn/tiy/t.asp?f=html_basic 在左边框敲代码，右边框可以实时预览。

***

# 1.02 HTML tags | HTML 标签
HTML tags 都是成对出现，有开始和结束标记（opening and closing tag）。

如`<h1> Recipe World</h1>`,

![2.opening and closing tag.PNG](http://upload-images.jianshu.io/upload_images/147665-5ebcd849a5ad817d.PNG?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
***

# 1.03 `<h1>` tag | 标题标签
`<h1></h1>`代表一级标题，一般用来显示网页标题或者公司名字等；
`<h2></h2>` 代表二级标题，一般用来显示网页主题；
`<h3></h3>` 代表三级标题，可以一直到`<h6></h6>`。

![3. title tag.png](http://upload-images.jianshu.io/upload_images/147665-f5c5006b26b03247.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

# 1.04 `<p>`tag | 自然段标签
`<p>` 代表paragraph，也就是段落的意思。

一般我们用回车来另起一段，但是在html语言里回车无法起到另起一段的效果，必须用`<p></p>`来标记。

下图例子分别显示了没有`<p></p>`标签和有`<p></p>`的效果显示。

![4.p tag.png](http://upload-images.jianshu.io/upload_images/147665-db6c977820cfa58a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

***

# 1.05 `<ul>` 和 `<ol>`tag | 列表标签
`<ul>`代表unordered list，也就是无序列表的意思；
`<ol>`代表ordered list，也就是有序列表的意思；
`<li>`代表list items，也就是列表的意思。
![5.list.png](http://upload-images.jianshu.io/upload_images/147665-726f712f81555313.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


***
最后，贪多嚼不烂。建议一个字一个字敲，练习练习再练习。

# ChangLog
- 20180318 sync to github, remove 下次预告章节
- 20161221 create

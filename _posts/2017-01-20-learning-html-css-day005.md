---
layout: post
title: 小白学编程之HTML/CSS-Day005
date: 2017-1-04
categories: HTML/CSS
tags: [HTML,CSS]
---


![Level 2 CSS](http://upload-images.jianshu.io/upload_images/147665-705f665ca7671139.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

# 本期概览
这一篇是学习HTML/CSS的第五天，从这篇开始要学习Level 2 CSS，主要内容有
> 2.06 Pseudo-selector
> 2.07 Pseudo-selector之first-child
> 2.08 CSS的代码放在哪里



## 2.06 Pseudo-selector？
Pseudo-selector，选定一个selector里的某个tag，并定义此tag在特定条件下的状态。
其写法如下
```
selector:pseudo-class {
    property:value;
}
```

没有pseduo-selector的CSS写法如下所示，在CSS里，我将“虾”的链接样式定义为没有下划线。
![2.06.1.png](http://upload-images.jianshu.io/upload_images/147665-2d17fe370a884ad9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


**如何为`a` 这个selector加入pseudo呢？如下图所示，`a`后面跟了pseudo-selector（hover），意思是，当鼠标悬浮在链接上时，这条链接的文字会变成深色。**

![2.06.2.png](http://upload-images.jianshu.io/upload_images/147665-72a091bed8db30b4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 2.07 Pseudo-selectors之first-child
有很多pseudo-selector可以用，`hover`只是其中一个，'first-child‘ 也是其中一个。
具体应用如下，在有序列表中，定义第一个子标签的字体颜色为红色。

![2.07.png](http://upload-images.jianshu.io/upload_images/147665-9a2b59c6040df437.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




## 2.08 CSS的代码放在哪里
CSS可以和HTML放在同一个文档里，也可以分开放。如果要把CSS和HTML放在一起的话，那么CSS应该写在`style`标签里，嵌套在`head`标签下：


![2.08.png](http://upload-images.jianshu.io/upload_images/147665-7b4c06b5088813c7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)



将CSS code放在单独文件里的做法是，先写好一份CSS文件，命名为“xxx.css", 如“style.css”。然后将此文件link到你的HTML文件里，在你的HTML文件的“head'标签下加入：
```
<link rel="stylesheet" type="text/css" href="style.css" />
```

***
# 下期预告
> The box
> Block-level tags
> Inline-level tags

**欢迎来纠错，也欢迎提意见和任何问题~~~**

# ChangLog
- 20180318 sync to github, remove 往期回顾章节
- 20170120 create

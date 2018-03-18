---
layout: post
title: 小白学编程之HTML/CSS-Day003
date: 2016-12-28
categories: HTML/CSS
tags: [HTML,CSS]
---


小白学编程之HTML/CSS Day 003

![从此妈妈再也不用担心我不懂编程了](http://upload-images.jianshu.io/upload_images/147665-d809afbec1cf065a.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


在上一篇学习笔记Day002中，主要学习了以下内容，

> Nesting tags| 标签的嵌套关系

> <body> tag | 包含一切的标签

> <head> tag | <head> 标签

> <html> tag | <html>标签

> !DOCTYPE | 设置HTML版本



# 本期概览

这一篇是学习HTML/CSS的第三天，主要内容有

> 11.Use `<a>` tag to make a link | 用`<a>` 标签来添加链接


## 11.1 `<a>` 标签要和href一起用

想给某部分文本加上链接，要使用到`<a></a>`标签。a代表anchor，锚点的意思。简单理解，如果给文字加上了`<a></a>`标签，说明这个文字会被锚定到另外一个地方。

但是要锚定定位到哪里呢？所以需要在`a` 后面加上`href`，讲清楚这文字到底要定位到哪里。`href`是**H**ypertext **Ref**erence的缩写，超文本参考引用。

我个人用“to where”来记，to就是a， href就是where，to where 就是 a href

例如
![](http://upload-images.jianshu.io/upload_images/147665-824b5f4c2c8cd218.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


```

<ul>

  <li><a href="https://www.douban.com/">豆瓣</a></li>

  <li><a href="http://www.jianshu.com/">简书</a></li>

</ul>

```

## 11.2 设定链接在当前窗口打开还是新窗口中打开

如是希望人家点了链接后在当前窗口中打开，需要加`targe="_self"`这样的字，英文意思是自己开自己，很好理解。

```
<a href="https://www.douban.com/" target="_blank">豆瓣</a>
```

如果希望在新的窗口中打开你的链接，那么就写`target=_blank`

```
<a href="http://www.jianshu.com/" target="_self">简书
```

![](http://upload-images.jianshu.io/upload_images/147665-d7b2fe0fe4148319.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


## 11.3 绝对路径和相对路径

给文本添加链接的时候会遇到两种格式的地址：

- 一种是长得像`http://XXX.com/XXX`，这就是绝对路（Absolute paths）径引用。

- 还有一种长得像`XXX.html`这种也就是前面没有`http://XXX.com`，这是相对路径（Relative paths）引用。

例如 你老婆喊你拿酱油过来做黯然销魂虾，如果是那自家的酱油，我们就不用复杂的说“把我们自己家的酱油拿过来”，而会直接说“把酱油拿来”——**这是相对路径**的喊法。如果拿别人家的酱油，我们就要指定是拿谁家酱油，这种情况下的喊法是“去隔壁老王家拿点酱油”——**这是绝对路径**的喊法。

也就是`http://gebilaowang.com/jiangyou.html`  

![](http://upload-images.jianshu.io/upload_images/147665-88fa2416fc379a5a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


# 12. Level 1 HTML 总结

这次就到这里了，到现在关于HTML部分基本知识也已经学习完了，如果忘记前面学过什么可以点文章开头链接复习一下

>1. What is HTML | 什么是HTML
>2. HTML tags | HTML 标签
3. `<h1>` tag | 标题标签
4. `<p> `tag | 自然段标签
5. `<ul>`和`<ol>` tag | 列表标签
6. Nesting tags| 标签的嵌套关系
7. `<body>` tag | 包含一切的`<body>`标签
8. `<head>` tag | `<head>` 标签
9. `<html>` tag | `<html>`标签
10. !DOCTYPE | 设置HTML版本
11. Use `<a>` tag to make a link | 用`<a>` 标签来添加链接


贪多嚼不烂，练习练习再练习。赶紧动手做个小作品吧，下面是我用所学到的HTML知识做的黯然销魂虾：

![Level1HTMLSample.png](http://upload-images.jianshu.io/upload_images/147665-9a174cc95e096b9e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
<!Doctype html>
<html>
  <head> </head>
  <body>
    <h1>黯然销魂虾的做法</h1>
    <p>跟着本菜谱，让你做出一盘黯然销魂虾。伤感虾仁，黯然销魂。</p>
    
    <h2>主料</h2>
      <ul>
        <li><a href="www.anranxiaohunxia.com">虾</a></li>
      </ul>
    
    <h2>辅料</h2>
      <ul>
        <li>葱</li>
        <li>姜</li>
        <li>红色干辣椒</li>
        <li>花椒</li>
        <li>生抽</li>
      </ul>
    
      <h2>步骤</h2>
      <ol>
        <li>如果你买回来的虾是活虾，先给下宝宝们年数遍
          <a href="http://baike.baidu.com/link?url=5XB6xX7c8qK0pLfLVw6ikqB-sieE-6r1zRBGat5bvcoI3NdrE2CxkMjImLB0ggcqDzwvBySUezVg8MrywWShF4Hg4n3pbV_wzc-JwQg8drRXe1f4Sdz3vq14RTVCwOb4" target="_blank">往生咒</a>。</li>
        <li>温柔滴将虾宝宝们的壳脱掉，头拿掉，虾线挑掉。</li>
        <li>葱、姜、蒜、干辣椒或切成末或切成片。</li>
        <li>锅热油，爆姜蒜爆香，再放干辣椒、花椒。</li>
        <li>放虾，翻炒几下后，倒一点料酒，适量生抽，一点醋，待虾肉变色，加点糖，试一下咸淡，炒一下就可以出锅了</li>
      </ol>
  </body>
</html>
```


# 下期预告

> Level 2 CSS，Selector

> Syntax, selector撰写格式

> 在一个selector里加多个properites

> 在一个selector里选择多个tags

> ……



***

欢迎来纠错，也欢迎提意见和任何问题~~~

---
layout: post
title: 如何push指定branch到git repo
date: 2017-3-01
categories: blog
tags: [编程笔记]
---

How to push a branch to git repo

在利用git做版本管理时，已经checkout了许多分支，如下所示。这时想push指定分支（story7_homepage2.0）到github，应该怎么做了。

```
MacBook-Pro ⮀ ~/jdstore ⮀ ⭠ story7_homepage2.0 ⮀ git branch
  EPIC-1
  EPIC-1-archive
  competion
  master
  story1
  story2
  story3
  story4
  story5
  story5_figaro
  story5_orderstatus
  story6header
* story7_homepage2.0
```

在命令窗口执行以下命令
`git add .`
`git commit -m ""`
`git push origin sotry7_homepage2.0`

```
MacBook-Pro ⮀ ~/jdstore ⮀ ⭠ story7_homepage2.0± ⮀ git add .
MacBook-Pro ⮀ ~/jdstore ⮀ ⭠ story7_homepage2.0± ⮀ git commit -m "upload gem 'fog' to 'fog-was';update carrierwave.rb"
[story7_homepage2.0 e392743] upload gem 'fog' to 'fog-was';update carrierwave.rb
 5 files changed, 15 insertions(+), 129 deletions(-)
 create mode 100644 lib/fog.rb
MacBook-Pro ⮀ ~/jdstore ⮀ ⭠ story7_homepage2.0 ⮀ git push origin story7_homepage2.0
Counting objects: 17, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (15/15), done.
Writing objects: 100% (17/17), 1.56 KiB | 0 bytes/s, done.
Total 17 (delta 12), reused 0 (delta 0)
remote: Resolving deltas: 100% (12/12), completed with 8 local objects.
To git@github.com:AnattaGuo/jdstore.git
 * [new branch]      story7_homepage2.0 -> story7_homepage2.0
```  

然后再去刷新Github的repo，发现`story7_homepage2.0`已经被成功的push上去了。

![](http://upload-images.jianshu.io/upload_images/147665-bac4d3bbb4e346a4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


![](http://upload-images.jianshu.io/upload_images/147665-4cd61c019a103b99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

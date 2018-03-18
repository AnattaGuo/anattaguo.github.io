---
layout: post
title: git-merge:如何merge一个branch到另外一个branch
date: 2017-2-28
categories: blog
tags: [编程笔记]
---

参考链接 http://superuser.com/questions/340471/how-can-i-merge-two-branches-without-losing-any-files

假如我现在有两个branch：story6header and competition. 我想把competition这个branch merge到 story6header 这个branch 上。执行以下操作：

> `git checkout story6header`   #切换到story6header分支
> `git merge competition`  #将competition merge到story6header
> `git status`   #查看story6header上的更改
> `git add .` #提交更改
> `git commit -m "add catagory function and seed"`  #提交commit信息

最后 不要忘记 push到github
`git push origin story6header`

**这也许是个错误的方法，我也不知道正确不正确，不过我尝试下来是成功了**。
***
20170715 更新
想了一下，觉得将一个分支merge到一个分支，这种做法不太合适，容易把branch搞乱，为了保持分支的干净整洁，还是建议将分支merge到master branch上。
所以，merge的正确方式应该是
```
git checkout master
git merge story6header
git branch -d story6header #删除此分支。这一步可选，我们可以选择删除分支，也可以选择保留，希望保留的话，这一步就不需要执行。
```

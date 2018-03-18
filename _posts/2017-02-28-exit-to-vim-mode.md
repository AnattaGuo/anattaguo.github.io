---
layout: post
title: 执行git-commit命令不小心进入了VI-VIM，怎么退出？
date: 2017-2-28
categories: blog
tags: [编程笔记]
---

参考链接http://stackoverflow.com/questions/19085807/please-enter-a-commit-message-to-explain-why-this-merge-is-necessary-especially

在vi模式下输入

To solve this:

> press "i"
> write your merge message
> press "esc"
> write ":wq"
> then press enter

 "i" is for "insert", "esc" is the exit the insertion, and ":wq" is just "write" and "quit".

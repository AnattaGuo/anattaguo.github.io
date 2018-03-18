---
layout: post
title: 如何快速新建一个Ruby-on-Rails项目
date: 2017-2-24
categories: blog
tags: [编程笔记]
---

此文根据如下链接撰写
https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1

首先必须安装Ruby on Rails。


#### 新建一个叫做`**myforum**`的Rails app（以下所有命令在iTerm中输入）：


```
rails new myforum
```


#### 生成 **MyForum** 的model

```
rails generate scaffold MyForm title:string descrption:text
```

把变更移到database
```
rake db:migrate
```

#### 编写seeds.rb文件，批量写入数据

打开`db/seeds.rb`文件，写入：

```
# db/seeds.rb

MyForum.create!(title: 'grocery shopping', descrption: 'pickles, eggs, red onion')
MyForum.create!(title: 'wash the car')
MyForum.create!(title: 'register kids for school', descrption: 'Register Kira for Ruby Junior High and Caleb for Rails High School')
Todo.create!(title: 'check engine light', descrption: 'The check engine light is on in the Tacoma')
Todo.create!(title: 'dog groomers', descrption: 'Take Pinky and Redford to the groomers on Wednesday the 23rd')

```

在ITerm里执行命令
```
rake db:seed
```

#### 设置主页路径

在 config/routes.rb 文件里, 加入 `root 'myforums#index'`

最后，在server上预览,在iTerm中输入：
```
rails s
```

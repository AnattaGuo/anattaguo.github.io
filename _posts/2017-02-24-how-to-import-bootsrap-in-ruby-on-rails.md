---
layout: post
title: 如何在RubyonRails项目里引用Bootstrap
date: 2017-2-24
categories: blog
tags: [编程笔记]
---

此文根据如下链接撰写
https://launchschool.com/blog/integrating-rails-and-bootstrap-part-1


Bootstrap是前端使用的framework，它包含（HTML）、CSS及Javascript, 其中

> - Bootstrap 的CSS放在rails application文件下的`assets/stylesheets/application.scss`.

> - Bootstrap 的Javascript 放在rails application文件下的`app/assets/javascripts/application.js`


### 1. 首先新建一个rails application
……

### 2. 通过Ruby Gems给Ruby装上Bootstrap
1. 在rails application的`gemfile`里加上如下gems：

```
# Gemfile
...

gem 'bootstrap-sass', '~> 3.2.0'   /** sass 是bootstrap的CSS预处理器 **/
gem 'autoprefixer-rails'

```

Autoprefixer (autoprefixer-rails) 是可选的，但是推荐安装。"It automatically adds the proper vendor prefixes to your CSS code when it is compiled."


2.保存gemfile的修改,then Run

```
bundle install
```

### 3. 导入Bootstrap的CSS assets
Bootstrap的CSS和JavaScript 要导入到 rails application 文件的 `app/assets`里面。

1. 重命名rails application的 `application.css`文件.

```
mv app/assets/stylesheets/application.css app/assets/stylesheets/application.scss
```

 2.在 `app/assets/stylesheets/application.css.sass` 文件里导入Bootstrap的CSS组件。

```
// app/assets/stylesheets/application.css.sass
...

@import "bootstrap-sprockets"
@import "bootstrap"
```

### 4. 导入 Bootstrap Javascript assets
在rails application的`app/assets/javascripts/application.js`文件里加入 如下代码：

```
// app/assets/javascripts/application.js
...

//= require jquery
//= require jquery_ujs
//= require turbolinks
//= require bootstrap-sprockets
//= require_tree .

```

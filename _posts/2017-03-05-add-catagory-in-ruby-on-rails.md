---
layout: post
title: 添加分类功能-Category-for-Ruby-On-Rails-app
date: 2017-3-5
categories: blog
tags: [编程笔记]
---

参考https://blog.skcript.com/implementing-categories-in-ruby-on-rails-14c2b5e77b34#.ugsdz8w8b
参考http://taomengdi99.logdown.com/posts/1420713

近日做了一个商品购物网站（https://github.com/AnattaGuo/jdstore2），想给admin账户添加商品分类功能。

1. 在命令端输入`rails g scaffold category name:string desc:text`
![Snip20170305_20.png](http://upload-images.jianshu.io/upload_images/147665-57cec15d505c8da9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

2. 在命令端输入`rake db:migrate`

3. 在命令端输入`rails generate migration AddColumnsToProducts category_id`，然后输入`rake db:migrate`
![Snip20170305_22.png](http://upload-images.jianshu.io/upload_images/147665-742f2e4d3844cc25.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

4. 建立product model和category model的relationship. 修改如下两个文件：
```
#app/models/product.rb
belongs_to :category
```
![Snip20170305_25.png](http://upload-images.jianshu.io/upload_images/147665-f2610836a96c1954.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
#app/models/category.rb
has_many :products
```
![Snip20170305_26.png](http://upload-images.jianshu.io/upload_images/147665-42eab464accb4dd8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)        5. 在admin::products#controller文件里给new、edit、update、create添加代码` @categories = Category.all.map{|c| [ c.name, c.id ] }`, 给product_params添加`:category_id`:

```
#app/controllers/admin/products_controller.rb

class Admin::ProductsController < ApplicationController

  layout "admin"
  before_action :authenticate_user!
  before_action :admin_required

  def index
    if params[:category].blank?
      @products = Product.all
    else
      @category_id = Category.find_by(name: params[:category]).id
      @products = Product.where(:category_id => @category_id)
    end
  end

  def new
    @product = Product.new
    @categories = Category.all.map{|c| [ c.name, c.id ] }
  end

  def edit
    @product = Product.find(params[:id])
    @categories = Category.all.map{|c| [ c.name, c.id ] }
  end

  def update
    @product = Product.find(params[:id])
    @product.category_id = params[:category_id]

    if @product.update(product_params)
      redirect_to admin_products_path
    else
      render :edit
    end
  end

  def create
    @product = Product.new(product_params)
    @product.category_id = params[:category_id]

    if @product.save
      redirect_to admin_products_path
    else
      render :new
    end
  end

  private

  def product_params
    params.require(:product).permit(:title, :description, :quantity, :price, :image, :category_id)
  end
end
```
![Snip20170305_33.png](http://upload-images.jianshu.io/upload_images/147665-d8052df42ad837de.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![ ](http://upload-images.jianshu.io/upload_images/147665-f6e9e435c8cbd3ad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![Snip20170305_35.png](http://upload-images.jianshu.io/upload_images/147665-b08b5277827164d3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)                 6. 在`app/views/admin/products/edit.html.erb` 和`app/views/admin/products/new.html.erb`两个文件里添加以下代码：

```
 <%= select_tag(:category_id, options_for_select(@categories), :prompt => 'Select one!') %>
```
![Snip20170305_29.png](http://upload-images.jianshu.io/upload_images/147665-7ea8455b4ef9fdf3.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)   7. 去[http://localhost:3000/categories](http://localhost:3000/categories) 新建类别
![new category.gif](http://upload-images.jianshu.io/upload_images/147665-34bc50e72fa18759.gif?imageMogr2/auto-orient/strip)      8. 将category的选项呈现在admin的页面上。在`app/views/layouts/admin.html.erb`里添加如下代码：
![ ](http://upload-images.jianshu.io/upload_images/147665-cb82598a3a20d84c.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

这样在http://localhost:3000/admin/products 下面就可看到catetory了
![Snip20170305_38.png](http://upload-images.jianshu.io/upload_images/147665-ca4ed978babd67df.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

 最终分类成果演示：
![new category-new product.gif](http://upload-images.jianshu.io/upload_images/147665-2b3dd6b13e409148.gif?imageMogr2/auto-orient/strip)

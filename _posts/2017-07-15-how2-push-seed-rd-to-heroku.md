---
layout: post
title: 如何把seed-rb推到Heroku上
date: 2017-7-15
categories: blog
tags: [编程笔记]
description: 不仅要研究成功者是如何成功的，有时候也要花点时间研究失败者是如何失败的
---

解法思路

在seed.rb 里输入
```
#账户的写法
#管理员账户
create_account = User.create([email: 'mjadmin@jdstore3.com', password:'123456', password_confirmation: '123456', is_admin: 'true'])
puts "Admin account created."

#一般账户
create_account = User.create([email: 'mjuser@jdstore3.com', password:'123456', password_confirmation: '123456', is_admin: 'false'])
puts "User account created."


#产品的写法
Product.create!(title: "Cup",
                description: "Nice Cup",
                price: 80,
                quantity: 10,
                image: open("http://ot4s5c6m1.bkt.clouddn.com/cup-glass-03.jpg")
                )
puts "Product created"

Product.create!(title: "Pen",
                description: "Wow Pen",
                price: 20,
                quantity: 100,
                image: open("http://ot4s5c6m1.bkt.clouddn.com/Pen.jpeg")
                )
puts "Product created"
```

![](http://upload-images.jianshu.io/upload_images/147665-7f067f658254a16f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

在terminal 里输入
```
rake db:seed
git add .
git commit -m "Add account and product to seed"
git push origin qiniu
git push heroku qiniu:master
heroku rake db:migrate
heroku rake db:seed
```

![](http://upload-images.jianshu.io/upload_images/147665-3a2c528aeb2bb531.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![](http://upload-images.jianshu.io/upload_images/147665-766e1405975d1ecf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

---
title: 三维空间的观察
date: 2018-04-19
tags: webGL
author: 孙继红
---
[学习地址:webGL中文网链接](http://www.hewebgl.com/article/getarticle/59)
###  1、 认识相机
相机  THREE.Camera  分为两类，正投影相机(THREE.OrthographicCamera)和透视投影相机(THREE.PerspectiveCamera)
[!两种相机的区别](http://www.hewebgl.com/attached/image/20130530/20130530145454_509.png)
###  2、 两者的区别
由上图可以看出透视投影远处比近处要小；而正投影的特点是远近高低比例都一样
在建筑工程领域，正投影例子很多，例如：
![正投影示例](http://www.hewebgl.com/attached/image/20130530/20130530145820_901.jpg)

###   3、正投影相机
构造函数 `OrthographicCamera(left,right,top,bottom,near,far)`
中文网实例的图特别清晰 ![投影详解](http://www.hewebgl.com/attached/image/20130530/20130530145859_920.jpg)

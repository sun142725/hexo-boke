---
title: 三维空间的观察
date: 2018-04-19
tags: webGL
author: 孙继红
---
[学习地址:webGL中文网链接](http://www.hewebgl.com/article/getarticle/59)
###  1、 认识相机
相机  THREE.Camera  分为两类，正投影相机(THREE.OrthographicCamera)和透视投影相机(THREE.PerspectiveCamera)
![两种相机的区别](http://www.hewebgl.com/attached/image/20130530/20130530145454_509.png)
###  2、 两者的区别
由上图可以看出透视投影远处比近处要小；而正投影的特点是远近高低比例都一样
在建筑工程领域，正投影例子很多，例如：
![正投影示例](http://www.hewebgl.com/attached/image/20130530/20130530145820_901.jpg)

###   3、正投影相机
构造函数 `OrthographicCamera(left,right,top,bottom,near,far)`
中文网实例的图特别清晰 ![投影详解](http://www.hewebgl.com/attached/image/20130530/20130530145859_920.jpg)
```bash
1、 left参数
left：左平面距离相机中心点的垂直距离。从图中可以看出，左平面是屏幕里面的那个平面。
2、 right参数
right：右平面距离相机中心点的垂直距离。从图中可以看出，右平面是屏幕稍微外面一点的那个平面。
3、 top参数
top：顶平面距离相机中心点的垂直距离。上图中的顶平面，是长方体头朝天的平面。
4、 bottom参数
bottom：底平面距离相机中心点的垂直距离。底平面是头朝地的平面。
5、near参数
near：近平面距离相机中心点的垂直距离。近平面是左边竖着的那个平面。
6、far参数
far：远平面距离相机中心点的垂直距离。远平面是右边竖着的那个平面。
有了这些参数和相机中心点，我们这里将相机的中心点又定义为相机的位置。通过这些参数，我们就能够在三维空间中唯一的确定上图的一个长方体。这个长方体也叫做视景体。
投影变换的目的就是定义一个视景体，使得视景体外多余的部分裁剪掉，最终图像只是视景体内的有关部分。
好了，看一个简单的例子：
var camera = new THREE.OrthographicCamera( width / - 2, width / 2, height / 2, height / - 2, 1, 1000 );
scene.add( camera );
这个例子将浏览器窗口的宽度和高度作为了视景体的高度和宽度，相机正好在窗口的中心点上。这也是我们一般的设置方法，基本上为了方便，我们不会设置其他的值。
```
###   4、透视投影相机
PerspectiveCamera( fov, aspect, near, far )
中文网实例的图特别清晰 ![投影详解](http://www.hewebgl.com/attached/image/20130530/20130530151418_279.jpg)
```bash
$ fov(视角)：这个最难理解,我的理解是,眼睛睁开的角度,即,视角的大小,如果设置为0,相当你闭上眼睛了,所以什么也看不到,如果为180,那么可以认为你的视界很广阔,但是在180度的时候，往往物体很小，因为他在你的整个可视区域中的比例变小了。
$ aspect(纵横比)： 窗口的横纵比，即宽除以高
$ near(近平面)： 眼睛距离近处的距离，不能为负值
$ far（远平面）： 表示远处的裁面
```
正投影和透视投影
![正投影](http://www.hewebgl.com/attached/image/20130530/20130530160142_562.jpg)   ![透视投影](http://www.hewebgl.com/attached/image/20130530/20130530160818_221.jpg)




---
title: 五彩的光源
date: 2018-04-19
tags: webGL
author: 孙继红
---
[文档地址](http://www.hewebgl.com/article/getarticle/60)
### 1、光源的基类
在three.js中，光源用Light来表示,它是所有光源的基类。构造函数`THREE.Light(hex)` 
他有一个参数hex，接收一个16进制的颜色，如：
var light = new THREE.Light(0xFF0000)
### 2、有基类派生出的其他种类光源
* THREE.AmbientLight(环境光)
* THREE.AreaLight(区域光)
* THREE.DirectionLight(方向光)
* THREE.PointLight(点光源)
* THREE.SpotLight(聚光灯)
### 3、材质和光源的关系
> 材质：在渲染程序中，他是表面各可视属性的结合，这些可视属性指表面的色彩、纹理、光滑度、透明度、反射率、折射率、发光度等。正是有了这些属性，才能让我们识别三维中的模型是什么做成的，也正是有了这些属性，我们计算机三维的虚拟世界才会和真实世界一样缤纷多彩

材质的真相=====>光

#### 不带任何光源的物体
var material = new THREE.MeshLambertMaterial({color: 0x000000}) // 兰伯特材质
![结果图](http://www.hewebgl.com/attached/image/20130515/20130515170232_15.png)

没有任何光源的时候，不论材质什么颜色，结果都将是黑色
####  兰伯特材质与光源
最常见的材质之一就是Lambert材质，这是在灰暗的或不光滑的表面产生均匀散射而形成的材质类型。比如一张纸就是Lambert表面。 首先它粗糙不均匀，不会产生镜面效果。我们在阅读书籍的时候，没有发现书上一处亮，一处不亮吧，它非常均匀，这就是兰伯特材质。

我们现在一直在使用环境光，从环境光的构造函数来看，它只有颜色，其位置对场景中的物体并没有影响，因为他是均匀的反射到物体的表面的。

####  环境光对物体的影响
环境光就是在场景中无处不在的光，它对物体的影响是均匀的，也就是无论你从物体的那个角度观察，物体的颜色都是一样的，这就是伟大的环境光。

####  方向光（平行光）
构造函数： `var light = new THREE.DirectionLight(hex,intensity)`
* hex: 光的颜色
* intensity: 光线强度，（0-1）默认为1





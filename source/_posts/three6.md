---
title: 3D模型
date: 2018-04-20
tags: webGL
author: 孙继红
---
[google的3D模型库](http://sketchup.google.com/3dwarehouse/)
[chrome浏览器加载本地文件](http://www.hewebgl.com/article/getarticle/105)
### 3D模型查看器
3D-Max,Maya  推荐使用 ParaView

###   模型
模型是由面组成，面分为三角形和四边形面。三角形和四边形面组成了网格模型。在Three.js中用THREE.Mesh来表示网格模型。THREE.Mesh可以和THREE.Line相提并论，区别是THREE.Line表示的是线条。THREE.Mesh表示面的集合。
`THREE.Mesh = function ( geometry, material )` // 接受两个参数  geometry 几何体 material  材质

###   模型的加载
![模型加载过程](http://www.hewebgl.com/attached/image/20140911/20140911145108_465.png)
注意：
```bash
1、服务器上的模型文件大多是存储的模型的顶点信息，这些信息可以以文本的方式存储的（并不一定需要用文本的方式存储）。Three.js支持很多种3D模型格式，例如ply，stl，obj，vtk等等。随着three.js的升级，会支持越来越多的文件格式，到目前为止，three.js已经能够支持市面上大多数3D模型格式了。

同时需要重点说明的是，如果认真理解完three.js对模型的加载、解析方法，那么写一种自己的3D文件解析器是非常便利的。

2、第二步是浏览器下载文本文件，这是一件很普通的事情，只需要使用javascript的异步请求就可以实现了。

3、Javascript解析文本文件并生成一个geometry，最终生成Mesh，也是一件简单的事情。我们会在后面介绍这个过程。

4、当产生Mesh后，将其加入到场景中，那就非常简单了。

Ok，整个模型的加载思路就是这样。


```

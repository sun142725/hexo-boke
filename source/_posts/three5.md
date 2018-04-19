---
title: 纹理入门
date: 2018-04-19
tags: webGL
author: 孙继红
---
[文档地址](http://www.hewebgl.com/article/getarticle/68)
###  纹理由图片组成
在three.js中，纹理类由THREE.Texture表示，其构造函数如下所示
THREE.Texture( image, mapping, wrapS, wrapT, magFilter, minFilter, format, type, anisotropy )
```bash
$ image: 图片类型  var image = THREE.ImageUtils.loadTexture(url); // url 是一个http://xxxx/aaa.jpg 的类似地址，javascript没有从本地加载数据的能力，所以没有办法从您电脑的C盘加载数据。
$  mapping: THREE.UVMapping()类型，表示纹理坐标
$  wrapS：表示x轴的纹理的回环方式，就是当纹理的宽度小于需要贴图的平面的宽度的时候，平面剩下的部分应该p以何种方式贴图的问题
$  wrapT：表示y轴的纹理回环方式。 magFilter和minFilter表示过滤的方式，这是OpenGL的基本概念，我将在下面讲一下，目前你不用担心它的使用。当您不设置的时候，它会取默认值，所以，我们这里暂时不理睬他。
$  format：表示加载的图片的格式，这个参数可以取值THREE.RGBAFormat，RGBFormat等。THREE.RGBAFormat表示每个像素点要使用四个分量表示，分别是红、绿、蓝、透明来表示。RGBFormat则不使用透明，也就是说纹理不会有透明的效果。
$  type：表示存储纹理的内存的每一个字节的格式，是有符号，还是没有符号，是整形，还是浮点型。不过这里默认是无符号型（THREE.UnsignedByteType）。暂时就解释到这里，有需要时，我们在仔细分析，或者给作者留言询问。
$  anisotropy：各向异性过滤。使用各向异性过滤能够使纹理的效果更好，但是会消耗更多的内存、CPU、GPU时间，暂时就了解到这里吧
```
示例 
```bash
var geometry = new THREE.PlaneGeometry( 500, 300, 1, 1 );
        geometry.vertices[0].uv = new THREE.Vector2(0,0);
        geometry.vertices[1].uv = new THREE.Vector2(2,0);
        geometry.vertices[2].uv = new THREE.Vector2(2,2);
        geometry.vertices[3].uv = new THREE.Vector2(0,2);
        //  坐标纹理部分
        //  这一块牵扯到图片的跨域 并亲javascript不能访问本地文件  Access-Control-Allow-Origin: *
        var texture = THREE.ImageUtils.loadTexture("http://www.google.cn/maps/vt/pb=!1m5!1m4!1i0!2i0!3i0!4i128!2m2!1e1!3i794!3m9!2szh-CN!3scn!5e1105!12m1!1e4!12m1!1e47!12m1!1e3!4e0!5m1!1e0",null,function(t) {});
        var material = new THREE.MeshBasicMaterial({map:texture});
        var mesh = new THREE.Mesh( geometry,material );
        scene.add( mesh )
```

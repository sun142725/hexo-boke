---
title: 点、线、面
date: 2018-04-18
tags: webGL
author: 孙继红
---
###  从点、线、面开始构建
* 创建一个点
`var point = new THREE.Vector3(4,8,9)` //  分别代表在XYZ轴的坐标
* 创建透视相机, 多了些参数，继续往下看(学成归来再补)
```bash
camera = new THREE.PerspectiveCamera(45, width / height, 1, 10000) //  创建透视相机
        camera.position.x = 0;
        camera.position.y = 1000;
        camera.position.z = 0;   // 相机位置
        camera.up.x = 0;
        camera.up.y = 0;
        camera.up.z = 1;
        camera.lookAt({
            x : 0,
            y : 0,
            z : 0
        });
```
* 声明一个可以存放点的几何体
`var geometry = new THREE.Geometry()`
* 声明一种线条材质
`var material = new THREE.LineBasicMaterial({ vertexColors: THREE.VexterColors})` // 一种线条的材质，并且多了参数，代表材质颜色由线条顶点颜色决定 具体参数见下图
```bash
LineBasicMaterial( parameters )

         Parameters是一个定义材质外观的对象，它包含多个属性来定义材质，这些属性是：

         Color：线条的颜色，用16进制来表示，默认的颜色是白色。

         Linewidth：线条的宽度，默认时候1个单位宽度。

         Linecap：线条两端的外观，默认是圆角端点，当线条较粗的时候才看得出效果，如果线条很细，那么你几乎看不出效果了。

         Linejoin：两个线条的连接点处的外观，默认是“round”，表示圆角。

         VertexColors：定义线条材质是否使用顶点颜色，这是一个boolean值。意思是，线条各部分的颜色会根据顶点的颜色来进行插值。（如果关于插值不是很明白，可以QQ问我，QQ在前言中你一定能够找到，嘿嘿，虽然没有明确写出）。

         Fog：定义材质的颜色是否受全局雾效的影响。
```
* 定义一个16进制颜色
```bash
 var color1 = new THREE.Color(0x444444), color2 = new THREE.Color(0xf65a41)
```
* 线的材质由两点的颜色决定
```bash
        var p1 = new THREE.Vector3(-100,0,100)
        var p2 = new THREE.Vector3(100,0,-100)
        geometry.vertices.push(p1)
        geometry.vertices.push(p2)
        geometry.colors.push(color1, color2)
        line =  new THREE.Line(geometry, material, THREE.LinePieces)
        scene.add(line)
```
------------画-------线-------完-------成---------------------------------
###  棋盘 源码见下
```bash
<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>网格</title>
    <script src="../three.js"></script>
</head>
<style>
    #canvas{
        width:100%;
        height: 600px;
        background-color: #333;
    }
</style>
<body>
<div id="canvas">

</div>
</body>
</html>
<script>
    var width = document.getElementById('canvas').offsetWidth
    var height = document.getElementById('canvas').offsetHeight
    //  创建场景
    var scene = new THREE.Scene()
    //  创建相机
    var camera
    function initCamera() {
        camera = new THREE.PerspectiveCamera(45, width/height,1 ,10000)
        camera.position.x = 0;
        camera.position.y = 1000;
        camera.position.z = 0;
        camera.up.x = 0;
        camera.up.y = 0;
        camera.up.z = 1;
        camera.lookAt({
            x: 0,
            y: 0,
            z: 0
        })
    }
    //  设置光源
    var light
    function initLight() {
        light = new THREE.DirectionalLight(0x0366d6, 1.0, 0)
        light.position.set(100,100,200)
        scene.add(light)
    }
    //  渲染器
    var renderer
    function initRenderer(){
        renderer = new THREE.WebGLRenderer({
            antialias: true
        })
        renderer.setSize(width,height)
        document.getElementById('canvas').appendChild(renderer.domElement)
        renderer.setClearColor(0xFFFFFF, 1.0)
    }
    //   划线
    function initObject() {
        var geometry = new THREE.Geometry()  //  创建几何体来存放点
        geometry.vertices.push(new THREE.Vector3(-500,0,0))
        geometry.vertices.push(new THREE.Vector3(500,0,0))
        var material = new THREE.LineBasicMaterial({color: 0xf65a41}) // 画线
        for(var i=0; i<=20; i++) {
            var line = new THREE.Line(geometry, material)
            line.position.z = i*50 - 500
            scene.add(line)
            var line = new THREE.Line(geometry, material)
            line.position.x = i*50 - 500
            line.rotation.y = Math.PI/180 * 90
            scene.add(line)
        }
    }
    function startThree() {
        initCamera()
        initLight()
        initRenderer()
        initObject()
        renderer.clear()
        renderer.render(scene, camera)
    }
    startThree()
</script>
```





















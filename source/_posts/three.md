[webGL中文网](http://www.hewebgl.com/article/getarticle/27)

### 三大组建
* 场景
`var scene = new THREE.Scene()`
* 相机
有很多种相机
` var camera = new THREE.PerspectiveCamera(75, window.innerWidth/window.innerHeight, 0.1, 1000)`
* 渲染器
`var renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.body.appendChild(renderer.domElement);
`
* 添加物体到场景中
`
var geometry = new THREE.CubeGeometry(1,1,2);  //  CubeGeometry(width, height, depth, segmentsWidth, segmentsHeight, segmentsDepth, materials, sides)
    // width/height/depth分别代表立方体XYZ三轴的长度，剩下的比较复杂，之后深入学习

    var material = new THREE.MeshBasicMaterial({color: 0xf65a41});
    var cube = new THREE.Mesh(geometry, material);
    scene.add(cube);
`
* 渲染

```bash
renderer.render(scene, camera);
原型
render( scene, camera, renderTarget, forceClear )

各个参数的意义是：

scene：前面定义的场景

camera：前面定义的相机

renderTarget：渲染的目标，默认是渲染到前面定义的render变量中

forceClear：每次绘制之前都将画布的内容给清除，即使自动清除标志autoClear为false，也会清除。
```
* 循环渲染
有实时渲染和离线渲染 两种方式
  * 离线渲染  事先处理好一帧一帧的图片，然后一次性渲染
  * 实时渲染：就是需要不停的对画面进行渲染，即使画面中什么也没有改变，也需要重新渲染。下面就是一个渲染循环：
  ```bash
  function render() {
    cube.rotation.x += 0.1;
    cube.rotation.y += 0.1;
    renderer.render(scene, camera);
    requestAnimationFrame(render);
}
其中一个重要的函数是requestAnimationFrame，这个函数就是让浏览器去执行一次参数中的函数，这样通过上面render中调用requestAnimationFrame()函数，requestAnimationFrame()函数又让rander()再执行一次，就形成了我们通常所说的游戏循环了。// 本质就是
  回调函数
  ```


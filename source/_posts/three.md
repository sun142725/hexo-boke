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

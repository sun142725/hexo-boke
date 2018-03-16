---
title: 模块化开发
date: 2017-10-12
tags: module
author: 孙继红
---
### CommonJS
`node.js为主要实践者`
`module`  `exports`  `require`  `global`
```bash
## socket.js
module.exports = function (io){
    console.log(io)
}
## index.js
// 引用自定义模块，不需要带 .js
var socket = require('./socket')
// 引用核心模块，不需要带路径
var http = require('http')
```

### ES6 Module
`export`  `import`
```bash
$  方式一
// 输出  dome.js
    export {add, dele}
// 引入
    import {add, dele} from './dome'
    add()  dele()

$  方式二
// 输出
    export default {add, dele}
// 引入
    import dome from './dome'
    dome.add()   dome.dele()
```

###  ES6模块化与CommonJS模块的差异
> CommonJS模块输出的值为拷贝，ES6模块输出的值是引用
    * CommonJS模块一旦输出一个值，模块内部的变化不会影响这个值
    * ES6模块是当解析脚本，遇到import会生成一个只读引用，去被加载的模块取值。ES6的import像是跨页面的变量调用，是动态引用，没有缓存，模块内部变化会直接影响这个值
> CommonJS模块是运行的时候加载,ES6模块是编译时输出接口。
    * CommonJS模块就是对象，输入时先加载整个模块，生成一个对象，然后再从这个对象上读取方法，这种加载被称为运行时加载
    * ES6模块不是对象，而是通过export命令显示只定输出的代码，import时采取静态命令的形式。即import时指定加载某个输出值，而不是加载整个模块，称为编译时加载

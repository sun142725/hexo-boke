---
title: ios中遇到的坑
date: 2018-01-12 16:56:37
tags: ios
author: 孙继红
---
### ios10
> vue项目在ios10上白屏的问题

* 打开 `build` 文件夹
* 找到 `webpack.prod.conf.js`文件
* 在`UglifyPlugin`的定义里添加关于`mangle`的选项

```$xslt
 new UglifyJsPlugin({
   uglifyOptions: {
     compress: {
       warnings: false
     },
     mangle: {
       safari10: true
     }
   },
   sourceMap: config.build.productionSourceMap,
   parallel: true
 }),
```

> vue项目在ios10上swiper插件报错的问题

  这是因为Swiper插件中用到了ES6的语法a = b c，a是b的c次方，而iOS 10的Safari里不认识这样的语法，认为这是一个错误，所以你需要让Swiper经过babel的包装，而缺省状态下babel是不对node_modules里的模块进行编译的
  
*  解决方法是在项目根目录下新建一个文件vue.config.js，在里面添加如下语句：
```$xslt
module.exports = {
  chainWebpack: config => {
    config.rule('js').include.add(/node_modules\/(dom7|swiper)\/.*/)
  }
}
```
> 在ios10,做原生跳H5时候白屏

```$xslt
你的表头白名单里要加入gap://ready和file:的权限，整个白名单可以如下这么写
<meta http-equiv="Content-Security-Policy" c gap://ready file:; style-src 'self' 'unsafe-inline'; img-src 'self' data:; script-src 'unsafe-inline' 'unsafe-eval'">
```

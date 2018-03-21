---
title: es6
date: 2018-01-12 16:56:37
tags: javascripts
author: 孙继红
---

### let/const
* let和var的区别：let声明的变量只有所在的代码块有效
* let没有变量的提升，只能先声明后使用
* const--常量，只可声明，不能改变
    ```bash
    const user={};
    user.name = 'zhangsan'
    console.log(user.name)
    // "zhangsan"
    //常量user储存的是一个地址，这个地址指向一个对象。
    //不可变的只是这个地址，即不能把user指向另一个地址，但对象本身的属性是可变的
    ```
### 变量的声明方法
es5: `var` `function`
es6: `var` `function` `let` `const` `import` `class`
### 块级作用域
* es5只有全局作用域和函数作用域没有块及作用域
* let实际是新增块及作用域
### set/map

### 函数的Rest参数和扩展
```bash
 function sum(...m){
 let total = 0;
 for(var i of m){
 total += i;
 }
 }
 sum(1,3,5,7)
 let arr1 = [1,2,3]
 let arr2 = [4,5,6]
 arr1.contact(arr2)
 
 let [a, b, c] = '123'
 let arr = [a,b,c]
 console.log(arr)
 ["1", "2", "3"]
 
```
### Promise
```bash
let checks = function(){
return new Promise(function(resolve,reject){
var a = Math.floor(Math.random()*2)
if(a){
resolve('success')
}else{
reject('error')
}
})
}
checks().then(res=>console.log(res))
.catch(err=>console.log(err))
```
### 箭头函数
* 当返回值有且只有一个时不用写return
`console.log((a)=>console.log(a))`
* 有多步时需要加{}
`console.log((a)=>{console.log(a)})`
* this的绑定
```bash
箭头函数中，this指向的固定化，并不是因为箭头函数内部有绑定this的

机制，实际原因是箭头函数根本没有自己的this，导致内部的this就是外

层代码块的this。正是因为它没有this，所以也就不能用作构造函数。
```
### 模板字符串

```bash
let a = '红红'
console.log(`${a}最帅`)

* '红红最帅'
```

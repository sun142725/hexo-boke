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
if(flag){
resolve({status:0,result:true})
}else{
reject('error')
}
})
}
checks().then(res=>console.log(res))
{status: 0, result: true}
```
### 箭头函数
* 当返回值有且只有一个时不用写return
`console.log((a)=>console.log(a))`
* 有多步时需要加{}
`console.log((a)=>{console.log(a)})`
### 模板字符串

```bash
let a = '红红'
console.log(`${a}最帅`)

* '红红最帅'
```
---
title: mongodb 入门
tag: server
author: 孙继红
---
[windows 安装mongodb](http://www.runoob.com/mongodb/mongodb-window-install.html)

[mongoose 文档](http://www.nodeclass.com/api/mongoose.html)
[mongodb中文社区](http://www.mongoing.com/)
## 基础知识
### 常用的数据类型
* String 字符串
* Integer 整数型值
* Boolean 布尔值
* Double 双精度浮点值
* Min/Max keys 将一个值与 BSON（二进制的 JSON）元素的最低值和最高值相对比。
* Arrays 用于将数组或列表或多个值存储为一个键
* Timestamp 记录文档或添加的具体时间
* Object 用于内嵌文档
* Null 用于空值
* Symbol 符号。该数据类型基本上等同于字符串类型，但不同的是，它一般用于采用特殊符号类型的语言。
* Date 时间日期用 UNIX 时间格式来存储当前日期或时间。你可以指定自己的日期时间：创建 Date 对象，传入年月日信息。
* Object ID 对象Id用于创建文档id
* Binary Data 二进制数据
* Code 代码类型。用于在文档中存储javascript代码
* Regular expression 用于存储正则
## 开始使用
```bash
mongod --logpath=/data/db/log/mongod.log --logappend --fork   //在服务器后台进程中打开
mongo  // 进入MongoDB后台管理
```
### 链接数据库
```bash
var mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/totoro')     //连接本地数据库totoro

var db = mongoose.connection;

module.exports = db;
```
### 创建表
```bash
var mongoose = require('mongoose');
var Schema = mongoose.Schema;
var userSchema = new Schema({
    username: {
        type: String,
        unique: true
    },
    password: {
        type: String
    }
});
// 将数据模型暴露出去
module.exports = mongoose.model('users', userSchema);
```

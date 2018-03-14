---
title: mongodb 入门
tag: server
author: 孙继红
---
[windows 安装mongodb](http://www.runoob.com/mongodb/mongodb-window-install.html)

[mongoose 文档](http://www.nodeclass.com/api/mongoose.html)
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
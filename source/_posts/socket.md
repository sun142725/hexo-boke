---
title: socket 入门
tag: server
author: 孙继红
---
# 聊天功能实现
### server
```bash
var express = require('express')
var app = express()
var server = require('http').Server(app)
var io = require('socket.io')(server, {
    pingInterval: 1000
})
$ 一个简易聊天室
io.on('connection', function(socket) {
    socket.on('content', function (data) {
        console.log(data)
        socket.broadcast.emit('news', {hello: data})
    })
})
app.get('/', function(req, res){
    res.sendFile(__dirname+'/index.html')
})
server.listen(18080, function(){
    console.log('服务器在18080端口启动');
});
```
### client
```bash

```
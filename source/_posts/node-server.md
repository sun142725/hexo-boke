---
title: 服务器上运行程序
tags: [server, node]
author: 孙继红
---
### node服务后台运行 
* 使用forever
`npm install forever -g`
* 启动服务
`forever start index.js`
* 停止服务
`forever stop index.js`
* 启动js文件并输出日志文件
`forever start -l forever.log -o out.log -e err.log index.js`
* 重启js文件
`forever restart index.js`
* 查看正在运行的进程
`forever list`

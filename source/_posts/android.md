---
title: android中遇到的坑
date: 2018-01-12 16:56:37
tags: android
author: 孙继红
---

> 使用vue-cli做单页面应用，在uc浏览器，微信浏览器，oppo等手机出现白屏

* 不支持es6语法
```$xslt
babel-loader转换es5语法,但是static文件属于静态文件，不转换
static文件夹中的js文件不能出现es6文件
```

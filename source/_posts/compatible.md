---
title: ie兼容
date: 2017-12-22
tags: [兼容]
author: 孙继红
---

###  使用强制
* 如果ie浏览器中，会让ie浏览器启用最高内核解析html代码
> <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />（目前百度采用这种写法）
```bash
<meta http-equiv="X-UA-Compatible" content="edge" />
<meta http-equiv="X-UA-Compatible" content="IE=edge">
//  几种ie的使用模式
// 让ie使用chrome引擎
<meta http-equiv=“X-UA-Compatible” content=“chrome=1″ />
// 强制ie8使用ie7模式来解析
<meta http-equiv=“X-UA-Compatible” content=“IE=EmulateIE7″><!– IE7 mode –>
  //或者
<meta http-equiv=“X-UA-Compatible” content=“IE=7″><!– IE7 mode –>
// 特定版本的IE支持所要求的兼容性模式
<meta http-equiv=“X-UA-Compatible” content=“IE=5; IE=8″ />

//  google的ie7 – js中是一个JavaScript库（解决IE与W3C标准的冲突的JS库），使微软的Internet Explorer的行为像一个Web标准兼容的浏览器，支持更多的W3C标准，支持CSS2、CSS3选择器。它修复了许多的HTML和CSS问题，并使 得透明PNG在IE5、IE6下正确显示。

<!–[if lt IE 7]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta)/IE7.js” type=”text/javascript”></script>
<![endif]–>
使IE5,IE6,IE7兼容到IE8模式

<!–[if lt IE 8]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.0(beta)/IE8.js” type=”text/javascript”></script>
<![endif]–>
使IE5,IE6,IE7,IE8兼容到IE9模式

<!–[if lt IE 9]>
<script src=”http://ie7-js.googlecode.com/svn/version/2.1(beta4)/IE9.js”></script>
<![endif]–>
```
* 如果在360浏览器中
```bash
// 启用极速模式
<meta name=”renderer” content=”webkit” /> 
// 启用ie兼容模式
<meta name=”renderer” content=”ie-comp” />  
// 启用ie标准模式
<meta name=”renderer” content=”ie-stand” />  
```

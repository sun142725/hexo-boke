---
title: css Hack
date: 2018-01-12 16:56:37
tags: css3
author: 孙继红
---
[CSDN freshlover的博客专栏](http://blog.csdn.net/freshlover/article/details/12132801)
###  原理
 >  由于不同的浏览器对css的支持和解析结果不一样，以及css优先级对浏览器解析结果的影响，所以要根据不同的浏览器应用场景来应用不同的css属性
  
###  方式
>  优雅降级，渐进增强

####  方法一  条件注释法
```bash
只在IE下生效
	<!--[if IE]>
	这段文字只在IE浏览器显示
	<![endif]-->
	
	只在IE6下生效
	<!--[if IE 6]>
	这段文字只在IE6浏览器显示
	<![endif]-->
	
	只在IE6以上版本生效
	<!--[if gte IE 6]>
	这段文字只在IE6以上(包括)版本IE浏览器显示
	<![endif]-->
	
	只在IE8上不生效
	<!--[if ! IE 8]>
	这段文字在非IE8浏览器显示
	<![endif]-->
	
	非IE浏览器生效
	<!--[if !IE]>
	这段文字只在非IE浏览器显示
	<![endif]-->
```

####   方法二   类内属性前缀法
* “-″减号是IE6专有的hack
* “\9″ IE6/IE7/IE8/IE9/IE10都生效
* “\0″ IE8/IE9/IE10都生效，是IE8/9/10的hack
* “\9\0″ 只对IE9/IE10生效，是IE9/10的hack

```bash
$ * ie(6~10)(Q)(兼容模式)  ie(6~7)(S)
$ + ie(6~10)(Q)  ie(6~7)(S)
$ - ie6(Q\S)专属
$ _ ie(6~9)(Q)   ie6(S)
$ # ie(6~10)(Q)  ie(6~7)(S) 

$
$
$ !important ie10(Q)  ie(7~10)(S)
```

####   方法三  选择器前缀法
给选择器加hack前缀
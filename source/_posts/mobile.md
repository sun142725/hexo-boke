---
title: 移动端注意点
date: 2017-05-12 16:56:37
tags: mobile
author: 孙继红
---
## 移动端遇到的一些问题

## 有关300ms延时
```bash
安卓已禁用屏幕放大缩小，主要针对iphone
方法一  禁止屏幕放大缩小
 <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

  方法二
  放弃click,使用touchend
```
###  使用a标签做按钮的时候或连接的时候，点击按钮会出现 "暗色的"背景
以及移动端IOS手机下清除输入框内阴影
```bash
	a,input,form{
		-webkit-tap-highlight-color:rgba(0,0,0,0);
		-webkit-appearance: none;

	}
```
###  属性控制元素在移动设备上是否使用滚动回弹效果.
```bash
body{
	-webkit-overflow-scrolling:touch;
	overflow-scrolling:touch;
	/* 当手指从触摸屏上移开，会保持一段时间的滚动 auto会立即停止 */
	font-size:0.14rem;
}
```
### 不同设备下的文本大小
```bash
*{
/*可以设为auto，none,百分比*/
   	-webkit-text-size-adjust: 100%;
   	text-size-adjust: 100%;
   	/*禁止用户选中*/
   	/*-webkit-user-select: none;*/
   	/*user-select: none;*/
   	 	max-height: 9999999px;
   	 	margin: 0px;
   	 	padding: 0px;
   	 	list-style: none;
	   box-sizing:border-box;
   }
```
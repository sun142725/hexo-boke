---
title: css奇淫技巧
tags: css
author: 孙继红
---
* 事件穿透
##### 语法
`pointer-events：auto | none | visiblepainted | visiblefill | visiblestroke | visible | painted | fill | stroke | all`
//  元素设置为none后，元素将不会成为点击事件的target,鼠标事件可以指向后代元素，在这种情况下，鼠标事件将在捕获或冒泡阶触发父元素的事件侦听器

* 显示节点层次结构
```bash
* { background-color: rgba(255,0,0,.2); }
* * { background-color: rgba(0,255,0,.2); }
* * * { background-color: rgba(0,0,255,.2); }
* * * * { background-color: rgba(255,0,255,.2); }
* * * * * { background-color: rgba(0,255,255,.2); }
* * * * * * { background-color: rgba(255,255,0,.2); }
```
* [!炫酷404](https://codepen.io/anon/pen/aRgWrg)
* [!hover.css](https://codepen.io/IanLunn/pen/hysxc)   [!git 地址](https://github.com/IanLunn/Hover/)

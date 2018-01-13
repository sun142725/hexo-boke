---
title: app-hbuilder
date: 2018-01-12 16:56:37
tags: mui
author: 孙继红
---
沉浸式状态栏

## 分类
 ### 1、正常
 ### 2、变色
 写法：
 使用5+API [plus.navigator.setStatusBarBackground）](https://hexo.io/docs/server.html)。

 首页配置
 首页需要在manifest.json文件中，plus->launchwebview下添加statusbar节点，并配置background的值（格式为#RRGGBB）。


 若首页为secondwebview，则调整launchwebview为secondwebview即可。

 终端支持：
 - Android5及以上系统支持；
 - iOS7.0及以上系统支持。

 前景色处理：
 当背景色调整后，如果调整不当，会造成前景的信号栏文字颜色与背景太相近，看不清前景，此时需要调整前景色。
 前景色的使用限制更多些，只能设置黑或白，通过plus.navigator.setStatusBarStyle('dark');设前景为黑色，'dark'换成light则前景色变为白色。
 同时前景色处理在终端支持方面：
 - Android5只有小米和魅族支持，Android6及以上所有安卓支持；
 - iOS7及以上支持

 > 高度处理：此时webview高度没有全屏，webview高度+状态栏高度=手机屏幕高度。


 ### 3、透明（也称沉浸式状态栏）

 一般会把状态栏变成透明，此时同时会处理成滚动后恢复为纯色title
  写法：

  HBuilder创建的应用默认不使用沉浸式状态栏样式，需要进行如下配置开启：
  打开应用的manifest.json文件，切换到代码视图，在plus -> statusbar 下添加immersed节点并设置值为true。
```bash
"plus": {
      "statusbar": {
          "immersed": true
      }
  }
```
  保存后提交App云端打包

  如果不生效，在distribute节点下的apple和goole两个节点下添加：

```bash
  "UIReserveStatusbarOffset": true,（apple节点下添加）
  "ImmersedStatusbar": true,/*设置为沉浸栏模式*/（goole节点下添加）
```



  终端支持：
  - Android4.4及以上系统支持；
  - iOS7.0及以上系统支持。
  前景色处理：
  与背景色调整相同，如果背景图颜色不当，会造成前景的信号栏文字颜色与背景太相近，看不清前景，此时需要调整前景色。
  前景色的使用限制更多些，只能设置黑或白，通过`plus.navigator.setStatusBarStyle('dark')`;设前景为黑色，'dark'换成light则前景色变为白色。
  同时前景色处理在终端支持方面：
  - Android5只有小米和魅族支持，Android6及以上所有安卓支持；
  - iOS7及以上支持

  > 高度处理：
  注意，此时webview高度为全屏，状态栏高度为0，也就是webview高度=屏幕高度。
  状态栏背景透明后前景图标覆盖在webview顶部。
  尤其注意此时dom里涉及fix定位计算的元素，可能需要重新排高度。
  在状态栏透明的情况下，转场动画时，webview动画是会通顶的，状态栏那里也会有条线左右移动。

  其他注意：
  沉浸式状态栏不支持动态调整，属于应用级，真机运行不生效，需要提交到云端打包后有效。
  一个app设置了沉浸式，就意味着里面的每个webview都变成沉浸式。
  这可能会造成很多页面都需要调整高度，此时有一种方案，就是在webview创建时，允许通过一个参数设置把这个webview的状态条再模拟显示出来，`plus.webview.create('http://m.weibo.cn/u/3196963860', 'test', {statusbar:{background:"#D4D4D4"}})`。这样设置后，webview的高度重新回到状态栏下方，不再顶到屏幕顶部。
  此api从HBuilder8.1 alpha版起生效。


 ### 4、全屏(没有状态栏)

  常见使用场景：如果页面是全屏游戏，一般会直接让状态栏消失，也就是页面全屏。webview高度全屏了，状态栏没有了。
  写法：
  设置应用全屏显示

  终端支持：
  没有终端类型限制
  > 高度处理：与状态栏透明相同，webview高度=屏幕高度，状态栏高度为0且不显示前景内容。需要注意dom元素的调整，注意顶部。
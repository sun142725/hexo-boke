---
title: audio,video
date: 2018-01-12 16:56:37
tags: video
author: 孙继红
---

## audio\video基础知识
###  属性
* audio.volume

(读/写) 音量

* audio.src

(读/写) 歌曲地址

* audio.currentTime

(读/写) 歌曲当前已播放时长

* audio.duration

(读) 歌曲的总长度

* audio.paused

(读) 布尔类型 是否处于暂停状态

* audio.ended

(读) 布尔类型 歌曲是否已经播放完毕

### 方法
* audio.play()   播放

* audio.pause()   暂停

###  事件
*   audio.oncanplay = fn()

 当歌曲下载完之后调用fn

* audio.onvolumechange = fn()

 当audio.volume发生变换的时候调用fn

* audio.onplay = fn()

 歌曲开始播放之后调用fn

* audio.onpause = fn()

 歌曲暂停之后调用fn

* audio.ontimeupdate = fn()

 歌曲在播放的过程中会一直调用fn

* audio.onended = fn()

 一首歌曲播放完之后调用fn

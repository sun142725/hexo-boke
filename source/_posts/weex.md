---
title: week
date: 2018-11-8 16:56:37
tags: weex
author: 孙继红
---
`Write Once, Run Anywhere`

* [weex 官网](http://weex.incubator.apache.org/cn/guide/index.html)
* [weex ui](https://github.com/alibaba/weex-ui)
* [weex ui中文文档](https://alibaba.github.io/weex-ui/#/cn/packages/wxc-button/)
* [Use Weex Ui with weex-toolkit](https://alibaba.github.io/weex-ui/#/docs/with-weex-toolkit)


### 源码参考
* [网易严选app感受weex开发](https://github.com/zwwill/yanxuan-weex-demo?utm_source=wechat_session&utm_medium=social)
* [基于Weex开发，适配Android\IOS\Web](https://github.com/CarGuo/GSYGithubAppWeex)

### 基础步骤

#### 初始化
```bash
// 全局安装weex-toolkit
npm install weex-toolkit -g
// 这条命令会向你命令行环境中注册一个 weex 命令。你可以用 weex create 命令来创建一个空的模板项目：
weex create awesome-app
// 命令执行完以后，在当前目录的 awesome-app 文件夹里就有了一个空的 Weex + Vue.js 项目。
```
#### 开发
```bash
npm install
npm start
```
然后工具会启动一个本地的 web 服务，监听 8081 端口。你可以打开 http://localhost:8081 查看页面在 Web 下的渲染效果。 源代码在 src/ 目录中，你可以像一个普通的 Vue.js 项目一样来开发.
除此之外，你还可以打开 http://localhost:8081/preview.html 开启一个预览页面，它会把 web 端的页面放在一个 iframe 中渲染，而且在右侧生成一个二维码。用 [Weex playground app](http://weex.incubator.apache.org/cn/tools/playground.html) 扫描这个二维码可以看到页面在手机上渲染的真实效果。
#### 编译和运行
默认情况下 weex create 命令并不初始化 iOS 和 Android 项目，你可以通过执行 weex platform add 来添加特定平台的项目。
```bash
weex platform add ios
weex platform add android
```
为了能在本地机器上打开 Android 和 iOS 项目，你应该配置好客户端的开发环境。对于 iOS，你应该安装并且配置好 [Xcode](https://developer.apple.com/xcode/)，对于android，你应该安装并且配置好[Android Studio](https://developer.android.com/studio/index.html)。当开发环境准备就绪后，运行下面的命令，可以在模拟器或真实设备上启动应用：
```bash
weex run ios
weex run android
weex run web
```
若遇到无法获取资源的错误，则是因为没有科学上网问题，需要更换依赖库下载地址。在项目文件夹`\platforms\android`找到`build.gradel`文件，将maven地址更改为阿里云的镜像地址，并注释掉前面的代码。
https://blog.csdn.net/zjw_python/article/details/81700719
```bash
buildscript {
    repositories {
        // mavenLocal()
        //jcenter()
        // mavenCentral()
        maven {
            url 'http://maven.aliyun.com/nexus/content/groups/public'
        }
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.2.2'
        classpath 'com.taobao.android:weexplugin-gradle-plugin:1.3'
    }
}

allprojects {
    repositories {
        // mavenLocal()
        //jcenter()
        // mavenCentral()
        maven {
            url 'http://maven.aliyun.com/nexus/content/groups/public'
        }
    }
}
```
### [参坑参考](https://www.jianshu.com/p/497f1a9ff33f)

### 环境变量
**weex.config.env === WXEnvironment**

### [常见坑](./weex_write.md)
---
title: app-cordova
date: 2018-01-12
tags: cordova
author: 孙继红
---
使用cordova打包app环境配置
### 安装nodejs

### 安装 cordova
### Cordova 打包成安卓APK需要用到ANT打包工具，首先配置好java环境：

下载安装Java JDK,在弹出的界面中建议使用默认值，所以一直点击“next>”,直到完成。

```bash
在系统变量中添加 JAVA_HOME   C:\Program Files\Java\jdk1.8.0_31
```

```bash
在Path中添加  %JAVA_HOME%\bin;
```

```bash
在命令行输入“Javac”，测试是否安装成功。
```



### 到ANT官方网站http://ant.apache.org/ 下载最新版本，解压至电脑。

```bash
在系统变量中添加 ANT_HOME   D:\WorkTools\apache-ant-1.9.4
```

```bash
在Path中添加   %ANT_HOME%\bin\
```

```bash
 查看是否安装成功：在dos窗口中输入命令ant
```


### 下载Android SDK，下载地址：http://developer.android.com

```bash
在系统变量中添加 ANDROID_HOME   D:\Program Files\adt-bundle-windows\sdk
```

```bash
在Path中添加   %ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools;
```

 Android SDK下载完毕后需要下载组件，否则打包时报错：[ Error: Please install Android target: "android-21"]



### 使用 Cordova 打包 app

创建项目（创建的时候文件夹必须存在）：

```bash
$cordova create [directory] [add-id] [app-name]
将web页面文件拷贝至项目的www目录下，cd进入项目文件夹，添加设备：

    $ cordova platform add ios
    $ cordova platform add amazon-fireos
    $ cordova platform add android
    $ cordova platform add blackberry10
    $ cordova platform add firefoxos
```
查看设备列表
```bash
  $ cordova platforms ls
```

删除一个设备

```bash
$ cordova platform remove blackberry10
$ cordova platform rm amazon-fireos
$ cordova platform rm android
```

打包
```bash
打包所有设备app

$ cordova build
或者只打包一个设备

$ cordova build android
```

```bash
测试app（在虚拟机或者连接的安卓设备上）

$ cordova emulate android

 打包并在虚拟机或者安卓设备上测试app

$ cordova run android
```

Cordova插件安装
```bash
$cordova plugin add [plugin-id]
$ cordova plugin add https://github.com/apache/cordova-plugin-console.git
```

例如：安装一个二维码扫描插件

```bash
$cordova plugin add com.blackberry.community.barcodescanner
```

查看插件列表

```bash
$ cordova plugin ls
```

删除一个插件

```bash
$ cordova plugin rm org.apache.cordova.console
$ cordova plugin remove org.apache.cordova.console    # same
```


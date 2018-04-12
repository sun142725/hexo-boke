---
title: git
tags: git
author: 孙继红
---
[阮一峰](http://www.ruanyifeng.com/blog/2014/06/git_remote.html)
### 基础知识
* 创建仓库
`git init`
* 克隆
git clone
* 添加或删除
`git add .`   `git add *`  `git add <file>`
* 检查
注意多用git status 检查上传内容以及所在分支
`git status`
* 创建分支
`git branch <name>`
* 切换分支
`git checkout <name>`
`git checkout -b <name>` 创建并切换
* 检查当前分支
`git branch`
commit
* 只要有变化就必须commit
`git commit -m ""`
* push
push前看好所在分支
第一次推送前注意
`git push -u origin master`
`git push`

### 在服务器搭建git环境
```bash
$ 1.安装
  sudo apt-get install git
$ 2 设置账号密码
  useradd -m <account>
  passwd <account>
$ 3 创建 git 仓库并初始化
  mkdir -p /data/repositories
  初始化  cd /data/repositories/ && git init --bare test.git
  * git init --bare test.git初始化的远程仓库没有工作目录
$ 4 配置用户权限
  chown -R <account>:<account> /data/repositories
  chmod 755 /data/repositories
  查找git-shell所在目录，编辑/etc/passwd文件，将最后一行关于《account》de denglu shell配置改为git-shell目录下  使用which git-shell查看文件位置
  实例： gituser:x:500:500::/home/gituser:/usr/local/git/bin/git-shell
$ 5 蒋项目克隆到本地
  git clone <account>@<您的 CVM IP 地址>:/data/repositories/test.git
```

### insufficient permission for adding an object
  原因  git库权限问题  `ls -la`查看权限
  解决  sudo chown -R <account>:<account> /data/repositories

### 在服务器初始化有工作目录的git仓库
* # 远程服务器初始化仓库
   git init <仓库名>
   # 设置允许远程接收文件
   git config receive.denyCurrentBranch ignore

* 在远程仓库,post-receive 钩子文件中添加自动更新工作目录内容
$ cd /home/git/test.git/hooks/
$ vim post-receive  
  WORK_TREE='../'
  git  --work-tree="${WORK_TREE}" reset --hard

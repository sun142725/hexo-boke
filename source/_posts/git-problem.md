---
title: git遇到的问题
author: 孙继红
---
``fatal: The remote end hung up unexpectedly
解决内存不够
``解决办法
`git config --global http.postBuffer 524288000`
`git config --global https.postBuffer 1048576000`

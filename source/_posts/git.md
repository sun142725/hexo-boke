---
title: git
author: 孙继红
---
``fatal: The remote end hung up unexpectedly
``解决办法
`git config --global http.postBuffer 524288000`
`git config --global https.postBuffer 1048576000`
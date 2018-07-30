---
title: Vue
tag: Vue
author: 孙继红
---
[vue实例、教程、实用库](https://github.com/opendigg/awesome-github-vue#UI%E7%BB%84%E4%BB%B6)
* 双向数据绑定  `Object.defineProperty`

### 项目中sass全局使用依赖
* sass-resources-loader
```bash
scss: generateLoaders('sass').concat(
      {
        loader: 'sass-resources-loader',
        options: {
          resources: path.resolve(__dirname, '../src/page/common/common.scss')
        }
      }
    ),
```

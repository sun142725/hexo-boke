[解决ie7,ie8](https://zhidao.baidu.com/question/583799354335504245.html)
###  使用强制
* 如果ie浏览器中，会让ie浏览器启用最高内核解析html代码
```bash
<meta http-equiv="X-UA-Compatible" content="edge" />
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```
* 如果在360浏览器中
```bash
// 启用极速模式
<meta name=”renderer” content=”webkit” /> 
// 启用ie兼容模式
<meta name=”renderer” content=”ie-comp” />  
// 启用ie标准模式
<meta name=”renderer” content=”ie-stand” />  
```

---
title: react Component
date: 2018-01-12 16:56:37
tags: react
author: 孙继红
---
### 组件的声明方式
* 函数式定义 `无状态组件`
* es5原生方式  `React.createClass`
* es6形式的  `extends React.Component

#### [无状态组建](https://reactjs.org/blog/2015/10/07/react-v0.14.html#stateless-functional-components)

``
在react项目中，大多数组件被写成无状态的组件，通过简单组合可以构建成其他的组件
``
```bash
const Home = (data) => (
    <div>
        <h2>喜欢{data.name}</h2>
    </div>
)
export default Home;
```

```bash
$ 组件不会被实例化，整体渲染性能得到提升
因为组件被精简成一个render方法的函数来实现的，由于是无状态组件，所以无状态组件就不会在有组件实例化的过程，无实例化过程也就不需要分配多余的内存，从而性能得到一定的提升。
$ 组件不能访问this对象
无状态组件由于没有实例化过程，所以无法访问组件this中的对象，例如：this.ref、this.state等均不能访问。若想访问就不能使用这种形式来创建组件
$ 组件无法访问生命周期的方法
因为无状态组件是不需要组件生命周期管理和状态管理，所以底层实现这种形式的组件时是不会实现组件的生命周期方法。所以无状态组件是不能参与组件的各个生命周期管理的。
$ 无状态组件只能访问输入的props，同样的props会得到同样的渲染结果，不会有副作用
```
无状态组件被鼓励在大型项目中尽可能以简单的写法来分割原本庞大的组件，未来React也会这种面向无状态组件在譬如无意义的检查和内存分配领域进行一系列优化，所以``只要有可能，尽量使用无状态组件``。

#### React.createClass
* React.createClass会自绑定函数方法（不像React.Component只绑定需要关心的函数）导致不必要的性能开销，增加代码过时的可能性。
* React.createClass的mixins不够自然、直观；React.Component形式非常适合高阶组件（Higher Order Components--HOC）,它以更直观的形式展示了比mixins更强大的功能，并且HOC是纯净的JavaScript，不用担心他们会被废弃。HOC可以参考无状态组件(Stateless Component) 与高阶组件。

#### React.Component
函数需手动绑定


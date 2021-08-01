---
title: 前端面试题
tags: 
- 前端面试
- Js
- Css
- Vue
categories: 前端
date: 2021-08-01 23:00:00
top_img: ../../img/bz-d.jpg
cover: ../../img/bz-d.jpg
---
个人前端面试经历，经典的面试题.

## Git

### Git常用指令

``` Git
$ 将远程仓库里的代码复制到本地：git clone 仓库地址.   
将暂存区的改动推送到远程仓库里：git push.
将远程仓库的代码拉取到本地：git pull. 
创建分支：git branch 分支名.
切换分支：git checkout 分支名.
合并分支：git merge 分支名.
删除分支：git branch -d 分支名.
```
More info: [Git](https://https://gitee.com/wlmwwww)

## Css

### 垂直居中的方法？

``` 
$ 垂直居中常用的2种
flex  方法
父元素设置
display：flex
justify-content：center
align-item：center.

position + transform 方法
父元素设置相对定位
子元素设置绝对定位
left:50%
top:50%
transform:translate(-50%,-50%)
```

### 常见问题

``` 
$ css常见问题
父类塌陷怎么解决？
为父元素添加overflow：hidden

添加伪类元素   div::after{ content:"" }

<style>
        table tr:nth-child(even){/*偶数行*/
            background: #ccc;
        }
        table tr:nth-child(odd){/*奇数行*/
            background: #0000ff;
        }
    </style>
```

### Css优化

``` 
$ 优化 CSS
减少关键 CSS 元素数量
```


## Js

### Js的数据类型

``` js数据类型
$ 基础数据类型.
string  number  boolean null undefined   symbol.
引用数据类型.
Object  function 数组.
```

### Js的内置对象
``` JS有哪些内置对象？
$ 数据封装类对象：Object、Array、Boolean、Number、String
其他对象：Function、Arguments、Math、Date、RegExp、Error
ES6 新增对象：Symbol、Map、Set、Promises、Proxy、Reflect

```

### Js的组成
``` JavaScript由以下三部分组成:
$ ECMAScript（核心）：JavaScript 语言基础
DOM（文档对象模型）：规定了访问 HTML 和 XML 的接口
BOM（浏览器对象模型）：提供了浏览器窗口之间进行交互的对象和方法
```
### this对象的理解
``` this 总是指向函数的直接调用者
$ 如果有 new 关键字，this 指向 new 出来的实例对象
在事件中，this 指向触发这个事件的对象
IE 下 attachEvent 中的 this 总是指向全局对象 Window
```
### Dom的操作

``` DOM 操作——怎样添加、移除、移动、复制、创建和查找节点?
创建新节点
$ createDocumentFragment() //创建一个 DOM 片段
createElement() //创建一个具体的元素
createTextNode() //创建一个文本节点
添加、移除、替换、插入
appendChild()
removeChild()
replaceChild()
insertBefore() //在已有的子节点前插入一个新的子节点
查找
getElementsByTagName() //通过标签名称
getElementsByName() // 通过元素的 Name 属性的值(IE 容错能力较强，会得到一个数组，其中包括 id 等于 name 值的) \* getElementById() //通过元素 Id，唯一性

```

### Js的深浅拷贝

``` 
$ 深浅拷贝
浅拷贝：也就是拷贝A对象里面的数据，但是不拷贝A对象里面的子对象.
深拷贝：会克隆出一个对象，数据相同，但是引用地址不同（就是拷贝A对象里面的数据，而且拷贝它里面的子对象).
```

### es6

``` 
$ es的常见问题
var let const 三者的区别
var声明变量可以重复声明
let声明变量不可重复声明
const声明常量不可改变
Set、Map的区别？
Set用于数据重组，Map用于数据储存
Set：
（1）成员不能重复
（2）只有键值没有键名，类似数组
（3）可以遍历，方法有add, delete,has
Map:
（1）本质上是健值对的集合，类似集合
（2）可以遍历，可以跟各种数据格式转换

Promise构造函数是同步执行还是异步执行，那么 then 方法呢？
promise构造函数是同步执行的，then方法是异步执行的

Promise 中reject 和 catch 处理上有什么区别？
reject 是用来抛出异常，catch 是用来处理异常

forEach, for in ,for of 三者的区别？
forEach更多的用来遍历数组
for in 一般常用来遍历对象或json
for of数组对象都可以遍历，遍历对象需要通过和Object.keys()
for in循环出的是key，for of循环出的是value

es6去重
法一：indexOf循环去重
let arr = [12,43,23,43,68,12];
let item = [...new Set(arr)];
console.log(item)

```

### 数组常用的方法

``` 
$ 参考回答
push()，pop()，shift()，unshift()，splice()，sort()，reverse()，map()等

```
### promise的三种状态？
``` 
$ pending     进行中
fulfilled      成功
rejected     失败

```

### 优化Js

``` 
$ 参考回答
优化 JavaScript
分析并用 **关键资源数 关键字节数 关键路径长度** 来描述我们的 CRP 。
最小化关键资源数: 消除它们（内联）、推迟它们的下载（defer）或者使它们异步解析（async）等等 。
优化关键字节数（缩小、压缩）来减少下载时间 。
优化加载剩余关键资源的顺序: 让关键资源（CSS）尽早下载以减少 CRP 长度 。

图片懒加载
通过图片懒加载可以避免一次性加载过多的图片导致请求阻塞，这样就可以提高网站的加载速度，提高用户体验

防抖/节流
防抖
输入搜索时，可以用防抖debounce等优化方式，减少http请求；
节流
节流函数：只允许一个函数在N秒内执行一次。滚动条调用接口时，可以用节流throttle等优化方式，减少http请求；

```

## Vue

### Vue.js是什么？

``` 
$ 是一套用于构建用户界面的渐进式框架

```
More info: [Vue](https://cn.vuejs.org)
### 什么是 mvvm？ mvvm 和 mvc 区别？

``` 
$ MVVM 是 Model-View-ViewModel 的缩写。mvvm 是一种设计思想。
Model 层代表数据模型，View 代表 UI 组件。
区别：主要就是 mvc 中 Controller 演变成 mvvm 中的 viewModel。mvvm 主要解决了 mvc 中大量的 DOM 操作使页面渲染性能降低，加载速度变慢，影响用户体验。和当 Model 频繁发生变化，开发者需要主动更新到 View 

```

### Vue 的双向绑定的原理是什么？

``` 
$ 采用数据劫持结合发布者-订阅者模式的方式，通过 Object.defineProperty()来劫持各个属性的 setter，getter，在数据变动时发布消息给订阅者，触发相应的监听回调.

```
More info: [双向绑定](https://www.cnblogs.com/qianxiaox/p/14119940.html)


### Vue的生命周期是什么？

``` 
$ 一个组件创建、数据初始化、挂载、更新、销毁，这就是一个组件所谓的生命周期。
总共分为 8 个阶段创建前/后，载入前/后，更新前/后，销毁前/后。
创建前/后： 在 beforeCreate 阶段
载入前/后：在 beforeMount 阶段
更新前/后：beforeUpdate 和 updated 方法
销毁前/后：在执行 destroy 方法后.

```
More info: [Vue生命周期](https://www.jianshu.com/p/410b6099be69)

### Vue Router
``` 
$ vue router的原理是什么？  
 更新视图但不重新请求页面
 Vue Router导航守卫是什么？
全局前置守卫  router.beforeEach    接收三个参数（to，from，next）
全局解析守卫  router.beforeResolve  和 router.beforeEach 类似，区别是在导航被确认之前，同时在所有组件内守卫和异步路由组件被解析之后，解析守卫就被调用。
全局后置钩子  router.afterEach  不会接受 next 函数也不会改变导航本身
路由独享守卫   与全局前置守卫的方法参数是一样的。
组件内守卫  beforeRouteEnter     beforeRouteUpdate    beforeRouteLeave
 Vue Router导航钩子
 全局导航钩子
  router.beforeEach(to, from, next),
  router.beforeResolve(to, from, next),
  router.afterEach(to, from ,next)
组件内钩子
  beforeRouteEnter,
  beforeRouteUpdate,
  beforeRouteLeave
单独路由独享组件
  beforeEnter
 Vue router两种模式
 hash  history    路径中有无  #  的区别
 vue router 路由传参 ?
get:params, post:data:{} 或者使用QS   this.$route.push('')
路由懒加载？
结合 Vue 的异步组件和 Webpack 的代码分割功能，实现路由组件的懒加载

```
### Vuex

``` 
$ Vuex 是什么？
Vuex 是一个专为 Vue.js 应用程序开发的状态管理模式。

vuex 有哪几种属性？
state：数据源存放地，对应于一般 vue 对象里面的 data
getter：getter 可以对 state 进行计算操作，它就是 store 的计算属性，getters 可以在多给件之间复用
mutation：更改 Vuex 的 store 中的状态的唯一方法是提交 mutation。
action：Action 提交的是 mutation，而不是直接变更状态。Action 可以包含任意异步操作。
module：将 store 分割成模块

```

















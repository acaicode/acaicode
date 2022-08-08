---
title: Vue2与Vue3
date: 2022-08-08 9:57:21
description: "Vue2与Vue3的API比较"
tags:
cover: https://pica.zhimg.com/80/v2-b442793f521ca651ca2afe7a312a29ef_720w.jpg?source=1940ef5c
---
## vue 2 选项式API
&emsp;&emsp;一个vue文件里面,有data,methods,created,computed,watch...等等区域,来一起处理页面.有时候一个功能要使用所有的区域来管理.代码东一块西一块,调试起来比较不容易.

&emsp;&emsp;如果想要使用模块化思想,需要使用mixin混入.mixin的一个问题是没有return提示,就是单纯给你返回,返回什么你也不知道,你就写mixin的时候知道有这个mixin的返回属性可以用.后来者根本不知道,必须要跑到mixin里去看看是不是这里的.另外一个问题是多个mixin的属性可能会冲突,会覆盖重写.


##vue3 组合式API
&emsp;&emsp;根据组件化思想,函数式编程思想,比较聚耦合.一个功能的所有部分都放在一起.
如下图,直接把选项式API七零八落的代码逻辑上是相同的代码归拢到了一起.

&emsp;&emsp;对于要拆出去独立书写的部分,不使用mixin混入,而是使用函数来拆分具体块区,拆为函数或者模块,对外表现为function,主体使用import引入.如下图


---
title: 享元模式 Flyweight Pattern
date: 2017-04-01 19:24:19
category: Design_pattern
tag: [design_pattern]
toc: true
---

## 定义
使用共享对象可有效地支持大量的细粒度的对象。

享元模式是池技术的重要实现方式。  
细粒度的对象，将这些对象的信息分为两个部分：内部状态和外部状态  
* 内部状态 对象可以共享出来的信息，不会随着环境改变而改变
* 外部状态 是对象得以依赖的一个标记，不可共享的状态；如唯一的索引值

## 优缺点
享元模式使得系统更加复杂。为了使对象可以共享，需要将一些状态外部化，这使得程序的逻辑复杂化。  
享元模式将享元对象的状态外部化，而读取外部状态使得运行时间稍微变长。


## 使用场景
* 一个系统有大量的对象。
* 这些对象耗费大量的内存。
* 这些对象的状态中的大部分都可以外部化。
* 这些对象可以按照内蕴状态分成很多的组，当把外蕴对象从对象中剔除时，每一个组都可以仅用一个对象代替。
* 软件系统不依赖于这些对象的身份，换言之，这些对象可以是不可分辨的。


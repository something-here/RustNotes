---
title: Java constructor 构造器
date: 2015-04-27 22:11:39
category: Java_note
tag: [Java]
toc: true
---


## 用构造器保证初始化
构造器名称必须与类名完全相同，所以“每个方法首字母必须小写”的风格不适合构造器。
不接受任何参数的构造器叫做默认构造器。Java文档中通常叫做无参构造器。
构造器没有返回值，但与返回值为空（void）不同。
如果已经定义了一个构造器，编译器就不会帮你自动穿件默认构造器。

如果构造器有参，而实例化对象时不传入参数，编译器会报错：没有找到匹配的构造器。

## 方法重载
每个重载的方法都必须有一个独一无二的参数类型列表。
参数顺序不同也可以区分两个方法。

## this关键字
表示发消息的那个对象。
static方法就是没有this的方法。在static方法内部不能调用非静态方法。

## 终结处理与垃圾回收
1.对象可能不被垃圾回收
2.垃圾回收并不等于“析构”
3.垃圾回收只与内存有关
使用垃圾回收器的原因就是回收程序不再使用的内存。
System.gc(); 用于强制进行进程终结。

## 构造器初始化
在类的内部，变量定义的先后顺序决定了初始化的顺序。即是变量散布在方法定义之间，它们
也会在任何方法（包括构造器）被调用前初始化。
无论创建多少个对象，静态数据都只占用一份存储区域。

初始化顺序是先“静态对象”，再“非静态对象”。

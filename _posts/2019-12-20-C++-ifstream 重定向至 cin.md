---
layout: post
title: "ifstream重定向至cin"
subtitle: 'redirect an ifstream to cin'
author: "YH space"
header-style: text
tags:
  - C++
---

**程序设计之初，只考虑从控制台输入。后因需求变更，需读取文件。但是函数已经写好，且不想修改函数参数。故寻求方法**

代码如下
```c++
ifstream infile;
infile.open("a.txt");
cin.rdbuf(infile.rdbuf());
```
在```main```函数中加入上述代码，即可完美解决问题。

[*我的简书*](https://www.jianshu.com/p/cccaf130d7e6)
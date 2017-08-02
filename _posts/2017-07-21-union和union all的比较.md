---
layout: post
title: union和union all的比较
author: zoranzzl

---


关于union和union all：union all的效率会高一点，因为union默认会做排序，耗时较多，所以工作中没有要求时尽量使用union all。

以下是试验验证过程：

这是使用union的：

![](https://github.com/zoranzzl/zoranzzl.github.io/blob/master/_posts/images/union.png?raw=true)

这是union all的：

![](https://github.com/zoranzzl/zoranzzl.github.io/blob/master/_posts/images/union%20all.png?raw=true)


果然是union all的效率更高一点，因为使用union的时候，还做了唯一性检查，耗费cost为10，，，而union all没有这个操作，也就没有花费这10个cost~~~

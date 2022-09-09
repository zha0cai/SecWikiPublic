---
description: SUMMARY.md 文件在 gitbook中的作用，如何制作 SUMMARY.md 文件，SUMMARY.md 文件自动生成教程。
---
# SUMMARY.md 文件

GitBook使用一个`SUMMARY.md`文件来定义文档的菜单。

虽说在官方文档中，它是可选的，但是它相当重要，控制了左边菜单栏的显示内容。

它通过 Markdown 中的列表语法来表示文件的父子关系。

#### 紧凑型的

```powershell
# Summary
* [Introduction](README.md)
* [Part I](part1/README.md)
    * [Writing is nice](part1/writing.md)
    * [GitBook is nice](part1/gitbook.md)
* [Part II](part2/README.md)
    * [We love feedback](part2/feedback_please.md)
    * [Better tools for authors](part2/better_tools.md)
```

#### 分散型的

也可以通过使用 标题 或者 水平分割线 标志将 GitBook 分为几个不同的部分。

你看到左侧菜单栏的部分 `SUMMARY.md`文件

```powershell
# Summary

### Part I

* [Part I](part1/README.md)
    * [Writing is nice](part1/README.md#writing)
    * [GitBook is nice](part1/README.md#gitbook)
* [Part II](part2/README.md)
    * [We love feedback](part2/README.md#feedback)
    * [Better tools for authors](part2/README.md#tools)

### Part II

* [feedback](part2/feedback.md)
* [tools](part2/tools.md)

----

* [Last part](part3/last.md)
```

#### 自动生成

如果你的 md 文件是少量的，自己编写 SUMMARY.md 文件当然不费事。

但是 md 文件数量非常多时，你可能希望自动生成这些内容，可以参见 [插件 summary](/custom/plugin/other/summary.md) 部分关于自动生成菜单 summary 文件的介绍。
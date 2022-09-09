---
description: 如何使用 gitbook 支持多语言，LANGS 文件在gitbook中的作用
---
# 多语言

### LANGS.md

GitBook支持多种语言编写的书籍或者文档。 首先需要在根目录创建一个名为LANGS.md的文件，然后按照语言创建子目录：

```powershell
# Languages

* [中文](zh/)
* [English](en/)
* [French](fr/)
```

### 每种语言的配置

每个语言(例如：en)目录中都可以有一个book.json来定义自己的配置，它将作为主配置的扩展。

唯一的例外是插件，插件是全局指定的，语言环境配置不能指定特定的插件。

### 示例

你可以从 git 的文档官方查看这种多语言带来的优势。

- 源代码：https://github.com/progit/progit 

- 电子书：https://git-scm.com/book/en/v2
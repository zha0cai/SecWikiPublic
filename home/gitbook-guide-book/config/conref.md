---
description: 使用 gitbook 来引用其他文件的内容，扩展 gitbook中的内容，gitbook导入本地或互联网上的资源，
---
# 内容引用

内容参考 (conref) 是便于用来重复使用其他文件和书本内容。


### 内联引用

有时，在写某一节的内容的时候，会希望读者参见另外一个章节的内容。
可以通过 markdown 的链接语法引导读者到该章节。

**例如**

`回到基础配置，点击 [这里](./basic.md)`

回到基础配置，点击 [这里](./basic.md)

`点击 [这里](./basic.html)，回到基础配置`

点击 [这里](./basic.html)，回到基础配置

这两种写法，都能回到首页，但是建议使用 md 文件引用，而不是 html 引用。

gitbook 会自动将 md 引用关联起来，这样无论转换为何种格式，都能使引用生效。

**注意**

- `回到基础配置，[绝对路径](/config/basic.md)` 
- 回到基础配置，[绝对路径](/config/basic.md)

- `回到基础配置，[相对路径](./basic.md)` 
- 回到基础配置，[相对路径](./basic.md)


### 导入本地文件

使用 include 标签导入其他文件的内容真的很简单：

{% raw %}

{% include "./footer.md" %}

{% endraw %}

### 从其他书本导入文件

GitBook 同样能处理使用了git协议的include路径：

{% raw %}
{% include "git+https://github.com/GitbookIO/documentation.git/README.md#0.0.1" %}
{% endraw %}

git的url格式是：

`git+https://user@hostname/project/blah.git/file#commit-ish`

真实的git url应该以 .git 结尾，导入的文件名从 .git 之后的url片段提取。

`commit-ish` 可以是任何可以作为 `git checkout` 参数的标签，sha，或分支。默认是 `master`。

### 举个例子

我在 `footer.md` 文档中的内容：

```
---

Copyright © 2019-2020 码谱
```

在本页面使用下面的代码引入后：

{% raw %}

{% include "./footer.md" %}

{% endraw %}

显示如下内容：

{% include "./footer.md" %}
---
description: gitbook 菜单折叠展开 插件, gitbook-plugin-chapter-fold，gitbook-plugin-expandable-chapters 使用教程
---

# toggle-chapters

GitBook插件：用于菜单收起、折叠、展开功能。

## chapter-fold

默认只在目录导航中显示章的标题，而不会显示小节的标题。

插件的效果是：点击每一章或者每一节会显示当前章或节的子目录，如果有的话，但是同时会收起其它之前展开的章节。

现在左边的菜单栏就是这个插件实现的。

使用这种插件有个弊端，就是无法知道整本书的结构，有利有弊吧。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-chapter-fold

```json
{
    "plugins": [
         "chapter-fold"
    ]
}
```

插件需要 SUMMARY 文件中的格式相对规范：

```markdown
## III 定制化

* [插件](custom/plugin/README.md)
    * [通用](custom/plugin/common/README.md)
        * [Alerts](custom/plugin/common/alerts.md)
```

本教程使用了该插件，效果如右边菜单栏。

## expandable-chapters

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-expandable-chapters

这个插件也有问题，就是如下写法的，需要点击箭头才能展开收缩菜单：

```markdown
## III 定制化

* [插件](custom/plugin/README.md)
    * [通用](custom/plugin/common/README.md)
```

```json
{
    "plugins": [
         "expandable-chapters"
    ]
}
```

如果发现使用其中的一个插件效果不好，可以一起使用，看看是不是有效：

```json
{
"plugins": [
    "expandable-chapters",
    "chapter-fold"
]
}
```
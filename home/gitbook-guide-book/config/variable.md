---
description: gitbook中如何使用变量，全局变量与局部变量使用教程
---

# 变量

Gitbook 内置了特别多的变量，可供模板使用。

## 全局变量

这些变量是 Gitbook 的基础变量，通过它们可以获取 Gitbook 的基本信息。

|变量	|说明                                         |
|--|--|
|book	|book.json的全书信息+配置设置。详情请参阅下文。|
|gitbook	|GitBook特定信息                          |
|page	|当前页特定信息                               |
|file	|与当前页特定信息相关联的文件                 |
|readme	|自述相关内容                                 |
|glossary	|词汇相关内容                             |
|summary	|菜单相关内容                             |
|languages	|多语言书籍列表                           |
|output	|输出相关内容                                 |
|config	 |book.json相关内容 |

## book 变量

该变量主要是 `book.json`中配置的数据。如果想自定义变量，book 变量是最佳选择。

|变量	|说明|
|--|--|
|book.language|	多语言书的当前语言
|book.[value]	|在book.json中的variables下的所有其他值都可以在这里访问

### 举个例子

变量被定义在 `book.json` 文件中：

```json
{
    "variables": {
        "mapull": "码谱，让编程更容易。"
    }
}
```

这样定义了一个变量 `mapull`，取值为 "码谱，让编程更容易。"

在页面上`{{ book.mapull }}`的语法会被显示为 -> {{ book.mapull }}


## gitbook 变量

该变量用来获取生成 book 的 gitbook 的基本信息，实际价值不大。

|变量	|说明|
|--|--|
|gitbook.time	|当前时间(当你运行gitbook命令时)。
|gitbook.version	|GitBook用于生成图书的版本

### 举个例子

该 book 使用的 gitbook 版本用 `{{gitbook.version}}` 显示为 -> {{gitbook.version}}

## file 变量

该变量用来获取此文件的相关信息。

|变量	|说明|
|--|--|
|file.path|	原始页面的路径
|file.mtime	|修改时间，上次修改文件的时间
|file.type	|用于编译此文件的语法解析器的名称(例如：markdown，asciidoc等)

### 举个例子

该文件使用的解析器的名称用 `{{file.type}}` 显示为 -> {{file.type}}

## page 变量

该变量用来获取当前页面的信息。

|变量|	说明
|--|--|
|page.title|	页面标题
|page.previous|	内容表中的前一页(可以是“null”)
|page.next	|内容表中的下一页(可以是“null”)
|page.dir	|文本方向，基于配置(rtl或ltr)

### 举个例子

当前页面的下一页 `{{page.previous.path}}` 显示为 -> {{page.previous.path}}

当前页面的标题 `{{page.title}}` 显示为  -> {{page.title}}

## 其他变量

|变量|	说明
|--|--|
|summary.parts	|内容列表，可以访问整个目录(SUMMARY.md)
|languages.list	|本书的语言环境列表
|output.name	|输出生成器的名称，可能的值是website，json，ebook
|output.format	|当output.name ==“ebook”，format定义将生成的电子书格式，可能的值是pdf，epub或mobi
|readme.path	|自述文件的路径
|glossary.path	|词汇表的路径

### 举几个例子

`summary.parts[0].articles[0].title` 将返回第一篇文章的标题 -> {{summary.parts[0].articles[0].title}}

本书的提供的词汇表的路径 `{{glossary.path}}` 显示为  -> {{glossary.path}}

本书使用的生成器名称 `{{output.name}}` 显示为  -> {{output.name}}
---
description: 配置 gitbook，自定义 gitbook，使用 book.json文件定制化生成的书籍网站
---
# 基础配置

所有的配置都以JSON格式存储在名为 `book.json` 的文件中。

### title

设置书本的标题

`"title" : "Gitbook 使用"`

### author

作者的相关信息

`"author" : "mapull"`

###  description

本书的简单描述，默认是从 README（第一段）中提取的。

`"description" : "码谱整理的Gitbook的配置和使用"`

### language

Gitbook使用的语言, 版本2.6.4中可选的语言如下：

`en, ar, bn, cs, de, en, es, fa, fi, fr, he, it, ja, ko, no, pl, pt, ro, ru, sv, uk, vi, zh-hans, zh-tw`

##### 配置使用简体中文

`"language" : "zh-hans"`

### gitbook

这个选项是用来指定生成书本的GitBook的版本的。

```
"gitbook" : "3.2.2",
"gitbook" : ">=3.0.0"
```

### root

指定存放 GitBook 文件（除了 book.json）的根目录

`"root": "."`

`"root": "./docs"`

### links

在左侧导航栏添加链接信息

```json:book.json
{"links" : {
    "sidebar" : {
        "首页" : "https://www.mapull.com"
    }
}}

```
### styles

自定义页面样式， 默认情况下各generator对应的css文件

```json
{"styles": {
    "website": "styles/website.css",
    "ebook": "styles/ebook.css",
    "pdf": "styles/pdf.css",
    "mobi": "styles/mobi.css",
    "epub": "styles/epub.css"
}}
```

例如使 `<h1> <h2>`标签有下边框， 可以在 `website.css` 中设置

```css:website.css
h1 , h2{
    border-bottom: 1px solid #EFEAEA;
}
```

### plugins

配置使用的插件

```json:book.json
{
"plugins": [
    "github"
]}
```
添加新插件之后需要运行 `gitbook install` 来安装新的插件

Gitbook默认带有7个插件：

- livereload        热加载插件
- highlight         语法高亮插件
- search            搜索插件
- lunr              搜索插件后台服务
- sharing           分享插件
- fontsettings      字体设置插件
- theme-default     主题

如果要去除自带的插件， 可以在插件名称前面加 `-`
移除搜索 search 插件：

```json
{
"plugins": [
    "-search"
]}
```

### pluginsConfig

配置插件的属性

```json
{"pluginsConfig": {
    "fontsettings": {
        "theme": "sepia",
        "family": "serif",
        "size":  1
    }
}}
```
### structure

指定 Readme、Summary、Glossary 和 Languages 对应的文件名，下面是这几个文件对应变量以及默认值：

|变量|	含义|默认值|
|--|--|--|
|structure.readme	|Readme file name |README.md |
|structure.summary	|Summary file name | SUMMARY.md |
|structure.glossary	|Glossary file name | GLOSSARY.md |
|structure.languages	|Languages file name | LANGS.md |

### variables

```json
{
    "variables": {
        "firstbook": "Hello World"
    }
}
```

这个选项定义在 [模板](./template.md) 中使用的变量值。
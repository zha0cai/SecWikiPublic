# 目录结构

GitBook使用`SUMMARY`文件管理目录结构，文件支持 `Markdown` 和 `Asciidoc` 两种语法。

之后的演示都是基于 `Markdown` 语法。

一个经典的 gitbook 文件目录如下：

```text
.
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md    
```

每一项简单的说明：

| 文件 |重要性 |	说明 |
|--|--|--|
|book.json	|可选，非常重要|保存配置文件数据 [详情](./book.html)
|README.md	|必选，重要|简介，书籍的简单介绍 [详情](./readmex.html)
|SUMMARY.md	|可选，非常重要|目录，控制左边侧边栏 [详情](./summaryx.html)

接下来，会详细说明每一种文件的作用。
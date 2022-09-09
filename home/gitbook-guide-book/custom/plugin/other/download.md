---
description: gitbook 下载PDF文件文件，下载按钮 插件, gitbook-plugin-download-pdf-link，gitbook-plugin-my-toolbar 使用教程
---
# 下载PDF文件

## download-pdf-link

Gitbook 插件：使 GitBook 支持下载 PDF 文件 。

插件只是支持下载 pdf 文件，这个 pdf文件是需要提前准备好的。

如果生成 pdf 文件，参照 [导出PDF](/extend/pdf.md)

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-download-pdf-link

[https://github.com/armandfardeau/gitbook-plugin-download-pdf-link](https://github.com/armandfardeau/gitbook-plugin-download-pdf-link)

```json:book.json
{
  "plugins": ["download-pdf-link"],
  "pluginsConfig": {
    "download-pdf-link": {
      "base": "http://localhost:4000/book.pdf",
      "label": {
          "en": "Download PDF",
          "zh-hans": "下载PDF"
      }
    }
  }
}
```

这个插件没有试验成功：

`http://localhost:4000/book.pdf/lang=`

`ENOENT: no such file or directory, stat 'D:\gitbook\book-theme-comscore\_book\book.pdf\index.html'`

## pdf-multi-link

插件官网竟然把配置信息写错了。

[https://github.com/armandfardeau/gitbook-plugin-download-pdf-link](https://github.com/armandfardeau/gitbook-plugin-download-pdf-link)

```json
{
  "plugins": ["pdf-multi-link"],
  "pluginsConfig": {
    "pdf-multi-link": {
      "base": "http://localhost:4000/book.pdf",
      "label": {
        "en": "Download PDF",
        "zh-hans": "下载PDF"
      }
    }
  }
}
```

这个插件又没有试验成功：

`http://localhost:4000/book.pdf/`

`ENOENT: no such file or directory, stat 'D:\gitbook\book-theme-comscore\_book\book.pdf\index.html'`

#### 放弃了这个思路

看了一下源代码，好像两个插件都有点问题，还有其他的几个 download 文件的插件好像都不咋行。

更奇怪的是，我设置了语言，但是代码不生效，显示下面的效果：

<i class="fa fa-file-pdf-o"></i>  `[object Object]`

### 另谋思路

从源代码看，这个下载功能实际上是将 `pdf` 的链接用一个按钮显示了出来。

## toolbar

Gitbook 插件：添加一个按钮到顶部的菜单栏。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-toolbar

[https://github.com/Simran-B/gitbook-plugin-toolbar](https://github.com/Simran-B/gitbook-plugin-toolbar)

```json
{"plugins": ["toolbar"]}
```

```json:book.json
{
"toolbar": {
      "buttons":
        [
          {
            "label": "下载PDF",
            "icon": "fa fa-file-pdf-o",
            "url": "http://localhost:4000/book.pdf",
            "target": "_blank"
          }
        ]
    }
    }
```

用了这个插件，发现它只显示图标，无法显示文字。于是下面这个插件出现了。

## my-toolbar

Gitbook 插件：添加一个按钮到顶部的菜单栏。是基于上面的插件改版的。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-my-toolbar

[https://github.com/neutree/gitbook-plugin-my-toolbar](https://github.com/neutree/gitbook-plugin-my-toolbar)

```json:book.json
{
    "my-toolbar": {
      "buttons":
        [
          {
            "label": "下载PDF",
            "icon": "fa fa-file-pdf-o",
            "url": "http://localhost:4000/book.pdf",
            "position":"left",
            "text": "下载PDF",
            "target": "_blank"
          }
        ]
    }
}
```

终于在左上角看到了下面的效果：

<i class="fa fa-file-pdf-o"></i>  `下载PDF`

点击按钮后，在 `Chorme`上正确显示（Chrome上会显示PDF内容，页面的右上角有浏览器自带的下载、打印等功能）。
_当前页面的下载功能是利用该插件实现的，为了保证性能，只有该页面开启了此功能，并且PDF文件只是用来演示。_


> [!WARNING|style:callout|iconVisibility:hidden|label:注意]
> 如果页面内容显示不完整，请F5刷新当前页面
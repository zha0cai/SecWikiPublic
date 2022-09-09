---
description: gitbook中常用插件的教程，演示如何使用gitbook常见插件，自定义 gitbook 插件
---
# 插件

记录一些实用的插件, 如果要指定插件的版本可以使用 `plugin@0.3.1`。

Gitbook默认带有7个插件（功能性5个，搜索有两个，主题一个）：

- livereload        热加载插件
- highlight         语法高亮插件
- search            搜索插件
- lunr              搜索插件后台服务
- sharing           分享插件
- fontsettings      字体设置插件
- theme-default     主题

下面的插件在 GitBook 的 3.2.3 版本中可以正常工作，因为一些插件可能不会随着 GitBook 版本的升级而升级，即下面的插件可能不适用高版本的 GitBook。
另外本文记录的插件在 windows 下都是可以正确工作的， Linux 系统没有测试。
这里只是列举了一部分插件，如果有其它的需求，可以到 [插件官网](https://plugins.gitbook.com/) 区搜索相关插件。

大部分插件都针对默认主题的，如果指定了其他主题插件，可能会导致部分插件失效或显示错乱。

**由于 Gitbook 的原创团队重心偏向 gitbook.com 的运行，目前 插件官网 https://plugins.gitbook.com 已无法打开。**

**示例中给出的插件链接换成了 github 的地址**

### 插件安装提示

插件的说明文档中，一般都建议使用下面的方式安装插件：

`gitbook install`

但是这种方式下载比较慢，推荐使用 `npm` 方式安装插件。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-xxx
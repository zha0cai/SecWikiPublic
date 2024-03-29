---
description: gitbook 中文文档，搭建自己的gitbook教程，Gitbook 使用学习演示平台，利用 Gitbook 开源工具搭建的说明文档网站，对 gitbook 插件，gitbook 主题进行了演示分析。对部分失效插件二次开发，确保插件能运行。由于 gitbook 不再维护，反复踩坑之后更新到 honkit 分支，使用更加的顺畅，nodejs 也支持更新的版本。
---

# Gitbook 打造的 Gitbook & Honkit 说明文档

> Create by mapull & Revise by zha0cai

![GitBook](images/gitbook.png)
[Honkit](https://github.com/honkit/honkit)

## GitBook是什么

官方给的定义：

> GitBook is a command line tool (and Node.js library) for building beautiful books using GitHub/Git and Markdown (or AsciiDoc).

GitBook 是基于 Node.js 的开源命令行工具，用于输出漂亮的电子书。

GitBook 支持 Markdown 和 AsciiDoc 两种语法格式，能够输出 `html`，`pdf`，`epub`，`mobi`等多种格式。

## GitBook 特性

- Markdown 或 AsciiDoc 语法
- 多类型支持：网站(html)或电子书 (pdf, epub, mobi)
- 多语言
- 目录、大纲
- 封面
- 模板和变量
- 模板继承
- 插件
- 主题

## 缺陷

#### 开源项目停止维护

活跃的开源项目，意味着不断完善的功能，不断修复 bug，及时的反馈，更多社区的帮助...

遗憾的是，GitBook 开源项目已经停止维护，专注打造的 gitbook.com 网站在国内访问受限。

#### 移动端不适配

现在有 PC 端的流量已经赶不上移动端了，但是 GitBook 对移动设备的支持不太友好。

虽然正文部分做到了 responsive，但是菜单栏没有做移动端适配。

大部分插件也没有考虑移动端的情形。

## 为何出这个文档

作为一个技术宅，经常性的写一些文档，或使用说明，由于很早就接触了博客系统，因此一直使用 markdown 来编写文档。

时间长了，资料越来越多，也越来越乱，它们经常散落在某个角落，内容不系统化，也不方便管理。于是希望有一个工具解决这个问题，然后就找到了 GitBook。(题外话 siyuan 笔记也很好用，gitbook 我主要当 blog 用)诚然，它不是最好的解决方案，很多博客系统提供了专栏功能，很多编辑器如有道云笔记都能通过 markdown 来管理自己的文档。但是它们都不够纯粹，我只希望将自己分散的 markdown 文件组织起来，形成类似一本书，就这个需求来看，GitBook 最符合我的需要。

接下来的内容，都是关于 GitBook 的使用，和 gitbook.com 没有啥关联，如果你希望通过 gitbook.com 来托管你的书籍，可以移步 [GitBook.com](https://www.gitbook.com/)

为了能更好地阐释 GitBook，我通过 GitBook 生成了一本电子书，来讲述...

### 选择不同版本

当前的版本是 gitbook 的彩色样式，是 Gitbook 定制的 `comscore` 主题。

如果想看一下原版的书，可以移步[这里](https://www.mapull.com/gitbook/default/)，两者的内容完全一致，但是内容更新没有当前版本及时。[Revise by zha0cai](https://github.com/zha0cai)
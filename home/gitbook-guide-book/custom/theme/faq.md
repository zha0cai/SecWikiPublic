---
description: 演示 使用 gitbook theme-faq 主题，主要用来制作知识库或者帮助中心
---
# FAQ 主题

GitBook主题：`theme-faq` 插件主要用来制作知识库或者帮助中心，GitBook 的 **帮助中心** 就是使用的该主题。

FAQ是英文`Frequently Asked Questions`的缩写，中文意思就是“经常问到的问题”，或者更通俗地叫做“常见问题解答”。

> [!NOTE|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-theme-fexa

[https://github.com/GitbookIO/theme-faq](https://github.com/GitbookIO/theme-faq)

为了支持中文搜索我们需要引入 `search-plus` 包。

```json
{
    "plugins": [
        "theme-faq",
        "-lunr",
        "search-plus"
    ]
}
```

### 定制化

这个 FAQ 如果不加以改造，界面是比较丑陋的。

扩展的功能需要**修改代码**才能达到效果。

### 演示平台

- 从当前页面的左上角下拉菜单中，选择对应的 `faq` 版本
- 直接访问 [在线示例](https://www.mapull.com/gitbook/faq/)
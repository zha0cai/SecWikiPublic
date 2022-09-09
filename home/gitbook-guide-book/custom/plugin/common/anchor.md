---
description: gitbook 锚点插件, gitbook-plugin-anchors, gitbook-plugin-anchor-navigation-ex, back-to-top-button 使用教程
---
# 锚点

Gitbook 插件：用来显示锚点，快速跳转到某个地方。

## Anchors

添加 Github 风格的锚点样式

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-anchors

[https://github.com/rlmv/gitbook-plugin-anchors](https://github.com/rlmv/gitbook-plugin-anchors)

`"plugins" : [ "anchors" ]`

下面的这个插件是增强版，功能比较全。

## Anchor-navigation-ex

添加Toc到侧边悬浮导航以及回到顶部按钮。需要注意以下两点：

本插件只会提取 `h1,h2,h3` 标签作为悬浮导航

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-anchor-navigation-ex

这个版本的配置项非常多，也有中文版的说明：

[https://github.com/zq99299/gitbook-plugin-anchor-navigation-ex](https://github.com/zq99299/gitbook-plugin-anchor-navigation-ex)

只有按照以下顺序嵌套才会被提取

```markdown
# h1
## h2
### h3
```

必须要以 h1 开始，直接写 h2 不会被提取 `## h2`

```json
{
    "plugins": [
        "anchor-navigation-ex"
    ],
    "pluginsConfig": {
        "anchor-navigation-ex": {
            "showLevel": false,
            "showGoTop": true,
            "isRewritePageTitle": true,
            "isShowTocTitleIcon": true,
            "tocLevel1Icon": "fa fa-hand-o-right",
            "tocLevel2Icon": "fa fa-hand-o-right",
            "tocLevel3Icon": "fa fa-hand-o-right"
        }
    }
}
```


效果：

![Anchor-navigation-ex](./anchor.gif)

该主题启用了此插件，可以用插件的配置`"showGoTop": true`实现 `返回顶部` 功能。

## back-to-top-button

如果想单独实现 `返回顶部` 功能，可以使用该插件。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-back-to-top-button

```json
{
    "plugins": [
        "back-to-top-button"
    ]
}
```
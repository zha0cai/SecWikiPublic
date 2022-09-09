---
description: gitbook 代码语法高亮 插件, gitbook-plugin-prism 使用教程
---
# Prism

使用 `Prism.js` 为语法添加高亮显示，开启插件时需要将 highlight 插件去掉。

该插件自带的主题样式较少，可以再安装 `prism-themes` 插件，里面多提供了几种样式。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-prism

[https://github.com/gaearon/gitbook-plugin-prism](https://github.com/gaearon/gitbook-plugin-prism)

```json
{
    "plugins": [
        "prism",
        "-highlight"
    ],
    "pluginsConfig": {
        "prism": {
            "css": [
                "prismjs/themes/prism-solarizedlight.css"
            ]
        }
    }
}
```

如果需要修改背景色、字体大小等，可以在 website.css 定义 pre[class*="language-"] 类来修改，下面是一个示例：

```css
pre[class*="language-"] {
    border: none;
    background-color: #f7f7f7;
    font-size: 1em;
    line-height: 1.2em;
}
```
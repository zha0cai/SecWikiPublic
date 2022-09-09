---
description: gitbook 添加版本选择的下拉菜单，多版本控制，多语言版本 插件, gitbook-plugin-versions-select 使用教程
---
# versions-select

Gitbook 插件：添加版本选择的下拉菜单

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install --save gitbook-plugin-versions-select

添加版本选择的下拉菜单，针对文档有多个版本的情况。

[https://github.com/prescottprue/gitbook-plugin-versions-select](https://github.com/prescottprue/gitbook-plugin-versions-select)

```json
{
    "plugins": [ "versions-select" ],
    "pluginsConfig": {
        "versions": {
            "options": [
                {
                    "value": "https://www.mapull.com/gitbook/api/",
                    "text": "API 主题"
                },
                {
                    "value": "https://www.mapull.com/gitbook/default/",
                    "text": "默认主题",
                    "selected": true
                }
            ]
        }
    }
}
```

我们可以自定义 css 来修改 select 的显示样式：

```css
.versions-select select {
    height: 2em;
    line-height: 2em;
    border-radius: 4px;
    background: #efefef;
}
```
效果见左上角。
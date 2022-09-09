---
description: 演示使用gitbook theme-api 主题，可以编写 API 文档，API 平台
---
# theme-api 插件

GitBook主题：同样可以编写 API 文档，只需要引入 `theme-api` 插件


> [!NOTE|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-theme-api

[https://github.com/GitbookIO/theme-api](https://github.com/GitbookIO/theme-api)

```json
{
    "plugins": ["theme-api"],
    "pluginsConfig": {
        "theme-api": {
            "theme": "dark"
        }
    }
}
```

引入之后会替换默认的样式。

使用 GitBook 的 API 文档模式时也可以使用插件，但是因为大部分插件可能针对写书的模式，所以有可能会出现不兼容的现象。

API文档的语法也很简单，因为主要是针对方法的，所以以方法为基本单位，通过下面的语法来定义一个方法

{% raw %}
```
{% method %}

内容区

{% endmethod %}
```

{% endraw %}

在内容区里面，通过 {% raw %} `{% sample lang="lang" %}` {% endraw %} 来定义一个针对特定语言的演示。

通过 {% raw %}`{% common %}` {% endraw %} 标识所有语言共同的部分。


### 演示平台

- 从当前页面的左上角下拉菜单中，选择对应的 `api` 版本
- 直接访问 [在线示例](https://www.mapull.com/gitbook/api/)
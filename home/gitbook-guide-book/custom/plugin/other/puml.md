---
description: gitbook 使用 `PlantUML` 展示 uml 图 插件, gitbook-plugin-puml 使用教程，插件在线演示
---
# Puml

Gitbook 插件：使用 `PlantUML` 展示 uml 图。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install --save gitbook-plugin-puml

[https://github.com/GitbookIO/plugin-puml](https://github.com/GitbookIO/plugin-puml)

PlantUML 地址：`http://plantuml.com/`

```
{
    "plugins": ["puml"]
}
```
##### 使用示例

{% raw %}

```java
{% plantuml %}
Class Stage
    Class Timeout {
        +constructor:function(cfg)
        +timeout:function(ctx)
        +overdue:function(ctx)
        +stage: Stage
    }
    Stage <|-- Timeout
{% endplantuml %}
```
{% endraw %}

效果如下所示：

![pulm](puml.png)
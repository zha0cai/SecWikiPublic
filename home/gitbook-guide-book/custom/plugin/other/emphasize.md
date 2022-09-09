---
description: gitbook 为文字加上底色 插件, gitbook-plugin-emphasize 使用教程
---
# Emphasize

Gitbook 插件：为文字加上底色

[插件地址](https://plugins.gitbook.com/plugin/emphasize)

```json
{"plugins": [
    "emphasize"
]}
```

#### 使用示例

```

{% raw %}

This text is {% em %}highlighted !{% endem %}
 
This text is {% em %}highlighted with **markdown**!{% endem %}
 
This text is {% em type="green" %}highlighted in green!{% endem %}
 
This text is {% em type="red" %}highlighted in red!{% endem %}
 
This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}

{% endraw %}

```

显示的效果：

This text is <span class="pg-emphasize pg-emphasize-yellow" style="">highlighted !</span>
 
This text is <span class="pg-emphasize pg-emphasize-yellow" style="">highlighted with <strong>markdown</strong>!</span>
 
This text is <span class="pg-emphasize pg-emphasize-green" style="">highlighted in green!</span>
 
This text is <span class="pg-emphasize pg-emphasize-red" style="">highlighted in red!</span>
 
This text is <span class="pg-emphasize pg-emphasize-yellow" style="background: #ff0000;">highlighted with a custom color!</span>
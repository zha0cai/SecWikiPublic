---
description: gitbook alert 插件, gitbook-plugin-flexible-alerts 使用教程
---
# Alerts

Gitbook 插件：对提示框的增强。

有两个类似的插件：

- `gitbook-plugin-alerts`
- `gitbook-plugin-flexible-alerts`

下面的插件是增强版，这里使用第二个。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-flexible-alerts

[https://github.com/zanfab/gitbook-plugin-flexible-alerts#readme](https://github.com/zanfab/gitbook-plugin-flexible-alerts)

添加不同 `alerts` 样式的 `blockquotes`，目前包含四种样式：

- `NOTE`
- `TIP`
- `WARNING` 
- `DANGER`

```json
{
    "plugins": ["flexible-alerts"]
}
```
下面是使用示例：

```
Info styling
> [!NOTE]
> An alert of type 'note' using global style 'callout'.

Info flat
> [!NOTE|style:flat]
> An alert of type 'note' using alert specific style 'flat' which overrides global style 'callout'.

Tip style
> [!TIP|style:flat|label:My own heading|iconVisibility:hidden]
> An alert of type 'tip' using alert specific style 'flat' which overrides global style 'callout'.
> In addition, this alert uses an own heading and hides specific icon.

Warning styling
> **[!WARNING] For warning**
> Use this for warning messages.

danger styling
> **[!DANGER] For danger**
> Use this for danger messages.
```

效果如下所示：

Info styling
> [!NOTE]
> An alert of type 'note' using global style 'callout'.

Info flat
> [!NOTE|style:flat]
> An alert of type 'note' using alert specific style 'flat' which overrides global style 'callout'.

Tip style
> [!TIP|style:flat|label:My own heading|iconVisibility:hidden]
> An alert of type 'tip' using alert specific style 'flat' which overrides global style 'callout'.
> In addition, this alert uses an own heading and hides specific icon.

Warning styling
> **[!WARNING] For warning**
> Use this for warning messages.

danger styling
> **[!DANGER] For danger**
> Use this for danger messages.
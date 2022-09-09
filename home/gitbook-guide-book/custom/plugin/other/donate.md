---
description: gitbook 打赏插件，显示二维码插件 插件, gitbook-plugin-donate 使用教程
---
# Donate

Gitbook 插件：打赏插件，显示二维码插件。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-donate

[https://github.com/willin/gitbook-plugin-donate](https://github.com/willin/gitbook-plugin-donate)

```json
{
    "plugins": ["donate"],
    "pluginsConfig": {
        "donate": {
          "wechat": "例：/images/qr.png",
          "alipay": "http://blog.willin.wang/static/images/qr.png",
          "title": "默认空",
          "button": "默认值：Donate",
          "alipayText": "默认值：支付宝捐赠",
          "wechatText": "默认值：微信捐赠"
        }
    }
}
```

虽然这个插件名称是 捐赠插件，实际是显示一个或两个二维码。

比如，当前版本的 `反馈` 功能就是用该插件显示了一个微信二维码。

使用的配置信息：

```json
{
    "pluginsConfig": {
        "donate": {
              "wechat": "/gitbook.png",
              "button": "反馈",
              "wechatText": "微信扫码"
        }
    }
}
```
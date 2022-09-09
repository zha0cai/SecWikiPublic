---
description: gitbook 更改网站的 favicon.ico 插件, gitbook-plugin-favicon 使用教程
---
# favicon

GitBook插件：更改网站的 favicon.ico，浏览器标题栏的图标。gitbook 默认图标是一本书，黑白色。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-favicon

[https://github.com/menduo/gitbook-plugin-favicon](https://github.com/menduo/gitbook-plugin-favicon)

```json
{
    "plugins": [
        "favicon"
    ],
    "pluginsConfig": {
        "favicon": {
            "shortcut": "assets/images/favicon.ico",
            "bookmark": "assets/images/favicon.ico",
            "appleTouch": "assets/images/apple-touch-icon.png",
            "appleTouchMore": {
                "120x120": "assets/images/apple-touch-icon-120x120.png",
                "180x180": "assets/images/apple-touch-icon-180x180.png"
            }
        }
    }
}
```

##### 注意以下几点

- 1、图标的格式一定要是.ico的，直接修改图片的后缀为.ico是无效的。
- 2、图标的分辨率要是32*32的。
- 3、可在线把图片转成图标：http://www.bitbug.net/
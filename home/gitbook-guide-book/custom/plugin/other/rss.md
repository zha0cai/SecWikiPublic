---
description: gitbook 添加 rss 订阅功能 插件, gitbook-plugin-rss 使用教程，插件在线演示
---
# RSS

Gitbook 插件：添加 rss 订阅功能。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-rss

[https://github.com/denysdovhan/gitbook-plugin-rss](https://github.com/denysdovhan/gitbook-plugin-rss)

```json
{
    "plugins": [ "rss" ],
    "pluginsConfig": {
        "rss": {
            "title": "GitBook 使用教程",
            "description": "记录 GitBook 的配置和一些插件的使用",
            "author": "Mapull",
            "feed_url": "https://www.mapull.com/rss",
            "site_url": "https://www.mapull.com/",
            "managingEditor": "mapull@123.com",
            "webMaster": "mapull@123.com",
            "categories": [
                "gitbook"
            ]
        }
    }
}
```

使用后，会在页面右上角添加一个 `rss` 的图标。

rss 的图标：<i class="fa fa-rss"></i>
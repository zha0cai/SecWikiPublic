---
description: gitbook 分享当前页面增强 插件, gitbook-plugin-sharing-plus 使用教程
---
# Sharing-plus

Gitbook 插件：分享当前页面，比默认的 `sharing` 插件多了一些分享方式。

分享增强插件。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-sharing-plus

`plugins: ["-sharing", "sharing-plus"]`

配置:

```json
{
"pluginsConfig": {
    "sharing": {
       "douban": false,
       "facebook": false,
       "google": true,
       "hatenaBookmark": false,
       "instapaper": false,
       "line": true,
       "linkedin": true,
       "messenger": false,
       "pocket": false,
       "qq": false,
       "qzone": true,
       "stumbleupon": false,
       "twitter": false,
       "viber": false,
       "vk": false,
       "weibo": true,
       "whatsapp": false,
       "all": [
           "facebook", "google", "twitter",
           "weibo", "instapaper", "linkedin",
           "pocket", "stumbleupon"
       ]
   }
}
}
```

开启插件后，会在页面右上角增加分享到对应平台的图标。
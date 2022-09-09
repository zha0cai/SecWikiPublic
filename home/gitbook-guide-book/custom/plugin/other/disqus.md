---
description: gitbook 页面评论 插件, gitbook-plugin-disqus，gitbook-plugin-gitalk 使用教程，插件在线演示
---
# 评论

GitBook插件：用于页面评论

## Disqus 评论

[Disqus](https://disqus.com/) 是一个非常流行的为网站集成评论系统的工具。
gitbook 可以集成 disqus 以便可以和读者交流。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-disqus

首先，需要在 disqus `https://disqus.com/` 上注册一个账号，然后添加一个 website，这会获得一个关键字，然后在集成时配置这个关键字即可。

[插件地址](https://plugins.gitbook.com/plugin/disqus)

虽然是一个不错的插件，但是 Disqus 在国内无法正常使用。

如果是国外服务服务器，面向海外用户，该插件效果还是不错的。


```json
{
"plugins": [
    "disqus"
],
"pluginsConfig": {
    "disqus": {
        "shortName": "mapull"
    }
}
}
```
`shortName`是在 Disqus 申请的唯一码。


## gitalk 评论

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-gitalk

[https://github.com/snowdreams1006/gitbook-plugin-mygitalk](https://github.com/snowdreams1006/gitbook-plugin-mygitalk)

和上面插件基本类似。
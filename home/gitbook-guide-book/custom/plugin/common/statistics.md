---
description: gitbook 搜索引擎统计，百度统计，谷歌统计 插件, gitbook-plugin-ga，gitbook-plugin-3-ba，gitbook-plugin-baidu 使用教程
---
# 统计

Gitbook 插件：用于搜索引擎统计。

## Google 统计

#### GA

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-ga

[https://github.com/GitbookIO/plugin-ga](https://github.com/GitbookIO/plugin-ga)

```json
"plugins": [
    "ga"
 ],
"pluginsConfig": {
    "ga": {
        "token": "UA-XXXX-Y"
    }
}
```

由于不使用 Google统计，就不演示了。

此类插件的原理是插入统计的 js 脚本到 head 中。

## 百度统计

#### 3-ba

百度统计插件，本站使用了该插件。

它的工作原理是在页面的请求`head`中添加统计的js代码。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-3-ba

[https://github.com/FrankFang/gitbook3-plugin-ba](https://github.com/FrankFang/gitbook3-plugin-ba)


```json
{
    "plugins": ["3-ba"],
    "pluginsConfig": {
        "3-ba": {
            "token": "xxxxxxxx"
        }
    }
}
```

启动以后，可以在浏览器中用 `F12` 看一下源代码是否包含如下片段：

`<script src="https://hm.baidu.com/hm.js?xxxxxxxxxxxxxxxxx"></script>`

#### baidu

这个插件名字是对的，就是功能不生效，如果要使用百度统计，请使用上面那个。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-baidu

[https://github.com/poppinlp/gitbook-plugin-baidu](https://github.com/poppinlp/gitbook-plugin-baidu)

```json
{
    "plugin": ["baidu"],
    "pluginsConfig": {
        "baidu": {
            "token": "YOUR TOKEN"
        }
    }
}
```


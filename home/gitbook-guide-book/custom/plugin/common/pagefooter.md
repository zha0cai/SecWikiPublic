---
description: gitbook 为页面添加页脚，自定义页脚 插件, gitbook-plugin-tbfed-pagefooter 使用教程
---
# Tbfed-pagefooter

Gitbook 插件：为页面添加页脚:

- 版权声明
- 修订时间

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-tbfed-pagefooter

[https://github.com/zhj3618/gitbook-plugin-tbfed-pagefooter](https://github.com/zhj3618/gitbook-plugin-tbfed-pagefooter)

```
"plugins": [
   "tbfed-pagefooter"
]
```

```json
{
"pluginsConfig": {
    "tbfed-pagefooter": {
        "copyright":"Copyright &copy mapull.com 2020",
        "modify_label": "该文件修订时间：",
        "modify_format": "YYYY-MM-DD HH:mm:ss"
    }
}
}
```

不过有个缺点，会在底部加一句英语 `powered by Gitbook`. 但是之后会提到，可以用一个插件[隐藏元素](../other/hideelement.md)去掉这句话。

其他主题均开启了该插件，可以从左上角的版本下拉菜单中选项不同的教程，看到该插件的效果。


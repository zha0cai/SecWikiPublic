---
description: gitbook 自动生成本页的目录结构 插件, gitbook-plugin-atoc，gitbook-plugin-simple-page-toc使用教程
---
# toc

Gitbook 插件：自动生成本页的目录结构。

## atoc

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-atoc

[https://github.com/willin/gitbook-plugin-atoc](https://github.com/willin/gitbook-plugin-atoc)

```json
{
	"plugins": ["atoc"],
	"pluginsConfig": {
		"atoc": {
			"addClass": true,
			"className": "atoc"
		}
	}
}
```

在网页中插入代码 `<!-- toc --> `就能生成本页目录。


## Simple-page-toc

自动生成本页的目录结构。另外 GitBook 在处理重复的标题时有些问题，所以尽量不适用重复的标题。 


> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-simple-page-toc

```json
{
    "plugins" : [
        "simple-page-toc"
    ],
    "pluginsConfig": {
        "simple-page-toc": {
            "maxDepth": 3,
            "skipFirstH1": true
        }
    }
}
```
使用方法: 在需要生成目录的地方加上 `<!-- toc -->`


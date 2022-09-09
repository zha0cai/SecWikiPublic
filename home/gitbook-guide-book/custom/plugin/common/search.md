---
description: gitbook 支持中文搜索 插件, gitbook-plugin-search-plus, gitbook-plugin-search-pro 使用教程
---
# 搜索增强

## Search Plus

Gitbook 插件：支持中文搜索, 需要将默认的 `search` 和 `lunr` 插件去掉。

需要 gitbook 的版本 >= 3.0.0

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-search-plus

[https://github.com/lwdgit/gitbook-plugin-search-plus](https://github.com/lwdgit/gitbook-plugin-search-plus)

```json
{
    "plugins": ["-lunr", "-search", "search-plus"]
}
```

当前版本的搜索功能使用了该插件。

## Search Pro

插件`Search Pro`也能支持搜索中文。

需要 gitbook 的版本 >= 3.0.0

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-search-pro

```json
{
    "plugins": ["-lunr", "-search", "search-pro"]
}
```

经过测试，两个插件都能达到搜索中文的效果。
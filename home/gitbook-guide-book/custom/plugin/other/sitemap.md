---
description: gitbook 用来生成网站地图 sitemap，搜索引擎使用 插件, gitbook-plugin-sitemap 使用教程，插件在线演示
---
# sitemap

Gitbook 插件：用来生成网站地图 sitemap

### sitemap

生成sitemap

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-sitemap

[https://github.com/GitbookIO/plugin-sitemap](https://github.com/GitbookIO/plugin-sitemap)

```json
{
    "plugins": ["sitemap"],
    "pluginsConfig": {
        "hostname": {
            "prefix": "https://www.mapull.com"
        }
    }
}
```

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9" xmlns:news="http://www.google.com/schemas/sitemap-news/0.9" xmlns:xhtml="http://www.w3.org/1999/xhtml" xmlns:mobile="http://www.google.com/schemas/sitemap-mobile/1.0" xmlns:image="http://www.google.com/schemas/sitemap-image/1.1">
<url> <loc>https://mapull.com/gitbook/./</loc> <changefreq>weekly</changefreq> <priority>0.5</priority> </url>
<url> <loc>https://mapull.com/gitbook/basic/command.html</loc> <changefreq>weekly</changefreq> <priority>0.5</priority> </url>
</urlset>
```

查看了`sitemap.xml`文件内容，不满足当前 **百度** 等搜索引擎的 sitemap 规则，没有修改时间 `<lastmod>`

### sitemap-general

生成的 sitemap 在 `./sitemap.xml`

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-sitemap-general

```json
{
    "plugins": ["sitemap-general"],
    "pluginsConfig": {
        "sitemap-general": {
            "prefix": "https://cyberzhg.gitbooks.io/clrs/content/"
        }
    }
}
```
用这个插件试了一下，好像也不行，生成的`sitemap.xml`文件内容和上面的插件一样。

之后，所有 sitemap 相关的插件都试了一遍，均不符合要求，然后只能作罢。


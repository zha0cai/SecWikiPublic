---
description: gitbook 添加github图标 插件, gitbook-plugin-github 使用教程
---
# Github

Gitbook 插件：添加github图标

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-github

安装完竟然无法使用：

`GitBook doesn't satisfy the requirements of this plugin: >=4.0.0-alpha.0.`

如果跟我一样报错，可以卸载后指定版本试试。

- `npm uninstall gitbook-plugin-github`

- `npm i gitbook-plugin-github@2.0.0`

[https://github.com/GitbookIO/plugin-github](https://github.com/GitbookIO/plugin-github)

```json
{
"plugins": [
    "github"
],
"pluginsConfig": {
    "github": {
        "url": "https://github.com/your/repo"
    }
}
}
```

效果就是，在页面右上角有个 github 小图标 <i class="fa fa-github"></i> ，点击小图标跳转到对应的Github地址。

## Github Buttons

添加项目在 `github` 上的 star，watch，fork情况

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-github-buttons

[https://github.com/azu/gitbook-plugin-github-buttons](https://github.com/azu/gitbook-plugin-github-buttons)

```json
{
  "plugins": [
    "github-buttons"
  ],
  "pluginsConfig": {
    "github-buttons": {
      "buttons": [{
        "user": "cj96248",
        "repo": "pikashop-parent",
        "type": "star",
        "size": "large"
      }, {
        "user": "cj96248",
        "type": "follow",
        "width": "230",
        "count": false
      }]
    }
  }
}
```
上面的配置会生成两个图标：

Star 图标：<a class="btn github-icon" aria-label="Star" href="https://gitee.com/mapull/gitbook-guide"><i class="fa fa-github"></i> Star </a>
直达github仓库地址。[演示地址是到gitee]

Follow 图标：<a class="btn github-icon" aria-label="Star" href="https://gitee.com/mapull"><i class="fa fa-github"></i> Follow @mapull </a>
直达github作者关注页面。[演示地址是到gitee]
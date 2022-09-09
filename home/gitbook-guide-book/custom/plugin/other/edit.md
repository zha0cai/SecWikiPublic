---
description: gitbook 在页面上显示编辑按钮 插件, gitbook-plugin-edit-link 使用教程
---
# Edit Link

Gitbook 插件：用来在页面上显示编辑按钮。

如果将 GitBook 的源文件保存到github或者其他的仓库上，使用该插件可以链接到当前页的源文件上。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm i gitbook-plugin-edit-link

点击编辑按钮，即可跳转到github仓库在线编辑这个文件。

```json
{
"plugins": ["edit-link"],
"pluginsConfig": {
    "edit-link": {
        "base": "https://github.com/USER/REPO/edit/BRANCH",
        "label": "Edit This Page"
    }
}
}
```

不过，这个编辑功能在github登录时，可以正常跳转，否则会直接到 github 的登录页面。

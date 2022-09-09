---
description: gitbook 自动生成 `summary.md` 文件内容 插件, gitbook-plugin-summary 使用教程，插件在线演示
---
# gitbook-plugin-summary

Gitbook 插件：自动生成 `summary.md` 文件内容，如果有很多md文件，这个插件可以帮助你生成初始版本。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-summary

如果需要自定义，生成一遍之后，建议去掉该插件。

该插件每次打包都会重新生成  `summary.md` 文件，如果手动修改了其中的内容会被覆盖掉。

如下是生成的一个示例，它不是标准的 SUMMARY 文件，因此某些插件无法识别。

```powershell
## basic

- [GitBook 基础命令](basic/command.md)
- [directory.md](basic/directory.md)
- [directory](basic/directory/README.md)

    - [assist]()
        - [忽略文件](basic/directory/assist/ignore.md)
        - [LANGS.md](basic/directory/assist/language.md)
        - [静态文件](basic/directory/assist/static.md)
        - [词汇表](basic/directory/assist/terms.md)
    - [book.json](basic/directory/book.md)
    - [common.md](basic/directory/common.md)
    - [README.md 文件](basic/directory/readmex.md)
    - [SUMMARY.md 文件](basic/directory/summaryx.md)
- [hello.md](basic/hello.md)
- [安装 Node.js](basic/install.md)
- [Markdown](basic/markdown.md)
- [对比](basic/vs.md)

## config

- [基础配置](config/basic.md)
```
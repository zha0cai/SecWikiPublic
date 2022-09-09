---
description: gitbook 可以为代码添加一个文件名 插件, gitbook-plugin-include-codeblock 使用教程
---

# codeblock-filename

## codeblock-filename

Gitbook 插件：可以为代码添加一个文件名

codeblock-filename 可以为代码添加一个文件名，以便显示当前代码段属于的文件。








## include-codeblock

Gitbook 插件：通过引用文件插入代码

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-include-codeblock

[https://github.com/azu/gitbook-plugin-include-codeblock](https://github.com/azu/gitbook-plugin-include-codeblock)

```json
{
  "plugins": [
    "include-codeblock"
  ]
}
```

### 语法

`[import:"tag",option0:"value0", ...](path/to/file)`

#### 举例

`[include](fixtures/test.js)`

`[import](fixtures/test.js)`

必须是一行，不能嵌套使用：

`Example of code [import](fixtures/test.js)`

~~这种方式不会生效~~

更多详细的例子参见 [github](https://github.com/azu/gitbook-plugin-include-codeblock/blob/master/examples)
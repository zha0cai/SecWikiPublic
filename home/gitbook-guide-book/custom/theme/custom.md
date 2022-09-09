---
description: 使用gitbook 开发主题，自定义主题，并发布主题
---
# 开发主题

GitBook默认使用`theme-default`主题，从3.0.0版本开始，可以自定义主题。

注意：自定义主题可能会导致某些插件不能正常工作。

### 主题的结构

主题是包含模板和资源文件的插件。可以选择只对单独的模板进行替换，因为主题都从默认主题扩展。

|文件夹	|说明
|--|--|
|_layouts	|包含所有模板的主文件夹
|_layouts/website/page.html	|普通页面的模板
|_layouts/ebook/page.html	|在电子书生成期间正常页面的模板(PDF，ePub，Mobi)

### 自定义主题

你可以直接从已有的主题创建模板。模板将首先在书的_layouts文件夹中解析，然后在已安装的插件/主题中解析。

### 简单的扩展

如果你自定义主题的目的只是让不同的文档和书有不同的显示，你可以使用[模板语法](/config/template.md)：

```markdown
{％extends template.self％}

{％block body％}
    {{super()}}
    ...这将被添加到“body”块
{％endblock％}
```

完整的例子可参考主题API。

### 发布主题

主题以`theme-`前缀插件方式发布，可参考(插件文档)。例如，主题`test`将从`theme-test`插件加载，然后从`gitbook-plugin-theme-test` NPM包加载。
---
description: gitbook 开发自己的插件主题，gitbook使用块 block。
---
# 块

扩展块是为作者提供额外功能的最佳方式。

最常见的用法是在运行时处理某些标记内的内容。它像filters。

### 定义一个新的块

`块`由插件定义，块是与块描述符相关联的名称的映射。块描述符需要至少包含一个process方法。

```javascript:index.js
module.exports = {
    blocks: {
        tag1: {
            process: function(block) {
                return "Hello "+block.body+", How are you?";
            }
        }
    }
};
```
`process` 返回替换的html标签内容。

### 处理块参数

参数可以传递给块：

```markdown
{% tag1 "argument 1", "argument 2", name="Test" %}
This is the body of the block.
{% endtag1 %}
```

参数在'process`方法中很容易访问：

```javascript:index.js
module.exports = {
    blocks: {
        tag1: {
            process: function(block) {
                // block.args equals ["argument 1", "argument 2"]
                // block.kwargs equals { "name": "Test" }
            }
        }
    }
};
```
### 处理子块

定义的块可以被拆分成不同的子块，例如：

```markdown
{% myTag %}
    Main body
    {% subblock1 %}
    Body of sub-block 1
    {% subblock 2 %}
    Body of sub-block 1
{% endmyTag %}
```
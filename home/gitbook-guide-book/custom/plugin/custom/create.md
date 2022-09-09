---
description: GitBook 创建和发布插件
---
# 创建和发布插件

GitBook插件是在NPM上发布的遵循定义的约定的节点包。

### 结构体

**package.json**

package.json是用于描述Node.js模块的清单格式。 

GitBook插件构建在Node模块之上，它声明了在GitBook中运行插件所需的依赖性，版本，所有权和其他信息。

插件清单package.json还可以包含有关所需配置的详细信息。 在package.json中配置gitbook字段，需要遵循JSON-Schema准则：
```json
{
    "name": "gitbook-plugin-test-demo",
    "version": "1.0.0",
    "description": "This GitBook plugin is a test demo",
    "engines": {
        "gitbook": ">3.x.x"
    },
    "gitbook": {
        "properties": {
            "myConfigKey": {
                "type": "string",
                "default": "default value",
                "description": "It defines my awesome config!"
            }
        }
    }
}
```
你可以从NPM文档了解更多关于`package.json`的内容。

包名称必须以`gitbook-plugin-`开头，包引擎应该包含gitbook。

**index.js**

index.js是插件运行时的入口：

```javascript:index.js
module.exports = {
    // Map of hooks
    hooks: {},

    // Map of new blocks
    blocks: {},

    // Map of new filters
    filters: {}
};
```

### 发布您的插件

GitBook插件可以在NPM上发布。

要发布新插件，您需要在npmjs.com上创建一个帐户，然后通过命令行发布：

`$ npm publish`

### 专用插件

专用插件可以托管在GitHub上，并使用`git urls`：

```json
{
    "plugins": [
        "myplugin@git+https://github.com/account/gitbookplugintest.git#1.0.0"
    ]
}
```
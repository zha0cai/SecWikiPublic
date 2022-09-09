---
description: 自定义gitbook配置文件，详细的gitbook配置文件 book.json是如何生成的，制作 book.json 教程
---
# 配置文件

### book.json

没有这个文件，也能正常出书。如果你需要个性化添加一些功能，就需要它来配置各种参数。

如果需要这个文件来配置参数，需要手动创建一个 `book.json`文件。
它必须是标准的 json 文件，格式错误将导致`出书`失败。

### 简单示例

简单的 `book.json` 文件：

```json:book.json
{
	"title": "Hello world",   // 书的标题
	"language":"en",          // 语言
	"plugins": [              // 插件
		"code",               // 添加了一个插件
		"-search"             // 去掉了一个插件
	],
	"pluginsConfig": {        // 插件的配置
		"code": {             // code 插件配置了一个参数
			"copyButtons": true
		}
	}
}
```

### 完整的配置

`book.json`文件是唯一一个 gitbook 的配置文件。
所有的参数都通过该文件传递，因此，配置项比较多，完整的配置选项可以参照 [基础配置](/config/basic.md)

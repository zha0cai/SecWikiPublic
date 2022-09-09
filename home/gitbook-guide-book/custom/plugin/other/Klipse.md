---
description: gitbook 集成 `Klipse`在线编辑代码，执行代码 插件, gitbook-plugin-klipse 使用教程，插件在线演示
---
# Klipse

Gitbook 插件：集成 `Klipse` (online code evaluator)

可以用来在线编辑代码:支持的代码有 clojure, javascript, python, ruby, scheme 和 php

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-klipse


```json:book.json
{
    "plugins": ["klipse"]
}
```

[https://github.com/brian-dawn/gitbook-plugin-klipse](https://github.com/brian-dawn/gitbook-plugin-klipse)

插件使用到了 google 的库，开启的时候，明显网页会慢一些。如果不会DIY，最好慎用。

`klipse` 目前支持下面的语言：

```x86asm
javascript: 执行完以后format打印结果
clojure[script]: evaluation is done with Self-Hosted Clojurescript
ruby: evaluation is done with Opal
C++: evaluation is done with JSCPP
python: evaluation is done with Skulpt
scheme: evaluation is done with BiwasScheme
PHP: evaluation is done with Uniter
```

#### 使用示例：

###### js 使用

```js:JS脚本
[1,2,3].map(function(x) { return x + 1;})
```
修改代码中的数字，可以直接显示答案：

```eval-js
[1,2,3].map(function(x) { return x + 1;})
```

###### python 使用

```python
print [x + 1 for x in range(10)]
```
修改代码中的数字，可以直接显示答案：

```eval-python
print [x + 1 for x in range(10)]
```

###### PHP 使用

```php:PHP脚本
$var = ["a" => 1];
var_dump($var);
```

修改代码中的数字，可以直接显示答案：

```eval-php
$var = ["a" => 1];
var_dump($var);
```

> [!WARNING|style:callout|iconVisibility:hidden|label:注意]
> 如果页面内容显示不完整，请F5刷新当前页面
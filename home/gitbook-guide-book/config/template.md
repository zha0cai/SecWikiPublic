---
description: 使用 gitbook中的模板，变量，自定义变量的使用，gitbook中循环if else 语法教程
---
# 模板

GitBook可使用模板特性来扩展定制化功能。

GitBook使用 `Nunjucks` 和 `Jinja2` 的语法。

语法使用大括号`{}`来标记需要处理的内容。

### 变量

变量会从书本内容中寻找对应的值。

如果你想简单地显示一个变量，你可以使用`{{variable}}`语法。

#### 定义变量

变量被定义在 `book.json` 文件中：

```json
{
    "variables": {
        "mapull": "码谱，让编程更容易。"
    }
}
```

这样定义了一个变量 `mapull`，取值为 "码谱，让编程更容易。"

#### 显示变量

定义在 `book.json` 中的变量可以在 `book` 作用域下被访问：

这会从书本的变量中寻找 `mapull` 并显示它。变量的名字可以存在点 (dot) 来查找属性。你同样可以使用方括号语法。

在页面上`{{ book.mapull }}`的语法会被显示为 -> {{ book.mapull }}

在页面上`{{ book["mapull"] }}`的语法会被显示为 -> {{ book["mapull"] }}

如果对应的值没有定义，那么什么也不会显示。

下面这些语句不会输出任何东西，如果 `foo` 没有定义的话：

`{{ book.foo }}`，`{{ book.foo.far }}`，`{{ book.foo.bar.baz }}`。

在页面上`{{ book.foo }}`的语法会被显示为 -> {{ book.foo }}

_什么都没有被显示出来，是因为根本没有定义该变量。_

#### 上下文变量

一些变量也可以用来获取当前文件或GitBook实例的信息。

变量内容比较多，参见 [变量](./variable.html)

### 标签

标签是在章节和模板中执行操作的特殊块

#### If

**if** 测试一个条件并让你选择性的显示内容。它的行为的和编程语言中的 `if` 一样。

如果 `variable` 被定义了并且是真的，那么 "变量为真" 就会被显示出来。否则，没有任何东西会被显示。

```markdown
	{% if variable %}
		变量为真
	{% endif %}
```

你可以使用elif和else来指定选择性条件：

```markdown
    {% if hungry %}
		我很饿
	{% elif tired %}
		我很累
	{% else %}
		我很好！
	{% endif %}
```

#### for

**for** 迭代数组和字典。

让我们来看一下 `book.json` 中的变量：

```json
{ 
  "variables": { 
    "ides": [ { "name": "Eclipse" }, { "name": "IntelliJ IDEA" },{ "name": "Visual Studio Code" } ]
  }
 }
```

编程常用的IDE：

```bash
{% for ides in ide %}

{{ide.name}}

{% endfor %}
```

上面的例子使用 ides 数组的每项的 name 属性作为显示的值，列出了所有的IDE。


### 转义

如果你想要输出任何特殊的目标标签，你可以使用raw，任何在其中的内容都会原样输出。

```bash
{% raw %}
   这些内容 {{ 不会被处理 }}
{% endraw %}
```
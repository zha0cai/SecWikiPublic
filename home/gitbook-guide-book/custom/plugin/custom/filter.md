# 过滤器

Gitbook filters 过滤器用来对变量进行函数操作：

- 常见过滤器 filters
- 自定义 Gitbook 过滤器

过器本质上是可以应用于变量的函数。它们用管道操作符(|)调用，并且可以接受参数。

{% raw %}

```markdown
{{ foo | title }}
{{ foo | join(",") }}
{{ foo | replace("foo", "bar") | capitalize }}
```

{% endraw %}

第三个例子显示了如何链式使用过滤器。首先用“bar”替换“foo”，然后将其大写，最后输出为“Bar”。

### Gitbook 常见过滤器 filters

|-|-|-|-|
|--|--|--|--|
|abs|capitalize|center|default|
|dump|escape|safe|join|
|length|list|lower|replace|
|reverse|round|slice|sum|
|sort|string|title|trim|
|truncate|upper|urlencode|wordcount|

这些filters 基本都能见名知意。

比较常用的 `default` 可以简写 为 `d`，`escape`可以简写 为 `e`。


### 定义过滤器

可以在过滤器的入口自定义函数来扩展过滤器。

过滤器函数将要过滤的内容作为第一个参数，并应返回新内容。 

```javascript
module.exports = {
    filters: {
        hello: function(name) {
            return 'Hello '+name;
        }
    }
};
```

过滤器hello然后可以在书中使用：

{% raw %}

`{{ "Aaron"|hello }}, how are you?`

{% endraw %}

### 处理块参数

参数可以传递到过滤器：

{% raw %}

`Hello {{ "Samy"|fullName("Pesse", man=true)}}`

{% endraw %}

参数传递给函数，命名参数作为最后一个参数(对象)传递。

```javascript
module.exports = {
    filters: {
        fullName: function(firstName, lastName, kwargs) {
            var name = firstName + ' ' + lastName;

            if (kwargs.man) name = "Mr" + name;
            else name = "Mrs" + name;

            return name;
        }
    }
};
```
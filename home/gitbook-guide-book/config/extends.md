---
description: 使用 gitbook 中的继承来扩展功能，gitbook的继承知识教程。
---
# 继承

模板继承是一种**重复使用模板**的简单方式。

当写完一个模板，你可以定义 "block" 让子模板来替换。

继承链可以任意长。

`block` 在模板中定义了一个区域并用一个名字标识了它。

基类模板可以指定一些块，而子类可以用新的内容替换它们。

```
{% extends "./common.md" %}

{% block pageContent %}
This is my page content
{% endblock %}

```


在文件 `common.md` 中，你应该指定用来替换内容的块。

```
{% block pageContent %}
This is the default content
{% endblock %}

{% include "./footer.md" %}
```

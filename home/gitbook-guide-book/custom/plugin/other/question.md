---
description: gitbook 制作在线知识问答，选择题，填空题，隐藏答案 插件, gitbook-plugin-mcqx，gitbook-plugin-fbqx 使用教程，插件在线演示
---
# 题目

Gitbook 插件：可以生成选择题，填空题等常见问题题型。

## 选择题 mcqx

Gitbook 插件：生成类似选择题的效果。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-mcqx

[https://github.com/ymcatar/gitbook-plugin-mcqx](https://github.com/ymcatar/gitbook-plugin-mcqx)

## 填空题 fbqx

Gitbook 插件：生成类似填空题的效果。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-fbqx

[https://github.com/Erwin-Chan/gitbook-plugin-fbqx](https://github.com/Erwin-Chan/gitbook-plugin-fbqx)

### 使用语法

{% raw %}
   {%fbq%}
   
   Testing the plugin, enter the word "hello" into the field ______, "world" into ______.
   
   {%endfbq%}
{% endraw %}


https://ymcatar.gitbooks.io/gitbook-test/content/testing_fbqx.html

回答以后，不能再次回答。

在页面左上角有一个清除历史的标识 <i class="fa fa-history"></i> ，点击以后就可以再次回答问题了。

## 隐藏答案 spoiler

[https://github.com/manchiyiu/gitbook-plugin-spoiler](https://github.com/manchiyiu/gitbook-plugin-spoiler)

隐藏答案，当鼠标划过时才显示.

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-spoiler

https://ymcatar.gitbooks.io/gitbook-test/content/testing_spoiler.html
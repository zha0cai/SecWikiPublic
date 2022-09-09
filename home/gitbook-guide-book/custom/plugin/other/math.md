---
description: gitbook 数学公式 & Tex 插件, gitbook-plugin-katex，gitbook-plugin-mathjax 使用教程，插件在线演示
---
# 数学公式 & Tex

GitBook插件： 可以使用插件支持数学公式和 Tex。

当前有两个官方的插件用来显示数学公式：`mathjax` 和 `katex`。

## 数学插件 katex

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-katex

[https://github.com/GitbookIO/plugin-katex](https://github.com/GitbookIO/plugin-katex)

```json
{
    "plugins": ["katex"]
}
```

#### 使用语法

**文字与公式混合显示** 

{% raw %}

数学公式：$$\int_{-\infty}^\infty g(x) dx$$

{% endraw %}

数学公式：$$\int_{-\infty}^\infty g(x) dx$$

**一行显示公式**

{% raw %}
$$

\int_{-\infty}^\infty g(x) dx

$$
{% endraw %}

页面的显示效果：

{% math %}\int_{-\infty}^\infty g(x) dx{% endmath %}

**更复杂一点的用法**

{% raw %}

When {% math %}a \ne 0{% endmath %}

there are two solutions to {% math %}(ax^2 + bx + c = 0){% endmath %} and 

they are {% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

{% endraw %}

页面的显示效果：

When {% math %}a \ne 0{% endmath %}

there are two solutions to {% math %}(ax^2 + bx + c = 0){% endmath %} and 

they are {% math %}x = {-b \pm \sqrt{b^2-4ac} \over 2a}.{% endmath %}

## 数学插件 mathjax

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-mathjax


[https://github.com/GitbookIO/plugin-mathjax](https://github.com/GitbookIO/plugin-mathjax)

```json
{
    "plugins": ["mathjax"]
}
```

#### 使用语法

两个数学公式插件的使用语法几乎一致。


### MathJax 和 KaTeX 的区别

mathjax 和 katex 插件是 Tex 公式绘制的不同实现，它们基于各自的开源库：KaTeX 和 MathJax 。

MathJax 支持整个 Tex 语法，但是在制作电子书版本时不是很完美。 

KaTex 在所有格式（网页和电子书）的绘制上都很完美，但是还不支持 所有的语法。



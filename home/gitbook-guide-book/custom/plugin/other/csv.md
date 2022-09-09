---
description: gitbook 支持 csv 文件 插件, gitbook-plugin-include-csv 使用教程
---
# Include-csv

Gitbook 插件：展示 csv 文件。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install --save gitbook-plugin-include-csv

[https://github.com/TakuroFukamizu/gitbook-plugin-include-csv](https://github.com/TakuroFukamizu/gitbook-plugin-include-csv)

```json
{
    "plugins": ["include-csv"]
}
```

#### 使用示例1：


{% raw %}

{% includeCsv  src="./demo.csv", useHeader="true" %}

{% endincludeCsv %}

{% endraw %}

其中， demo.csv 中的内容：

```
编程语言,排名,份额
Java, 1,16.88
C , 2,16.18
Python, 3,9.09
```

效果如下所示：


|编程语言|排名|份额|
|--|--|--|
|Java| 1|16.88|
|C | 2|16.18|
|Python| 3|9.09|

#### 使用示例2：

{% raw %}

```shell
{% includeCsv %}
hoge,fuga
a,0001
b,002
{% endincludeCsv %}
```

{% endraw %}

效果如下所示：


|编程语言|排名|份额|
|--|--|--|
|Java| 1|16.88|
|C | 2|16.18|
|Python| 3|9.09|

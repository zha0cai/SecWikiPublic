---
description: gitbook ace 插件, gitbook-plugin-ace 使用教程
---
# Ace Plugin

Gitbook 插件：使 GitBook 支持ace 。

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-ace

[https://github.com/ymcatar/gitbook-plugin-ace](https://github.com/ymcatar/gitbook-plugin-ace)

```json:book.json
{
"plugins": [
    "ace"
]}
```

#### 使用示例


```c:hello-world
// This is a hello world program for C.
#include <stdio.h>

int main(){
  printf("Hello World!");
  return 1;
}
```

{%ace edit=true, lang='c_cpp'%}
// This is a hello world program for C.
#include <stdio.h>

int main(){
  printf("Hello World!");
  return 1;
}
{%endace%}

> [!WARNING|style:callout|iconVisibility:hidden|label:注意]
> 如果页面内容显示不完整，请F5刷新当前页面
---
description: gitbook 中如何忽略文件，使用 gitignore文件排除不想要的文件或文件夹
---
# 忽略文件

### 忽略的文件和文件夹

GitBook将读取`.gitignore`、`.bookignore`和`.ignore`文件，以获取要忽略的文件和文件夹的列表。
被忽略的文件不会被上传到版本中，这些文件中的格式遵循与`.gitignore`相同的约定：

```bash
＃这是一行注释

＃忽略文件 test.md
test.md

＃忽略所有 test 命名的文件
test.*

＃忽略所有 html 类型的文件
*.html

＃忽略目录 test 中的所有内容
test/*
```
---
description: gitbook 图片显示优化相关 插件, gitbook-plugin-image-captions 使用教程，插件在线演示
---
# 图片

Gitbook 插件：Gitbook 图片显示优化相关插件。

## Image Captions

抓取内容中图片的`alt`或`title`属性，在图片下面显示标题 

> [!TIP|style:flat|iconVisibility:hidden|labelVisibility:hidden]
> npm install gitbook-plugin-image-captions

[https://github.com/todvora/gitbook-plugin-image-captions](https://github.com/todvora/gitbook-plugin-image-captions)

```json
{
    "plugins": [
         "image-captions"
    ]
}
```

可以自定义显示信息：

```json
{
  "pluginsConfig": {
      "image-captions": {
          "caption": "Image - _CAPTION_"
      }
  }
 }
```

其中的 `_CAPTION_` 会被替换为图片的 `title`或者 `alt`

`caption`几个取值：

- `_PAGE_LEVEL_` : chapters 序号
- `_PAGE_IMAGE_NUMBER_`：图片在章节中的序号
- `_BOOK_IMAGE_NUMBER_`：图片在整本书中的序号

#### 举个例子

本主题没有启用该功能，下图是一个示例：

使用的配置：

```json
{
  "plugins": ["image-captions"],
  "pluginsConfig": {
      "image-captions": {
          "caption": "Image - _CAPTION_"
      }
  }
 }
```

显示的效果：

![Image](./img.png)
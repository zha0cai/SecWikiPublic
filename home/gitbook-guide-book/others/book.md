---
description: book.json文件格式演示，一般的book.json文件教程，gitbook 的book.json例子，常见的gitbook配置文件举例
---
# Gitbook book.json 配置文件

本站的 `book.json` 配置文件

```json
{
  "title": "GitBook 简明教程",
  "language": "zh-hans",
  "author": "码谱",
  "links": {
    "sidebar": {
      "码谱": "http://www.mapull.com"
    }
  },
  "plugins": [
    "-search",
    "-lunr",
    "-sharing",
    "-livereload",
    "github",
    "donate",
    "chart",
    "todo",
    "graph",
    "puml",
    "katex",
    "code",
    "ace",
    "sitemap-general",
    "mermaid-gb3",
    "include-csv",
    "flexible-alerts",
    "chapter-fold",
    "anchor-navigation-ex",
    "theme-comscore"
  ],
  "pluginsConfig": {
    "anchor-navigation-ex": {
      "showLevel": false,
      "showGoTop": true
    },
    "sitemap-general": {
      "prefix": "https://www.mapull.com/gitbook/comscore/"
    },
    "my-toolbar": {
      "buttons": [
        {
          "label": "下载PDF",
          "icon": "fa fa-file-pdf-o",
          "url": "https://www.mapull.com/gitbook/comscore/book.pdf",
          "position": "left",
          "text": "下载PDF",
          "target": "_blank"
        }
      ]
    },
    "donate": {
      "wechat": "https://www.mapull.com/logo/mapull-qr.png",
      "button": "反馈",
      "wechatText": "微信扫码"
    },
    "versions": {
      "options": [
        {
          "value": "https://www.mapull.com/gitbook/api/",
          "text": "Theme API"
        },
        {
          "value": "https://www.mapull.com/gitbook/comscore/",
          "text": "Theme comscore",
          "selected": true
        }
      ]
    },
    "github": {
      "url": "https://gitee.com/mapull/gitbook-guide"
    },
    "edit-link": {
      "base": "https://gitee.com/mapull/gitbook-guide",
      "label": "Edit This Page"
    }
  },
  "variables": {
    "mapull": "码谱，让编程更容易。",
    "ides": [{"name": "Eclipse"}, {"name": "IntelliJ IDEA"}, {"name": "Visual Studio Code"}]
  },
  "structure": {
    "readme": "home.md"
  }
}
```
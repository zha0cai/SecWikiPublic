---
description: 手把手教你如何制作自己的 gitbook plugin 插件，演示 gitbook 插件的制作教程
---
# 制作第一个 gitbook 插件

## 起个名字

gitbook规定，插件必须是以`gitbook-plugin`开头，一般插件名称类似 `gitbook-plugin-xxx`

其中 `xxx`是你插件的名称，可以先去 [npm.js官网](https://www.npmjs.com) 查看是否名称存在。

或者使用命令行，也可以查看：

```x86asm
E:\gitbook\>npm search gitbook-plugin-mapull-default
No matches found for "gitbook-plugin-mapull-default"
```

这样表示名称可以用，可以继续操作。

要是有类似下面这样的输出，就说明不能使用这个名字，需要换个名称。

```x86asm
E:\gitbook\>npm search gitbook-plugin-search
NAME                      | DESCRIPTION          | AUTHOR          | DATE       | VERSION  | KEYWORDS
gitbook-plugin-search     | Search input for…    | =jpreynat…      | 2016-04-20 | 2.2.1    |
```

## github

#### 创建 github账号

首先去 [github 官网](https://github.com/mapull)申请账号，有的话最好了。

#### 创建 github项目

创建一个 public 的项目，名称就是上面的那个 `gitbook-plugin-xxx`，这里我使用的名称是 `gitbook-plugin-mapull-default`。

是 mapull 站点的 gitbook 专属插件。

#### Clone仓库到本地

在计算机的任意目录，clone项目：

```x86asm
E:\temp>git clone https://github.com/mapull/gitbook-plugin-mapull-default.git
Cloning into 'gitbook-plugin-mapull-default'...
remote: Enumerating objects: 21, done.
remote: Counting objects: 100% (21/21), done.
remote: Compressing objects: 100% (14/14), done.
remote: Total 21 (delta 2), reused 21 (delta 2), pack-reused 0
Unpacking objects: 100% (21/21), done.
```

注意命令是 `git clone`

如果项目未初始化，那么下载的文件夹啥也没有。

## npm 初始化

进入之前下载好的文件夹，比如我的`gitbook-plugin-mapull-default`:

执行 

`npm init`

里面的内容，把认知的内容填一下，其他默认，直接回车：

```x86asm
E:\temp\gitbook-plugin-mapull-default>npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (temp)
version: (1.0.0)
description:
entry point: (index.js)
test command:
git repository:
keywords:
author: mapull
license: (ISC)
About to write to E:\temp\gitbook-plugin-mapull-default\package.json:

{
  "name": "temp",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "mapull",
  "license": "ISC"
}


Is this OK? (yes) yes
```

有个关于 test 的错误，直接忽略它。

## 编写代码

正规插件的目录结构应该是这样的：

```text
.gitbook-plugin-mapull-default
├── assets
|    ├── plugin.css
|    └── plugin.js
├── index.js
├── package.json
└── README.md
```

上面的内容，有些插件没有 css，则不需要 `plugin.css`文件，有些插件没有 js ，则不需要 `plugin.js`文件

### package.json 文件

`package.json`是之前 npm 自动生成的文件。

请在`package.json`中加上需要的引擎版本：

```json:package.json
{
  "version": "1.0.0",
  "engines": {
      "gitbook": ">=3.0.0-pre.0"
  }
}
```

### README.md 文件

需要新建该文件，`README.md`文件应该添加对于该插件的描述信息，说明该插件的用途，以及如何使用。

### index.js

在 `index.js`文件中添加如下内容：

```javascript:index.js
module.exports = {
    website: {
        assets: './assets',
        js: [
            'mapull.js'
        ],
        css: [
            'mapull.css'
        ]
    }
};
```

### plugin.css

css 文件没有特殊的要求，按照 css 的书写规范即可。

### plugin.js

建议 `plugin.js`有如下的格式，引入'gitbook'是最小化的要求。

```javascript:plugin.js
require(['gitbook'], function(gitbook) {
    // 所有的代码写在这里
});
```

如果代码中需要用到 jQuery ，那么

```javascript:plugin.js
require(['gitbook', 'jQuery'], function(gitbook, $) {
    // 所有的代码写在这里
});
```

## 上传代码

代码写完以后，提交到 `github`：

提交代码：

`git commit`

提交到远程：

`git push`

如果提交成功，可以在 github 看到刚才的代码， [gitbook-plugin-mapull-default](https://github.com/mapull/gitbook-plugin-mapull-default)

## 发布插件

### npm 创建账号

在 [npmjs 官网](https://www.npmjs.com/)注册一个账号。

### 发布到 npm

在刚才执行 `npm init`的文件夹，执行 `npm publish`.

> [!WARNING|style:flat|label:注意|iconVisibility:hidden]
> 如果使用的淘宝的镜像源，是不能成功的，因为淘宝源不接受代码(只读)，它只从中央仓库同步代码。

推荐使用 cnpm 代替 npm, 而不是直接修改镜像源，参见[淘宝 NPM 镜像](https://npm.taobao.org/)。

第一次推送，需要先登录,控制台会提示输入用户名，密码信息。

`npm publish`

```x86asm:推送
E:\workspace\gitbook-plugin-mapull-default>npm publish
npm notice
npm notice package: gitbook-plugin-mapull-default@1.0.0
npm notice === Tarball Contents ===
npm notice 0     _layouts/assets/mapull.css
npm notice 1.6kB _layouts/website/page.html
npm notice 60B   index.js
npm notice 181B  _layouts/assets/mapull.js
npm notice 623B  package.json
npm notice 86B   README.md
npm notice === Tarball Details ===
npm notice name:          gitbook-plugin-mapull-default
npm notice version:       1.0.0
npm notice package size:  1.4 kB
npm notice unpacked size: 2.6 kB
npm notice shasum:        cc787a8e62dce65fa9886c1949ad0bd18999d850
npm notice integrity:     sha512-ESeQqOPjxVcai[...]Quhsjs9BSRKvg==
npm notice total files:   6
npm notice
+ gitbook-plugin-mapull-default@1.0.0
```

推送以后，可以在 [npmjs 官网](https://www.npmjs.com/) 找到推送的插件。

此时，淘宝镜像源还没有，需要等待至少10分钟才能看到。

#### 推送注意

- 确保插件可用，因为npm官网对一个插件，只能发一个相同的版本

```x86asm
npm ERR! code E403
npm ERR! 403 403 Forbidden - PUT https://registry.npmjs.org/gitbook-plugin-mapull-default - 
You cannot publish over the previously published versions: 1.0.0.
```

- 再次发布插件时，需要修改`package.json`中的版本号， 即 version 值
- 免费用户，每24小时，只能发布一次，发布失误，就得等到第二天

```x86asm
npm ERR! code E403
npm ERR! 403 403 Forbidden - PUT https://registry.npmjs.org/gitbook-plugin-mapull-default 
- gitbook-plugin-mapull-default cannot be republished until 24 hours have passed.
```
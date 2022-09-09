---
description: 如何安装 gitbook, gitbook 与 gitbook-cli，gitbook 版本选择
---

# 安装

GitBook的安装非常简单。您的系统只需满足这两个要求：

- NodeJS（推荐使用v4.0.0及以上版本）
- Windows，Linux 或 Mac OS X

### 安装 Node.js

首先我们需要做的是安装 Node.js。大家可以到 [Node.js](http://nodejs.cn/) 的中文官网进行下载。

下载完成后，执行双击进行运行安装。

安装完成后，打开 cmd 命令行，输入 `node -v` 查看安装的 nodejs 的相关版本信息。

Windows 建议安装 [nvm](https://github.com/coreybutler/nvm-windows/releases) 进行 nodejs 和 npm 版本管理，后续会更一篇 nvm 安装文章。

```x86asm
C:\Users\admin>node -v
v12.14.0
```

### Node.js 镜像配置

`Node.js` 安装完成后，我们就可以开始安装 gitbook 了。但是在安装之前，最好先配置一下`Node.js` 源的下载镜像地址。

因为默认的镜像地址是在国外，国内访问速度极慢，因此我们需要设置国内的镜像地址。

国内的我推荐大家使用阿里巴巴的镜像地址 `http://registry.npm.taobao.org` 。

执行下面的命令，进行配置：

`npm config set registry http://registry.npm.taobao.org`

除了上面的方法外，我们也可以在用户主目录下编辑 `.npmrc` 文件，添加一行

`registry=http://registry.npm.taobao.org`

保存就可以了。

Windows用户的主目录一般在 `C:\Users\Administrator` ，具体随你的操作系统系统盘而定。

### 安装 gitbook

执行命令：
`npm install gitbook-cli -g`

`gitbook-cli` 是安装和管理 GitBook 版本库的程序。它会自动安装 GitBook 所需的模块来创建一本书。

安装完成后，可以执行 `gitbook --version` 查看安装的版本信息。

第一次执行 `gitbook --version` 会进行 gitbook 的安装。可能会出错，建议安装低版本的 nodejs。解决办法参考[错误解决]()章节

```x86asm
C:\Users\admin>gitbook --version
CLI version: 2.3.2
GitBook version: 3.2.3
```

### 安装其他版本

gitbook 命令可以方便地下载和安装不同版本的 GitBook 来测试你的书：

使用 `gitbook ls-remote` 列出可用于安装的远程版本。

```x86asm
C:\Users\admin>gitbook ls-remote
Available GitBook Versions:

     4.0.0-alpha.6, 4.0.0-alpha.5, 4.0.0-alpha.4, 4.0.0-alpha.3, 4.0.0-alpha.2, 4.0.0-alpha.1, 3.2.3....

Tags:

     latest : 2.6.9
     pre : 4.0.0-alpha.6
```

输出的版本内容比较长，用 ... 省略。

使用 `gitbook fetch` 可以来指定需要获取的版本。

`gitbook fetch 4.0.0-alpha.6`

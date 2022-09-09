---
description: 学习如何使用 gitbook 基础命令，演示 gitbook 常用命令，关于 gitbook 命令的学习教程。
---
# 基础命令

这里主要介绍一下 GitBook 的命令行工具 gitbook-cli 的一些命令, 首先说明两点:

- gitbook-cli 和 gitbook 是两个软件
- gitbook-cli 会将下载的 gitbook 的不同版本放到 ~/.gitbook中, 可以通过设置 GITBOOK_DIR 环境变量来指定另外的文件夹

- honkit 是 gitbook-cli 的一个正在维护的分支。
- 下面会同步介绍 honkit 的一些命令和注意事项。

### 列出 gitbook 所有的命令：

##### 初始化 gitbook：

`gitbook init`

##### 初始化 honkit:

`honkit init`

该命令主要用户初始化 book，创建必要的 README 和 SUMMARY 文件。

---

##### 输出 gitbook 的帮助信息：

`gitbook help`

```bash
D:\gitbook>gitbook help
    build [book] [output]       build a book
        --log                   Minimum log level to display (Default is info; Values are debug, info, warn, error, disabled)
        --format                Format to build to (Default is website; Values are website, json, ebook)
        --[no-]timing           Print timing debug information (Default is false)

    serve [book] [output]       serve the book as a website for testing
```

##### 输出 honkit 的帮助信息：

`honkit help`

```bash
PS D:\xxx\zha0cai> honkit help
Usage: honkit [options] [command]

Options:
  -V, --version                    output the version number
  -h, --help                       display help for command

Commands:
  build [options] [book] [output]  build a book
  serve [options] [book] [output]  serve the book as a website for testing
  parse [options] [book]           parse and print debug information about a book
  init [options] [book]            setup and create files for chapters
  pdf [options] [book] [output]    build a book into an ebook file
  epub [options] [book] [output]   build a book into an ebook file
  mobi [options] [book] [output]   build a book into an ebook file
  help [command]                   display help for command
```

##### 输出 gitbook-cli 的帮助信息：

`gitbook --help`

```powershell
D:\gitbook>gitbook --help

  Usage: gitbook [options] [command]


  Options:

    -v, --gitbook [version]  specify GitBook version to use
    -d, --debug              enable verbose error
    -V, --version            Display running versions of gitbook and gitbook-cli
    -h, --help               output usage information


  Commands:

    ls                        List versions installed locally
    current                   Display currently activated version
    ls-remote                 List remote versions available for install
    fetch [version]           Download and install a <version>
    alias [folder] [version]  Set an alias named <version> pointing to <folder>
    uninstall [version]       Uninstall a version
    update [tag]              Update to the latest version of GitBook
    help                      List commands for GitBook
    *                         run a command with a specific gitbook version
```

---

##### 下载所需的资源，如插件等：

`gitbook install`

```x86asm
D:\gitbook\book2-theme-default>gitbook install
info: installing 3 plugins using npm@3.9.2
info:
info: installing plugin "splitter"
info: install plugin "splitter" (*) from NPM with version 0.0.8
D:\gitbook\book2-theme-default
-- gitbook-plugin-splitter@0.0.8
info: >> plugin "splitter" installed with success
...
```

相比之下 honkit 移除了 `install` 命令

> Remove install command
> Instead of it, just use `npm install` or `yarn install`

如果插件比较多，下载会花很长时间。

- gitbook 可以用 `npm install gitbook-plugin-xxx` 这种方式单个下载插件。

- honkit 完美兼容了几乎所以的 gitbook 插件，如下安装： 
  
  > Almost all plugins work without changes!
  > Support `gitbook-plugin-*` packages
  > 
  > - You should install these plugins via npm or yarn
  > - `npm install gitbook-plugin-<example> --save-dev`
  > 
  > 在 honkit 中你可以直接全局安装，只需要加上 `-g` 参数，那么就不用为每本书都安装插件了。

---

##### 生成静态网页：

`gitbook build`

指定输出目录 

`gitbook build ./ ./bookname`

- 参数一：书籍所在的目录，如果执行 build 指令时位于当前项目目录，输入 `./`
- 参数二：书输出的目录，相对于当前目录

```bash
D:\temp>gitbook build
info: 7 plugins are installed
info: 6 explicitly listed
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 2 pages
info: found 4 asset files
info: >> generation finished with success in 0.4s !
```

`honkit build`

指定输出目录

`honkit build ./ ./bookname`

```
PS D:\xxx\zha0cai> honkit build
(node:26172) [DEP0147] DeprecationWarning: In future versions of Node.js, fs.rmdir(path, { recursive: true }) will be removed. Use fs.rm(path, { recursive: true }) instead
(Use `node --trace-deprecation ...` to show where the warning was created)
info: 6 plugins are installed
info: 6 explicitly listed
info: plugin "versions-select" is loaded
info: plugin "highlight" is loaded
info: plugin "search" is loaded
info: plugin "lunr" is loaded
info: plugin "fontsettings" is loaded
info: plugin "theme-default" is loaded
info: found 1 pages
info: found 145 asset files
info: >> generation finished with success in 0.7s !
```

运行完该命令后，会在当前文件夹中生成一个 `_book`文件夹，其中就是解析出来的静态网站，包含了点子书中的所有信息。

可以将它直接放置在如 nginx 、apache server 、tomcat 等服务器中直接运行。

_用浏览器直接打开生成的 html 文件是可以的，但是无法完成基本的交互。_

这里 Window 下编译会遇到一个坑，可以参考[错误解决]()章节。

---

##### 生成静态网页并运行服务器：

`gitbook serve`

```x86asm
D:\temp>gitbook serve
Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 7 plugins are installed
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 2 pages
info: found 4 asset files
info: >> generation finished with success in 0.5s !

Starting server ...
Serving book on http://localhost:4000
```

用浏览器直接访问 [http://localhost:4000/](http://localhost:4000/)，就可以看到生成的电子书网站。

`honkit serve` 同理

---

##### 生成时指定 gitbook 的版本, 本地没有会先下载：

`gitbook build --gitbook=2.0.1`

##### 列出本地所有的 gitbook 版本：

`gitbook ls`

```x86asm
D:\temp>gitbook ls
GitBook Versions Installed:

    * 3.2.3

Run "gitbook update" to update to the latest version.
```

##### 列出远程可用的 gitbook 版本：

`gitbook ls-remote`

```x86asm
D:\temp>gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```

`gitbook --version` 可以得到同样的结果。

```x86asm
C:\Users\admin>gitbook --version
CLI version: 2.3.2
GitBook version: 3.2.3
```

---

##### 安装对应的 gitbook 版本：

`gitbook fetch 标签/版本号`

##### 更新到 gitbook 的最新版本：

`gitbook update`

##### 卸载对应的 gitbook 版本：

`gitbook uninstall 2.0.1`

---

##### 指定 log 的级别：

`gitbook build --log=debug`

log 很有用，就是 `--log debug` 帮我定位了问题。

##### 输出错误信息：

`gitbook build --debug`

```x86asm
D:\temp\>gitbook build --debug
info: 23 plugins are installed
info: 9 explicitly listed
info: loading plugin "splitter"... OK
info: loading plugin "anchor-navigation-ex"... OK
info: loading plugin "versions-select"... OK
info: loading plugin "highlight"... OK
info: loading plugin "search"... OK
info: loading plugin "lunr"... OK
info: loading plugin "sharing"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 28 pages
info: found 68 asset files
info: >> generation finished with success in 4.6s !
```

- 生成其他格式的文件命令在 [扩展章节](../extend/export.md)
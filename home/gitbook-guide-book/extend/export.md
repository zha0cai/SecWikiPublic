---
description: gitbook导出多种格式，如导出pdf,导出ePub,导出Mobi格式，Word docx格式转换为 md 格式
---
# 输入/输出

GitBook可以把你的书本生成为不同格式的电子书。

## 输出格式

### 静态网站

这是默认的格式。它生成一个可交互的静态站点。

### PDF (Portable Document Format)

Portable Document Format (PDF) 是一以一种独立于软硬件，以及操作系统的方式来保存文档的格式。这是一种很普遍的格式。文件拥有的扩展名为 .pdf。

### ePub (electrontic publication)

EPUB (electrontic publicaton的简称，有时称它为epub) 是一个由国际电子出版物论坛 (IDPF) 制定的免费并开放的电子书标准。文件拥有的扩展名为 .epub，苹果和谷歌的设备支持ePub格式。

### Mobi (Mobipocket)

Mobipocket电子书格式是基于使用XHTML的开放电子书标准，并且可以包含JavaScript以及框架。亚马逊的设备 (Kindle) 支持这样的格式。


## gitbook-convert

`gitbook-convert` 可以把docx、xml、html、odt文档转成GitBook

#### 安装命令

`$ npm install gitbook-convert -g`

测试是不是安装成功。

```x86asm
D:\gitbook>gitbook-convert
Usage: gitbook-convert [options] <file>
Options:
  -V, --version                  output the version number
  -t, --document-title [string]  Name used for the main document title (default: null)
  -a, --assets-dir [dirname]     Name of the documents assets export directory (default: "assets")
  -m, --max-depth [integer]      Maximum title depth to use to split your original document into sub-chapters (default: 2)
  -p, --prefix                   Prefix filenames by an incremental counter
  -d, --debug                    Log stack trace when an error occurs
  -h, --help                     output usage information
  gitbook-convert accepts the following formats:
    .docx: Microsoft Office Open XML Document
    .html: HyperText Markup Language
    .xml: Docbook Markup Language
    .odt: OpenOffice / Open Document Format

  After converting your document, the corresponding GitBook files will be placed in ./export/<file>/.
```

#### 转换文件

`$ gitbook-convert [options] <file> [export-directory]`


##### 举个例子

```powershell
D:\gitbook>gitbook-convert settings.docx
[log]: "Creating export folder..."
[log]: "Creating assets folder..."
[log]: "Creating summary file..."
[log]: "Done."
[log]: "Converting docx file to HTML..."
[log]: "Done."
[log]: "Extracting footnotes..."
[log]: "Parsing chapters..."
[log]: "Processing chapters..."
[log]: "Converting chapters to markdown..."
[log]: "Writing summary..."
[log]: "Writing file: D:\\gitbook\\export\\README.md"
[log]: "Done."
```

看一下生成的 `D:\\gitbook\\export`中的文件：

```
.
|- assert
|- README.md
|- SUMMARY.md
```

所有的数据都解析到了 `REAMDE.md` 中。
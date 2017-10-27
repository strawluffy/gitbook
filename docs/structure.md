# 目录结构

GitBook的目录结构很简单.在[SUMMARY](pages.md)文件罗列的Markdown/Asciidoc文件，之后会被转换为HTML多行标签，并且他们结构会稍有[不同 ](languages.md).

一个基本的GitBook目录结构一般会像下面这样：

```
├── book.json
├── README.md
├── SUMMARY.md
├── chapter-1/
|   ├── README.md
|   └── something.md
└── chapter-2/
    ├── README.md
    └── something.md
```

这些文件的作用解释如下：

| File | Description |
| --- | --- |
| `book.json` | 存储 [配置](config.md) 数据 \(可选\) |
| `README.md` | 前言 / 关于书籍的介绍 \(必须\) |
| `SUMMARY.md` | 目录结构 \(查阅 [页面](pages.md)\) \(可选\) |
| `GLOSSARY.md` | 词典 / 术语解释 \(查阅 [术语](lexicon.md)\) \(可选\) |

### 静态文件和图片

静态文件并不会在`SUMMARY.md` 中列出，所有的静态文件，除非是[忽略的](#ignore)，都会被拷贝到输出目录中。



忽略的文件以及目录

GitBook 会读取 `.gitignore`, `.bookignore` and `.ignore` 文件来获取哪些需要被忽略的文件或者目录。

这些文件内的格式 和 `.gitignore`中的设定规则相同.

```
# This is a comment

# Ignore the file test.md
test.md

# Ignore everything in the directory "bin"
bin/*
```

### Project integration with subdirectory  {#subdirectory}

在软件工程中，你可以使用子目录\(如 docs/\)来存储工程文档相关的文件。你可以配置 [`root` 选项](config.md) 来强调GitBook可以从这个位置找到文档文件。

```
.
├── book.json
└── docs/
    ├── README.md
    └── SUMMARY.md
```

需要在 `book.json` 加入下面的内容:

```
{
    "root": "./docs"
}
```




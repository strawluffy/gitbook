# GitBook FAQ

本页面涵盖了通用的问题以及GitBook格式和工具链方面的回答。

关于GitBook.com以及编辑器的问题应合并到这个栏目里面: [help.gitbook.com's FAQ](http://help.gitbook.com/faq.html).

#### How can I host/publish my book? 我如何托管/发布我的图书?

书籍可以在 [GitBook.com](https://www.gitbook.com).上托管和发布非常容易。GitBook的输出文件，可以被托管到任何静态文件网站上。

#### 我可以使用什么工具来编辑我的内容？

任何文本编辑器都可以。但是我们推荐使用: [GitBook Editor](https://www.gitbook.com/editor). [GitBook.com](https://www.gitbook.com) 也提供了一个在线版本的编辑器.

---

#### GitBook 是否支持 RTL/bi-directional 文本 ?

The GitBook 格式支持 right to left, 以及 bi-directional 来编写. 为了使他生效，你需要指定一个语言 \(ex: `ar`\), 或者强制GitBook 在 `book.json`中使用RTL :

```json
{
    "language": "ar",
    "direction": "rtl"
}
```

With version 3.0 of GitBook, it's automatically detected according to the content.  
_Note that, while the output book will indeed respect RTL, the Editor doesn't support RTL writing yet_.

#### Should I use an `.html` or `.md` extensions in my links?

You should always use paths and the `.md` extensions when linking to your files, GitBook will automatically replace these paths by the appropriate link when the pointing file is referenced in the Table of Contents.

#### Can I create a GitBook in a sub-directory of my repository?

Yes, GitBooks can be created in [sub-directories](structure.md#subdirectory). GitBook.com and the CLI also looks by default in a serie of [folders](structure.md).

#### Does GitBook supports RTL languages?

Yes, GitBook automatically detect the direction in your pages \(`rtl` or `ltr`\) and adjust the layout accordingly. The direction can also be specified globally in the [book.json](config.md).

---

#### Does GitBook support Math equations?

GitBook supports math equations and TeX thanks to plugins. There are currently 2 official plugins to display math: [mathjax](https://plugins.gitbook.com/plugin/mathjax) and [katex](https://plugins.gitbook.com/plugin/katex).

#### Can I customize/theme the output?

Yes, both the website and ebook outputs can be customized using [themes](themes/README.md).

#### Can I add interactive content \(videos, etc\)?

GitBook is very [extensible](plugins/README.md). You can use [existing plugins](https://plugins.gitbook.com) or create your own!


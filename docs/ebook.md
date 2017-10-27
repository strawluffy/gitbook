# 生成 eBooks and PDFs

GitBook 可以生成网站, 也可以生成电子书\(ePub,Mobi,PDF\).

```
# Generate a PDF file
$ gitbook pdf ./ ./mybook.pdf

# Generate an ePub file
$ gitbook epub ./ ./mybook.epub

# Generate a Mobi file
$ gitbook mobi ./ ./mybook.mobi
```

### 安装 ebook-convert 

`ebook-convert` 是产生电子书籍\(epub, mobi, pdf\)所必须的.

##### GNU/Linux

安装 [Calibre application](https://calibre-ebook.com/download).

```
$ sudo aptitude install calibre
```

在一些 GNU/Linux 发布的版本中，node会被安装为nodejs，这时你需要手动来创建链接:

```
$sudo ln -s /usr/bin/nodejs /usr/bin/node
```

##### OS X

Download the [Calibre application](https://calibre-ebook.com/download). After moving the `calibre.app` to your Applications folder create a symbolic link to the ebook-convert tool:

```
$ sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

You can replace `/usr/bin` with any directory that is in your $PATH.

### Cover封面

封面在所有的电子书格式中都会用到。你可以自己提供一个，或者通过下面的插件生成一个: [autocover plugin](https://plugins.gitbook.com/plugin/autocover).

为了提供一个封面，需要在你的书籍的跟慕下放置一个 `cover.jpg` 的图片。增加一个 `cover_small.jpg` 可以指定一个小一些版本的封面。封面应该是一个**JPEG** 文件.

一个号的封面应该满足下面的要求:

* Size of 1800x2360 pixels for `cover.jpg`, 200x262 for `cover_small.jpg`
* 没有边框
* 清洗可见的书籍标题。
* 任何重要的内容需要在小版本中可见。




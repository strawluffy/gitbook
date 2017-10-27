# 设置和安装GitBook

需要花费数分钟的时间来安装好GitBook。

### GitBook.com

[GitBook.com](https://www.gitbook.com) 是一个编写、发布并托管书籍的网站。在上面发布内容以及协同工作非常的便捷。

这个网站集成 [GitBook Editor](https://www.gitbook.com/editor).

### 本地安装

##### 需求

GitBook的安装非常容易，你的系统只需要满徐下面两个需求：

* NodeJS \(v4.0.0 以上的版本\)
* Windows, Linux, Unix, or Mac OS X

##### 使用NPM安装

安装GitBook最好的方法就是通过**NPM**工具. 在命令提示符下，输入下面的命令来安装GitBook:

```
$ npm install gitbook-cli -g
```

`gitbook-cli` 可以在相同的系统上面安装和使用多个GitBook版本的工具。他会自动安装一个构建书籍所有需要的GitBook版本.

##### 创建书籍

GitBook 会首先创建一个模板文件：

```
$ gitbook init
```

如果你希望创建在一个新目录下创建书籍，你需要运行下面的命令: `gitbook init ./directory`

预览并为书籍启动一个web服务:

```
$ gitbook serve
```

或者只创建静态web文件:

```
$ gitbook build
```

##### 安装之前的版本

`gitbook-cli`  下载和安装其他版本的GitBook非常的容易，这些版本用于测试你的书籍:

```
$ gitbook fetch beta
```

使用 `gitbook ls-remote` 来查询远程可用的GitBook版本。

##### 排错

你可以使用`--log=debug` 以及 `--debug` 选项来获取更多错误信息 \(堆栈跟踪\). 例如:

```
$ gitbook build ./ --log=debug --debug
```




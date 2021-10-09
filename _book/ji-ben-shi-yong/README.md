# 基本使用

#### 基本使用

```text
gitbook init
```

初始化书籍目录

> `README.md` 和 `SUMMARY.md` 是两个必须文件, `README.md` 是对书籍的简单介绍, `SUMMARY.md` 是书籍的目录结构

```text
gitbook serve
```

 serve 命令也可以指定端口：

```text
gitbook serve --port 2333
```

编译和预览书籍

> 注: `gitbook serve` 命令实际上会首先调用 `gitbook build` 编译书籍，完成以后会打开一个 web 服务器，监听在本地的 4000 端口

6、生成静态网页 执行 gitbook build 命令构建书籍，默认将生成的静态网站输出到 \_book 目录。实际上，这一步也包含在 gitbook serve 里面，因为它们是 HTML，所以 gitbook 通过 Node.js 提供服务了。

```text
gitbook build #生成静态网页
```

可以生成 PDF 格式的电子书：

```text
gitbook pdf ./ ./mybook.pdf
```

生成 epub 格式的电子书：

```text
gitbook epub ./ ./mybook.epub
```

生成 mobi 格式的电子书：

```text
gitbook mobi ./ ./mybook.mobi
```

如果生成不了，还需要安装工具[ebook-convert](https://calibre-ebook.com/)，安装好后，还需要执行以下命令

```text
ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
```

编辑 SUMMARY.md 文件


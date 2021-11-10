# 基本使用

## 初始化书籍目录

```text
gitbook init
```

> `README.md` 和 `SUMMARY.md` 是两个必须文件, `README.md` 是对书籍的简单介绍, `SUMMARY.md` 是书籍的目录结构

## 启动服务

运行一个 web 服务，通过[http://localhost:4000](http://localhost:4000/) 可以预览该书籍

```text
gitbook serve
```

 serve 命令也可以指定端口：

```text
gitbook serve --port 2333
```

## 编译和预览书籍

> 注: `gitbook serve` 命令实际上会首先调用 `gitbook build` 编译书籍，完成以后会打开一个 web 服务器，监听在本地的 4000 端口

## 生成静态网页

执行 gitbook build 命令构建书籍，默认将生成的静态网站输出到 \_book 目录。实际上，这一步也包含在 gitbook serve 里面，因为它们是 HTML，所以 gitbook 通过 Node.js 提供服务了。

```text
gitbook build #生成静态网页
```

## 可以生成 PDF 格式的电子书：

```text
gitbook pdf ./ ./mybook.pdf
```

## 生成 epub 格式的电子书：

```text
gitbook epub ./ ./mybook.epub
```

## 生成 mobi 格式的电子书：

```text
gitbook mobi ./ ./mybook.mobi
```



注：如果生成不了，还需要安装工具[ebook-convert](https://calibre-ebook.com/)，安装好后，还需要执行以下命令

```text
ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
```

## Debugging

可以获取更好的错误信息 (使用堆栈跟踪)

```
gitbook build ./ --log=debug --debug
```

## 输出帮助信息

```
gitbook --help
```

## 生成静态网页

```
gitbook build
```

## 生成静态网页并运行服务器

```
gitbook serve
```

##  生成指定 gitbook 的版本

```
gitbook build --gitbook=2.0.1
```

## 列出本地所有的 gitbook 版本

```
gitbook ls
```

## 列出远程可用的 gitbook 版本

```
gitbook ls-remote
```

## 安装对应的 gitbook 版本

```
gitbook fetch 标签/版本号
```

## 更新到 gitbook 的最新版本

```
gitbook update
```

## 卸载对应的 gitbook 版本

```
git book uninstall 2.0.1
```

## 指定 log 级别

```
gitbook build --log=debug
```

## 输出错误信息

```
gitbook build --debug
```
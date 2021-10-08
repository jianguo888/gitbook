# 运行 bug 报错

### 运行 bug 报错

下载较新版本的 node.js 会导致 gitbook 运行报错，如果你也遇到了

gitbook init ::初始化 出错  
if \(cb\) cb.apply\(this, arguments\)，cb.apply is not a function 

## 解决方案1 

产生这个报错的原因在于，nodejs的版本不对，不支持这个gitbook. 切换成nodejs的v10.21.0版本就会成功。

## 解决方案2

 打开报错 文件 62行 // fs.stat = statFix\(fs.stat\) // fs.fstat = statFix\(fs.fstat\) // fs.lstat = statFix\(fs.lstat\) 注销

注意：gitbook-cli已经不维护了，所以对高版本的node会有兼容性问题。目前来看，node10版本还是能稳定运行的


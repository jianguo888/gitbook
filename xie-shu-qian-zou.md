# 写书前奏

本地安装nvm进行npm的版本控制

### **【1】安装nvm**

可以从Github获取nvm最新版本自行安装：https://github.com/coreybutler/nvm-windows/releases

![](.gitbook/assets/image%20%2812%29.png)



![](.gitbook/assets/image%20%2813%29.png)

![](.gitbook/assets/image%20%2811%29.png)



| 命令 | 说明 |
| :--- | :--- |
| nvm v | 查看nvm版本 |
| nvm list | 查看node安装列表 |
| nvm install version | 安装指定版本的node |
| nvm use version | 切换使用版本 |
| nvm uninstall version | 卸载对应版本 |

nvm下载慢问题的解决：在nvm安装包中的setting.txt文件中添加

```text
node_mirror: https://npm.taobao.org/mirrors/node/
npm_mirror: https://npm.taobao.org/mirrors/npm/
```

  
作者：HOM  
链接：https://juejin.cn/post/6982074406273024030  
来源：稀土掘金  
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。


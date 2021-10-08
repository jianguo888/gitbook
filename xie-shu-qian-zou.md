# 写书前奏

本地安装nvm进行npm的版本控制

### **【1】安装nvm**

可以从Github获取nvm最新版本自行安装：https://github.com/coreybutler/nvm-windows/releases

![](.gitbook/assets/image%20%2812%29.png)



![](.gitbook/assets/image%20%2814%29.png)

![](.gitbook/assets/image%20%2811%29.png)



| 命令 | 说明 |
| :--- | :--- |
| nvm v | 查看nvm版本 |
| nvm list | 查看node安装列表 |
| nvm install version | 安装指定版本的node |
| nvm use version | 切换使用版本 |
| nvm uninstall version | 卸载对应版本 |

[https://nodejs.org/download/release/](https://nodejs.org/download/release/)

nvm下载慢问题的解决：在nvm安装包中的setting.txt文件中添加

```text
node_mirror: https://npm.taobao.org/mirrors/node/
npm_mirror: https://npm.taobao.org/mirrors/npm/
```

  
安装指定版本

nvm install 版本号

 使用指定版本

nvm use 版本号 

 安装cnpm

npm install -g cnpm 

 当使用cnpm install的时候可能遇到如下异常：

```text
cnpm : 无法加载文件 C:\Users\12746\AppData\Roaming\npm\cnpm.ps1，因为在此系统上禁止运行脚本。有关详细信息，请参阅 https:/go.microsoft.com/fwlink/?LinkID=135170 中的 about_Execution_Policies。
所在位置 行:1 字符: 1
+ cnpm install
+ ~~~~
    + CategoryInfo          : SecurityError: (:) []，PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess

```

此时找到Power shell，以管理员身份运行，然后输入：set-ExecutionPolicy RemoteSigned 然后A回车 

```text
set-ExecutionPolicy RemoteSigned 
```





## 设置node，npm的安装目录

```text
npm config set prefix "D:\nodejs\node_global"
npm config set cache "D:\nodejs\node_cache"
同时将D:\nodejs\node_global加到系统变量path中

```



  



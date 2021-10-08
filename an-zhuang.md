# 安装

## 安装Gitbook

1. 安装 [Node.js](https://nodejs.org/)
2. 通过 npm 来安装 gitbook

   ```text
   npm install gitbook-cli -g
   ​
   yarn global add gitbook-cli
   ```

   安装完成后，输入 `gitbook --version`来查看是否安装成功 **第一次使用，cli 会自动安装`gitbook`,安装时间视网络环境而定，请耐心等待**

   若要卸载，就执行 `npm uninstall gitbook-cli -g`来删除

   由于我这里已经安装了，安装完成可用以下命令查看。

   ![img](https://luckly007.oss-cn-beijing.aliyuncs.com/img/1750888-20200827093429403-214093467.png)

   **npm通过gitbook-cli安装gitbook出现问题，一直安装Gitbook 3.2.3报错**

   问题原因 大概意思是：gitbook-cli引用了旧版的graceful-fs，导致出现问题

   解决方式 需要更新graceful-fs库

   执行如下命令

   ```text
   # 进入gitbook-cli全局安装目录的node依赖文件夹
   ​
   F:\environment\nodejs\node_modules\gitbook-cli\node_modules\npm\node_modules
   ​
   # 更新graceful-fs库
   ​
   npm install graceful-fs@latest --save
   ​
   ```

   再次执行，gitbook -V即可 ，需要耐心等待一会。

   之后再次查看，OK。

nodejs历史版本下载：[https://nodejs.org/dist/](https://nodejs.org/dist/)

![image-20211007094646266](https://luckly007.oss-cn-beijing.aliyuncs.com/img/image-20211007094646266.png)

我选择的是node-v12.22.3-x64.msi：

{% embed url="https://nodejs.org/dist/latest-v12.x/node-v12.22.3-x64.msi" %}

如果依旧报错，请用10.21.0版本吧

或者按照后面的[运行bug报错章节](https://gitbook.luckly.work/yun-hang-bug-bao-cuo)



或者：

降级nodejs版本为：[node-v9.11.2-x64.msi](https://nodejs.org/dist/latest-v9.x/node-v9.11.2-x64.msi)

重新安装nodejs。

重试：


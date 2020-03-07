**Linux下搭建git环境**



**安装node.js**

（1）去官网下载和自己系统匹配的文件：

 中文网址：http://nodejs.cn/download/

通过 uname -a 命令查看到我的Linux系统位数是64位（备注：x86_64表示64位系统， i686 i386表示32位系统），如图

![1583558068301](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583558068301.png)

因此下载64位node.js

![1583558085388](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583558085388.png)



2、下载下来的tar文件上传到服务器并且解压，然后通过建立软连接变为全局；

1）上传服务器可以是自己任意路径，目前我的放置在在家目录下一个文件夹1_AI 路径为 cd /home/linux/1_AI

（就是说把下载的node的.tar压缩包放到一个指定目录，目录位置你随意）

2）把下载的node-v12.16.1-linux-x64.tar.xz压缩包剪切到1_AI 并解压

   tar -xvf  node-v6.10.0-linux-x64.tar.xz  

​    打开node文件夹，确认一下nodejs下bin目录是否有node 和npm文件，如果有执行软连接，如果没有重新下载执行上边步骤；

3）建立软连接，变为全局，进入node.js下的bin目录

\# ln -s /home/linux/1_AI/node-v12.16.1-linux-x64/bin/npm   /usr/local/bin/npm

\# ln -s /home/linux/1_AI/node-v12.16.1-linux-x64/bin/node   /usr/local/bin/node

![1583558304682](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583558304682.png)

4）最后一步检验nodejs是否已变为全局

在Linux命令行node -v 命令会显示nodejs版本，如图所示为大功告成

**Gitbook安装:**

gitbook Ubuntu下，在安装好nodejs后直接使用如下命令安装,依据自己安装的目录可能有权限问题，自行加上

npm install -g gitbook-cli

由于网络的原因，安装的时间可能会较长一些，请耐心等待直到安装完成。安装完成后，同样的在bin目录下（其他路径不能运行）设置一个符号链接。 

\# ln -s /home/linux/1_AI/node-v12.16.1-linux-x64/bin/gitbook  /usr/local/bin/gitbook

![1583558349463](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583558349463.png)然后查看gitbook版本，检查是否安装成功。

gitbook -V #查看gitbook版本  （有时候因为是第一次安装可能需要多等一会儿）

成功：

![1583558367218](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583558367218.png)


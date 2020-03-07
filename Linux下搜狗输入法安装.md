## Ubuntu下的搜狗输入法安装教程

方法一：

我已经将搜狗安装包发给大家。大家把包复制到家目录下即可：

（1）把搜狗拼音安装包放到家目录下：

![1583557527441](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583557527441.png)

（2）在当前终端位置运行：sudo dpkg -i sogoupinyin_2.3.1.0112_amd64

运行后，发现提示少了一些依赖包，于是运行下面的命令：sudo apt-get -f install

![1583557654466](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\1583557654466.png)



这里由于之前已经运行过此命令，所以没有出现安装信息。如果是之前提示有依赖包没有安装，此时会出现安装信息。等安装完成之后，再运行一下命令：sudo dpkg -i sogoupinyin_2.3.1.0112_amd64

此时就应该提示安装成功。

​    重启电脑，搜狗输入法就能正常使用了。（Ctrl+空格   就可以换出搜狗输入法了）





方法二：

使用 Linux 最大的烦恼就是中文输入法了，但是在 Ubuntu 下面，这都不是事！搜狗拼音已经有 Ubuntu 版本 了，所以我们照样可以使用中文输入法。

（1）在 Ubuntu 下打开搜狗输入法 Linux 版的官网（或Windows下下载然后放到Ubuntu）

 http://pinyin.sogou.com/linux/?r=pinyin，并下载你需要 的版本，这里选择 32 位版，如图所示，

​             ![image-20200115094730521](2_Linux下搜狗输入法安装.assets/image-20200115094730521.png)                  

选择立即下载 32bit 以后，然后选择“SaveFiles”浏览器会将 deb 安装包下载到当前用户目录的 Download 子目录下。

（2）从图形用户界面进入 Download 目录，双击下载得到的 deb 软件包，Ubuntu 会自动弹出软件管理器，然 后点击右上角的 Install，输入 root 密码即可安装搜狗输入法。

 ![image-20200115094737016](2_Linux下搜狗输入法安装.assets/image-20200115094737016.png)

（3）在终端中输入 im-config，这时会出现一个对话框，点击 OK，有一个对话框，点击 Yes，你会看到下图所示对话框。

 ![image-20200115094743383](2_Linux下搜狗输入法安装.assets/image-20200115094743383.png)

如果上面选中的是 fcitx，就不用管，直接关闭；如果不是，在 select 栏目下，勾选 fcitx，点击 OK 即可。又会出现一个对话框，接着就是 OK，最后重启 Ubuntu 虚拟机。

（4）重启以后在终端中输入：fcitx-config-gtk3 出现下图所示对话框。

 ![image-20200115094752740](2_Linux下搜狗输入法安装.assets/image-20200115094752740.png)

点击对话框左下角的（+）按钮， 弹出另一个对话框。然后，取消 Only Show Current Language（很重要，否则不能找到刚安装过的搜狗输入法!） 最后，在输入框中输入 sogou，选中点击 OK 即可，这时候输入法列表就会多出搜狗拼音了，如下图

 ![image-20200115094759544](2_Linux下搜狗输入法安装.assets/image-20200115094759544.png)

（5）关闭这些对话框，使用 ctr+空格键就可以进行 3 输入法的切换了。可以在浏览器，文本编辑器以及命令 行输入中文，其效果下图所示。

 ![image-20200115094805476](2_Linux下搜狗输入法安装.assets/image-20200115094805476.png)

 
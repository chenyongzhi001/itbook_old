# 十七、Windows平台Itunes软件更换备份路径 {#第十七章windows平台itunes软件更换备份路径}

前期准备：拷贝Junction文件到本地，文件路径：\192.168.10.33\Share\共享\日常软件 for Windows\其它 ，

1下载Junction文件，解压后将Junction.exe复制粘贴到Windows目录下![](https://ws3.sinaimg.cn/large/006tKfTcly1fj2zqs6pa1j31c20q2n3t.jpg)

2 打开iTunes备份路径：C:\Users\用户名\AppData\Roaming\Apple Computer\MobileSync，其中目录MobileSync就是用来存放backup文件的。\(用户名为本机用户名\)![](https://ws3.sinaimg.cn/large/006tKfTcly1fj2zr8za83j31c20rogr9.jpg)

3 将目录MobileSync剪切到其它你想备份的盘，比如D盘：D:\Itunes（建议选择较大空间的硬盘，可用空间尽量超过手机容量）![](https://ws4.sinaimg.cn/large/006tKfTcly1fj2zrkn2h8j31c20pt422.jpg)

4 运行cmd。输入以下指令：junction "C:\Users\用户名\AppData\Roaming\Apple Computer\MobileSync" D:\Itunes\MobileSync，需要注意的是用户名要改为你的主机名，例如:pc。然后enter,就会弹出Junction应用请求对话框。![](https://ws2.sinaimg.cn/large/006tKfTcly1fj2zrypv6yj31c20mbwj4.jpg)

5 点击Agree,则会提示：Created: C:\Users\用户名\AppData\Roaming\Apple Computer\MobileSync\Targetted at: D:\Itunes\MobileSync表示已经成功，此时再看回原备份文件夹的图标会多了一个快捷方式的小箭头。这样就成功更改了iTunes的备份路径了。![](https://ws2.sinaimg.cn/large/006tKfTcly1fj2zrypv6yj31c20mbwj4.jpg)![](https://ws1.sinaimg.cn/large/006tKfTcly1fj2zsps74cj31c20md790.jpg)

6 多了一个小箭头的文件夹，表明这是一个链接目录，以上的操作相当于把C盘的文件夹挪到了F盘，而C盘的目录只是一个连接目录，它就像一个实实在在有这个目录一样，程序不会发现连接目录与普通目录有什么不同，连接目录与原始目录的文件夹内容是一样的，如果你对任意一个文件夹的内容作出修改，那另一个也会相应改变，但磁盘空间使用量并没有改变，因为只是实现连接罢了，并不是将原文件复制以及同步，这是与一般的文件夹快捷方式最大的区别。


# QQ for Ubuntu16
____
参考资料：  
https://im.qq.com/linuxqq/download.html
____
1. [QQ官网](https://im.qq.com/linuxqq/download.html)官网下载 Linux 版QQ，此处用的 shell 文件
2. 安装 QQ 前确保你的系统已安装 gtk2.0。
```shell
sudo apt install libgtk2.0-0
```
3. 安装
```shell
sudo ./linuxqq_1.0.1-b1-100_x86_64.sh
```
4. 卸载，卸载时尽量使用你安装时对应的方式卸载（参考你所使用的系统安装包管理器说明），例如
```shell
sudo rpm -e linuxqq
sudo dpkg -r linuxqq
```
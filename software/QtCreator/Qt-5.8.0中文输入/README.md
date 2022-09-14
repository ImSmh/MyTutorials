# Ubuntu16 环境下 Qt-5.8.0 无法输入中文的解决方案
1. 安装 fcitx-frontend-qt5
```
sudo apt-get install fcitx-frontend-qt5
```
2. 到该目录下复制 libfcitxplatforminputcontextplugin.so 文件
```
/usr/lib/x86_64-linux-gnu/qt5/plugins/platforminputcontexts
```  
3. 将文件粘贴至你的 Qt 文件的两个目录中(YourFile:你的 Qt 安装路径)
```
YourFile/5.8/gcc_64/plugins/platforminputcontexts
YourFile/Tools/QtCreator/lib/Qt/plugins/platforminputcontexts
```
4. 重启


# win 系统 Qt 输出乱码
https://blog.csdn.net/qq_39791014/article/details/120791691

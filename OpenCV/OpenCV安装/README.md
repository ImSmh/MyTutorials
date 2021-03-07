# Ubuntu 16.04 安装 OpenCV     

* ### 1.1 下载OpenCV  
本教程所使用的 OpenCV 版本为 OpenCV-3.4.3，要使用其他版本到 [OpenCV官网](http://opencv.org/releases.html) 下载 Sources 。  

* ### 1.2 解压zip包  
```shell
unzip opencv-3.4.3.zip  
cd opencv-3.4.4.zip  
```
  
* ### 1.3 安装依赖库  
```shell
sudo apt-get install build-essential libgtk2.0-dev libavcodec-dev libavformat-dev libjpeg.dev libtiff4.dev libswscale-dev libjasper-dev  
```

* ### 1.4 安装并执行 cmake  
期间会下载东西，耐心等待  
```shell
sudo apt-get install cmake  
mkdir build  
cd build  
cmake ..  
```

* ### 1.5 执行 make  
```shell
sudo make  
```

* ### 1.6 执行 install  
```shell
sudo make install  
```

* ### 2.1 OpenCV 编译结束，接下来配置 OpenCV 的编译环境，首先讲 OpenCV 的库添加到路径，从而让系统找到  
```shell
sudo gedit /etc/ld.so.conf.d/opencv.conf   
```
该命令执行后可能会打开一个空白文件，在文件末尾添加  
```shell
/usr/local/lib   
```

* ### 2.2 执行以下命令使得刚才的配置生效  
```shell
sudo ldconfig  
```

* ### 2.3 配置 bash  
```shell
sudo gedit /etc/bash.bashrc  
```
在文件末尾添加  
```shell
PKG_CONFIG_PATH=$PKG_CONFIG_PATH:/usr/local/lib/pkgconfig  
export PKG_CONFIG_PATH  
```

* ### 2.4 执行以下命令使得配置生效  
```shell
source /etc/bash.bashrc  
```

* ### 2.5 更新  
```shell
sudo updatedb  
```

* ### 3.1 测试安装。在 opencv-3.4.3/samples/cpp/example_cmake 目录下，有一个官方的 demo，执行以下命令，程序会打开摄像头，能看到 Hello OpenCV，即代表OpenCV安装成功。
```shell
cmake .  
make  
./opencv_example  
```

* ### 4 [QtCreator 安装及建立 OpenCV项目](https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/README.md)


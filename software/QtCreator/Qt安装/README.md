# Ubuntu16 安装 QtCreator
到 [Qt](https://www.qt.io/download) 官网下载 Qt 文件  
- 在文件所在目录内打开终端，给文件添加运行权限，并运行
```shell
chmod +x qt-opensource-linux-x64-5.8.0.run   
./qt-opensource-linux-x64-5.8.0.run   
```
- 除了第二步点击 skip，其余全点 next 就行了 
- 新建 C++ 控制台应用
    - 点击 New Project
    <img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2017-13-40%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">  
    
    - 选择 Qt Console Application，点击 Choose
    <img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2017-13-56%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">   
    
    - 更改项目名称及路径，点击下一步
    <img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2017-14-18%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">   
    
    - 下一步
    <img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2017-14-31%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">  
    
    - 完成
    <img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2017-14-36%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">  
    
- 如果建立 OpenCV 项目，将以下内容加入如图 .pro 文件中
```
INCLUDEPATH += /usr/local/include \
/usr/local/include/opencv \
/usr/local/include/opencv2

LIBS += /usr/local/lib/libopencv_calib3d.so \
/usr/local/lib/libopencv_core.so \
/usr/local/lib/libopencv_features2d.so \
/usr/local/lib/libopencv_flann.so \
/usr/local/lib/libopencv_highgui.so \
/usr/local/lib/libopencv_imgcodecs.so \
/usr/local/lib/libopencv_imgproc.so \
/usr/local/lib/libopencv_ml.so \
/usr/local/lib/libopencv_objdetect.so \
/usr/local/lib/libopencv_photo.so \
/usr/local/lib/libopencv_shape.so \
/usr/local/lib/libopencv_stitching.so \
/usr/local/lib/libopencv_superres.so \
/usr/local/lib/libopencv_videoio.so \
/usr/local/lib/libopencv_video.so \
/usr/local/lib/libopencv_videostab.so
```
<img src = "https://github.com/ImSmh/MyTutorial/blob/master/QtCreator/Qt%E5%AE%89%E8%A3%85/images/2019-09-06%2018-11-25%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png" width = "60%">

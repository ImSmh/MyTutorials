# Ubuntu16.04 系统 Python 版本切换
Ubuntu16.04 自带 Python2 和 Python3 ，默认使用 Python2，输入以下命令切换为 Python3  
```shell
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 100  
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 150  
```

# IDEA 连接 MySQL
## win10
### IDE 直接连接
1. 打开一个 Web 项目，点击 IDEA 右上位置 Database
![点击Database](1.png)
2. 点击 + ，选择Data Source，点击 MySQL
![MySQL](2.png)
3. 填写 Name、Host、Port、User、Password，点击 Test CONNECTION
![Test_Connection](3.png)

- 连接问题
    Server returns invalid timezone. Need to set 'serverTimezone' property. 
    点击 Advanced，找到 serverTimezone，输入GMT
    ![Test_Connection](4.png)
    ![succeeded](5.png)

### jdbc 连接
1. 新建 Java 项目，项目右键添加 lib 文件夹，将 mysql-connector-java 驱动放入文件夹
![jdbc](6.png)
2. 右键 lib，选择 Add as libary
![add_as_library](7.png)
3. 测试
![结果](8.png)
- mysql-connector-java 下载地址 https://dev.mysql.com/downloads/connector/j/
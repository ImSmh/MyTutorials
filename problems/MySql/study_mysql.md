# MySQL 学习记录
1. 登录 `mysql -u root -p`
2. 创建数据库 `create database dbname`
3. 删除数据库 `drop database dbname`
4. 查看数据库 `show databases`
5. 选择数据库 `use bdname`
6. 创建表
```mysql
CREATE TABLE runoob_tbl(
runoob_id INT NOT NULL AUTO_INCREMENT,
runoob_title VARCHAR(100) NOT NULL,
runoob_author VARCHAR(40) NOT NULL,
submission_date DATE,
PRIMARY KEY ( runoob_id )
)ENGINE=InnoDB DEFAULT CHARSET=utf8;
Query OK, 0 rows affected (0.16 sec)
```
注解：
- 如果你不想字段为 NULL 可以设置字段的属性为 NOT NULL， 在操作数据库时如果输入该字段的数据为NULL ，就会报错。
- AUTO_INCREMENT定义列为自增的属性，一般用于主键，数值会自动加1。
- PRIMARY KEY关键字用于定义列为主键。 您可以使用多列来定义主键，列间以逗号分隔。
- ENGINE 设置存储引擎，CHARSET 设置编码。
7. 删除表 `drop table tablename`
8. 查看表 `show tables`
9. 查看表格式 `desc tablename`
10. 插入
```mysql
INSERT INTO tablename
(col1, col2, col3)
VALUES
(value1, value2, value3);
```
11. 查询数据
- 查看全部
    ```mysql
    select * from tablename
    ```
- 查看列
    ```mysql
    select col1, col2 from tablename
    ```
- 查看特定
    ```mysql
    select * from tablename where (BINARY: 用于区分大小写) ...
    ```
12. 修改或更新数据 `update tablename set col1=value1 (where ...)`
13. 删除数据 `delete from tablename (where ...)`
14. LIKE 查找 `select * from runoob_tbl where col like "(%)"`
15. UNION 跨表
```
select * from tablename1
(where ...)
UNION (ALL: 添加ALL为全部数据，否则不包含重复数据)
select * from tablename2
(where ...)
```
16. ORDER BY 排序 `select * from tablename order by col asc/desc`
17. GROUP BY 分组 
18. JOIN https://www.runoob.com/mysql/mysql-join.html


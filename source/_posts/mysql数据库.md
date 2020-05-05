

## []()数据持久化保存

#### []()服务端

数据库：mysql、mongodb、redis、oracle
⽂件存储 ：fs

#### []()客户端

本地缓存 locastorage 、 sessionStorage、cookie…

## []()数据库

数据库（Database）是按照数据结构来组织、存储和管理数据的仓库。

>###### []()进入mysql命令环境
>
>`mysql -u 用户名 -p`
>`Enter Password`  输入密码
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327182318283.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>###### []()数据库操作
>
>命令都需要`;`隔开
>
>1. `SHOW DATABASES` 显示数据库
>
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327182410814.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`CREATE DATABASE 数据库名`  创建数据库
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327182841852.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`SHOW CREATE DATABASE 数据库名` 查看数据库信息
>4.`ALTER DATABASE 数据库名 CHARACTER SET = utf8`修改数据库编码格式
>5. `DROP DATABASE 数据库名` 删除数据库
>6.`quit` 退出

>###### []()数据库中的表操作
>
>1.`USE 数据库名`选择数据库
>2.`SELECT DATABASE()`查看当前选择的数据库
>3.`CREATE TABLE tablename()`创建数据表
>   `CREATE TABLE users(`
>    `username VARCHAR(20),`
>    `age TINYINT UNSIGNED,`
>    `salary FLOAT(8,2) UNSIGNED`
>   `)`
>4.`SHOW TABLES`查看数据表
>5.`SHOW COLUMNS FROM 表名`查看数据表的结构

>###### []()数据库中的数据操作
>
>1.添加：`INSERT INTO 表名 (字段⼀,字段⼆,字段三) VALUES ("值⼀","值⼆","值三")`
>2.删除：`DELETE FROM 表名 WHERE 条件;`
>3.修改：`UPDATE 表名 SET 设置的内容 WHERE 条件语句;`
>4.查找：`SELECT 字段 FROM 表名 WHERE 条件语句;`
>5.条件语句：
>   1)ADN和  2)OR或  3)LIKE
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200403154552162.png)
>   4) ORDER BY (DESC/ASC)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200403154904139.png#pic_center)
>   5)LIMIT 限制查询
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200403154729452.png#pic_center)
>
>   6)JOIN ON  7)AS 别名，将复杂的表明简化
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200403160057726.png#pic_center)

>###### []()mysql2模块
>
>下载：`npm install mysql2`
>引入：`const mysql = require("mysql2")`
>使用：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327184958606.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>配置完成后，存入这个常量中
>常量中内置一个query()方法，有两个参数
>第一个参数数据操作，一般为查询语句；
>第二个参数为一个回调函数，函数中返回一个错误信息和数据，这个函数会返回一个promise对象
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327192619230.png#pic_center)
>第二种方法： `connection.promise().query(1，2)`
>参数1数据操作 参数2 添加操作时的具体数据
>返回一个数组，解构赋值
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405105716395.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

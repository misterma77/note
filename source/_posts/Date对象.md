

创建一个Date对象，用来处理时间和日期
使用关键字new配合，生成一个Date对象
Date对象是用来处理时间和日期，内置了一系列获取和设置日期和时间的方法

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128151722514.png)
>显示时间：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128151732836.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

tolocalString() 把时间对象转换为字符串
getTime() 返回1970年1月1日距今的毫秒数

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128152544355.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128152559242.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()设置set

**1.`setTime()`     以毫秒数设置Date对象**

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153509107.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153518306.png)

**2.`setFullYear()`   设置年，月，日**

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153651621.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153654337.png)

**3.`setMonth()`   设置月，日(毫秒)**

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153806445.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153814509.png)

**4.`setHours()`   设置时，分，秒**

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153943693.png)
>显示：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128153950921.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**5.`setMinutes()`   设置分，秒**

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154133656.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154151341.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**6.`setSeconds()` 设置秒**
代码：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154334567.png)
显示效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154343753.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()获取get

**1.getFullYearr()  获取年份
2.getMonth()   获取月份
3.getDate()     获取一个月中的第几天
4.getDay()    获取一周中的第几天
5.getHours()   获取小时
6.getMinutes()   获取分钟
7.getSeconds() 获取秒数**
代码:
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154938396.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128154948936.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()计算活了多久

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128160717566.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200128160725279.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()定时器

`setInterval(参数1,参数2)` 用来重复执行某一功能
参数1：执行的具体功能，自定义
参数2：每次执行的间隔时间，自定义，单位为毫秒

## []()一次性定时器

`setTimeout(参数1,参数2)` 只执行一次的定时器
参数1：执行的具体任务
参数2：间隔多久执行，(延迟)

## []()清除定时器

`clearInterval()`
需要有记录器(变量自增),来记录运行次数，到达指定条件时触发
定义定时器时，要用一个变量来储存定时器
`clearInterval`的括号中放储存定时器的变量名,清除之后，将这个变量置空(null)
代码:
![在这里插入图片描述](https://img-blog.csdnimg.cn/2020012816030448.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

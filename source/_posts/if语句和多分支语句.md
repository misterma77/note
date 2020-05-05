

## []()if语句

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125125045465.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125125513698.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125125526325.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()多分支语句

switch.case
作用：提供多个分支，功能类似`if-else`级联式，但是代码可读性更好
语法：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125130705242.png)

>switch 后面是整型或字符型的表达式
>case 后面是整型或字符型的常量
>break case和default都默认跟随一个，结束当前语句
>default 类似于`if-else`中的`else`
>如果case的值，都无法和表达式匹配，那么执行default后的代码
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125132806360.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125132503365.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125132837192.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()prompt

输入框，返回的数据，默认是字符串类型，即使不是，也会自动转换

## []()数据类型转化

数据类型转换分为隐式转换和显示转换

>###### []()隐式转换
>
>又叫自动转化
>在变量中，储存的数据是什么类型
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125133631887.png)
>显示效果:
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020012513364736.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>###### []()显示转化
>
>又叫手动转换
>`parseInt()`将小括号中的内容，转换为Number类型，并返回
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125134008754.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125134018457.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>`String()`将括号中的内容，转化为字符串类型，并返回
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125134237650.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200125134248886.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)



Tween.js是一个让元素能够平滑地执行动画效果的js库

###### []()使用

1.下载，引入或网络链接
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200201103834932.png)
2.Quad,二次方缓动效果
3.Cubic,三次方缓动效果
4.Quart，四次方缓动效果
5.Quint，五次方缓动效果
6.Sine，正弦缓动效果
7.Expo，指数缓动效果
8.Circ，圆形缓动效果
9.Elastic，指数衰减正弦曲线缓动函数
10.Back，超过范围的三次方的缓动函数
11.Bounce，指数衰减的反弹曲线缓动函数

>以上每种函数的三种效果(速率)，不影响总时间，总路程
>1.easeIn加速
>2.easeOut减速
>3easeInOut先加速后减速

12.Linear，线性(匀速)

###### []()四个参数

t:动画已经执行的时间
b:初始的位置
c:变化的值
d:总时间(总步数)

代码：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200201103808883.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

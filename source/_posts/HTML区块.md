

## []()块元素和行元素

大多数HTML元素被分为块级元素和行级元素(内联元素)

>**块级元素**：块级元素在浏览器显示时，通常会以新行来开始（和结束）
>独占一行，可以设置宽、高、内外间距，具备盒模型

>**行级元素**：内联元素在显示时通常不会以新行开始
>只占内容大小的区域，不可以设置宽、高、内外间距，不具备盒模型

## []()display属性

display元素的显示方式

>属性值：
>none无（隐藏）不单单是视觉上的，在页面布局中也彻底消失，不占位置
>block块元素
>inline行元素
>inline-block行内块元素（内联块元素）

>display:inline-block会导致元素之间产生间隔
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121111807819.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121111822248.png)

消除inlne-block导致的元素间隔的方法
1.删除标签之间的空格和换行
问题：导致代码的可读性比较差

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121111940122.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121111958841.png)

2.将父元素的字体设置为0px
问题：通过继承性，会影响自身字体的大小
同时会导致布局混乱（em之类参考父元素字体的值则无法使用）

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121112542530.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121112600490.png)

3.给父级和自身设置字间距或词间距
问题：较小

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114210758.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114223403.png)

4.删除掉闭合标签（结束标签）
不建议使用

5.修改外间距

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114459495.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114503123.png)

6.使用浮动

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114756230.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121114735438.png)

## []()盒模型

盒模型是由margin(外间距)border(边框)padding(内间距)组成

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020012111500024.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

### []()外间距

>margin外间距，设置元素之间的距离
>外间距单属性：margin-top(上)/margin-left(左)/margin-right(右)/margin-bottom(下)
>复合属性：
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121120939933.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>只有一个值时，`margin:1px;`设置上下左右的外间距
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121121157326.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>两个值时，`margin:10px 20px;`第一个为上下的外间距，第二个为左右的外间距
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121121205876.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>三个值时，`margin:1px 2px 3px;`第一个上间距，第二个左右间距，第三个下间距
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121121220866.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>四个值，`margin:1px 2px 3px 4px;`第一个上，第二个右，第三个下，第四个左
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121121226985.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

### []()内间距

padding 用于控制内容与边框的距离
padding-top(上)/padding-bottom(下)/padding-left(左)/padding-right(右)
复合属性：
一个值：上下左右内间距
两个值：上下，左右
三个值：上，左右，下
四个值：上，右，下，左

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121230655857.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121230709664.png)

## []()边框切圆

border-radius 复合属性
一个值：四个角
两个值：左上右下，坐下右上
三个值：左上，右上左下，右下
四个值：左上，右上，右下，左下

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121231635325.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200121231649160.png)

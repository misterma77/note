

###### []()显示和隐藏

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203120937877.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**`目标.hide()` 让目标隐藏**

>第一个按钮效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121001112.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121057188.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

`目标.show()`  让目标显示

>第二个按钮效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121158314.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121245389.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

`目标.toggle()` 判断目标属性，如果是显示，修改为隐藏；如果是隐藏，则修改为显示

>第三个按钮的效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121441469.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121447913.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203121453851.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()淡入和淡出

>`目标.fadeIn()` 淡入
>`目标.fadeOut()` 淡出
>`目标.fadeToggle()` 淡入和淡出
>`目标.fadeTo(参数1，参数2)` 渐变到指定透明度
>参数1：执行事件 参数2：指定透明度

###### []()滑入和滑出

>`目标.slideDown()` 滑入
>`目标.slideUp` 滑出
>`目标.slideToggle()` 滑入和滑出

###### []()自定义动画

`animate({styles},speed,easing,callback)`
`style` 必选。css属性
`speed` 可选。规定动画的速度(ms,slow,fast)	
`easing` 可选。

>规定在动画的不同点中元素的速度 默认为swing
>`linear` 匀速移动
>`swing` 在开头/结尾移动慢，在中间移动快

`callback` 可选。animate 函数执行完之后，要执行的函数。

###### []()停止动画

`stop(参数1，参数2)` 停止所有在指定元素上正在运行的动画
参数1：true，清空队列，可以立即结束动画
参数2：true，完成队列，可以立即执行动画

###### []()each()

用于循环遍历成员/数据，它常用于多元素或任意数组和对象属性的循环访问

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203205309936.png)
>显示效果:
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203205329857.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()$.each()

是一个全局函数，功能与`目标.each()`相同
语法：`$.each(参数1，参数2)`
参数1：需要遍历的目标
参数2：每个目标需要执行的功能

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203211940543.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203211951351.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()判断样式

目标.is()

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203212740364.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果:
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203212753782.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

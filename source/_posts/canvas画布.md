

#### []()canvas的基本使用

canvas是一个标签，必须设置宽高，画布是canvas的属性
在绘制之前，先通过标签获取画布，通过画布调用绘制方法
获取画布：`canvas.getContext("2d")`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205120115803.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205120127148.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()绘制直线的流程

>1.开始绘制(落笔) `beginPath()`
>2.设置起点 `moveTo()`
>3.设置终点 `lineTo()`
>可以将最后一个终点和起点 相连接 `closePath()`
>4.根据设置的点，来连接 `stroke()`
>`save()` 保存当前环境的状态
>`restore()` 返回之前保存的路径状态和属性
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205130534110.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205130547940.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c=,size_16,color_FFFFFF,t_70

###### []()线条样式和阴影

**属性：**

>1.`fillstyle`：设置或返回用于填充绘画的颜色，渐变或模式
>属性值：1.color 指示绘图填充色的css颜色值
>    2.gradient 用于填充绘画的渐变对象
>    3.pattern 用于填充绘图的pattern对象
>2.`strokestyle`：设置或返回用于笔触的颜色，渐变或模式
>属性值：1.color 指示绘图笔触颜色的 CSS 颜色值
>    2.gradient 用于填充绘图的渐变对象（线性 或 放射性）
>    3.pattern 用于创建 pattern 笔触的 pattern 对象
>3. `shadowColor`：设置互殴返回用于阴影的颜色
>属性值：color 用于阴影的 CSS 颜色值
>4.`shadow'Blur`：设置或返回阴影的模糊级数
>属性值：number，阴影的模糊级数
>5.`shadowOffsetX/Y`：设置或返回阴影与形状的水平/垂直距离

**方法：**

>1.`createLinearGradient(x0,y0,x1,y1)`：创建线性渐变
>属性值：1.`x0,y0` 渐变开始点的x，y坐标
>    2.`x1,y1` 渐变开始点的x，y坐标
>2.`createPattern(参数1,参数2)` 在指定的方向上重复指定的元素
>属性值：参数1:`image`		规定要使用的模式的图片、画布或视频元素
>    参数2:`repeat`		默认。该模式在水平和垂直方向重复
>         `repeat-x` 	该模式只在水平方向重复
>         `repeat-y` 	该模式只在垂直方向重复
>         `no-repeat` 	该模式只显示一次（不重复）
>3.`createRadialGradient(x0,y0,r0,x1,y1,r1)`：创建放射状/环形的渐变（用在画布内容上）
>属性值：1.`x0` 	渐变的开始圆的 x 坐标
>    2.`y0` 	渐变的开始圆的 y 坐标
>    3.`r0` 	开始圆的半径
>    4.`x1` 	渐变的结束圆的 x 坐标
>    5.`y1` 	渐变的结束圆的 y 坐标
>    6.`r1` 	结束圆的半径
>4.`addColorStop(参数1，参数2)`:规定渐变对象中的颜色和停止位置
>属性值：参数1.`stop` 	介于 0.0 与 1.0 之间的值，表示渐变中开始与结束之间的位置。
>    参数2.`color` 	在 stop 位置显示的 CSS 颜色值。

###### []()线条样式

**属性：**

>1.`lineCap` 	设置或返回线条的结束端点样式
>属性值：1.`butt` 	默认。向线条的每个末端添加平直的边缘
>    2.`round` 	向线条的每个末端添加圆形线帽
>    3.`square` 	向线条的每个末端添加正方形线帽
>2.`lineJoin` 	设置或返回两条线相交时，所创建的拐角类型
>属性值：1.`bevel` 	创建斜角
>    2.`round` 	创建圆角
>    3.`miter` 	默认。创建尖角
>3.`lineWidth` 	设置或返回当前的线条宽度
>属性值：`number` 	当前线条的宽度，以像素计
>4.`miterLimit` 	设置或返回最大斜接长度
>属性值：`number` 	正数。规定最大斜接长度
>如果斜接长度超过 miterLimit 的值，边角会以 lineJoin 的 “bevel” 类型来显示

###### []()矩形

**方法：**

>1.`rect(x,y,width,height)` 	创建矩形
>参数值：1.`x` 	矩形左上角的 x 坐标
>   2.`y` 	矩形左上角的 y 坐标
>   3.`width` 	矩形的宽度，以像素计
>   4.`height` 	矩形的高度，以像素计
>2.`fillRect(x,y,width,height)` 	绘制"被填充"的矩形
>参数值：1.`x` 	矩形左上角的 x 坐标
>   2.`y` 	矩形左上角的 y 坐标
>   3.`width` 	矩形的宽度，以像素计
>   4.`height` 	矩形的高度，以像素计
>3.`strokeRect(x,y,width,height)` 	绘制矩形（无填充）
>参数值：1.`x` 	矩形左上角的 x 坐标
>   2.`y` 	矩形左上角的 y 坐标
>   3.`width` 	矩形的宽度，以像素计
>   4.`height` 	矩形的高度，以像素计
>4.`clearRect(x,y,width,height)` 	在给定的矩形内清除指定的像素
>参数值：1.`x` 	要清除的矩形左上角的 x 坐标。
>   2.`y` 	要清除的矩形左上角的 y 坐标。
>   3.`width` 	要清除的矩形的宽度，以像素计。
>   4.`height` 	要清除的矩形的高度，以像素计。

###### []()路径

>1.`fill()` 	填充当前绘图（路径）。
>使用`fillstyle`来改变内填充颜色
>如果路径未关闭，那么`fill()` 方法会从路径结束点到开始点之间添加一条线，以关闭该路径（正如 `losePath()` 一样），然后填充该路径
>2.`stroke()` 	绘制已定义的路径。
>`strokestyle`来改变颜色
>3.`beginPath()` 	起始一条路径，或重置当前路径
>4.`moveTo()` 	把路径移动到画布中的指定点，不创建线条
>5.`closePath()` 	创建从当前点回到起始点的路径
>6.`lineTo()` 	添加一个新点，然后在画布中创建从该点到最后指定点的线条
>7.`clip()` 	从原始画布剪切任意形状和尺寸的区域
>8.`quadraticCurveTo(cpx,cpy,x,y)` 	创建二次贝塞尔曲线
>参数值：1.`cpx` 	贝塞尔控制点的 x 坐标
>   2.`cpy` 	贝塞尔控制点的 y 坐标
>   3.`x` 	结束点的 x 坐标
>   4.`y` 	结束点的 y 坐标
>9.`bezierCurveTo(cp1x,cp1y,cp2x,cp2y,x,y)` 	创建三次贝塞尔曲线
>参数值：1.`cp1x` 	第一个贝塞尔控制点的 x 坐标
>   2.`cp1y` 	第一个贝塞尔控制点的 y 坐标
>   3.`cp2x` 	第二个贝塞尔控制点的 x 坐标
>   4.`cp2y` 	第二个贝塞尔控制点的 y 坐标
>   5.`x` 	结束点的 x 坐标
>   6.`y` 	结束点的 y 坐标
>10.`arc(x,y,r,sAngle,eAngle,counterclockwise)` 	创建弧/曲线（用于创建圆形或部分圆）
>参数值：1.`x` 	圆的中心的 x 坐标
>   2.`y` 	圆的中心的 y 坐标
>   3.`r` 	圆的半径
>   4.`sAngle` 	起始角，以弧度计（弧的圆形的三点钟位置是 0 度）
>   5.`eAngle` 	结束角，以弧度计
>   6.`counterclockwise` 	可选。规定应该逆时针还是顺时针绘图。false = 顺时针，true = 逆时针。
>11.`arcTo(x1,y1,x2,y2,r)` 	创建两切线之间的弧/曲线
>参数值：1.`x1` 	两切线交点的横坐标
>   2.`y1` 	两切线交点的纵坐标
>   3.`x2` 	第二条切线上一点的横坐标
>   4.`y2` 	第二条切线上一点的纵坐标
>   5.`r` 	弧的半径

###### []()转换

>1.`scale(width,height)` 	缩放当前绘图至更大或更小
>参数值：1.`width` 缩放当前绘图的宽度（1=100%，0.5=50%，2=200%，依次类推）
>    2.`height` 	缩放当前绘图的高度（1=100%，0.5=50%，2=200%，依次类推）
>2.`rotate()` 	旋转当前绘图
>参数值：以弧度记，`Math.PI/180为1°`
>3.`translate(x,y)` 	重新映射画布上的 (0,0) 位置
>参数值：1.`x` 	添加到水平坐标（x）上的值
>    2.`y` 	添加到垂直坐标（y）上的值
>4.`transform(a,b,c,d,e,f)` 	替换绘图的当前转换矩阵
>参数值：1.`a` 	水平缩放绘图
>    2.`b` 	水平倾斜绘图
>    3.`c` 	垂直倾斜绘图
>    4.`d` 	垂直缩放绘图
>    5.`e` 	水平移动绘图
>    6.`f` 	垂直移动绘图
>5.`setTransform(a,b,c,d,e,f)` 	将当前转换重置为单位矩阵。然后运行 transform()
>参数值：1.`a` 	水平缩放绘图
>    2.`b` 	水平倾斜绘图
>    3.`c` 	垂直倾斜绘图
>    4.`d` 	垂直缩放绘图
>    5.`e` 	水平移动绘图
>    6.`f` 	垂直移动绘图

##### []()文本

**属性：**

>1.`font` 设置或返回画布上文本内容的当前字体属性
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205145203507.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205145207785.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`textAlign` 设置或返回文本内容的当前对齐方式
>属性值：`start`   默认。文本在指定的位置开始。
>    `end`    文本在指定的位置结束。
>    `center`    文本的中心被放置在指定的位置。
>    `left` 	    文本在指定的位置开始。
>    `right` 	  文本在指定的位置结束。
>3.`textBaseline` 设置或返回在绘制文本时使用的当前文本基线
>属性值：1.`alphabetic` 	  默认。文本基线是普通的字母基线。
>    2.`top`       文本基线是 em 方框的顶端。
>    3.`hanging` 	    文本基线是悬挂基线。
>    4.`middle` 	        文本基线是 em 方框的正中。
>    5.`ideographic` 	文本基线是表意基线。
>    6.`bottom` 	        文本基线是 em 方框的底端。

**方法：**

>1.`fillText(text,x,y,maxWidth)`绘制被填充的文本
>属性值：1.`text` 	   规定在画布上输出的文本。
>    2.`x` 	      开始绘制文本的 x 坐标位置（相对于画布）。
>    3.`y` 	      开始绘制文本的 y 坐标位置（相对于画布）。
>    4.`maxWidth` 	 可选。允许的最大文本宽度，以像素计。
>2.`strokeText(text,x,y,maxWidth)` 	在画布上绘制文本（无填充）
>属性值：1.`text` 	   规定在画布上输出的文本。
>    2.`x` 	      开始绘制文本的 x 坐标位置（相对于画布）。
>    3.`y` 	      开始绘制文本的 y 坐标位置（相对于画布）。
>    4.`maxWidth` 	 可选。允许的最大文本宽度，以像素计。

# []()拖拽Drag

拖拽是指鼠标点击源对象后，不松手将其拖拽到目标对象，或半途松手(释放)的过程
**源对象**：指定鼠标点击的一个事物
**目标对象**：指的是我们拖动源对象后，预计要进入的区域

##### []()源对象触发的事件

>1.`ondragstart` 源对象开始被拖动
>2.`ondrag` 被拖动过程中
><mark>drag事件最后一刻，无法读取鼠标坐标，x和y会变成0
>添加if判断，直接结束，不赋值给元素</mark>
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205152309950.png)
>3.`ondragend` 源对象被拖动结束

##### []()源对象进入目标对象触发

>1.`ondragenter` 源对象进入目标对象时触发
>2.`ondragleave` 源对象被拖动着离开目标对象时触发
>3.`ondragover`  源对象悬停在目标对象上方时触发
>4.`ondrop` 源对象在目标对象上松手时触发
><mark>ondrop直接使用时，无法触发，需要在ondragover中阻止默认事件</mark>
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020515291894.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

<mark>draggable 标签自带属性，设置是否可以拖拽，默认为false不可以拖拽</mark>

##### []()数据传递对象

>**event.dataTransfer**
>功能：用于在源对象和目标对象之间传递数据
>方法：`setData(key,value)` 设置数据 value必须是字符串
>   `getData(key)` 获取数据

##### []()JSON方法

>JSON.stringify(对象) 将对象类型转换为字符串
>JSON.parse(字符串) 将字符串类型转换为对象类型

# []()本地储存

本地储存分为`localStorange`(永久存储)和`sessionStorage`(临时存储)
<mark>区别：</mark>

>1.`localStorage` 这里做永久存储，浏览器关闭与否并不影响它
>多数使用在用户自动登录，客户端保存数据方面
>2.`sessionStorage` 做临时存储，浏览器或页面关闭时，数据自动删除，不再存储
>多用于安全性较高的网站

<mark>方法：</mark>

>1.`setItem(key,value)` 保存数据
>2.`getItem(key)` 获取数据
>3.`removeItem(key)/clear()` 删除数据

# []()CSS3选择器

###### []()兄弟选择器

>1.`+` 紧邻选择器 相邻兄弟选择器
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205160914495.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205160955668.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`~` 间接兄弟选择器 所有下面的兄弟
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161054826.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161053950.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()属性选择器

>1.`a[target]` 选择带有target属性的a标签
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161551485.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161600348.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`a[target=_blank]` 选择带有`target=_blank`的所有a标签
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161753178.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205161809968.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`[title~=flower]` 选择title属性包含"flower"的元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205162028259.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020516204725.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.`[lang|=en]` 选择lang属性以"en"开头的元素，均为自定义
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205162241261.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205162255218.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()链接伪类

>1.`:link` 选择所有未被访问过的链接
>2.`:visited` 选择所有已被访问过的链接
>3.`:active` 选择所有活动链接
>4.`:hover` 选择鼠标指针位于其上的链接

###### []()元素状态伪类

>1.`:enabled` 选择每个被启用的元素
>2.`:disabled` 选择每个未被启用的元素
>3.`:checked` 选择每个没选中的元素
>4.`:focus` 选择获得焦点的元素

###### []()结构伪类

单一类型：

>1.`first-of-type` 匹配父元素下第一个子元素
>2.`last-of-type` 匹配父元素下最后一个子元素
>3.`nth-of-type(n) 匹配父元素下第n个子元素 4.`nth-last-of-type(n)`匹配父元素下倒数第n个子元素 5.`only-of-type` 匹配属于其父元素的唯一子元素

多类型：

>1.`first-child` 匹配父元素下第一个子元素
>2.`last-child` 匹配父元素下最后一个子元素
>3.`nth--child(n)` 匹配父元素下第n个子元素
>4.`nth-last-child(n)` 匹配父元素下倒数第几个子元素
>5.`only-child` 匹配属于其父元素的唯一子元素

###### []()伪元素选择器

>1.`:first-letter` 选择冒号前元素的第一个单词
>2.`:first-line` 选择冒号前元素的第一行
>3.`::selection` 匹配元素中被用户选中的部分

###### []()内容生成器

>1.`:before` 在···之前，配合content使用
>2.`:after` 在···之后，配合content使用

>`:lang(en)` 选择带有以"en"开头的lang属性值的每个元素 en为自定义
>`[class^=“xxx”]` 选择class属性值以xxx开头的所有元素
>`[class$="xxx"]` 选择class属性值以xxx结尾的所有元素
>`[class*="xxx"]` 选择class属性值包含"xxx"的所有元素
>`:root` 选择文档的根元素
>`:empty` 选择没有子元素的元素 包括文本节点
>`:target` 选择当前活动的元素
>`:not(n)` 非n元素外的所有元素

#### []()CSS2D效果

1.旋转 单位`deg`度
`rotate()` `rotateX()` `rotateY()` `rotateZ()`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205185416291.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020518542632.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

2.位移：单位 px 像素
`translate(参数1，参数2)` `translateX()` `translateY()` `translateZ()`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205202750416.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205202927906.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

3.缩放：正常比例为1，大于1放大，小于1缩小
`scale(参数1，参数2)` `scaleX()` `scaleY()`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205203325901.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205203335664.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

4.倾斜 单位 deg 度
`skew(参数1，参数2)` `skewX()` `skewY()`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205204028887.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200205204039763.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()设置3D效果

`transform-style:preserve-3d;` 设置给父级

###### []()开启景深效果

`perspective` 属性 属性值单位为px

###### []()指定变形中心

`transform-origin:top/center/bottom/left/right`

#### []()自定义动画

也叫关键帧动画，分为制作动画和绑定动画

###### []()制作

`@keyframes` 声明自定义动画的关键词，后面需要写自定义动画的名称，空格间隔

>代码：可多次使用
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206103411208.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()绑定

`animation:动画名称,动画执行时间,动画执行的速度曲线,动画开始前的延迟,动画执行的次数,是否轮流反向播放`
是一个简写属性，用于设置六个动画属性

>属性：1.`animation-name`:动画名称<mark>必填</mark>
>   2.`animation-duration`:动画执行所需的时间(<mark>必填</mark>)
>   3.`animation-timing-function`:动画执行的速度曲线,<mark>可选</mark>，默认值为ease
>   属性值：1.`linear` 匀速
>       2.`ease` 默认值。低速开始，然后加快，结束前变慢
>       3.`ease-in` 低速开始
>       4.`ease-out` 低速结束
>       5.`ease-in-out` 低速开始低速结束
>       6.`cubic-bezier(n,n,n,n)` 可能值是从0到1的数值
>   4.`animation-delay`:动画开始前的延迟，<mark>可选</mark>默认值为0s
>   5.`animation-iteration-count`:动画执行的次数,<mark>可选</mark> 默认值1 没有单位 `infinite` 无限次
>   6.`animation-direction`:规定是否轮流反向播放(注意：播放次数至少为2)<mark>可选</mark>
>    `alternate` 反向播放 `normal` 默认 正常播放
>   7.`animation-fill-mode`:规定动画在播放之前或之后，其效果是否可见
>   属性值：1.`none` 不改变默认行为
>       2.`forwards` 动画完成后，保持最后一个属性值
>       3.`backwards` 在`animation-delay`所指定的一段时间内，在动画显示之前，应用开
>       始属性值(在第一个关键帧中定义)
>       4.`both` 向前和向后填充模式都被应用
>   8.`animation-play-state` 规定动画执行或暂停
>   属性值：1.`paused` 动画暂停
>       2.running 动画正在播放

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206105833527.png)

#### []()盒模型

###### []()标准盒模型

>`box-sizing:content-box`
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206110301427.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206110310760.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()怪异盒模型(不影响实际占地面积）

>`box-sizing:border-box`
>不会改变元素的占地面积，但是会改变内容的区域大小
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206110518275.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206110527813.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206110535302.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()弹性盒模型

>`display:flex`开启弹性盒模型

**根据主轴上的位置变化，对齐方式 `justify-content`**

>1.`flex-start` 开始位置，默认
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113132258.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113137216.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`flex-end` 结束位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113038809.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113047264.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`center` 中心位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113232580.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113248428.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.`space-around` 两端对齐(元素到边框的距离是元素之间的一半)
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113442805.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113455100.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5.`space-between` 两端对齐(元素到边框之间无距离)
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113340792.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113342509.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**改变主轴的方向 `flex-direction`**

>1.`row` 从左到右，默认
>2.`row-reverse` 从右到左
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113716606.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/202002061137266.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`colume` 从上到下
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113832233.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113841483.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.`colume-reverse` 从下到上
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113914903.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206113933316.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**交叉轴的对齐方式 `align-items`**

>1.`flex-start` 交叉轴的起点对齐
>2.`flex-end` 交叉轴的终点对齐
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114145169.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114200829.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`center` 交叉轴的中点对齐
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114041104.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114050208.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.`baseline` 项目的第一行文字的基线对齐
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114418704.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114432340.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5.`stretch` 如果项目未设置高度或为auto,将占满整个容器的高度

**换行 `flex-wrap`**

>开启换行，弹性盒模型下，默认为不换行
>1.`nowrap` 不换行
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020611465190.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114659175.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`wrap` 换行
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114755686.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114807436.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`wrap-reverse` 倒序换行
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206114959451.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206115013959.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

**`align-content`**

>功能与`align-items`类似，该属性对单行元素无效，可以去掉多余的行间距

**元素缩放**

>`flex-shrink` flex的收缩默认是按等比

**元素排序**

>`order:number;` 需要将当前层级的每一个元素都排序

**盒子阴影 `box-shadow`**

>1.水平位置偏移(必填) 单位px
>2.垂直位置偏移(必填) 单位px
>3.模糊度(可选) 单位px
>4.阴影面积(可选)单位px
>5.阴影颜色
>6.内外阴影，默认为外阴影，`inset` 外阴影
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206115424942.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206115433253.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

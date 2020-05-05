

# []()JQuery

jQuery 是一个 JavaScript 库。

jQuery 极大地简化了 JavaScript 编程。

jQuery 很容易学习

###### []()使用

必须先引入JQuery库

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202113251166.png)

###### []()jQuery的变量声明

`var $one=10;`
`$`声明该变量是jq变量，`$`是jquery的简写

###### []()DOM变量和jq变量之间的转换

1.DOM变量转换为jq变量

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202113359539.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202113419778.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

2.jq变量转换为DOM变量

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202113703396.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202113713496.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

jq中 顶级对象  是 `$` 或者`jQuery关键字`
jQuery中的`$`和`jQuery关键字`本身同为一个对象

###### []()入口函数

JS中的入口函数：`window.onload`
JQ中的入口函数：`$(document).ready(function(){}`可简写为`$(function(){})`
区别：

>文档加载步骤：
>1.解析HTML结构
>2.加载外部的样式表和脚本
>3.解析并执行脚本
>4.解析HTML—DOM模型(执行ready方法)
>5.加载图片等外部资源
>6.页面加载完毕(执行onload方法)

###### []()jq选择器

>1.`$("#XX")`        id选择器
>2.`$(".XX")`        class选择器
>3.`$("标签名")`      标签选择器
>4.`$("*")`        通用选择器
>5.`$("div>span")`    层级选择器
>6.`$("div span")`    后代选择器
>7.`$("div>ul>li")`  连续后代选择器
>8.`$("div,p")`     群组选择器
>9.`$("div.box")`      交叉选择器
>10.`$(".box+p")`      紧邻且在下方
>11.`$(".box~p")`      下方所有的目标元素
>
>###### []()过滤选择器
>
>1.`:first`   匹配到第一个符合条件的元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141530112.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141549261.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`:last`     匹配到最后一个符合条件的元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141707126.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141709432.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`:not()`   除了括号中指定的条件，获取`:`前指定的所有元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020214273537.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142746930.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.`:even`     索引为偶数的
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141830329.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020214184094.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141846925.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5`:odd`   索引为奇数的
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020214195126.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202141958698.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>6`:eq(指定索引值)`
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142116249.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142118125.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>7.`:gt(大于索引值)`
>8.`:lt(小于索引值)`
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142412190.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142428246.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202142446234.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>
>###### []()方法
>
>1.`find()`    查找指定元素的所有指定的后代元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202143817136.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202143837745.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`children()` 查找指定元素的所有子元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144328440.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144340169.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`next()`    获取下一个紧邻的元素
>4.`nextAll()`   获取后面所有的元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020214450880.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144512243.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5.`prev()`    获取上一个紧邻的元素
>6.`prevAll()`   获取前面所有的元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144649526.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144700583.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>7.`val()`      获取input框的value值
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144846693.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202144859877.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>8.`siblings()`  获取所有的兄弟元素
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145111880.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145128728.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

######jq设置css样式
css(参数1，参数2)
参数1：属性名 参数2：属性值
只有一个参数时，返回指定属性名的值

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145814851.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145824900.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>两个参数时，会修改指定属性名的值
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145418293.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145426949.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()链式编程

jq的优点之一
冒号赋值，逗号结尾
最后一个属性结尾时，不需要任何符号

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200202145559660.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020214561027.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()创建节点

>js中：`document.creatElement()`
>jq中:`var $li=$("<li></li>")`

###### []()添加节点

>1.`内容.appentTo(目标)`
>将内容添加到目标中的最后一位
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203111834677.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203111843440.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)2.`目标.prepend(内容)` `内容.prependTO(目标)`
>将内容添加到目标的第一位
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020311245019.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203112458598.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`目标.after(内容)`
>在指定元素后面插入元素，如果内容是页面已有元素，则将内容移动到指定位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203113417482.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203113426932.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)4.`内容.insertAfter(目标)`
>将内容添加到目标之后
>如果内容是页面已有元素，则该元素会被移动到指定位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203113726717.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203113734726.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)5.`目标.before(内容)`
>将内容添加到目标之前
>如果内容是页面已有元素，则该元素会被移动到指定位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114034268.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114042762.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)6.`内容.insertBefore(目标)`
>将内容添加到目标之前
>如果内容是页面已有元素，则该元素会被移动到指定位置
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114331636.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114335933.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()删除节点

>1.`指定目标.remove()` 删除指定目标
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203115128678.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203115138232.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`目标.empty()` 清空目标子节点，但不对目标造成影响
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114945348.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203114946189.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`目标.clone()` 复制 会返回指定目标的复制体，需要接收或直接使用
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203115640916.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203115648419.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

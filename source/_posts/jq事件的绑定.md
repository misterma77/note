

#### []()事件绑定

1.on/off
2.bind/unbind
3.live/delegete
在JQuery1.7之后推出了`on/off`，废弃了`live/delegete`方法
`on/off`整合了`bind/unbind`方法
`.on(参数1，参数2，参数3，参数4)`

>参数1：必填。事件类型，，可同时绑定多个事件，仅限于功能相同时,事件之间空格间隔
>   功能不同时，采用链式编程
>参数2：可选。具体执行功能的子元素
>参数3：可选。传递到函数内部的数据（类似实参），通过event.data来获取
>参数4：具体功能
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204115810173.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：**依次点击第二、第三、第一个div**
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204115824620.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>代码：通过对象的方法添加多个事件
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204120407859.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204120410689.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)#### 事件的命名空间
>有时，我们想对事件进行移除。但对于同名同元素绑定的事件移除往往比较麻烦，这个时候，可以使用事件的命名空间解决
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204121752276.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204121750775.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()接除事件绑定

`.off(参数1，参数2，参数3)`

>参数1：必须要符合要解除的事件类型，事件命名
>参数2：可选。指定哪些后代元素可以触发绑定的事件
>参数3：可选。规定当事件发生时运行的函数
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204121915182.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204121923299.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()区别

通过on绑定和直接通过事件名绑定的区别

>`事件名`：在页面加载后，获取所有符合条件的元素，然后绑定事件，如果通过其它操作再生成一个新的符合条件的元素，则新元素不会绑定这个事件
>`.on()`：只起到了监听的效果，可以实现动态html元素绑定

###### []()读取和使用鼠标状态

`event.which`
返回1为鼠标左键，返回2为鼠标中键，返回3为鼠标右键

###### []()return

`return true`返回正常的处理结果
`return false` 返回错误的处理结果;终止处理;阻止提交表单;阻止执行默认的行为
`return` 把控制权返回给页面

#### []()事件委托

事件委托是利用事件冒泡来实现，只指定一个事件处理程序 来管理某一类型的所有事件

###### []()为什么要用事件委托

1.在js中添加到页面的事件处理程序的个数直接关系到页面的整体加载速度.
因为每个事件处理程序都是一个对象，对象会占用内存。对象越多需要加载的内存就越多
2.有很多个数据的表格以及很长的列表逐个添加事件，对于开发人员而言，就是噩梦。
事件委托能极大的提高页面的加载速度 ，减少开发人员的工作量

###### []()事件委托的使用场景/作用

1.操作子元素时，不用一 一遍历，可以根据事件触发的对象来进行相应的操作
2.将事件委托给父级后，动态创建(删除)的子元素不用重新绑定(解绑)事件，实现了时间和元素的同步更新

###### []()适用性

1.`focus()` `blur()`方法本身没有事件冒泡，无法使用事件委托
2.`mouseover` `mouseout`这两个事件的触发频率较高，经常需要计算，所以偶尔会出现卡顿，偏差
3.比较适用：`click` `mousedown` `mouseup` `keydown` `keyup` `keypress`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204135112261.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204135113382.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()对象的创建和使用

###### []()创建

`var obj={ };` 创建一个空对象

###### []()赋值

>创建时赋值
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204135510392.png)

>创建后赋值
>`obj.hobby="玩"`
>如果该对象有这个属性，那么找到这个属性，并赋值；如果没有，

###### []()访问

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204140744788.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020414081355.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()插件封装

##### []()释放/更改`$`的作用

`var $s=jQuery.noConflict()`

##### []()给jq添加方法的方式

###### []()对象级别的添加

>1.`$.fn.extend({`
>  `函数名:function(){`
>
>  `},`
>  `函数名:function(){`
>
>  `},`
>`});`
>2.`$.fn.函数名=function(){}`

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020414224355.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204142309393.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()类级别的添加

>1.`$.extend({`
>  `函数名:function(){`
>
>  `},`
>  `函数名:function(){`
>
>  `}`
>`})`
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204143952290.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204144007881.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>2.`$.函数名=function(){`
>`}`
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204144105123.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200204144116219.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>**直接通过`$`来调用，不再受到调用者的约束，如果`$`的所有权被修改了，使用修改后的，或者使用jQuery**

###### []()使用jquery的好处/为什么使用jquery

>1.因为它是轻量级别的框架，大小不超过30kb
>2.它有强大的选择器，出色的DOM操作封装
>3.有可靠的事件处理机制
>4.完善的ajax
>5.出色的浏览器兼容性
>6.支持链式操作，隐式迭代
>7.行为层(功能)和结构层(页面元素)的分离，还支持丰富的插件

###### []()JQuery库中的$()是什么？

>`$()`是JQuery()的别称；`$()`函数用于将任何对象包裹成jquery对象，接着你就可以调用定义再jQuery对象上的多个不同方法
>将一个选择器字符串传入`$()`函数,它会返回一个包含所有匹配的DOM元素数组的jQuery对象

###### []()`$(document).ready()`是个什么函数？为什么要用它？

>`ready()` 函数用于在文档进入ready状态时执行代码，当HTML被完全解析DOM树构建完成时，jQuery允许你执行代码
>它适用于所有浏览器，解决了跨浏览器的难题

###### []()`window.onload`和`$(document).ready()`的不同

>1.前者会等DOM创建和包括图片、视频、音频在内所有外部资源都加载完成，如果加载外部资源花费大量时间，用户就会感受到定义在`window.onload`事件上的代码执行时有明显延迟
>后者只需等待DOM树的创建，执行更快
>2.前者只能在单一函数里使用
>后者可以在网页里多次使用，浏览器会按他们在HTML中出现的顺序执行它们

###### []()`$(this)`和`this`关键字在jQuery中有何不同？

>`$(this)`返回一个jQuery对象，可以对它调用多个jQuery方法
>`this`代表当前元素，它是JavaScript关键词中的一个，表示上下文中的当前DOM元素，不能对它调用jQuery方法

###### []()jquery中`detach()`和`remove()`方法的区别

>都用来移除一个DOM元素
>`detach()`会保持对过去被解除元素的跟踪，因此它可以被取消解除
>`remove()`则会保持对过去被移除对象的引用

###### []()`attr()`和`prop()`的区别

>相同点：都是获取或设置元素的属性值
>不同点：1.`prop()`是处理元素自带的属性,`attr()`处理的是自定义的DOM的属性
>2.操作固有属性时，`prop()`会返回正确的值，`attr()`则会返回`undefined`

###### []()`document.getElementById("#box")`相较于`$("#box")`更高效，因为它直接调用了JavaScript引擎

###### []()在一个jQuery事件处理程序里返回false，通常用于阻止事件向上冒泡

###### []()jQuery方法链是对一个方法返回的结果调用另一个方法，使得代码简洁明了，同时由于只对DOM进行了一轮查找，性能方面更加出色

###### []()jQuery设置onclick属性

获取：`$().attr("onclick")`
删除：`$().removeattr("onclick")`
设置：`$().attr("onclick","test()")`



### []()什么是JavaScript？

>  javascript是一种具有**面向对象**能力的**解释型**语言
>  它是基于**对象**和**事件驱动**并具有**相对安全性**的**客户端脚本语言**，因为他不需要在一个语言环境下运行，只需要有一个浏览器即可
>  它的主要目的就是验证发往服务器的数据，增加web互动，加强用户体验

>###### []()面向对象
>
>   是编程思维的一种，我们初期接触的是面向过程
>
>###### []()解释型
>
>  直接读代码运行，而不是编译型的，比如java，需要把源代码编译成一个.class文件，然后执行这个class文件
>
>###### []()对象
>
>  在这里指的面向对象 比如：window对象(BOM对象) document对象(DOM对象) 内置对象
>
>###### []()事件驱动
>
>  大部分情况下是基于浏览器的，点击页面、点击按钮才会触发JavaScript程序的执行
>
>###### []()相对安全性
>
>  它没有阻止文件，删除、修改文件夹此类恶意的操作
>
>###### []()客户端
>
>  不是在服务器(远程端)上执行的，而是当你打开一个网站，它的网页存放到你的本地的临时空间的时候，才会执行
>
>###### []()脚本语言
>
>  不需要像java、.net一样，需要一个环境(SDK、JDK)，他只是一门脚本语言，只是寄存在浏览器上就可以运行

### []()JavaScript的特点

>1.松散型：它的变量不具有一个明确的类型(比如创建一个变量a 并不知道他是什么类型，只有赋值之后才知道)
>2.对象属性：javascript中的对象把属性名映射未任意属性值
>3.继承机制：javascript中的继承是基于原型的

### []()JavaScript的历史

>  1992年，Netscape(网景)公司开发了一种叫做c–的嵌入式语言4，后来觉得名字比较晦气，于是乎，改名为scriptEase。这种可以嵌入网页中的理念成为了因特网的一块重要的基石。
>  后来，布兰登未解决类似于向服务器提交数据之前验证的问题，在网景浏览器2.0和sun公司联合开发了一个称之为liveScript的脚本语言，为了营销便利，改名为JavaScript。
>  当时，它的主要目的是处理以前由服务器端语言负责的一些输入验证操作。
>如今，JavaScript的用途早已不再局限于简单的数据验证，而是具备了与浏览器窗口及其内容等几乎所有方面交互的能力。
>  今天的JavaScript已经成为一门功能全面的编程语言，能够处理复杂的计算和交互。

### []()JavaScript的核心

>1.核心——ECMAScript5.0
>ECMAScript只是规范了JavaScript的语法，它与web浏览器没有依赖关系，web浏览器只是他的宿主环境之一

>2.文档对象模型——DOM
>文档对象模型就是HTML中的树。

>3.浏览器对象模型——BOM
>开发人员使用BOM可以控制浏览器显示页面以外的部分，BOM至今没有相关标准，所以每个浏览器对它支持的不一样。

### []()JavaScript能做什么？

>1.嵌入动态文本于HTML页面。
>2.对浏览器事件做出响应。
>3.读写HTML元素。
>4.在数据被提交到服务器之前验证数据。
>5.检测访客的浏览器信息。
>6.控制cookies，包括创建和修改等。
>7.基于Node.js技术进行服务器端编程。

### []()引入外部js文件

`<script src="文件地址"></script>`

### []()js内联样式

`<script type="text/javascript"></script>`

### []()基础数据类型(内置对象)

>1.Number——数字类型(不区别小数、整数)
>2.String——字符串类型(包括字母、符号、汉字)
>     所有字符串都需要用引号包裹起来，单双不限
>3.Bool——布尔类型，分为true(正确)和false(错误)
>4.Null——空类型
>5.undefined——未定义类型
>6.object——对象类型

### []()声明并使用变量和常量

常量

>不可能改变的数值

变量

>可以改变的数值

变量的声明

>声明一个变量，需要使用关键字`var`
>分为两步：1.声明变量 `var a` 向系统申请一块内存空间，名为`a`
>     2.定义变量 `a = 1` 向已经存在的变量赋值`1`
>语法：var XX = 储存的内容;
>     在编程中,单等号`=`,是赋值号
>     `var a = 1;` 将赋值号左边的数据储存到左边的变量中

### []()测试方法

>`console.log()`输出到控制台
>控制台不影响页面的运行
>这是编程中最常见的测试方式
>控制台打开方式：
>火狐:右击页面，查看元素
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020012318530281.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`alert()`
>会暂时阻断程序运行，知道用户点击弹出框中的确定
>将内容输出到语法自带的提示框
>这个提示框，通常用于测试，在页面中弹出。不用于实际开发
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200123185822320.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200123185921152.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`typeof`数据类型测试
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200123190737777.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/202001231907521.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

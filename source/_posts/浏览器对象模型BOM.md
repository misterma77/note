

BOM主要用于管理窗口与窗口之间的通讯，其核心对象为window
所有浏览器都支持window对象，是BOM顶层（核心）对象
所有javascript全局对象，函数以及变量均成为window对象的成员
全局变量是window对象的属性
全局函数是 window 对象的方法
由于window对象是顶层对象，因此调用他的子对象时可以不显示的指明window对象，例如下面这俩行代码是一样的：
`document.write(“今天天气真不错”);`
`window. document.write(“今天天气真不错”);`

##### []()window的子对象

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203183002277.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()window函数

**窗体控制函数：**

>moveBy( )  window.moveBy(60,50);相对
>moveTo( )  window.moveTo(60,50);绝对
>resizeBy( )  window.resizeBy(60,50);相对
>resizeTo( )  window.resizeTo(60,50);绝对

**窗体滚动轴控制函数：**

>scrollTo( )  绝对
>scrollBy( )  相对

**新建窗体函数：**

>close( )
>Open( )
>**语法**：`window.open(url,name,feature,replace);`
>`url` – 要载入窗体的URL
>`name` – 新建窗体的名称(也可以是HTML target属性的取值，目标)
>`features` – 代表窗体特性的字符串，字符串中每个特性使用逗号分隔
>`replace` – 一个布尔值，说明新载入的页面是否替换当前载入的页面，此参数通常不用指定
>
>###### []()feature参数
>
>1.height(number):设置窗体的高度，不能小于100
>2.left(number):说明创建窗体的左坐标，不能为负值
>3.location(Boolean):窗体是否显示地址栏，默认为no
>4.resizable(Boolean):窗体是否允许通过拖动边线调整大小，默认为no
>5.scrollable(Boolean):窗体内部超出窗口可视范围时是否允许拖动,默认为no
>6.toolbar(Boolean):窗体是否显示工具栏，默认值no
>7.top(number):创建窗体的上坐标
>8.status(Boolean):窗体是否显示状态栏，默认为no
>9.width(number):创建窗体的宽度，不能小于100
>**特性字符串的每个特性使用逗号分隔，每个特性之间不允许有空格**

###### []()系统对话框

>1.`alert()`
>用于显示带有一条指定消息和一个确定按钮的警告框
>2.`confirm()`
>用于显示一个带有指定消息和确定及取消按钮的对话框
>如果用户点击确定按钮，则 confirm() 返回 true。如果点击取消按钮，则 confirm() 返回 false。
>3.`prompt()`
>用于显示可提示用户进行输入的对话框
>语法：`prompt(text,defaultText)`
>`text`	可选。要在对话框中显示的纯文本。
>`defaultText`     可选。默认的输入文本
>如果用户单击提示框的取消按钮，则返回 null
>如果用户单击确认按钮，则返回输入文本框当前显示的文本

###### []()Location对象

>Location 对象包含有关当前 URL(统一资源定位符) 的信息
>Location 对象是 Window 对象的一个部分，可通过 window.location 属性来访问
>`location.hostname`   返回当前 URL 的主机名。
>`location.pathname`  返回当前 URL 的路径部分。
>`location.protocol`   返回当前 URL 的协议。
>`location.href`      返回完整的 URL。
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200203185517657.png)

###### []()Navigator对象

>Navigator 对象包含有关浏览器的信息
>`appName`  返回浏览器的名称
>`appCodeName` 返回浏览器的代码名称的字符串
>`cookieEnabled` 指明浏览器中是否启用 cookie 的布尔值。
>`platform`  返回运行浏览器的操作系统平台。
>`appVersion` 返回浏览器的平台和版本信息。
>`userAgent` 用户代理头的字符串表示
>注意：navigator中最重要的是userAgent属性，返回浏览器版本等信息的字符串
>cookieEnabled可以判断用户浏览器是否开启了cookie

###### []()Screen对象

>Screen 对象包含有关客户端显示屏幕的信息。
>`height`   返回显示屏幕的高度。
>`width`   返回显示器屏幕的宽度。
>`availHeight`  显示屏幕的可用高度 (除 Windows 任务栏之外)。
>`availWidth`  显示屏幕的可用宽度 (除 Windows 任务栏之外)。

###### []()History对象

>History 对象包含用户(在浏览器窗口中)访问过的 URL。
>`back()`  加载历史列表中的前一个 URL（如果存在）。
>`forward()`   加载历史列表中的下一个 URL。

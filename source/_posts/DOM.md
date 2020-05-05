

## []()什么是DOM？

DOM 是 W3C（万维网联盟）的标准。

DOM 定义了访问 HTML 和 XML 文档的标准：

>“W3C 文档对象模型 （DOM） 是中立于平台和语言的接口，它允许程序和脚本动态地访问和更新文档的内容、结构和样式。”

W3C DOM 标准被分为 3 个不同的部分：

>核心 DOM - 针对任何结构化文档的标准模型
>XML DOM - 针对 XML 文档的标准模型
>HTML DOM - 针对 HTML 文档的标准模型
>什么是 HTML DOM？

HTML DOM 是：

>HTML 的标准对象模型
>HTML 的标准编程接口
>W3C 标准

HTML DOM 定义了所有 HTML 元素的对象和属性，以及访问它们的方法。

换言之，HTML DOM 是关于如何获取、修改、添加或删除 HTML 元素的标准。

## []()DOM基础方法

###### []()父节点的获取方法

>1.`XX.parentNode` 获取该节点的父节点
>2.`XX.parentElement` 获取该节点的父元素节点
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130212555301.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130212603261.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()子节点的获取方法

>**1.`XX.childNodes` 获取该节点的所有子节点**
>代码：该方法会将元素之间的空格也算作子节点
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020013022072617.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130220734771.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.**`XX.childElementCount` 获取并返回该节点的子元素节点的数量**
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221017431.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020013022102622.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.**`XX.children` 获取该节点的所有子元素节点**
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221255970.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221258281.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>4.**`XX.firstElementChild` 获取第一个子元素节点**
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221458513.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221518935.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5.**`XX.firstChild` 获取第一个子节点**
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221619479.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020013022163470.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>6.**`XX.lastChild` 获取最后一个子节点**
>7.**`XX.lastElementChild` 获取最后一个子元素节点**

###### []()兄弟节点的获取方式

>1.`XX.nextElementSibling` 获取该节点的下一个兄弟元素节点
>2.`XX.nextSibling` 获取该节点的下一个兄弟节点
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221834714.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130221846187.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`XX.previousElementSibling` 获取该节点的上一个兄弟元素节点
>4.`XX.previousSibling` 获取该节点的上一个兄弟节点

###### []()创建元素和添加元素

创建完成的元素，不在Dom树中，需要主动添加
`document.crearElement( )` 创建元素
1.`目标.appendChild(内容)` 添加到目标里的最后一位
2.`父节点.insertBefore(新节点，已有节点)` 添加到已有节点之前

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020013022214275.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130222144291.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()删除元素

1.指定目标的父元素.removeChild(指定目标)
2.指定目标.remove()

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130222405705.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130222415288.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()替换元素

替换目标的父元素.replaceChild(新的元素,被替换的元素)

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130222655757.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130222705385.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

###### []()克隆元素

`需要克隆的目标.cloneNode()` 克隆节点 该方法会将克隆体返回

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130223005125.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130223013746.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>XX.nodeName 返回节点名称
>XX.nodeValue 返回节点属性
>XX.nodeType 返回节点类型
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130223251379.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200130223302160.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

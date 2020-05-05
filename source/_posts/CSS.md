

## []()CSS

(Cascading Style Sheets) 用于渲染HTML元素标签的样式.
引入方式：

>1.**行间样式**：优先级最高
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117184134363.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117184152908.png)

>2.**内联样式**：优先级第二
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117184543648.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117184558940.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>3.**外部样式**：优先级最低：
>`<link>`：引入外部资源，包括css，网页小图标
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117185318738.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117185341785.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200117185348962.png)

>`<link>`标签，单标签，只能存在与`<head>`标签，主要用于引入外部资源

>属性：[菜鸟教程-`<link>`标签](https://www.runoob.com/tags/tag-link.html)
>1.href：定义被链接文档的位置

>2.rel：定义当前文档与被链接文档之间的关系
>属性值：[rel属性值](https://www.runoob.com/tags/att-link-rel.html)
>icon：网页小图标
>stylesheet：默认。要导入的样式表的 URL

>3.target：定义在何处加载被链接文档

>4.type：规定被链接文档的 MIME（媒体类型） 类型

### []()!important

优先级最高，但是仅作用于一行

>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118145757331.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118145916497.png)
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118150007911.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/202001181501039.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()css常用属性

>`width：100px;`——宽。单位为px
>`height：100px;`——高。单位为px
>`border：1px solid red;`——边框。符合属性
>共有三个属性，边框宽，边框类型(solid(实线),dashed(虚线),dotted(点线))，边框颜色
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118161143693.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118161201645.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`background`:背景。复合属性
>`background-color：red;` ——背景色
>`background-image:url(路径);`——背景图
>`background-size：100% 100%;`——图片宽与高
>`background-repeat：repeat-x(水平铺满) / repeat-y(垂直铺满) / no-repeat(不铺满);`
>——图片平铺。默认为全铺满
>`background-position：水平位置 垂直位置;`——背景图的位置
>形式：1.垂直(top，center，bottom);水平(left,center,right) 2.px 3. %(大小%参考标签自身大小，移动%参考图片自身大小)
>
>`background-attachment：scroll(图随页面一同滚动) / fiexd(图片固定不动)；`

>`font-size：20px/2em;`——字体大小。单位px(像素)/em(默认字体大小的几倍)
>`color：red;`——字体颜色。
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118161610346.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118161634297.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`border-radius：50%;`——边框切圆。可用px和%
>`line-height:10px;`——行高，用来垂直居中，单位px
>`text-align:left/center/right;`——水平对齐方式
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118162019942.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118162031375.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`vertical-align(垂直对齐方式):top/center/bottom;`
>——适用于表格单元格中对象及图片，对块级元素不起作用

>`font-family:楷体;`——字体，如果有多个字体，需要用","隔开
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118154541501.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118154558308.png)

>`font-style(文字倾斜):`
>`normal(正常)/oblique(偏斜体)/italic(斜体);`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118162616318.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118162627441.png)

>`font-weight(文字加粗):`
>`normal(正常)/bold(比正常粗)/bolder(比bold粗)/lighter(比正常细)`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/2020011816283526.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118162844681.png)

>`text-transform（英文字母大小写）:`
>`capitalize(首字母大写)/uppercase(全部大写)/lowercase(全部小写);`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118163119178.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118163129425.png)

>`text-decoration(文字装饰):`
>`none(正常显示,可用来去除超链接下划线)underline(下划线)line-throungh(删除线)overline(加顶线)`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118191026285.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020011819103879.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`text-indent(段落首行缩进):10px/10em(首行缩进几个字的距离);`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118191351193.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118191409416.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`word-spacing(单词/词语间距):10px;`
>`letter-spacing(字母/文字间距):10px;`
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118192215185.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200118192229300.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

>`text-align-last(属性规定如何对齐文本的最后一行) : auto(默认值。最后一行被调整，并向左对齐) / left / center / right / start / end / justify(两端对齐);`
>代码测试：[代码测试](https://www.runoob.com/try/playit.php?fplaycss_text-align-last&prevalauto)



CSS选择器使用基本流程：
1.制作所需要的选择器，并在其中写入样式
2.将选择器绑定到指定的html标签上

### []()通用选择器

>书写格式：*{ }
>其优先级是选择器中最低的，它可以修改整个页面，所有标签样式，包括body，html
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119190841858.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119190857338.png)

### []()标签选择器

>用标签名来定义，将当前页面所有与名字相同的标签都绑定上样式
>优先级低于class选择器
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119191823572.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119191908555.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

### []()class选择器

>class选择器用" . "来标识自身
>自定义名称（可以用数字，字母，下划线，但是不能以数字开头）
>可以给多个标签使用，可以给指定的标签绑定，优先级高于标签选择器
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119192126466.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119192133529.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

### []()id选择器

>id选择器用" # "来标识自身，命名规则与class选择器相同
>优先级高于class选择器
>不具有重用性，具有唯一性，如果多个标签使用，会造成不可预知的错误
>禁止重复使用同一个id

### []()群组选择器

>只能用于大批量的样式，如果需要给个别的标签写样式，请使用class或id选择器
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119192756338.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119192809871.png)

### []()子代选择器

>语法：父级>子级{  样式  }
>对指定父级下指定的子级进行修改
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119193435222.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119193446952.png)

### []()后代选择器

>语法:父级 空格 子级 { }  `父级 子级{ }`
>对指定父级下的所有元素进行操作
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119194355503.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200119194357771.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

### []()交叉选择器

需要同时满足两个条件

>div.box选择的是标签是div，class名为box的元素
>或者说是class名为box的div标签
>交叉选择器中没有空格
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120112819654.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120112844552.png)

## []()鼠标伪类hover

效果：在鼠标移入该元素时，触发指定效果，移出时回到初始样式
语法：`XXX:hover{ }` 冒号前是触发者，冒号之后是显示者
使用hover时，子代、后代选择器写在hover之后`XXX:hover>XX{ }`
代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120113627229.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
显示效果：鼠标移入前
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120113653573.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
鼠标移入后
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200120113708748.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

## []()transition过渡

transition是复合属性
transition：值1 值2；
值1：需要修改的样式
值2：改变所用的时间，单位为s

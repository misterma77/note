

#### []()`let`

`let` 写法与`var`一致，同用于声明变量

###### []()区别

>###### []()**var**
>
>1.可以重复声明
>2.作用域：全局作用域，函数作用域(局部作用域)
>3.可以预解析(变量提升）

>###### []()**let**
>
>1.不可以重复声明 会报错
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206145055849.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206145104675.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.作用域：全局作用域，块级作用域({}花括号包裹的区域)
>3.不可以预解析(变量提升)严格遵守先声明，后使用
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206144942511.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206144942637.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()const

用于声明常量
1.let 声明的变量能修改，const声明的变量不可以修改

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206145612496.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206145612920.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

2. 声明的时候，必须赋值
3. 其他情况，可以let一致(不重复，块级作用域，不预解析)

#### []()解构赋值

>解构：解开目标的整体结构
>赋值：将目标中的数据赋值到我们定义的变量中

>1.对象的结构赋值
>{}中，名字必须和obj保持一致
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150237665.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150240771.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.数组的解构赋值
>保持顺序一致
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150457888.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150507609.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.字符串的解构赋值
>与数组相同，变量名的储存顺序与字符串储存顺序一致
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150741338.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206150759733.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()展开运算符

`...`
在需要展开的目标前加`...`,即可将该目标的值取出
不影响原有数据，对原有数据进行复制

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151203616.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151212789.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()剩余参数

解构赋值+展开运算符

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151450559.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151509517.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()Set对象

本质上是一个函数
用来构建某一个类型对象，叫做构造函数
Set()可以接受指定目标来作为参数(和直接使用的区别： 达成去重的目的)

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151904404.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206151909209.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

size属性与length属性一样

>方法：1.`clear()` 清除所有数据 无参无返回值
>   2.`delete()` 删除指定数据 返回true或false,没有这个值才会返回false
>   3.`has()` 查找是否有该元素 返回true或false
>   4.`add(添加的内容)` 添加数据  会返回添加之后的整体内容
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020615303783.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206153040782.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()Map对象

`size`属性

>方法：1.`clear()` 清除所有数据
>   2.`delete(key)` 删除指定数据，返回true或false
>   3.`get(key)` 获取key值相应的value值
>   4.`has(key)` 测试元素是否包含指定key值
>   5.`set(key,value)` 添加一对新数据到元素中，无返回值

###### []()object与map的比较

>**相同点**
>都允许你按键存取一个值、删除键、检测一个键是否绑定了值
>**不同点**
>Object的键只能是字符串或者 Symbols
>Map 的键可以是任意值，包括函数、对象、基本类型
>Map 中的键值是有序的，而添加到对象中的键则不是
>因此，当对它进行遍历时，Map 对象是按插入的顺序返回键值
>可以通过 size 属性直接获取一个 Map 的键值对个数
>Object的键值对个数只能手动计算
>Object有自己的原型，原型链上的键名可能和自己在对象上的设置的键名产生冲突
>Map 在涉及频繁增删键值对的场景下会有些性能优势

#### []()箭头函数

`(形参)=>返回值`
没有参数或多个参数时，都需要带有()
只有一个参数的时候，可以省略()
箭头函数在定义的时候，需要绑定一个变量或者自调用

###### []()箭头函数的不定参

>在ES5中，当我们不确定函数参数的时候，可以使用arguments对象来调用参数
>在ES6中，没有arguments对象来帮助我们调用参数
>**rest(剩余参数)**
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206160331860.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020616035131.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()this指向问题

>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206161005913.png)
>在箭头函数中，没有this，this会指向定义函数时所在作用域

#### []()默认参数

>在括号中直接赋值，即为默认参数
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020020616152486.png)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206161532308.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()数组新增的方法

>1.`Array.from(参数1，参数2，参数3)` 将类数组转换为数组
>类数组：有下标，有length，但是无法使用数组的方法
>参数1：需要转化的类数组
>参数2：处理的方式(可选)
>参数3：函数执行时的this指向(可选)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207130259156.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>2.`Array.isArray()` 检测数据是否是个数组
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207125814595.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207125806778.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>3.`Array.of()` 将参数组成一个新数组，并返回
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207125452450.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207125500488.png)
>**<mark>注：以上三个方法，都是构造函数的方法，格式为`Array.`</mark>**
>4.`flat()` 将指定层数数据处理成一层(扁平化数组）
>参数：需要处理掉的层数，默认为1
>在未知层数的情况下，infinity 无限
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207130008383.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果:
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207130018613.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>5.`flatMap()` 处理扁平化数组
>因为它只能处理一层数组，所以使用`flat()`处理为1层后再使用`flatMap()`方法
>6.`filter()` 该方法返回一个新数组，用来储存通过函数测试的元素
>7.`find()` 返回第一个满足条件的值
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207140412256.png)
>8.`findIndex()` 返回第一个满足条件的值的索引(下标)
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207140508997.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>9.`fill(参数1，参数2，参数3)`  向指定数组填充指定的数据，覆盖原数据
>参数1：用来填充数组元素的值
>参数2：起始索引，默认为0
>参数3：终止索引，默认为this.index
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207140534919.png)
>10.includes() 判断是否包含一个指定的值
>参数1：需要查找的值
>参数2：指定位置后，开始查找(包含该位置)
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200207140610330.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

#### []()字符串新增的方法

>1.`startsWith()` 判断是否以指定字符串开头的
>参数1：指定字符串
>参数2：指定位置开始(包括该字符串)
>2.`endsWith()` 判断是否以指定字符串结尾的
>参数1：指定字符串
>参数2：结尾字符串下标的最后一位
>3.`repeat()` 将字符串重复指定次数，并返回新字符串

#### []()模板字符串和插值运算符

`` 模板字符串
`${}` 插值运算符

>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206164259845.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)
>显示效果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200206164309490.png)

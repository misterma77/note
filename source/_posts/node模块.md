

## []()fs模块

**fs是文件操作内置模块**
**文件操作**

>**所有文件操作都有同步异步之分，特点是同步操作会带有`Sync`**
>
>1.`writeFile(参1,参2)`/`writeFileSync()`
> 作用：写入文件
> 参数1：文件名称,包括文件格式
> 参数2：文件中，需要写入的内容
> 参数3：配置对象{ }中的flag属性，a(追加写入)，w(正常写入，默认)写入文件存在时会覆盖
> 参数4：回调函数，执行完成后，如果执行错误会返回一个错误信息
>代码：![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322112852792.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>2.`readFile(参1,参2)`/`readFileSync()`
> 作用：文件读取
> 参数1：文件名称
> 参数2：“utf-8”,如果不写此参数，需要将回调函数中的第二个参数用toString()转换，否则无法读取中文
> 参数3：回调函数，读取完成后，会返回两个参数
>      错误信息和读取到的信息
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322113452212.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>3.`rename(参1,参2)`
> 作用：给文件重命名
> 参数1：修改之前的文件名及格式
> 参数2：修改之后的文件名及格式
> 参数3：回调函数，传入参数，表示是否成功
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322113953625.png#pic_center)
>4`unlink(参1,参2)`
> 作用：删除
> 参数1：删除的文件
> 参数2：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322114523987.png#pic_center)
>5.`copyFile(参1,参2)`
> 作用：复制文件
> 参数1：被复制的文件
> 参数2：复制文件
> 参数3：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322114719873.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322114816159.png#pic_center)
>6.`xx.isFile()`
>作用：判断目标是否是文件

**目录操作/文件夹操作**

>操作目录时，不需要后缀格式
>1.`mkdir(参1，参2)`
> 作用：创建目录
> 参数1：目录名
> 参数2：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020032211515471.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>2.`rename(参1,参2)`
> 作用：修改目录名称
> 参数1：被修改的目录名
> 参数2：修改后的目录名
> 参数3：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322115617676.png#pic_center)
>3.`readdir(参1,参2)`
> 作用：读取目录
> 参数1：读取目标
> 参数2：回调函数(错误信息,读取到的内容)
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322115859876.png#pic_center)
>4.`rmdir(参1,参2)`
> 作用：删除空目录/文件夹
> 参数1：删除的目标
> 参数2：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322120346758.png#pic_center)
>删除非空目录
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322121827586.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>5.`exists(参1,参2)`
> 作用：判断文件或文件夹是否存在
> 参数1：指定内容
> 参数2：回调函数，参数为一个布尔值
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322120914697.png#pic_center)
>6.`stat(参1,参2)`
> 作用：获取文件或文件夹的详细信息
> 参数1：指定内容
> 参数2：回调函数
> 代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020032212132242.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>7.`xx.isDirectory()`
>作用：判断目标是否是文件夹

## []()Stream流

基于fs模块
文件流，会把数据分成64kb的多个小文件，然后进行传输
耗时会变长，但是传输稳定，可以避免系统崩溃
`fs.creatReadStream(文件名)` 读取数据，用来打开一个刻度的文件流，返回一个js.ReadStream对象
`fs.createWriteStream()` 写入数据
`on("data",chunk=>{})`   数据传输时触发的方法,`chunk`读取的数据
`on("end",()=>{})` 数据传输完成后触发的方法

## []()url模块

url模块提供了一些实用函数，用于URL的处理与解析
引入：`let url = require("url")`
常用方法：1.`url.oarse()`字符串类型解析为对象
2.`url.format()` 对象类型转字符串

## []()path模块

path模块提供了一些用于处理文件路径的小文件
引入：`let path = require("path")`
常用方法：1.`path.extname()` 返回路径中文件的后缀名，即路径中最后一个"."之后的部分
       2.`path.pare()`返回路径字符串的对象
       3.`path.format()`	从对象中返回路径字符串

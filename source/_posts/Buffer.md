

## []()Buffer

buffer是数据的缓冲区，是内置的一个类，不是模块

>**buffer的创建**
>node6.0之前的方法： `new Buffer()`
>现在的方法：Buffer.alloc(参数) 参数为内容大小，单位为b

buffer会把数据(不限) 转换成二进制， 然后以十六进制的方式展示出来

>`from()` 每个字转换为三组十六进制的数据
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322123146691.png#pic_center)
>输出结果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322123154470.png#pic_center)
>如果要将这些十六进制的数据转换回去，需要在每组数据之前添加`0x`，用作标识十六进制数据
>代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/202003222026364.png#pic_center)输出结果：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322202647912.png#pic_center)

`string_decoder` class类
StringDecoder 固定名称
代码：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322205714764.png#pic_center)输出结果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200322205728631.png#pic_center)

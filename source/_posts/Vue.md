

# []()Vue.js

vue.js前端主流框架，一套用于构建用户界面的渐进式框架，研发者尤雨溪
vue.js的引入
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415164700689.png#pic_center)
构建用户界面：ui html css 静态页面
渐进式框架：延伸出来有五部分
   1.模板引擎 类似于pug nunjucks
   2.组件(核心功能之一),增加页面的复用性
   3.路由
   4.状态管理器(统筹管理属性-可伸缩性)
   5.自动化构建
渐进式的原理：一步一步执行

>###### []()模板引擎
>
>三个核心：
>  1.`el`   挂载点
>  2.`template`  模板(最终形成用户界面的原始结构)
>  3.`data`  数据
>vue将data和template相结合，最后添加到挂载点上
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415163639103.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
><mark>1.在模板生成后，会替换掉挂载点指定的元素</mark>
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165035722.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165043211.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
><mark>2.每个独立的模板有且只能有一个顶级的根节点</mark>
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165611798.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165621913.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
><mark>3.如果有指定的el而没有template,那么el中的outerHTML将作为template</mark>
> <mark>如果有template,则会优先选择template中的内容</mark>
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165836260.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415165845795.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>vue渲染
>template→加载到VDOM(虚拟dom,与dom规则一致)→将结果返还给html页面

>**vue的<mark>render</mark>函数**
> 渲染的方式有两种，template和render
> render是字符串模板的代替方案，允许我们发挥JavaScript最大的编程能力,该写法相对复杂
> 该渲染函数接收一个 `createElement`方法作为第一个参数用来创建Vnode
> 这个`createElement`名字可自定义，它就是上面所说的虚拟DOM
> `createElement()`有三个参数
>   参数1：元素或标签名
>   参数2：属性
>   参数3：内容 可以是一个数组也可以是一个字符串
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415171219958.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415171227410.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
> 
> render依然会覆盖掉挂载点el,可通过重新创建一个一样的元素来解决这个问题
> 
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415175908849.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415175917763.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

><mark>**延迟挂载**</mark>
>实例化Vue时没有设置el挂载点的挂载方式
>指定挂载点
>1.el  挂载点不能是`body`和`html`
>2.当实例被挂载以后，实例对象上就会有一个`$el`的属性,这个属性中存的内容就是挂载的元素
>3.vue实例上的内置属性都是以$或者_开头的，加上会被认为是内置属性
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415173144497.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415173153250.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

><mark>data</mark>
>1.在当前模板中可以直接使用(不需要去使用this一类的关键字)
>2.data中的数据命名不要使用$或_开头
> 因为Vue解析data以后，会把当前data中的数据加载到 实例对象中
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415174950774.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415174958857.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

><mark>视图更新</mark>
> 响应数据的变化(原理是数据驱动视图)
> 数据的变化会自动更新视图 根据数据劫持
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415181714525.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415181548470.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415181654156.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>数据劫持
> `Object.defineProperty()` 该方法只能监听某个对象中的某个属性
>  参数1：被监听的对象
>  参数2：被监听对象的属性
>  参数3：被监听的属性发生改变时调用的方法，以对象的形式传入`set(){}和get(){}`
>       每当数据发生改变时将新的值赋值给被监听的属性，但因为方法问题，会陷入死循环
>       所以需要一个数据,来代替被监听对象
> 流程：当被监听的属性发生改变时，会赋值给替代数据，然后渲染视图,渲染视图时会去找被监听的属
>    性，运行`get()`事件
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041518255856.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415182757384.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041518280632.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
><mark>无法对新增的属性进行监听</mark>
> 只有更新已有属性时，才能更新未被监听的属性
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415183126595.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415183252539.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415183304714.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415183405563.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>在模板中，如果我们使用了一个不存在的数据，需要一个方法来添加这个属性
>`Vue.set()`或`实例.$set()`方法可以添加属性并监听该属性
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415190706972.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/2020041519072195.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415190932734.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415191004461.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>以下的操作中并不会触发监听拦截
>  属性新增属性
>  数组方法：push、pop、shift、unshift、splice、sort、reverse
>  数组新增值：[ ]
>  数组 length 属性
>`vue` 对数组中的 `push`、`pop` 等方法进行重新包装，所以在 `vue` 中调用这些方法，可以对数组的修改进行监听拦截
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415191849247.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415191825293.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415192008370.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200415192051155.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

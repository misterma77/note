

# []()koa

#### []()koa介绍

  koa是express原班⼈⻢打造的轻量、健壮、富有表现⼒的nodejs框架。⽬前koa有koa1和koa2两个版本；koa2依赖Node.js 7.6.0或者更⾼版本；koa不在内核⽅法中绑定任何中间件，它仅仅是⼀个轻量级的函数库，⼏乎所有功能都必须通过第三⽅插件来实现

#### []()koa使用

安装：`npm install koa`
简单的搭建一个koa服务器
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327141716166.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70)

##### []()Application对象

> -application是koa的实例化对象，简称为app
> -app.use()将给定的中间件方法添加到此应用程序，分为异步和同步  异步通过es7中的`async`和`await`来处理
> -app.listen() 来设置服务器端口
> -app.on()  错误处理

##### []()上下⽂context对象常⽤属性及⽅法

> context 将node中的request和response 封装到⼀个对象中，并提供⼀些新的api提供给⽤户进⾏
>操作；
>  ctx.app:应⽤程序实例引⽤,等同于app;
>  ctx.req:Node 的 request 对象.
>  ctx.res:Node 的 response 对象.
>  ctx.request:koa中的Request对象；
>  ctx.response:koa中的response对象；
>  ctx.state：对象命名空间，通过中间件传递信息；
>  ctx.throw:抛出错误；
>  ctx.redirect()重定向
> ctx.status 获取响应状态
>  默认情况下， response.status 设置为 404 ⽽不是像 node 的res.statusCode 那样默认为 200 。
> http状态码：1xx(消息)、2xx(成功)、3xx(重定向)、4xx(请求错误)、5xx和6xx(服务器错误)
> 常用状态码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327143753419.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

##### []()中间件

>Koa 利⽤中间件 控制"上游"，调⽤"下游“
>koa是包含⼀组中间件函数的对象；可以将app.use⾥的函数理解成中间件
>![在这里插入图片描述](https://img-blog.csdnimg.cn/202003271439414.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)通过next()将控制转交给另⼀个中间件
>上述过程也可以通过"洋葱模型“来解释中间件执⾏顺序
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327144045248.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)代码：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327144446866.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>输出显示：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327144530438.png#pic_center)

##### []()koa常用中间件

中间件在实际使用中，全都是模块

>##### []()koa-router
>
>-路由是引导匹配之意，是匹配url到相应处理程序的活动
>-安装：`npm install koa-router -S`
>-引入：`const Router = require("koa-router")`
>-实例化：`let router = new Router()`
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327150022765.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327150321665.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327150330659.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>###### []()koa-static
>
>koa-static 是⽤于加载静态资源的中间件，通过它可以加载css、js等静态资源
>安装：`npm install koa-static`
>引入：`const static = require("koa-static")`
>使用：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327153910767.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>###### []()koa-views
>
>Koa-views⽤于加载html模板⽂件；
>安装：`npm install koa-views -S`
>引入：`const views = require("koa-views")`
>使用：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200327162012593.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

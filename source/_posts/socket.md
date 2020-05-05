

# []()单工通信

  所谓单工通信，是指消息只能单方向传输的工作方式
  单工通信信道是单向信道，发送端和接收端的身份是固定的，发送端只能发送信息，不能接收信息；接收端只能接收信息，不能发送信息，数据信号仅从一端传送到另一端，即信息流是单方向的

### []()前端轮循

前端以ajax的方式来循环定时的获取数据
前端轮循环，获取数据
 循环ajax请求 ，获取数据
 消耗性能，消耗资源，不推荐

>jquery
>同源策略：协议，域名，端口号都一样
>`$.ajax()` jquery获取ajax请求
> `url` 路由
> `method` 提交方式 get post
> `success(){}` 请求+响应完成后，执行的方法,固定名称
> `data:{}` 传递的数据
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405111309832.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

### []()SSE (server send event) 服务器推送数据

  Server-sent events:使⽤server-sent 事件的⽅法,服务器可以在任何时刻向我们的web⻚⾯推送数据和信息.这些被推送进来的信息可以在这个⻚⾯上作为事件+data来处理
  服务端设置
   设置头部`"Content-type","text/event-stream"`
  推送数据格式
   data: 声明数据开始
   \r\n\r\n 标志数据结尾
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200405112008830.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
  前端获取
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200329111938952.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

# []()双工同讯

### []()websocket

WebSocket 是 HTML5 开始提供的⼀种在单个 TCP 连接上进⾏全双⼯通讯的协议
websocket基于tcp协议

>###### []()服务端
>
>`var WebSocketServer = require("ws").Server`
>创建服务及指定端口号
> `let ws = new WebSocketServer({port:3601})`
>连接成功之后
> `ws.on("connection",回调函数)`
>发送数据到服务端
> `ws.send()`
>接收数据
> `ws.onmessage = function(d){d.data即为数据}`

>###### []()客户端
>
>同源策略：协议，域名，端口号都一样
>不同源的情况下需要写全称
>连接服务器
> `let ws = new WebSocket("ws://localhost/3601")`
>打开协议
> `ws.open=function(){}`
>发送数据到服务端
> `ws.send()`
>关闭协议,关闭后不能发送数据
> `ws.close()`
>接收数据
> `ws.onmessage = function(d){d.data即为数据}`
> `ws.addEventListener("message",function(){})`

### []()socket.io模块

>###### []()服务端
>
>下载socket.io模块
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200329150709573.png#pic_center)
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200406104042781.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)
>建立连接：
> 建立连接会传入一个socket对象,表示当前的连接者
> `io.on("connection",(socket)=>{`
>    传递数据
>    `socket.emit(1,2)`参1自定义事件，参2 传递的数据
>    把数据发送给除了当前连接者以外的所有连接者
>    `socket.broadcast.emit()`
> `})`

>###### []()客户端
>
>引入socket.io.js
>js位置 下载模块后`node_modules/socket.io-client/dist/socket.io.js`
>![在这里插入图片描述](https://img-blog.csdnimg.cn/2020032915163265.png#pic_center)
>接收数据：
> `socket.io(参1,参2)` 参1是那个自定义的事件，参2回调函数，传入被传递的数据

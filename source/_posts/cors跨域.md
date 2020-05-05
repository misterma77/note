# CORS跨域设置
- CORS(Cross-origin resource sharing)，跨域资源共享，是⼀份浏览器技术的规范，⽤来避开 浏览器的同源策略
- 简单来说就是解决跨域问题的除了jsonp外的另⼀种⽅法；⽐jsonp更加优雅
1. ('Access-Control-Allow-Origin', '*') //这个表示任意域名都可以访问，默认不能携带 cookie了。(必须字段)
```js
res.header('Access-Control-Allow-Origin', 'http://www.baidu.com'); //这样写，只有 www.baidu.com 可以访问
res.header('Access-Control-Allow-Origin', '*'); //这个表示任意域名都可以访问。
```
2. Access-Control-Allow-Headers ：设置允许requset设置的头部；
```js
res.header('Access-Control-Allow-Headers', 'Content-Type, Content-Length, Authorization, Accept, X-Requested-With , yourHeaderFeild');
```
3. Access-Control-Expose-Headers 允许客户端获取的头部key;
>('Access-Control-Expose-Headers'，'Content-Type, Content-Length, Authorization, Accept, X- Requested-With , yourHeaderFeild') CORS请求时， XMLHttpRequest 对象的 getResponseHeader() ⽅法只能拿到6个基本字段： CacheControl 、 Content-Language 、 Content-Type、 Expires 、 Last-Modified 、 Pragma 。如果想拿到其 他字段，就必须在 Access-Control-Expose-Headers⾥⾯指定
4. 预检请求
> - 简单的请求直接发送
```bash
   GET
   HEAD 
   POST 
   或者 
   content-type 
   text/plain 
   multipart/form-data 
   application/x-www-form-urlencoded

```
> - 预检请求
```bash
PUT 
DELETE 
CONNECT 
OPTIONS 
TRACE 
PATCH

```
- Access-Control-Max-Age⽤来指定本次预检请求的有效期，单位为秒，在此期间不⽤发出另⼀条 预检请求。(预检请求) 
  + 发送预检请求



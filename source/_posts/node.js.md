

# []()node.js

#### []()node介绍

  Node.js 诞生于2009年，Node.js采用C++语言编写而成，是 一个Javascript的运行环境。Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境 ，让JavaScript的运行脱离浏览器端，可以使用JavaScript语言 书写服务器端代码。

#### []()node安装

  [Node.js官网](https://nodejs.org)下载稳定版本,node偶数版本为稳定版本，奇数版本为非稳定版本。
  指令：node -v 用来检查node是否安装完成和版本号

#### []()初步感受

![在这里插入图片描述](https://img-blog.csdnimg.cn/20200320094347637.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center) - Google Chrome 默认非安全端口列表，尽量避免以下端口。

```
1,    // tcpmux
7,    // echo
9,    // discard
11,   // systat
13,   // daytime
15,   // netstat
17,   // qotd
19,   // chargen
20,   // ftp data
21,   // ftp access
22,   // ssh
23,   // telnet
25,   // smtp
37,   // time
42,   // name
43,   // nicname
53,   // domain
77,   // priv-rjs
79,   // finger
87,   // ttylink
95,   // supdup
101,  // hostriame
102,  // iso-tsap
103,  // gppitnp
104,  // acr-nema
109,  // pop2
110,  // pop3
111,  // sunrpc
113,  // auth
115,  // sftp
117,  // uucp-path
119,  // nntp
123,  // NTP
135,  // loc-srv /epmap
139,  // netbios
143,  // imap2
179,  // BGP
389,  // ldap
465,  // smtp+ssl
512,  // print / exec
513,  // login
514,  // shell
515,  // printer
526,  // tempo
530,  // courier
531,  // chat
532,  // netnews
540,  // uucp
556,  // remotefs
563,  // nntp+ssl
587,  // stmp?
601,  // ??
636,  // ldap+ssl
993,  // ldap+ssl
995,  // pop3+ssl
2049, // nfs
3659, // apple-sasl / PasswordServer
4045, // lockd
6000, // X11
6665, // Alternate IRC [Apple addition]
6666, // Alternate IRC [Apple addition]
6667, // Standard IRC [Apple addition]
6668, // Alternate IRC [Apple addition]
6669, // Alternate IRC [Apple addition]
```

#### []()<mark>nodemon工具</mark>

 可自动重启node服务
 安装:`npm i nodemon -g`

#### []()<mark>npm包管理器</mark>

 npm包管理器，又叫模块管理器
 NPM(Node Package Manager)  官网的地址是 [npm官网](https://www.npmjs.com)	
 安装完Node.js会自动安装NPM(Node Package Manager)
 npm常用指令:

>1.`npm-version(npm -v)`	查看npm版本
>2.`npm init`	引导创建一个package.json文件
>3.`npm install(npm i) 模块名`安装默认在当前目录，没有node_modules
> 则会创建文件夹
> `npm install 模块名 -S或--s`     写入dependencies
> `npm install 模块名 -D或--save-dev` 写入devDependencies
> `npm install 模块名 -g`         全局安装(命令行使用)
> `npm install 模块名 @1.0`       通过"@"符号安装指定版本模块
>4.`npm uninstall 模块名`   卸载模块
>5.`npm root`          查看当前包安装的路径
>6.`npm root -g`        查看全局安装路径
>7.`npm search`         查找
>8.`npm help(-h)`        查看npm帮助信息

#### []()<mark>package.json</mark>

 `.json` 配置信息文件
 `package.json` 当前模块中的配置信息
![在这里插入图片描述](https://img-blog.csdnimg.cn/20200320100534697.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

>`name` 模块名
>`version` 版本号
>`main` 主入口，未指定时，默认未`index.js`文件
>`dependencies` 运行依赖	 如`jquery`
>`devDependencies` 开发依赖  辅助写代码的工具 `sass`

## []()模块化

#### []()<mark>为什么会有模块化</mark>

 在JavaScript发展初期就是为了实现简单的页面交互逻辑，寥寥数语即，如今随着前端代码日益膨胀

 这时候JavaScript作为嵌入式的脚本语言的定位动摇了，JavaScript却没有为组织代码提供任何明显帮助，JavaScript极其简单的代码组织规范不足以驾驭如此庞大规模的代码；

>1. 使代码的结构更加清晰，便于后期维护
>2. 避免变量污染，每一个模块 都有自己独立的命名空间
>3. 可以按需加载, 提升性能

## []()数据的导出和导入

 **导出**

>导出多个：module.exports = {}
>     接收一个对象，对象中包含多个需要导出的内容(数量不限)
>导出单个：
>![在这里插入图片描述](https://img-blog.csdnimg.cn/20200320103035318.png?x-oss-processimage/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hCRl9fY2c,size_16,color_FFFFFF,t_70#pic_center)

 **导入**

>使用变量接收:`let obj = require("")`
>使用解构赋值:`let {a,Person} = require("")`

## []()node模块

 **模块的导入通过`require()`实现**
 **自定义模块**

>不需要安装，自定义使用，同级目录必须加"./"
>位置自定义，导入时前缀添加"./"

 **内置模块**

>由node自带，直接导入即可使用
>位置 node_modules
>导入时，直接写模块名称
>不需要安装

 **外置模块**

>使用npm通过指令，按需安装
>位置 node_modules
>导入时，直接写模块名称
>需要安装

## []()js模块和js文件的区别

 **文件:**

>1.使用时，script标签引入整体文件
>2.需要文件名+文件格式
>3.同级目录下直接写文件名+文件格式即可

 **模块：**

>1.使用时，require引入的是模块中导出的部分
>2.只需要模块名称即可
>3.同级目录下，路径的前缀必须加"./"

## []()**common.js规范**

  CommonJS规范的提出，主要是为了弥补JavaScript没有标准的缺陷，已达到像Python、Ruby和Java那样具备开发大型应用的基础能力，而不是停留在开发浏览器端小脚本程序的阶段

CommonJS模块规范主要分为三部分：模块引用、模块定义、模块标识。

###### []()CommonJS模块规范的好处

>CommonJS模块规范很好地解决变量污染问题，每个模块具有独立空间，互不干扰，命名空间等方案与之相比相形见绌。
>CommonJS规范定义模块十分简单，接口十分简洁。
>CommonJS模块规范支持引入和导出功能，这样可以顺畅地连接各个模块，实现彼此间的依赖关系。

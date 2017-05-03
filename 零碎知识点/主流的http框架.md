# androidnote

1，HttpURLConnection
2，HttpClient
3，OkHttp
   OkHttp是square自己实现的一个的一个http库，需要Android 2.3以上。OKHttp非常高效，支持SPDY、连接池、GZIP和 HTTP 缓存。
   默认情况下，OKHttp会自动处理常见的网络问题，像二次连接、SSL的握手问题。从Android4.4开始HttpURLConnection的底层实现采用的是okHttp。
4，volley
    早期使用HttpClient，后来使用HttpURLConnection，是谷歌2013年推出的网络请求框架，非常适合去进行数据量不大，
    但通信频繁的网络操作，而对于大数据量的网络操作，比如说下载文件等，Volley的表现就会非常糟糕。
5，Retrofit
Retrofit
    是一个封装比较好的，相对更面向开发者的rest请求库，和Volley框架的请求方式很相似，它的底层网络请求可以使用不同的网络库来处理，比如OkHttp（默认），HttpClient。
    采用注解方式来指定请求方式和url地址，减少了代码量。
    如果你的应用程序中集成了OKHttp，Retrofit默认会使用OKHttp处理其他网络层请求。
6，AsyncHttpClient
    也是一个较高层的封装，底层使用的是HttpClient。


1、volley
项目地址 https://github.com/smanikandan14/Volley-demo
 (1)  JSON，图像等的异步下载；
 (2)  网络请求的排序（scheduling）
 (3)  网络请求的优先级处理
 (4)  缓存
 (5)  多级别取消请求
 (6)  和Activity生命周期的联动（Activity结束时同时取消所有网络请求）

2、android-async-http
项目地址：https://github.com/loopj/android-async-http
文档介绍：http://loopj.com/android-async-http/
(1) 在匿名回调中处理请求结果
(2) 在UI线程外进行http请求
(3) 文件断点上传
(4) 智能重试
(5) 默认gzip压缩
(6) 支持解析成Json格式
(7) 可将Cookies持久化到SharedPreferences

3、xUtils和Afinal框架
项目地址：https://github.com/yangfuhai/afinal
主要有四大模块：
(1) 数据库模块：android中的orm框架，使用了线程池对sqlite进行操作。
(2) 注解模块：android中的ioc框架，完全注解方式就可以进行UI绑定和事件绑定。无需findViewById和setClickListener等。
(3) 网络模块：通过httpclient进行封装http数据请求，支持ajax方式加载，支持下载、上传文件功能。
(4) 图片缓存模块：通过FinalBitmap，imageview加载bitmap的时候无需考虑bitmap加载过程中出现的oom和android容器快速滑动时候出现的图片错位等现象。

4、ThinkAndroid
项目地址：https://github.com/white-cat/ThinkAndroid
主要有以下模块：
  (1)  MVC模块：实现视图与模型的分离。
  (2)  ioc模块：android中的ioc模块，完全注解方式就可以进行UI绑定、res中的资源的读取、以及对象的初始化。
  (3)  数据库模块：android中的orm框架，使用了线程池对sqlite进行操作。
  (4)  http模块：通过httpclient进行封装http数据请求，支持异步及同步方式加载。
  (5)  缓存模块：通过简单的配置及设计可以很好的实现缓存，对缓存可以随意的配置
  (6)  图片缓存模块：imageview加载图片的时候无需考虑图片加载过程中出现的oom和android容器快速滑动时候出现的图片错位等现象。
  (7)  配置器模块：可以对简易的实现配对配置的操作，目前配置文件可以支持Preference、Properties对配置进行存取。
  (8)  日志打印模块：可以较快的轻易的是实现日志打印，支持日志打印的扩展，目前支持对sdcard写入本地打印、以及控制台打印
  (9)  下载器模块:可以简单的实现多线程下载、后台下载、断点续传、对下载进行控制、如开始、暂停、删除等等。
  (10) 网络状态检测模块：当网络状态改变时，对其进行检

5、LoonAndroid
项目地址：https://github.com/gdpancheng/LoonAndroid
主要有以下模块：
  (1)  自动注入框架（只需要继承框架内的application既可）
  (2)  图片加载框架（多重缓存，自动回收，最大限度保证内存的安全性）
  (3)  网络请求模块（继承了基本上现在所有的http请求）
  (4)  eventbus（集成一个开源的框架）
  (5)  验证框架（集成开源框架）
  (6)  json解析（支持解析成集合或者对象）
  (7)  数据库（不知道是哪位写的 忘记了）
  (8)  多线程断点下载（自动判断是否支持多线程，判断是否是重定向）
  (9)  自动更新模块
  (10) 一系列工具类
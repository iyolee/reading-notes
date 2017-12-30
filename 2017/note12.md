## 2017.12.05
阅读：[SICP 介绍](https://zhuanlan.zhihu.com/p/27268471)  
笔记：
- 大脑创造思维，思维创造程序，程序由计算机运行，计算机必须遵循物理定律。
- 程序必须写得能够供人们阅读，其次才是去供计算机执行。

阅读：[React 设计思想](https://github.com/react-guide/react-basic)  
笔记：
- 设计 React 的核心前提是认为 UI 只是把数据通过映射关系变换成另一种形式的数据。
- 通过在一个函数中调用另一个函数来实现复杂的 UI，这就是抽象。
- “组合”就是将两个或者多个不同的抽象合并为一个。

阅读：[Redux 源码解析](http://www.ahonn.me/2017/07/04/redux-source-code-insight/#思考总结)  

阅读：[为什么 [ ] 是 false 而 !![ ] 是 true](https://www.h5jun.com/post/why-false-why-true.html)  
笔记：
- If Type(y) is Boolean, return the result of the comparison x == ToNumber(y).
- If Type(x) is Object and Type(y) is either String, Number, or Symbol, return the result of the comparison ToPrimitive(x) == y.

## 2017.12.07
阅读：[具有代表性的 HTTP 14 个状态码](https://juejin.im/post/5a276865f265da432c23b8d2?utm_medium=fe&utm_source=weixinqun)  
笔记：  
1. 2XX 响应的结果标明请求被正常处理了
    - 200：表示从客户端发来的请求在服务器端被正常处理了
    - 204：该状态码代表服务器接收的请求已成功处理，但在返回的响应报文中不含实体的主体部分
    - 206：该状态码表示客户端进行了范围请求，而服务器成功执行了这部分的 GET 请求响应报文中包含由 Content-Range 指定范围的实体内容
2. 3XX(Redirection 重定向状态码)
    - 301：永久性重定向
    - 302：临时性重定向
    - 303：该状态码表示由于请求对应的资源存在着另一个 URI，应使用 GET 方法定向获取请求的资源
    - 304：该状态码表示客户端发送附带条件的请求时，服务器端允许请求访问资源，但未满足条件的情况
    - 307：临时重定向， 会遵照浏览器标准，不会从 POST 变成 GET
3. 4XX(Client Error 客户端错误状态码)
    - 400：该状态码表示请求报文中存在语法错误
    - 401：该状态码表示发送的请求需要有通过 HTTP 认证(BASIC 认证、DIGEST 认证)的认证信息
    - 403：该状态码表明对请求资源的访问被服务器拒绝了
    - 404：该状态码表明服务器上无法找到请求的资源
    - 405：客户端请求的方法虽然能被服务器识别，但是服务器禁止使用该方法
4. 5XX(Server Error 服务器错误状态码)
    - 500：该状态码表明服务器端在执行请求时发生了错误
    - 502：该状态码表明扮演网关或代理角色的服务器，从上游服务器中接收到的响应是无效的
    - 503：该状态码表明服务器暂时处于超负载或正在进行停机维护，现在无法处理请求

阅读：[用js优美的写各种斐波那契数列](https://zhuanlan.zhihu.com/p/27205391?group_id=921827598683185152)  
笔记：把前两位数字做成参数巧妙的避免了重复计算 从而达到了性能的提升
``` JavaScript
function fib(n){
  function fib_(n,a,b){
    if(n==0)  return a
    else return fib_(n-1,b,a+b)
  }
  return fib_(n,0,1)
}
```

## 2017.12.13
阅读：[WebSocket 探秘](https://segmentfault.com/a/1190000012319848)  
  
阅读：[学习Less-看这篇就够了](https://segmentfault.com/a/1190000012360995#articleHeader11)

## 2017.12.14
- [前端跨域解决方案](https://segmentfault.com/a/1190000012256432)

## 2017-12-30
- [HTTP 2.0 协议详解](http://blog.csdn.net/zqjflash/article/details/50179235)  
    1. 所有http请求都建立在一个TCP请求上，实现多路复用
    2. 可以给请求添加优先级
    3. 服务器主动推送 server push
    4. HTTP2的头部会减小，从而减少流量传输
- [关于跨域，你想知道的全在这里](https://zhuanlan.zhihu.com/p/25778815)
- [Ajax 知识体系大梳理](https://juejin.im/post/58c883ecb123db005311861a?utm_source=gold_browser_extension)
- [10 分钟理解 BFC 原理](https://zhuanlan.zhihu.com/p/25321647)  
    1. 具有 BFC 特性的元素可以看作是隔离了的独立容器，容器里面的元素不会在布局上影响到外面的元素，并且 BFC 具有普通容器所没有的一些特性。
    2. 只要元素满足下面任一条件即可触发 BFC 特性：
        - body 根元素
        - 浮动元素：float 除 none 以外的值
        - 绝对定位元素：position (absolute、fixed)
        - display 为 inline-block、table-cells、flex
        - overflow 除了 visible 以外的值 (hidden、auto、scroll)
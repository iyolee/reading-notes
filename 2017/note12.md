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
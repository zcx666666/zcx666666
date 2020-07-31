---
title: 1:node介绍
date: 2020-07-29 13:39:33
tags:
---

# vscode插件运行node

*vscode运行nodejs需要插件  code runner*，然后再执行文件中右键选择第一个Run Code即可执行。![image-20200729135640309](C:\Users\ZIAN KANG\AppData\Roaming\Typora\typora-user-images\image-20200729135640309.png)

# node的引入

```javascript
function add(a,b){
   return a+b
}

module.exports = add
```

*a.js以上用来写函数方法，然后module.exports导出这个函数名*，函数内部来处理计算问题。调用方只需要传参即可。

```javascript
const add = require('./a')
console.log(add(100,222))
```

*b.js以上使用require('./a')引入a.js后调用add函数传参进去。返回值打印则显示处理后的数据*

```javascript
//如果导出多个方法
      function add(a,b){
         return a + b
      }
      function mul(a,b){
         return a * b
      }

      module.exports = {
         add,
         mul
      }

   //引入也需要改
      const {add,mul} = require('./a')

      console.log(add(100,222))
      console.log(mul(5,5))
```

容易遇到的问题：

编辑器提示使用ES6语法export default后直接报错。node是使用module.exports来导出的。

https://juejin.im/post/5d8c1fc26fb9a04e10438388#heading-10

  https://blog.csdn.net/u010419337/article/details/79290776

# 引用npm包

使用其他的写好的包，首先需要初始化

```javascript
 npm init -y
```

初始化完成以后会自动生成一个package.json的文件。文件中的main则是主文件入口。 "main": "a.js",为什么主文件入口就是什么。![image-20200729141056765](C:\Users\ZIAN KANG\AppData\Roaming\Typora\typora-user-images\image-20200729141056765.png)

配置好以后就可以使用包的安装了。安装任何包都是使用node。

```javascript
npm i lodash --save
//在页面引入lodash
const _ = require('lodash')
console.log(_.concat([1,2],3))
```

安装lodash工具库 ，引入lodash操作数组。lodash工具库就是对数组的操作。可以参考api进行https://www.lodashjs.com/。

# 模块化

模块化是一种规范，为什么要使用模块化。模块化再前端再后端都有不同的标准，再nodejs中就是手写commonjs就可以了。

好处：对代码进行拆分。工具函数分到不同的文件中然后再去别的地方引用。这样代码有拆分关系。比较符合设计原则。

# node中debugger

![image-20200729143259218](C:\Users\ZIAN KANG\AppData\Roaming\Typora\typora-user-images\image-20200729143259218.png)

打断点的话就是在文件中的代码前点击出现圆形红点后点击执行即可。








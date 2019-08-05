
npm install -g typescript

tcs greeter.ts

typescript的好处是：

TypeScript can offer static analysis based on both the structure of your code, and the type annotations you provide.

https://www.runoob.com/typescript/ts-type.html  教程

typeof "John"                // 返回 string 
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
typeof undefined             // undefined
typeof null                  // object
null === undefined           // false
null == undefined            // true

首先，== equality 等同，=== identity 恒等。
==， 两边值类型不同的时候，要先进行类型转换，再比较。
==，不做类型转换，类型不同的一定不等。



你可以设置为 undefined 来清空对象:
你可以设置为 null 来清空对象:

注意：TypeScript 和 JavaScript 没有整数类型。



----
一个知识点：

Null 和 Undefined
null
在 JavaScript 中 null 表示 "什么都没有"。

null是一个只有一个值的特殊类型。表示一个空对象引用。

用 typeof 检测 null 返回是 object。

undefined
在 JavaScript 中, undefined 是一个没有设置值的变量。

typeof 一个没有值的变量会返回 undefined。

Null 和 Undefined 是其他任何类型（包括 void）的子类型，可以赋值给其它类型，如数字类型，此时，
赋值后的类型会变成 null 或 undefined。而在TypeScript中启用严格的空校验（--strictNullChecks）
特性，就可以使得null 和 undefined 只能被赋值给 void 或本身对应的类型，示例代码如下：

-----------
变量作用域
变量作用域指定了变量定义的位置。

程序中变量的可用性由变量作用域决定。

TypeScript 有以下几种作用域：

全局作用域 − 全局变量定义在程序结构的外部，它可以在你代码的任何位置使用。

类作用域 − 这个变量也可以称为 字段。类变量声明在一个类里头，但在类的方法外面。 该变量可以通过类的对象来访问。类变量也可以是静态的，静态的变量可以通过类名直接访问。

局部作用域 − 局部变量，局部变量只能在声明它的一个代码块（如：方法）中使用。
----------
在 ES6 中引入的 for...of 循环，以替代 for...in 和 forEach() 
----------
构造函数
TypeScript 也支持使用 JavaScript 内置的构造函数 Function() 来定义函数：
----------
Lambda 函数
Lambda 函数也称之为箭头函数

单个参数 () 是可选的：
var display = x => { 
    console.log("输出为 "+x) 
} 
display(12)
---
无参数时可以设置空括号：

TypeScript
var disp =()=> { 
    console.log("Function invoked"); 
} 
disp();
----------
函数重载
重载是方法名字相同，而参数不同，返回类型可以相同也可以不同。

每个重载的方法（或者构造函数）都必须有一个独一无二的参数类型列表。
----------
pop()
删除数组的最后一个元素并返回删除的元素。

shift()
删除并返回数组的第一个元素。
----------
访问控制修饰符
TypeScript 中，可以使用访问控制符来保护对类、变量、方法和构造方法的访问。TypeScript 支持 3 种不同的访问权限。

public（默认） : 公有，可以在任何地方被访问。

protected : 受保护，可以被其自身以及其子类和父类访问。

private : 私有，只能被其定义所在的类访问。
----------
用近似静态语言、强类型语言的TypeScript开发属于动态语言、弱类型语言的JavaScript
----------
 大家最熟知的JavaScript模块加载器是服务于 Node.js 的 CommonJS 和服务于 Web 应用的 Require.js。

此外还有有 SystemJs 和 Webpack。

----------
模块的差别：
AMD format的主要目就是为developer提供javascript模块化变成的方案；跟CommonJS的主要区别是：AMD是为browser端而设计；CommonJS面向的是server端；

AMD和CommonJS的简单区别(可能不完全):

　　1)scoping:browser中无法对js代码进行完全隔离，只能在function中定义变量使其不会在global中出现，这样很容易导致错误出现: var a=b=0;

　　　　AMD不能很好的解决这个问题。相反，AMD支持将external resource引入local function scope，进而实现local scoping；

　　　　CJS是干净的server端环境，如node，没有global scope；

　　2)Distance:对浏览器来说，很多资源都是remote的，虽然资源可能被cache到本地，可请求/获得资源总是费时间的；如果要执行的function在另一个文件中，我们就无法知道这个文件是否已经被load进来或者还要花数秒去获得这个文件；如果不知道function是否已经被定义，那么就不能擅自调用它；

　　　　CJS解决这个问题的方法是：假设所有请求的资源都在本地，或者至少可以在毫秒级甚至微秒级时间内请求到；

　　3)Asynchrony:上边所说的distance问题造成的直接结果是，需要异步执行task。浏览器在单独线程内执行javascript，如果此线程在等待远程资源，此时啥也不会执行，用户感觉浏览器没反应了。

　　　　解决这个问题的方法是，当资源被准备好了就执行提取初始化操作和请求回调函数操作(callback function)；

　　　　Node主要通过事件驱动编程模型来实现异步；

　　　　简单地说，CJS同步提取module resource，因为资源在微秒级的时间内可以到达，不需要异步！
----------
20190718 over
----------

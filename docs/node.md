----------
chapter 2： 模块机制
包的出现，是在模块基础上进一步组织javascript代码

npm ls  查看包依赖

amd（asynchronous Module definition)  规范是CommonJS模块规范的一个延伸。
cmd 是国内 玉伯提出， 更简单

javascript线程 是一个分配任务和处理结果的大管家，IO线程池里的各个io线程都是小二，兢兢业业地完成分配来的任务。

cpu密集型不是node的长项， cpu处理时间超过10ms的可以通过setImmediate()来处理。

-----------
chapter 3： 异步I/O

它的优秀之处并非原创，它的原创之处并不优秀。

select  限制是 1024个文件描述符

epoll Linux下最高的io事件通知机制
kqueue：仅仅freebsd

-------------
chapter 4: 异步编程

高价函数是 可以把函数作为参数，或者将函数作为返回值的函数。

Javascript 没有类的概念，只有对象概念。
***
当然也可以使用apply, apply 和 call 的不同在于call，就是call方法接受的是若干个参数的列表，而apply方法接受的是一个包含多个参数的数组。
改变当前对象
***

Promise/Deffered 没有搞懂

-------------
chapter 5： 内存控制

64位： 1.4G
32： 0.7G

到了strict模式里，使用with会直接报错：

闭包：在javascript中，实现外部作用域访问内部作用域中变量的方法。

堆外内存
-------------
chapter 6： 理解Buffer
chapter 7： 网络编程



-------------
-------------
-------------
-------------
-------------
-------------




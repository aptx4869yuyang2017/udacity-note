# Object-Oriented JavaScript

> <https://classroom.udacity.com/courses/ud015>

## Scope 作用域

* Lexical Scope：作用域 就是函数可以调用的范围 **js 比较特殊 可以调用外围的 global 变量  不用特别声明 global**
* Execution Contexts 执行环境 就是变量的存储机制 寻找变量值的过程是从内向外的

## Closures 闭包

* the function can remain the available after outer scopes have returned
* 即使跳出当前函数的作用域 依然保留了访问之前临时变量的机制

## Keywords "this"  

* "this" 的调用 感觉像是 python 里面的 self  不过，这个机制真的有点晕
* 一般就是看“.”前面的内容
* 然而单独赋值也会重写
* 注意 setTimeout 的调用 直接赋值 global 了

## The object prototype 对象继承的特性

* 和 python 的 类的继承 很像  都继承了 prototype
* `var new_object = Objdect.creat(old_object)`

## Object Decorator Pattern

* 代码的重复利用
* 可以牺牲部分内存，获取代码的简洁性

# 详解Javascript中prototype属性



在典型的面向对象的语言中，如java，都存在类（class）的概念，类就是对象的模板，对象就是类的实例。但是在Javascript语言体系中，是不存在类（Class）的概念的，javascript中不是基于‘类的'，而是通过构造函数（constructor）和原型链（prototype chains）实现的。但是在ES6中提供了更接近传统语言的写法，引入了Class（类）这个概念，作为对象的模板。通过class关键字，可以定义类。基本上，ES6的class可以看作只是一个语法糖，它的绝大部分功能，ES5都可以做到，新的class写法只是让原型对象的写法更加清晰、更像面向对象编程的语法而已。  


按照我的习惯，在写文章前我会给出文章目录。  


以下内容会分为如下小节：  


　　1.构造函数的简单介绍  


　　2.构造函数的缺点  


　　3.prototype属性的作用  


　　4.原型链（prototype chain）  


　　5.constructor属性  


　　　　5.1：constructor属性的作用  


　　6.instanceof运算符  


**1.构造函数的简单介绍**  


　　在我的一篇Javascript 中构造函数与new命令的密切关系文章中，详细了介绍了构造函数的概念和特点，new命令的原理和用法等，如果对于构造函数不熟悉的同学，可以前往细细品味。以下做一个简单的回顾。

　　所谓构造函数，就是提供了一个生成对象的模板并描述对象的基本结构的函数。一个构造函数，可以生成多个对象，每个对象都有相同的结构。总的来说，构造函数就是对象的模板，对象就是构造函数的实例。  


　　构造函数的特点有：  


　　　　a：构造函数的函数名首字母必须大写。  


　　　　b：内部使用this对象，来指向将要生成的对象实例。  


　　　　c：使用new操作符来调用构造函数，并返回对象实例。  


　　看一个最简单的一个例子。详解Javascript中prototype属性\(推荐\)\_javascript技巧\_脚本之家

```
function Person(){
 this.name = 'keith';
} 
 var boy = new Person();
console.log(boy.name); //'keith'

```



**2.构造函数的缺点**  


　　所有的实例对象都可以继承构造函数中的属性和方法。但是，同一个对象实例之间，无法共享属性。


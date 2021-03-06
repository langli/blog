# 随笔
## javascript 必须理解的概念
### 闭包
**简单描述一下闭包吧:** 闭包的问题是每个前端开发者必须理解的概念. 有不少开发人员总是搞不清匿名函数和闭包这两个概念，因此经常混用。闭包是指有权访问另一个函数作用域中的变量的函数。创建闭包的常见方式，就是在一个函数内部创建另一个函数。
###立即执行函数表达式
以下两种写法都可以:
```javascript
(function(){
  /* code */
  console.log("Hello world!");
}());  // 推荐使用这个

(function(){
  /* code */
  console.log("OK!");
})();//这个也可以
```
### 对象字面量
在JavaScript中对象字面量非常常用, 它定义在一对大括号中, 由多个 name/value 名值对组成. 使用对象字面量可以封装和组织代码.
```javascript
var person = {
  id: "110",
  name: "XXX",
  getName: function() {
    console.info("Hello world");
  }
};
```
## javascript 要点记录
* delete 操作符可以完全删除实例属性，而不会删除原型属性。从而能够访问原型中同名属性。delete person.name;
* hasOwnProperty('name')判断是否为实例属性，in 操作符可以单独使用，不论实例属性和原型属性都为true;  'name' in person;
* 动态原型模式---是为了解决独立的构造函数和独立的原型，最佳方案。基于组合模式---组合使用构造函数模式和原型模式时，使用构造函数定义实例属性，而使用原型定义共享的属性和方法;
* 寄生组合式继承，集寄生式继承和组合继承的优点与一身，是实现基于类型继承的最有效方式;
* YUI的YAHOO.lang.extend()方法采用了寄生组合继承，从而让这种模式首次出现在了一个应用非常广泛的JavaScript库中。要了解有关YUI的更多信息，请访问http://developer. yahoo.com/yui/;
* 使用命名函数表达式来实现递归，如：var factorial = (function f(num){if(num<=1)return 1;return num*f(num-1);});
* 闭包是指有权访问另一个函数作用域中的变量的函数。创建闭包的常见方式，就是在一个函数内部创建另一个函数;
* 闭包是一系列代码块（在ECMAScript中是函数），并且静态保存所有父级的作用域。通过这些保存的作用域来搜寻到函数中的自由变量。
* this是执行上下文环境的一个属性，而不是某个变量对象的属性
* javascript 使用静态作用域
* 在函数原型中定义的两个方法（因此所有的函数都可以访问它）允许去手动设置函数调用的this值。它们是.apply和.call方法。
* 作用域链正是内部上下文所有变量对象（包括父变量对象）的列表。
## 提升
* 如果学习一门技术仅仅在用的层面上, 你就没有完全吸取其中的精华, 而且学习的收益会随着技术的过时而消失.
* 资深开发者与新手的最大区别在于解决问题的能力.
* 架构师和开发者一样, 也经常写代码, 简单的说, 开发者和架构师之间最大的区别就是技术领导力.
## 开发书籍
* 《Scaling Isomorphic Javascript Code》
* 《程序员必读之软件架构》
* 《海量运维运营规划》
* 《构建高性能web站点》
* 《大型网站技术架构》

## 教程参考：
>- [廖雪峰的 JavaScript全栈教程](http://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000)  
>- [阮一峰的 JavaScript 标准参考教程](http://javascript.ruanyifeng.com/#introduction)

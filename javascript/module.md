#Module 模块模式
优点: 
面向对象的开发方式, 采用封装的思想.
支持私有数据和公有数据, 公有部分可以访问私有部分, 外部无法接触私有部分, 只能通过开放接口;
如果正确使用, Module 模式是非常有用的;
缺点:
如果改变一个成员的可见性, 我们必须修改每一个曾经使用过该成员的地方. 暴露在外部的接口尽量不要频繁修改;
无法为私有成员创建自动化单元测试;
示例代码如下:
https://github.com/Ivanwangcy/ISourcePlayer/blob/master/design-pattern/module.js


Revealing Module (揭示模块) 模式

Module 模式的改进版本 -- Christina Heilmann 的 Revealing Module 模式. 

Revealing Module 模式的产生是因为 Heilmann 很不满意这种状况:
当他想从另一个方法调用一个公有方法或公有变量时, 必须要重复主对象的名称. 他也不喜欢使用 Module 模式时, 必须要切换到对象字面量表示法来让某种方法变成公有方法. 

他努力的结果就是创建一个更新的模式, 能够在私有范围内简单定义所有的函数和变量, 并返回一个匿名对象, 它拥有指向私有函数的指针, 改函数是他希望展示为公有的方法.

有关如何使用 Reveal Module 模式的示例如下所示: 


优点:
该模式可以使脚本语法更加一致. 在模块代码底部, 它也会很容易指出哪些函数和变量可以被公开访问, 从而改善可读性. 

缺点: 
如果一个私有函数引用一个公有函数, 在需要打补丁时, 公有函数是不能被覆盖的. 这是因为私有函数将继续引用私有实现, 该模式并不适用于公有成员, 只适用于函数. 

引用私有变量的公有对象成员也遵守无补丁规则.

采用Reveal Module 模式创建的模块可能比哪些采用原始 Module 模式创建的模块更加脆弱, 所以使用时应该特别小心.



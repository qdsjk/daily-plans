# 总结： 第一次计划完成70%吧 ###
#1. **六级单词**#
	
- 9.26 200
	
- 9.27 200左右
- 9.28 200左右
- 9.29 200左右
- 9.30 200左右
# **2. leetcode第100题第101题** #
- [https://leetcode-cn.com/problems/same-tree/](https://leetcode-cn.com/problems/same-tree/ "100")树的遍历，干递归就完事了
- [https://leetcode-cn.com/problems/symmetric-tree/](https://leetcode-cn.com/problems/symmetric-tree/)中序遍历能搞，但是我不会写？还是菜的一批

# **3. Java基础语法** #
	9.27

- 类名：首字母大写 例如 MyFirstJavaClass
	


- 方法名：小写 若干单词，则后面的每个单词首字母大写。例如 myFirstFunction
	
- 访问控制修饰符 : default, public , protected, private 
> 类的访问控制符只能是空或者 public，方法和属性的访问控制符有 4 个，分别是 public、 private、protected 和 friendly，其中 friendly 是一种没有定义专门的访问控制符的默认情况。

- 非访问控制修饰符 : 
> final   修饰类、方法和变量，final 修饰的类不能够被继承，类中的 final 方法可以被子类继承，但是不能被子类修改。


> abstract  1.用来创建抽象类和抽象方法。抽象类不能用来实例化对象，声明抽象类的唯一目的是为了将来对该类进行扩充。2.一个类不能同时被 abstract 和 final 修饰。如果一个类包含抽象方法，那么该类一定要声明为抽象类。3.抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。
任何继承抽象类的子类必须实现父类的所有抽象方法，除非该子类也是抽象类。
> 
>  static 用来修饰类方法和类变量。一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。
> 
> synchronized和 volatile 修饰符，主要用于线程的编程

- 变量 
> 局部变量      
> 类变量（静态变量） static修饰的变量称为静态变量  
> 成员变量（非静态变量）
> 数据存储位置不同
> 成员变量存储在堆内存的对象中，所以也叫对象的特有数据。
> 静态变量数据存储在方法区（共享数据区）的静态区，所以也叫对象的共享数据。

- 枚举 enum FreshJuiceSize{ SMALL, MEDIUM , LARGE }  
- throw 和 throws 的区别：
> throws 用来声明一个方法可能产生的所有异常，不做任何处理而是将异常往上传，谁调用我我就抛给谁。

>throw 则是用来抛出一个具体的异常类型。

> throws 在方法后边声明异常，其实就是自己不想对异常做出任何的处理，告诉别人自己可能出现的异常，交给别人处理，然别人处理。
> 
> throw 就是自己处理一个异常，有两种方式要么是自己捕获异常 try...catch 代码块，要么是抛出一个异常（throws 异常）。

	9.28

- 匿名类

> 主要是用于在我们需要的时候创建一个对象来执行特定的任务，可以使代码更加简洁。
匿名类是不能有名字的类，它们不能被引用，只能在创建时用 new 语句来声明它们。

- 内部类
> 非静态内部类是一个类中嵌套着另外一个类。 它有访问外部类成员的权限， 通常被称为内部类。
> 
> 由于内部类嵌套在外部类中，因此必须首先实例化外部类，然后创建内部类的对象来实现。
> 
> OuterClass.InnerClass myInner = myOuter.new InnerClass();
# LeetCode #
- 111. 二叉树的最小深度 [https://leetcode-cn.com/problems/minimum-depth-of-binary-tree/](https://leetcode-cn.com/problems/minimum-depth-of-binary-tree/) 和最大深度一个套路，注意一点就是根和叶子的关系
- 559. N叉树的最大深度[https://leetcode-cn.com/problems/maximum-depth-of-n-ary-tree/](https://leetcode-cn.com/problems/maximum-depth-of-n-ary-tree/)  BFS 按照层序遍历  DFS 即递归思想

# JAVA #
- 继承 已有的类派生出新的类
> 子类继承父类的特征和行为（方法、变量等）  支持单继承，多重继承，不支持多继承
> 
> 使用 implements 关键字可以变相的使java具有多继承的特性，使用范围为类继承接口的情况
> 
> 子类是不继承父类的构造器，它只是调用（隐式或显式）。如果父类的构造器带有参数，则必须在子类的构造器中显式地通过 super 关键字调用父类的构造器并配以适当的参数列表。

- Java 转型问题，只要记住一句话：父类引用指向子类对象

`Father f1 = new Son(); //（向上转型) 现在 f1 引用指向一个Son对象`

`Son s1 = (Son)f1;   //downcasting (向下转型) 现在f1 还是指向 Son对象`

- 重写(Override)是子类对父类的允许访问的方法的实现过程进行重新编写, 返回值和形参都不能改变。即外壳不变，核心重写！

> 声明为 static 的方法不能被重写，但是能够被再次声明。
> 
> 重写的方法能够抛出任何非强制异常，无论被重写的方法是否抛出异常。但是，重写的方法不能抛出新的强制性异常，或者比被重写方法声明的更广泛的强制性异常，反之则可以。

- 重载(overloading) 是在一个类里面，方法名字相同，而参数不同。返回类型可以相同也可以不同。
> 方法重载是一个类的多态性表现,而方法重写是子类与父类的一种多态性表现。

- java中的异常分为两大类， 强制性异常(CheckedException)和非强制性异常(UncheckedException)。 

> 而java中除了RuntimeException外，都是强制性异常。 



> 强制性异常：所谓强制性异常就是在编写程序的过程中必需在抛出异常的部分try catch  或者向上throws异常。 


> 非强制性异常：所谓非强制性异常就和上面相反了。不过你当然也可以try catch或者thows，只不过这不是强制性的。 
> 

- 多态 同一个行为具有多个不同表现形式或形态的能力。同一个接口，使用不同的实例而执行不同操作
> 多态存在的三个必要条件。继承，重写，父类引用指向子类对象

-  抽象类 一个类中没有包含足够的信息来描绘一个具体的对象
> 抽象类必须被继承因为不能实例化对象。其他和普通类一样

 
- 抽象方法 该方法的具体实现由它的子类确定 abstract void fun(); 无实现功能

> 如果一个类包含抽象方法，那么该类必须是抽象类
> 
> 继承抽象方法的子类必须重写该方法。否则，该子类也必须声明为抽象类
> 
> 构造方法，类方法（用 static 修饰的方法）不能声明为抽象方法。

- 接口 可以理解成统一的协议

> 只能够有静态的不能被修改的数据成员 static final ，不过在 interface 中一般不定义数据成员
> 
> 其实 abstract class 表示的是 "is-a" 关系，interface 表示的是 "has-a" 关系。

- 枚举(enum) 一般表示一组常量
> enum Color 
> { 
>     RED, GREEN, BLUE; 
> } 

# 作业 #
- RAS 非对称加密算法
> 找质数，P和Q（1024位目前安全）：P = 3  Q = 11

> 计算公共模数 ： N=P*Q N=3*11
> 
> 欧拉函数φ(N) = (P-1)(Q-1) ：φ(N)=2*10=20
> 
> 计算公钥1<E<φ(N) ： E可选 {3, 7, 9, 11, 13, 17, 19} E=3
> 
> 计算私钥E * D % φ(N) = 1 ：  3 * D  % 20 = 1   D=7
> 
> 加密C=M E mod N：C = 23 % 33 = 8
> 
> 解密M ＝C D mod N：M = 87 % 33

# 论文 #
- 视觉加密 ：看不懂看不懂看不懂！！！


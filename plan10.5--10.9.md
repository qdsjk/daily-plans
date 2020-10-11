# 单词 # 
- 10.5  150
- 10.6  150
- 10.7  150
- 10.8  6级没有报上。不想背单词了
#  leetcode#
- 104.二叉树的最大深度 深度优先用递归，广度优先用队列 [https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/](https://leetcode-cn.com/problems/maximum-depth-of-binary-tree/ "二叉树的最大深度")  二叉树的最大深度，还是用递归，也可以用层序遍历（不会声明队列）又重新看看了关于队列的知识点。 Queue<TreeNode> queue = new LinkedList<TreeNode>();链式队列


- 110 平衡二叉树 [https://leetcode-cn.com/problems/balanced-binary-tree/](https://leetcode-cn.com/problems/balanced-binary-tree/ "110. 平衡二叉树") 

> 自顶向下递归(类似先序）：遍历树的整个节点，如当前节点是根节点，先计算左右子树树高判断是否为平衡二叉树，然后递归计算左右子树的所有节点的子树是否AVL树。return Math.abs(height(root.left) - height(root.right)) <= 1 && isBalanced(root.left) && isBalanced(root.right);(判断参数的节点是否为空，否则报空指针错误）
> 
> 自底向上(类似后序）：对于当前遍历到的节点，先递归地判断其左右子树是否平衡，再判断以当前节点为根的子树是否平衡。如果一棵子树是平衡的，则返回其高度（高度一定是非负整数），否则返回 −1。如果存在一棵子树不平衡，则整个二叉树一定不平衡。



# 作业 #
- AES的使用，自己照着博客敲了一遍，出问题。最后发现是main函数要throws Exception,百度后main函数抛出异常由JVM进行处理异常。属于检查异常类，看了一篇知乎[https://zhuanlan.zhihu.com/p/93836930](https://zhuanlan.zhihu.com/p/93836930)对异常有了大概的了解
#  java#
- 引用类型  
MyDate today;          //将变量分配一个保存引用的空间
today = new MyDate();     // 这句话是2步，首先执行new MyDate（），给today变量开辟数据空间，然后再执行赋值操作

- 实例变量

> 当一个对象被实例化之后，每个实例变量的值就跟着确定；
> 
> 实例变量在对象创建的时候创建，在对象被销毁的时候销毁；
> 
> 实例变量的值应该至少被一个方法、构造方法或者语句块引用，使得外部能够通过这些方式获取实例变量信息；
> 实例变量可以声明在使用前或者使用后；
> 
> 访问修饰符可以修饰实例变量；
> 实例变量对于类中的方法、构造方法或者语句块是可见的。一般情况下应该把实例变量设为私有。通过使用访问修饰符可以使实例变量对子类可见；
> 
> 实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。
> 
> 变量的值可以在声明时指定，也可以在构造方法中指定；
> 
> 实例变量可以直接通过变量名访问。但在静态方法以及其他类中，就应该使用完全限定名：ObejectReference.VariableName。

- 类变量（静态变量）

> 类变量也称为静态变量，在类中以 static 关键字声明，但必须在方法之外。
> 
> 无论一个类创建了多少个对象，类只拥有类变量的一份拷贝。
> 
> 静态变量除了被声明为常量外很少使用，静态变量是指声明为 public/private，final 和 static 类型的变量。静态变量初始化后不可改变。
> 
> 静态变量在第一次被访问时创建，在程序结束时销毁。
> 
> 与实例变量具有相似的可见性。但为了对类的使用者可见，大多数静态变量声明为public类型。
> 
> 默认值和实例变量相似。数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null。变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静态变量还可以在静态语句块中初始化。
> 
> 静态变量可以通过：ClassName.VariableName的方式访问。


- Scanner 类 next() 与 nextLine() 区别

> next():一定要读取到有效字符后才可以结束输入。对输入有效字符之前遇到的空白，next() 方法会自动将其去掉。next() 不能得到带有空格的字符串。

> nextLine()：以Enter为结束符,也就是说 nextLine()方法返回的是输入回车之前的所有字符。可以获得空白。

-  StringBuffer 和 StringBuilder 类
> String 长度大小不可变
> 
> StringBuffer 和 StringBuilder 长度可变
> 
> StringBuffer 线程安全 StringBuilder 线程不安全
> 
> StringBuilder 速度快
> 
> stringbuffer 基本没有适用场景，你应该在所有的情况下选择使用 stringbuiler，除非你真的遇到了一个需要线程安全的场景

- SimpleDateFormat 格式化日期
>  Date dNow = new Date( );   SimpleDateFormat ft = new SimpleDateFormat ("yyyy-MM-dd hh:mm:ss");

- Calendar类 获取日期数据的特定部分
> Calendar c = Calendar.getInstance();//默认是当前日期 
c1.set(2009, 6 - 1, 12);

<p align="center">
<img alt="AndroidInterviewQuestions" src="https://github.com/stormzhang/android-interview-questions-cn/blob/master/assets/android-interview-questions.png?raw=true">
</p>

# Android 面试指南

### 关于

本项目 Fork 自 [stormzhang](http://stormzhang.com) 的 [android-interview-questions-cn](https://github.com/stormzhang/android-interview-questions-cn) 项目，为个人对这些问题的答案整理，该项目最新进展还请至原项目查看。

## Contents

 * [数据结构和算法](#数据结构与算法)
 * [Java 核心](#java-核心)
 * [Android 核心](#android-核心)
 * [架构](#架构)
 * [设计问题](#设计问题)
 * [工具和技能](#工具和技能)
 * [Android 测试驱动开发](#android-测试驱动开发)
 * [其他](#其他)


### 数据结构与算法

> 数据结构与算法问题的难度完全取决于你所申请的公司

* 数组
    - 数组由一组相同的数据类型组成。它存储在连续的内存空间内，使用索引可以找到元素的地址。数组包括一维数组和多维数组,一维数组是最简单的数据结构,也是最常用的。

        | 算法 | 平均 | 最坏 |
        |:-------------:|:-----:|:-----:|
        | 空间（Space）  | O(n)  | O(n)  |    
        | 查找（Search） | O(n)  | O(n)  |
        | 插入（Insert） | O(n)  | O(n)  |
        | 删除（Delete） | O(n)  | O(n)  |

* 链表
   - 链表看起来更像树，而不是数组，它使用一组结点来表示一个序列。每一个结点都包含数据和一个指针。在链表中，结点中的数据可以为任意类型，而指针则是指向下一结点的引用。链表包含一个头结点和一个尾结点。头结点是链表中的第一个结点，尾结点是最后一个结点。链表不是一个循环数据结构，所以尾结点没有指向头结点的指针，指针为空。一些基础方法的时间复杂度如下：

        | 算法          | 平均 | 最坏  |
        |:------------:|:----:|:----:|
        | 空间 (Space)  | O(n) | O(n) |
        | 查找 (Search) | O(n) | O(n) |
        | 插入 (Insert) | O(1) | O(1) |
        | 删除 (Delete) | O(1) | O(1) |

* 双向链表
   - 一个双向链表首先是一个链表，但是在每个结点中有两个指针，前驱指针指向前驱结点，后继指针指向后继结点。双向链表也有一个头结点，头结点的后继指针指向第一个结点。最后一个结点的后继指针指向空，但是如果最后一个结点的后继指针指向第一个结点，这时称这个链表为双向循环链表。双向循环链表能非常方便地从每个结点查找它的前驱结点和后继结点。

       ![双向链表](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5e/Doubly-linked-list.svg/610px-Doubly-linked-list.svg.png)
            
        | 算法          | 平均 | 最坏  |
        |:------------:|:----:|:----:|
        | 空间 (Space)  | O(n) | O(n) |
        | 查找 (Search) | O(n) | O(n) |
        | 插入 (Insert) | O(1) | O(1) |
        | 删除 (Delete) | O(1) | O(1) |

* 栈
    - 栈是一个有着「后进先出」特性的基础数据结构，这就意味着最后一个入栈的元素，也是第一个出栈的。栈就像是一堆书，想要得到书堆中的第一本书（最下面一本），必须把其他的书都先拿走。向栈中添加一个元素的操作被称为 Push（入栈），删除一个元素的操作被称为 Pop（出栈），查看且不删除最后一个入栈的元素的操作被称为 Top 。[实现栈的常用方法是使用链表（LinkedList），也可以使用不允许空值的 StackArray（使用数组实现），还有允许空值的 Vector](https://en.wikibooks.org/wiki/Data_Structures/Stacks_and_Queues#Performance_Analysis)

        <table>
            <tr>
                <th>算法</th>
                <th>平均</th>
                <th>最坏</th>
                <th>图形表示</th>
            </tr>
            <tr>
                <td>空间 (Space)</td>
                <td>O(n)</td>
                <td>O(n)</td>
                <td rowspan="5">
                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/29/Data_stack.svg/250px-Data_stack.svg.png"/>
                </td>
            </tr>
            <tr>
                <td>查找 (Search)</td>
                <td>O(n)</td>
                <td>O(n)</td>
            </tr>
            <tr>
                <td>入栈 (Push)</td>
                <td>O(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
                <td>出栈 (Pop)</td>
                <td>O(1)</td>
                <td>O(1)</td>
            </tr>
            <tr>
              <td>查看栈顶 (Top)</td>
              <td>O(1)</td>
              <td>O(1)</td>
            </tr>
        </table>

* 队列

* 优先队列

* 动态编程

* 字符串操作

* 二叉树

* 二叉搜索树

* 排序算法

* 哈希表与哈希图

* 广度优先搜索

* 深度优先搜索

* 贪心算法


### Java 核心

- 解释一下 OOP（Object-oriented programming） 的概念

	从对象和三大特性方面来讲：
  - 万物皆对象，对象是程序的基本单元
  - 类的定义包含数据的形式以及对数据的操作，对象是类的实例
  - 每个对象都有自己的空间，可以容纳其他对象
  - 面向对象编程三大特性：封装、继承、多态
  - 封装隐藏了类的内部实现机制，可以在不影响使用的情况下改变类的内部结构，同时也保护了数据
  - 继承可以重用父类代码，达到代码复用和可扩展的效果
  - 多态就是父类引用可以持有子类对象。非静态成员方法的调用：编译时看父类，运行时看子类
  - 多态优点：不用创建一堆子类对象的引用
  - 多态缺点：不能使用子类特有的成员属性和子类特有的成员方法

- 抽象类和接口的区别？[Link](https://arjun-sna.github.io/java/2017/02/02/abstractvsinterface/)

  - 抽象类可同时包含具体方法和抽象方法(方法未被实现)。
  - 抽象方法必须被该抽象类的子类实现。抽象类是可以继承的。
  - 接口像是描述类的一张蓝图或者说是类的一种契约，它包含了许多空方法，代表着它的所有的子类都应该拥有共同点。它的子类应该提供这些空方法的具体实现。
  - 一个类需要用 `implements` 来实现接口，接口可以用 `extends` 来继承其他接口。
  - 一个接口可以继承多个父接口，一个抽象类只可以继承一个父类

- 序列化是什么?如何实现它?

  - 序列化是一种将对象转换为字节流的过程，目的是为了将该对象存储到内存中，等后面再次构建该对象时可以获取到该对象先前的状态及数据信息。
  - Java 中，有两种方式可以实现序列化，既可以实现 Serializable 接口，也可以实现 Parcelable 接口。
  - 然而，在 Android 中，我们不应该使用 Serializable 接口。因为 Serializable 接口使用了反射机制，这个过程相对缓慢，而且往往会产生出很多临时对象，这样可能会触发垃圾回收器频繁地进行垃圾回收。相比而言，Parcelable 接口比 Serializable 接口效率更高，性能方面要高出 10x 多倍。

- 什么是单例？[几种写法](http://wuchong.me/blog/2014/08/28/how-to-correctly-write-singleton-pattern/)

  - 单例模式是一种对象创建型模式，指的是一个类只能被初始化一次，即只有一个实例。
  - 这个类只能有一个实例
  - 它必须自行创建这个实例
  - 它必须自行向整个系统提供这个实例

- 什么是匿名内部类？

	* 匿名内部类即没有名字的内部类，只可被使用一次
	* 使用匿名内部类前提条件：必须继承自一个父类或实现一个接口
	* 语法格式为 new SuperType(construction parameters){}
	* 语法格式为 new 父类构造器(参数列表)|实现接口(){}
	* 直接将抽象类的方法或者接口方法在大括号中实现，可以省略一个类的书写
	* 匿名内部类中不能定义构造方法，但可以使用初始化语块代替构造方法

- 对字符串进行 `==` 和 `equals()` 操作时有什么区别？

	* == 用来判断内存地址是否相同
	* equals()用来判断字符串的内容是否相同

- `hashCode()` 和 `equals()` 何时使用？

	* 相等（相同）的对象必须具有相等的哈希码（或者散列码）
	* 如果两个对象的 hashCode 相同，它们并不一定相同

	* 往 Set 集合中添加元素时，要保证元素不重复，先调用该元素的 hasCode 方法，定位到它应该放置的物理位置。 如果这个位置上没有元素，就可以直接存储在这个位置上，不用再进行任何比较；如果这个位置上已经有元素了，就调用它的 equals 方法与新元素进行比较，相同的话就不存了，不相同就散列其它的地址。
	* 集合查找时，hashcode 能大大降低对象比较次数，提高查找效率

- Java 中的 `final`, `finally` 和 `finalize`?

	* final：修饰基本数据类型时，代表常量（不可修改）；修饰类或对象引用时，引用不可重新赋值，而类或者对象依然可以修改；修饰方法时，代表该方法不可被重写；修饰类时，代表该类不可被继承
	* finally：异常处理时 try／catch／finally 语句中的 finally 语句块无论有没有异常都会执行 finally 语句块，当然也有特殊情况不执行 finally
	* finalize：垃圾回收器要回收对象的时候，首先会调用这个类的 finalize 方法，可以在该方法中释放调用本地方法时分配的内存

- 什么是内存泄露，Java 是如何处理它的？

	* 存在下面的这种对象，这些对象不会被 GC 回收，却占用着内存，即为内存泄漏（简单说：存在已申请的无用内存无法被回收）

		* 该对象是可达的，即还在被引用着
		* 该对象是无用的，即程序以后不会再使用该对象

	* 长生命周期的对象持有短生命周期的引用，就很可能会出现内存泄露


- 垃圾收集器是什么?它是如何工作的

	* 垃圾收集是一种自动的内存管理机制

  - 所有的对象实例都在 JVM 管理的堆区域分配内存
  - 只要对象被引用，JVM 就会认为它还存活于进程中
  - 一旦对象不再被引用，垃圾收集器将删除它并重新声明为未使用的内存

- 比较 `Array` 和 `ArrayList`[链接](http://blog.qianlicao.cn/translate/2016/03/09/array-vs-arraylist/)

	不同点：

	* 实现上：Array 是本地的程序设计组件或者数据结构，ArrayList 是一个 Java 集合类的类
	* 性能上：Array 会优于 ArrayList
	* 类型安全方面：ArrayList 是类型安全的，支持编译时检查；Array 不是类型安全的，支持运行时检查
	* 灵活性：ArrayList 优于 Array，ArrayList 是动态的；Array 是静态的，创建了数组就无法更改它的大小
	* 基本类型：Array 既可以保存基本类型，也可以保存对象；ArrayList 不可以保存基本类型，可以保存封装类
	* 泛型：ArrayList 可以显示的支持泛型，Array 不可以
	* 维度：Array 可以是多维度的，ArrayList 并不支持指定维度

	相同点：
	
	* 数据结构：都是基于 index 的数据结构
	* 空值：都可以存储空值（null），但只有 Object 的数组可以这样，基本类型会存储他们的默认值
	* 重复：都允许元素重复

- 比较 `HashSet` 和 `TreeSet`

	* TreeSet 会自动按自然排序法给元素排序，HashSet 不会
	* 如果不需要使用排序功能,应该使用 HashSet,因为其性能优于 TreeSet
	* 如果 TreeSet 传入的是自定义的对象,必须让该对象实现 Comparable 接口

- Java 中的类型转换
	Java 中的类型转换分为基本数据类型和引用数据类型
	
	* 基本数据类型

		基本数据类型的转换分为自动转换和强制转换
		
		* 自动转换是从位数低的类型向位数高的类型转换
		* 强制类型转是从位数高的类型向位数低的类型转换，需要转型的数据前加上“()”，然后在括号内加入需要转化的数据类型，转换会导致精度丢失

	* 引用数据类型

		* 子类可以转换成父类
		* 父类转换为子类不一定可行：当父类（引用）引用的为子类对象时，此时父类可以正常转换为子类；而当父类（引用）引用的确实为父类对象时，此时无法转换为子类，会抛出 ClassCastException 异常

- 方法重载和重写的区别[链接](http://droidyue.com/blog/2014/12/28/static-biding-and-dynamic-binding-in-java/index.html)

  ![](https://github.com/stormzhang/android-interview-questions-cn/blob/master/assets/overloading-vs-overriding.png)
  
  * 重载是在同一个类中完成的，重写父类需要有子类。
  * 方法重载时返回值类型、参数列表可以不同；方法重写时返回值类型、参数列表必须相同
  * 重载的方法使用静态绑定完成，发生在编译时；重写的方法使用动态绑定完成，发生在运行时。性能：重载比重写更有效率

  
  * 静态方法可以重载，意味着一个类可以有多个同名的静态方法。静态方法不能被重写，即使在子类中声明了一个相同的静态方法，它与父类的相同方法无关
  * 私有方法和用 `final` 修饰的方法可以重载但不可重写。意味着一个类可以有多个同名的 `private/final` 方法，子类不能重写父类的 `private/final` 方法。

- 什么是访问修饰符？它们能做什么？

	* 访问修饰符是指能够控制类、成员变量、方法的使用权限的关键字
	* 可以使用它们来保护对类、变量、方法和构造方法的访问
	* public：共有的，对所有类可见
	* protected：受保护的，对同一包内的类和所有子类可见
	* private：私有的，在同一类内可见
	* 默认：在同一包内可见。默认不使用任何修饰符。

- 接口可以继承另一个接口吗？

	可以，Java 允许一个接口继承多个父接口。

- Java 中 `static` 关键字是什么意思？[链接](http://www.cnblogs.com/chenssy/p/3386721.html)

	* static 表示“全局”或者“静态”的意思，用来修饰成员变量和成员方法，也可以修饰代码块

	* static 所蕴含“静态”的概念表示着它是不可恢复的，即在那个地方，你修改了，他是不会变回原样的，你清理了，他就不会回来了
	* 被 static 修饰的成员变量和成员方法是独立于该类的，它不依赖于某个特定的实例变量，也就是说它被该类的所有实例共享
	* 所有实例的引用都指向同一个地方，任何一个实例对其的修改都会导致其他实例的变化
	* 静态变量是随着类加载时被完成初始化的；静态方法也是类加载时就存在了，所以不可为 abstract，必须实现；静态代码块也会随着类的加载一块执行

- Java 中静态方法可以被重写吗？

	* 不可以被重写，静态方法隶属于某个类，只和类相关

- 什么是多态？什么是继承？[链接](http://www.cnblogs.com/chenssy/p/3354884.html)
	
	多态：
	
	- 多态就是父类引用可以持有子类对象。非静态成员方法的调用：编译时看父类，运行时看子类
	- 多态优点：不用创建一堆子类对象的引用
	- 多态缺点：不能使用子类特有的成员属性和子类特有的成员方法

	继承：
	
	* 继承是使用已存在的类的定义作为基础建立新类的技术，新类的定义可以增加新的数据或新的功能，也可以用父类的功能，但不能选择性地继承父类
	* 通过使用继承我们能够非常方便地复用以前的代码，大大提高开发的效率

- `Integer` 和 `int` 之间的区别[自动装箱、自动拆箱](http://droidyue.com/blog/2015/04/07/autoboxing-and-autounboxing-in-java/index.html)

	* int 是基本数据类型，Integer 是包装类
	* Java中，会对 -128 到 127 的 Integer 对象进行缓存，当创建新的 Integer 对象时，如果符合这个这个范围，并且已有存在的相同值的对象，则返回这个对象，否则创建新的 Integer 对象

- Java 中的对象是否会以引用传递或者值传递？详细说明。

- 什么是 ThreadPoolExecutor？ [Link](https://blog.mindorks.com/threadpoolexecutor-in-android-8e9d22330ee3)

	* 线程池的目的是实现线程复用，减少频繁创建和销毁线程，提高系统性能
	* ThreadPoolExecutor 是线程池的核心类，用于创建线程池

- 本地变量、实例变量以及类变量之间的区别？

	* 类体由两部分组成，变量定义和方法定义
	* 本地变量即局部变量，定义在方法内部或者方法的行参中
	* 实例变量为为非静态变量，每一个对象的实例变量都不同
	* 类变量为静态变量，属于类所有

- 什么是反射？ [Link](http://tutorials.jenkov.com/java-reflection/index.html)

- 在 Java 中什么是强引用、软引用、弱引用以及虚引用？[参考链接](http://blog.csdn.net/mazhimazh/article/details/19752475)

	* 强引用：是使用最普遍的引用。如果一个对象具有强引用，那垃圾回收器绝不会回收它。
	* 软引用：如果一个对象只具有软引用，且内存空间足够，垃圾回收器就不会回收它；如果内存空间不足了，就会回收这些对象的内存。
	* 弱引用：只具有弱引用的对象拥有比软引用更短暂的生命周期，在垃圾回收器线程扫描它所管辖的内存区域的过程中，一旦发现了只具有弱引用的对象，不管当前内存空间足够与否，都会回收它的内存。不过，由于垃圾回收器是一个优先级很低的线程，因此不一定会很快发现那些只具有弱引用的对象。
	* 如果一个对象仅持有虚引用，那么它就和没有任何引用一样，在任何时候都可能被垃圾回收器回收。

- 什么是依赖注入？能说几个依赖注入的库么？你使用过哪些？

- 关键字 `synchronized` 的作用是什么？[参考链接](http://www.cnblogs.com/GnagWang/archive/2011/02/27/1966606.html#!comments)

	* 当它用来修饰一个方法或者一个代码块的时候，能够保证在同一时刻最多只有一个线程执行该段代码。
	* 当两个并发线程访问同一个对象 object 中的这个 synchronized(this) 同步代码块时，一个时间内只能有一个线程得到执行。另一个线程必须等待当前线程执行完这个代码块以后才能执行该代码块。
	* 然而，当一个线程访问 object 的一个 synchronized(this) 同步代码块时，另一个线程仍然可以访问该 object 中的非 synchronized(this) 同步代码块。
	* 尤其关键的是，当一个线程访问 object 的一个 synchronized(this) 同步代码块时，其他线程对 object 中 *所有其它 synchronized(this) 同步代码块* 的访问将被阻塞。
	* 上一个例子同样适用其它同步代码块。也就是说，当一个线程访问 object 的一个 synchronized(this) 同步代码块时，它就获得了这个 object 的对象锁。结果，其它线程对该 object 对象 *所有同步代码部分* 的访问都被暂时阻塞。

- 为什么说 `String` 不可变的？[参考链接](http://blog.csdn.net/zhangjg_blog/article/details/18319521)

	* 什么是不可变对象

		* 如果一个对象，在它创建完成之后，不能再改变它的状态，那么这个对象就是不可变的。
		* 不能改变状态的意思是，不能改变对象内的成员变量，包括基本数据类型的值不能改变，引用类型的变量不能指向其他的对象，引用类型指向的对象的状态也不能改变。


	* 在 Java 中 String 类其实就是对字符数组的封装
	* String 类中有一个 char 数组的 value 引用变量，value 指向真正的数组对象
	* JDK 1.6 及以前还有 offset 和 count 两个变量
	* 这三个变量都是 private final 的，即一旦这三个值被初始化，就不能再改变了
	* 但是可以通过反射改变 value 变量引用的对象，进而改变 String 对象

- 修饰符 `transient` 和 `volatile` 的作用是什么？

- `finalize()` 方法的作用是什么？

- 异常捕获中的 `try{} finally{}` 块儿是如何工作的?

- 对象的实例化和初始化之间的区别是什么?[参考链接](https://www.caoqq.net/java-class-initialization.html)

	* 初始化执行顺序：静态代码块 -> 构造代码块 -> 成员变量 -> 构造方法
	* 实例化执行顺序：构造代码块 -> 成员变量 -> 构造方法

- 静态块何时运行?[链接](http://www.jianshu.com/p/8a3d0699a923)

	* 静态块在 JVM 加载类时执行，仅执行一次
	* 一个类中可以有多个静态代码块
	* 类调用时，先执行静态代码块，然后才执行主函数
	* 执行静态代码块 -> 执行构造代码块 -> 执行构造函数
	* 静态代码块其实就是给类初始化的，而构造代码块是给对象初始化的
	* 静态代码块中的变量是局部变量，与普通函数中的局部变量性质没有区别

- 解释一下 Java 中的泛型?

	* 泛型即宽泛的数据类型
	* 

- `StringBuffer` 和`StringBuilder` 的区别在哪里?

- `StringBuilder` 是怎么避免不可变字符串分配的问题？

- 什么是自动装箱和拆箱？

	* 自动装箱就是 Java 自动将原始类型值转换成对应的对象，比如将 int 的变量转换成 Integer 对象
	* 反之将 Integer 对象自动转换成 int 类型值，这个过程叫做拆箱
	* 自动装箱时编译器调用 valueOf 将原始类型值转换成对象
	* 自动拆箱时，编译器通过调用类似 intValue(), doubleValue() 这类的方法将对象转换成原始类型值
	* 自动装箱、拆箱主要发生在
		* 赋值时
		* 方法调用时

- 枚举和迭代器有什么区别？

- Java 中 *fail-fast* 和 *fail-safe* 的区别？

- 什么是 Java 优先级队列？

- 什么是设计模式 [Link](https://github.com/iluwatar/java-design-patterns)


### Android 核心

* 阐述一下 Activity 的生命周期。

* 谈谈 Android 的四大组件。

* Service 与 IntentService 的区别。[Link](https://stackoverflow.com/a/15772151/5153275)

* Android 应用的结构是什么？

* Android 应用中如何保存数据。

* 如何在 Android 应用中执行耗时操作。

* 两个 Fragment 之间如何通信。

* 阐述一下 Android 的通知系统。

* 两个不同的 app 之间如何交互。

* 什么是 Fragment？

* 为什么建议只使用默认的构造方法来创建 Fragment？[Link](https://stackoverflow.com/a/16042750/2809326)

* 为什么 Bundle 被用来传递数据，为什么不能使用简单的 Map 数据结构？

* 阐述一下 Fragment 的生命周期。[Link](https://www.techsfo.com/blog/wp-content/uploads/2014/08/complete_android_fragment_lifecycle.png)

* 如何理解 Android 的 Dialog ？

* 解释下 Android 的 View 。

* 你能创建自定义 View 吗？具体是如何创建的？

* 什么是 ViewGroup ，它与 View 的区别在哪里？

* Fragment 和 Activity 有什么区别？它们之间又有什么关系？

* 谈谈 Serializable 接口和 Parcelable 接口的区别。在 Android 中最好使用哪种接口？

* Activity 的启动模式有哪些？[Link](https://blog.mindorks.com/android-activity-launchmode-explained-cbc6cf996802)

* 解释一下 Android 中的 Intent 。[Link](https://stackoverflow.com/questions/6578051/what-is-an-intent-in-android)

* 什么是隐式 Intent ？

* 什么是显式 Intent ？

* 解释一下 AsyncTask 。

* 如何理解 Android 中的广播。[Link](https://stackoverflow.com/questions/5296987/what-is-broadcastreceiver-and-when-we-use-it)

* 如何理解 Android 的 LocalBroadcastManager 。[Link](https://developer.android.com/reference/android/support/v4/content/LocalBroadcastManager.html)

* 什么是 JobScheduler ？[Link](http://www.vogella.com/tutorials/AndroidTaskScheduling/article.html)

* 什么是 DDMS ？你可以用它来做什么？

* 解释一下什么是 support libary ，以及为什么要引入 support library ？[Link](http://martiancraft.com/blog/2015/06/android-support-library/)

* 如何理解 Android 中的 ContentProvider 。它通常用来干什么？

* 什么是 Data Binding ？[Link](https://developer.android.com/topic/libraries/data-binding/index.html)

* Android 的核心组件具体都有什么？[Link](https://developer.android.com/topic/libraries/architecture/index.html)

* 什么是 ADB ？

* 什么是 ANR ？如何避免发生 ANR ？

* AndroidManifest.xml 是什么？

* 解释一下 broadcast 和 intent 在 app 内传递消息的工作流程。

* 当 Bitmap 占用较多内存时，你是怎么处理的？

* Android 应用有哪些不同的存储数据的方式？

* 什么是 Dalvik 虚拟机？

* AsyncTask 的生命周期和(它所属的) Activity 的生命周期有什么关系？这种关系可能会导致什么样的问题？ 如何避免这些问题发生？


* Intent filter 是用来做什么的？

* 什么是 Sticky Intent？[Link](http://www.androidinterview.com/what-is-a-sticky-intent/)

* 什么是 AIDL ？列举一下通过 AIDL 创建被绑定的服务（bounded service）的步骤。

* Android 的权限有多少个不同的保护等级？

* 在转屏时你如何保存 Activity 的状态？[Link](https://stackoverflow.com/questions/3915952/how-to-save-state-during-orientation-change-in-android-if-the-state-is-made-of-m)

* 相对布局和线性布局的区别。

* 如何实现 XML 命名空间？

* View.GONE 和 View.INVISIBLE 之间的区别。

* Bitmap 和 .9（nine-patch）图片之间有什么区别？

* 谈谈位图池。[Link](https://blog.mindorks.com/how-to-use-bitmap-pool-in-android-56c71a55533c)

* 在 Android 中如何避免内存泄漏？

* Android 桌面的小部件是什么？

* 什么是 AAPT ？

* 你是如何在 Android 应用程序中发现内存泄漏的？

* 你如何排查应用崩溃的原因？

* 为什么你应该避免在主线程上运行非用户界面相关的代码？

* 你是如何适配不同分辨率的手机的？

* 如何理解 Doze 模式。如何理解应用程序待机模式（App Standby）。

* 在 Android 中，你可以使用什么来进行后台操作?

* 什么是 ORM ？它是如何工作的？

* 什么是 Loader ？

* 什么是 NDK ，为什么它是有用的？

* 如何理解严格模式（StrictMode）。 [Link](https://blog.mindorks.com/use-strictmode-to-find-things-you-did-by-accident-in-android-development-4cf0e7c8d997)

* 什么是 Lint ？它的用途是什么？

* 什么是 SurfaceView ？

* ListView 和 RecyclerView 有什么区别？

* 什么是 ViewHolder 模式？为什么我们应该使用它？

* 什么是 PendingIntent ？

* 你能手动调用垃圾回收吗？

* 周期地更新页面的最好方式是什么？

* 有哪些类型的广播？

* 你开发过组件吗？请描述一下。[Link](https://blog.mindorks.com/android-widgets-ad3d166458d3)

* 如何理解上下文（Context）。怎么使用它？[Link](https://medium.com/p/understanding-context-in-android-application-330913e32514)

* 你知道什么是视图树(View Tree)吗？怎样优化它的深度？

* onTrimMemory() 方法是什么？

* Android 应用可以使用多进程吗？怎样使用？

* 内存溢出（OutOfMemory）是怎么发生的？

* 文本样式接口（Spannable）是什么？

* 什么是过度绘制（overdraw）？

* 什么是渲染脚本（renderscript）？[Link](https://blog.mindorks.com/comparing-android-ndk-and-renderscript-1a718c01f6fe)

* Dalvik 虚拟机模式和 ART（Android Runtime）虚拟机模式的区别。

* FlatBuffers 和 JSON 的区别。[Link](https://blog.mindorks.com/why-consider-flatbuffer-over-json-2e4aa8d4ed07)

* 谈谈 Android 的注解。[Link1](https://blog.mindorks.com/creating-custom-annotations-in-android-a855c5b43ed9), [Link2](https://blog.mindorks.com/improve-your-android-coding-through-annotations-26b3273c137a)

* 描述一下约束布局（Constraint Layout）。[Link](https://blog.mindorks.com/using-constraint-layout-in-android-531e68019cd)

* 阐述一下 Android 中的 HashMap , ArrayMap 和 SparseArray 。[Link](https://blog.mindorks.com/android-app-optimization-using-arraymap-and-sparsearray-f2b4e2e3dc47)

* 阐述一下 Looper, Handler 和 HandlerThread 。[Link](https://blog.mindorks.com/android-core-looper-handler-and-handlerthread-bd54d69fe91a)

* 如何降低 Android 应用的耗电量？[Link](https://blog.mindorks.com/battery-optimization-for-android-apps-f4ef6170ff70)

* SnapHelper 是什么？[Link](https://blog.mindorks.com/using-snaphelper-in-recyclerview-fc616b6833e8)

* 在 Android 中怎么处理多点触控？[link](https://arjun-sna.github.io/android/2016/07/20/multi-touch-android/)


### 架构

* 请介绍一下你做的上一个 App 的架构。

* 请介绍一下 MVP。 [Link](https://blog.mindorks.com/essential-guide-for-designing-your-android-app-architecture-mvp-part-1-74efaf1cda40)

* Presenter 是什么？

* 什么是模型？

* 请介绍一下 MVC。

* Controller 是什么？

* 请介绍一下 MVVM。 [Link](https://github.com/MindorksOpenSource/android-mvvm-architecture)

* 谈谈你对代码整洁之道（clean code）的理解。[Link](https://blog.mindorks.com/every-programmer-should-read-this-book-6755dedec78d)


### 设计问题

* 请设计 Uber App。

* 请设计 Facebook App。

* 请设计 Facebook Near-By Friends App。

* 请设计 WhatsApp。

* 请设计 SnapChat。

* 基于地理位置 App 的设计问题。


### 工具和技能

* Git. [Link](https://github.com/git-tips/tips)

* RxJava. [Link](https://blog.mindorks.com/a-complete-guide-to-learn-rxjava-b55c0cea3631)

* Dagger 2. [Link](https://medium.com/p/a-complete-guide-to-learn-dagger-2-b4c7a570d99c)

* Android 开发实用工具。 [Link](https://blog.mindorks.com/android-development-useful-tools-fd73283e82e3)

* Firebase. [Link](https://firebase.google.com/)


### Android 测试驱动开发

* Espresso 是什么？ [Link](https://developer.android.com/training/testing/ui-testing/espresso-testing.html)

* Robolectric 是什么？ [Link](http://robolectric.org/)

* UI-Automator 是什么？ [Link](https://developer.android.com/training/testing/ui-testing/uiautomator-testing.html)

* 请解释一下单元测试。

* 请解释一下设备化测试。

* 你是否做过单元测试或者自动测试？

* 为什么要使用 Mockito？ [Link](http://site.mockito.org/)

* 请描述一下 JUnit 测试。


### 其他

* 描述一下 REST APIs 如何工作 ？

* 描述一下 SQLite 。

* 描述一下 数据库 。

* 项目管理工具 - trello ，basecamp ，kanban ，jira ，asana 。

* 关于构建系统 - gradle , ant , buck 。

* APK 逆向工程 。

* 混淆器用于什么 ？

* 什么是混淆？ 用于什么？ 如何压缩 ？

* 如何构建你的发布版本的 APP ？

* 如何面向特定用户群体更新应用程序版本 ？

* 可以识别卸载我们的应用程序的用户吗 ？

* 缩小 APK 的体积 。[Link](https://blog.mindorks.com/how-to-reduce-apk-size-in-android-2f3713d2d662)

* Android 开发最佳实践 。[Link](https://blog.mindorks.com/android-development-best-practices-83c94b027fd3)

* Android 代码风格和指南 。[Link](https://blog.mindorks.com/android-code-style-and-guidelines-d5f80453d5c7)

* 你尝试使用过 Kotlin 吗 ？[Link](https://blog.mindorks.com/why-you-must-try-kotlin-for-android-development-e14d00c8084b)

* 开发 Android 应用程序时应该连续测量哪些指标 ？[Link](https://blog.mindorks.com/android-app-performance-metrics-a1176334186e)


### 贡献者

感谢这些无私的贡献者，排名不分先后。

[mengxn](https://github.com/mengxn)、[innovatorCL](https://github.com/innovatorCL)、[SmartNJ](https://github.com/SmartNJ)、[Zhiw](https://github.com/Zhiw)、[lanyuanxiaoyao](https://github.com/lanyuanxiaoyao)、[934079371](https://github.com/934079371)、[cdevelopr](https://github.com/cdevelopr)、[smartbeng](https://github.com/smartbeng)、[ikook](https://github.com/china-kook)、[mrfanr](https://github.com/mrfanr)、[androidZzT](https://github.com/androidZzT)、[qiaojialin](https://github.com/qiaojialin)、[maokai1229](https://github.com/maokai1229)、[renxuelong](https://github.com/renxuelong)、[dzx1994](https://github.com/dzx1994)


### License

```
   Copyright (C) 2017 stormzhang

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.
```

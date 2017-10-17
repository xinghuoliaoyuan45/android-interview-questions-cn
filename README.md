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
	* 内存泄漏可能的情况：

		* 静态集合类引起的
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

Java 中的对象以按值传递的形式进行调用，所有方法得到的都是参数值的拷贝
	
* 对于基本数据类型的参数，方法得到的是其值的拷贝
* 对于引用数据类型的参数，方法得到的也是其值（所指向对象的内存地址）的拷贝
* 方法均不可以修改参数变量的值，对于引用类型参数来说，就是不能让引用类型参数指向新的对象
* 但是方法可以修改引用类型参数所指向对象的内容，因为方法得到的是该对象地址的拷贝，可以根据地址获取到该对象

- 什么是 ThreadPoolExecutor？ [Link](https://blog.mindorks.com/threadpoolexecutor-in-android-8e9d22330ee3)

	* 线程池的目的是实现线程复用，减少频繁创建和销毁线程，提高系统性能
	* ThreadPoolExecutor 是线程池的核心类，用于创建线程池
	* ThreadPoolExecutor 的构造方法包括如下参数：

		* corePoolSize 核心线程池大小
		* maximumPoolSize 线程池最大容量
		* keepAliveTime 线程池空闲时，线程存活时间
		* TimeUnit 时间单位
		* ThreadFactory 线程工厂
		* BlockingQueue 任务队列
		* RejectedExecutionHandler 线程拒绝策略

- 本地变量、实例变量以及类变量之间的区别？

	* 类体由两部分组成，变量定义和方法定义
	* 本地变量即局部变量，定义在方法内部或者方法的形参中
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

- 对象的实例化和初始化之间的区别是什么?[参考链接1](https://www.caoqq.net/java-class-initialization.html)、[参考链接2](http://blog.csdn.net/czhpxl007/article/details/50558319)、[参考链接3](http://blog.csdn.net/justloveyou_/article/details/72466416)

	* 1.执行顺序不同：
	
		* 初始化执行顺序：静态成员变量／静态代码块 -> 成员变量／构造代码块  -> 构造方法
		* 实例化执行顺序：成员变量／构造代码块  -> 构造方法
		* 以上，静态成员变量／静态代码块的执行顺序为定义顺序，成员变量／构造代码块的执行顺序也为定义顺序
	
	* 2.执行时机不同
		
		类的初始化时机：
		
		* 类的一个实例被创建时
		* 类的一个静态方法被调用时
		* 类声明的一个静态变量被赋值时
		* 类声明的一个静态变量被使用且这个变量不是常量时
		* 一个类初始化时，如果父类没初始化则需要先初始化父类
	
		类的实例化时机
		
		* 当创建一个类的新的实例时（可以通过 new 关键字、反射机制、clone 方法、反序列化方式等）

- 静态块何时运行?[链接](http://www.jianshu.com/p/8a3d0699a923)

	* 静态块在 JVM 加载类时执行，仅执行一次
	* 一个类中可以有多个静态代码块
	* 类调用时，先执行静态代码块，然后才执行主函数
	* 执行静态代码块 -> 执行构造代码块 -> 执行构造函数
	* 静态代码块其实就是给类初始化的，而构造代码块是给对象初始化的
	* 静态代码块中的变量是局部变量，与普通函数中的局部变量性质没有区别

- 解释一下 Java 中的泛型?[参考链接](http://www.infoq.com/cn/articles/cf-java-generics)

	* 泛型即宽泛的数据类型
	* 允许在定义类和接口的时候使用类型参数（type parameter）
	* 声明的类型参数在使用时用具体的类型来替换
	* 使用泛型的时候加上的类型参数，会被编译器在编译的时候去掉，这个过程就称为类型擦除

- `String`、`StringBuffer` 和`StringBuilder` 的区别在哪里?

	* String 是不可变对象，因此每次对 String 对象进行更改时，都会生成一个新的对象，然后将指针指向新的对象。
	* 使用 StringBuffer 类时，每次都是对 StringBuffer 对象本身进行操作，并不是生成新的对象并改变引用。
	* StringBuilder 和 StringBuffer 非常类似，但是是非线程安全的，在单线程中性能比 StringBuffer 高

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

* 阐述一下 Activity 的生命周期。[参考链接](https://developer.android.com/guide/components/activities.html?hl=zh-cn)

	![](http://oj1xifth5.bkt.clouddn.com/activity_lifecycle.png)

	Activity 生命周期的顺序为：

	onCreate() -> onContentChanged() -> onStart() -> onPostCreate()-> onResume() -> onPostResume -> onPause() -> onStop() -> onDestroy()

	* onCreate() 方法：首次创建 Activity 时调用，应该在此方法中执行所有正常的静态设置 — 创建视图、将数据绑定到列表等等。
	* onRestart() 方法：在 Activity 已停止（调用 onStop()）并即将再次启动前调用，始终后接 onStart()
	* onStart() 方法：在 Activity 即将对用户可见之前调用，可后接 onStop()进入隐藏状态
	* onResume() 方法：在 Activity 即将开始与用户进行交互之前调用，始终后接 onPause()
	* onPause() 方法：当系统即将开始继续另一个 Activity 时调用。用于确认对持久性数据的未保存更改、停止动画以及其他可能消耗 CPU 的内容。应该非常迅速地执行所需操作，因为它返回后，下一个 Activity 才能继续执行。
	* onStop() 方法：在 Activity 对用户不再可见时调用。可后接 onRestart()。
	* onDestroy() 方法：在 Activity 被销毁前调用。

	方法调用后终止问题：

	* onCreate(),onRestart(),onStart(),onResume() 调用后，系统不能随时终止 Activity 进程。
	* 而 onPause(),onStop(),onDestroy() 调用后，可以终止。
	* Activity 创建后，onPause() 必定成为最后调用的方法，然后才能终止进程 — 如果系统在紧急情况下必须恢复内存，则可能不会调用 onStop() 和 onDestroy()。
	* 所以，在 onPause() 调用时，向存储设备写入至关重要的持久性数据（例如用户编辑）。
	* 不过，应该对 onPause() 调用期间必须保留的信息有所选择，因为该方法中的任何阻止过程都会妨碍向下一个 Activity 的转变并拖慢用户体验。

* 谈谈 Android 的四大组件。[参考链接1](http://wiki.xuchongyang.com/Android/%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86%E7%82%B9.html)、[参考链接2](http://www.cnblogs.com/bravestarrhu/archive/2012/05/02/2479461.html)

	四大组件：Activity、Service、BroadcastReceiver、ContentProvider
	
	* Activity：

		* 一个 Activity 通常就是一个单独的屏幕，它上面可以显示一些控件也可以监听并处理用户的事件做出响应
		* Activity 之间通过 Intent 进行通信，应用内使用显示 Intent，跨应用使用隐式 Intent
		* 在隐式 Intent 中，有三个最重要的部分：动作（Action）、类别（category）以及动作对应的数据（data）
		* Action、category 和 Uri 分别对应着 intent-filter 中的 action、category 和 data

	* Service：

		* Service 是实现程序后台运行的解决方案，非常适合去执行不需要和用户交互（即没有界面）并且还要求长期执行的任务
		* 通过 Context 的 startService 和 stopService 可以启动、停止服务，启动服务后启动者和服务就没有关系了，启动者结束生命周期，服务依然在
		* 通过 Context 的 bindService 和 unBindService 可以绑定、解绑服务，绑定服务后服务会返回给启动者一个 IBind 接口实例，启动者可以通过这个接口实例回调服务的方法。此时 Context 退出，服务也会跟着解绑退出

	* BroadcastReceiver：

		* 应用可以使用广播接收器对感兴趣的外部事件或内部事件进行注册监听，可以静态注册、动态注册
		* 广播接收器没有用户界面。但它们可以启动一个 Activity 或 Service 来响应它们收到的信息，或者用 NotificationManager 来通知用户
		* 广播分为普通广播、有序广播、粘性广播。注册有序广播接收器可以设定接收优先级按序接收或拦截；发送粘性广播后注册广播接收器也可以接收到该粘性广播

	* ContentProvider：可参考《第二行代码》Page 270

		* 内容提供器用于提供在不同程序之间实现数据共享的功能，允许一个程序访问另一个程序中的数据，同时还能保证被访数据的安全性
		* 每个 ContentProvider 都用一个 Uri 作为独立的标识

		* 访问其他程序中的数据

			* 可以通过 Context 的 getContentResolver 方法获取到 ContentResolver 的实例，通过该实例的一系列方法对目标数据进行 CRUD 操作
			* 通过内容 Uri 表明想要访问的目标程序

		* 创建自己的内容提供器

			* 继承 ContentProvider，实现抽象方法
			* 通过 UriMacther 类的 match 方法判断其他程序想要访问的数据地址

* Service 与 IntentService 的区别。[Link](https://stackoverflow.com/a/15772151/5153275)

	* 相同点：

		* 都是在后台运行，不可见
		* 都可在任何线程、系统组件进行开启

	* 不同点：

		* Service 默认运行在主线程，不可直接做耗时操作；
		* IntentService 默认运行在子线程，可直接执行耗时操作
		* Service 不会自动退出，需要手动 stopSelf、stopService 或者 unbindService；
		* IntentService onHandleIntent 方法执行完毕后会自动退出。当有多次请求（即多次调用 startService）时，因只有一个工作线程，所以会一个一个进行处理，处理完毕后退出

* Android 应用的结构是什么？

* Android 应用中如何保存数据。

	分为保存键值集、保存文件（分为内部存储和外部存储）、在 SQL 数据库中保存数据以及在网络中使用网络存储。
	
	其中：
	
	* 键值集中适合保存私有原始轻量化数据
	* 内部存储适合保存私有数据
	* 外部存储适合保存公共数据
	* 私有数据库中适合保存结构化数据
	* 网络存储需使用自己的网络服务器存储数据

* 如何在 Android 应用中执行耗时操作。

	将耗时操作放到非 UI 线程执行，常用的包括：AsyncTask、Handler、Thread 等。

* 两个 Fragment 之间如何通信。[参考链接](http://blog.csdn.net/u012702547/article/details/49786417)

	* 通过宿主 Activity 拿到 FragmentManager，进而再 findFragmentById 获取到另一个 Fragment
	* 使用接口：在一个 Fragment 中定义接口，并在 onAttach 方法中拿到 Activity 初始化接口对象。Activity 来实现该接口，并在实现中调用另一个 Fragment 的相应方法
	* 使用 Activity 的公共方法：直接 getActivity 并调用 Activity 的公共方法
	* 使用广播
	* 使用 EventBus
	* 使用 Fragment 的 setArguments？

* 阐述一下 Android 的通知系统。

* 两个不同的 app 之间如何交互。

* 什么是 Fragment？

	* 碎片是一种可以嵌入在活动中的 UI 片段
	* 可以将多个碎片组合在一个 Activity 中，也可以在多个 Activity 中重复使用一个碎片
	* 可以在 Activity 运行时动态添加、删除碎片
	* 可以把碎片当作 Activity 的模块化组成部分，具有自己的生命周期，能接收自己的输入事件

* 为什么建议只使用默认的构造方法来创建 Fragment？[Link](https://stackoverflow.com/a/16042750/2809326)

	* 应当使用默认构造方法创建 Fragment，然后使用 setArguments 添加 Bundle 来传递参数
	* 因为系统在储存 Fragment 的状态时（比如说屏幕旋转导致的重新加载），系统会为我们自动存储 Bundle

* 为什么 Bundle 被用来传递数据，为什么不能使用简单的 Map 数据结构？[链接1](https://github.com/android-cn/android-discuss/issues/142)，[链接2](http://www.codes51.com/article/detail_163576.html)，[链接3](http://droidyue.com/blog/2017/02/12/dive-into-arraymap-in-android/index.html)

	原因一：速度和内存占用问题
	
	* 使用 Bundle 传递数据一般用于启动 Activity，启动 Fragment 时，数据量一般都不大
	* Bundle 内部由 ArrayMap 实现。ArrayMap 的内部实现是两个数组，一个数组存放 key 的 hashCode 值，一个数组存放 key 与 value 值。在查找、添加、删除数据时，会根据二分查找法查找 key 的 hashCode 值所对应的 index 值，再根据 index 去查找 key 所对应的 value 值
	* HashMap 的实现则是采用数组加链表的结构，默认使用一个容量为 16 的数组来存储，数组中每一个元素又是一个链表的头节点
	* 所以在小数据量的情况下，ArrayMap（Bundle） 比 HashMap 在速度和内存上都更占优势
	
	原因二：序列化问题
	
	* Android 中使用 Intent 来传递数据时，需要保证数据是基本数据类型或可序列化类型
	* Bundle 使用 Parcelable 序列化，HashMap 使用 Serialable 序列化
	* 在 Android 中，更推荐使用 Parcelable 序列化，因为 Serializable 接口使用了反射机制，这个过程相对缓慢，而且往往会产生出很多临时对象，可能会触发垃圾回收器频繁地进行垃圾回收。相比而言，Parcelable 接口比 Serializable 接口效率更高，性能方面要高出 10x 多倍。

* 阐述一下 Fragment 的生命周期。[参考链接](https://developer.android.com/guide/components/fragments.html?hl=zh-cn)

	![](http://oj1pajfyu.bkt.clouddn.com/fragment_lifecycle.png)

	* Fragment 的生命周期与 Activity 的生命周期协调一致
	* Activity 的每次生命周期回调都会引发每个片段的类似回调
	* 片段还有几个额外的生命周期回调，用于处理与 Activity 的唯一交互，以执行构建和销毁片段 UI 等操作，包括：
		* onAttach：在片段已与 Activity 关联时调用
		* onCreateView：在这可创建片段的视图层次结构
		* onActivityCreated：在 Activity 的 onCreate() 方法已返回时调用
		* onDestroyView：在移除与片段关联的视图层次结构时调用
		* onDetach：在取消片段与 Activity 的关联时调用

	下图为 Activity 的每个连续状态如何决定片段可以收到的回调方法
	![](http://oj1pajfyu.bkt.clouddn.com/activity_fragment_lifecycle.png)

* 如何理解 Android 的 Dialog ？

* 解释下 Android 的 View 。

	* View 是 UI 组件最基本的构建块
	* 一个 View 占据屏幕的一块区域，负责绘制和事件处理

* 你能创建自定义 View 吗？具体是如何创建的？

* 什么是 ViewGroup ，它与 View 的区别在哪里？

	* ViewGroup 是一个放置 View 的容器，继承自 View，是一种特殊的 View
	* ViewGroup 的职能为：给 childView 计算出建议的宽、高和测量模式；决定 childView 的位置；
	* View 的职能为：根据测量模式和 ViewGroup 建议的宽高计算出自己的宽和高；在 ViewGroup 为其指定的区域内绘制自己的形态

* Fragment 和 Activity 有什么区别？它们之间又有什么关系？

* 谈谈 Serializable 接口和 Parcelable 接口的区别。在 Android 中最好使用哪种接口？

* Activity 的启动模式有哪些？[Link](https://blog.mindorks.com/android-activity-launchmode-explained-cbc6cf996802)

* 解释一下 Android 中的 Intent 。[Link](https://stackoverflow.com/questions/6578051/what-is-an-intent-in-android)

	* Intent 是一个消息传递对象，在启动其他应用组件时使用
	* 可以启动 Activity，启动 Service，发送广播
	* Intent 可以描述目标组件的一些特性，并可以携带一些必要数据

* 什么是隐式 Intent ？

	* 不指定特定的组件，而是声明要执行的常规操作（Action），从而允许其他应用中的组件来处理它
	* 如声明发送功能，那么拥有发送 Action 的组件都可进行响应

* 什么是显式 Intent ？

	* 按名称指定要启动的组件，完全限定类名
	* 通常会在自己的应用中使用显式 Intent 来启动组件，因为知道想要启动的 Activity 或服务的类名

* 解释一下 AsyncTask。[参考链接](http://markxu.coding.me/wiki/%E5%A4%9A%E7%BA%BF%E7%A8%8B/Android%E5%9F%BA%E7%A1%80%EF%BC%9AAsyncTask%E7%9A%84%E5%BA%94%E7%94%A8.html)

	* AsyncTask 是 Android 提供的一个助手类，对 Thread 和 Handler 进行了封装，方便我们在后台线程执行耗时操作，在主线程更新 UI 等
	* AsyncTask 有四个回调方法：onPreExecute、doInBackground、onProgressUpdate、onPostExecute。
		* onPreExecute 在执行后台操作之前调用，运行在主线程
		* doInBackground 是必须实现的一个核心方法，可以执行后台耗时操作，运行在自子线程
		* onProgressUpdate 在 doInBackground 方法中调用publishProgress 方法时会进行回调，可以进行后台操作状态的展示更新，运行在主线程
		* onPostExecute 在后台操作完成后调用，运行在主线程

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

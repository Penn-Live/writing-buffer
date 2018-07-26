- Switch能否用string做参数？ 

  *在 Java 7  之前, switch 只能支持byte,short,char,int 或者其对应的封装类以及 Enum 类型。在JAVA 7中,String 支持被加上了。* 

- ”static”关键字是什么意思？Java中是否可以覆盖(override)一个private或者是static的方法？ 

  *“static”关键字表明一个成员变量或者是成员方法可以在没有所属的类的实例变量的情况下被访问。*

  *Java中static方法不能被覆盖，因为方法覆盖是基于运行时动态绑定的，而static方法是编译时静态绑定的。static方法跟类的任何实例都不相关，所以概念上不适用。*

  *java中也不可以覆盖private的方法，因为private修饰的变量和方法只能在当前类中使用，如果是其他的类继承当前类是不能访问到private变量或方法的，当然也不能覆盖。*

- 什么是值传递和引用传递？ 

  *值传递是对基本型变量而言的,传递的是该变量的一个副本,改变副本不影响原变量.*

  *引用传递一般是对于对象型变量而言的,传递的是该对象地址的一个副本, 并不是原对象本身 。*

  *一般认为,java内的基础类型数据传递都是值传递. java中实例对象的传递是引用传递*

- 为什么集合类没有实现Cloneable和Serializable接口？ 

  *克隆(cloning)或者是序列化(serialization)的语义和含义是跟具体的实现相关的。因此，应该由集合类的具体实现来决定如何被克隆或者是序列化。* 

- hashCode()和equals()方法的重要性体现在什么地方？ 

  *Java中的HashMap使用hashCode()和equals()方法来确定键值对的索引，当根据键获取值的时候也会用到这两个方法。如果没有正确的实现这两个方法，两个不同的键可能会有相同的hash值，因此，可能会被集合认为是相等的。而且，这两个方法也用来发现重复元素。所以这两个方法的实现对HashMap的精确性和正确性是至关重要的。* 

- HashMap和Hashtable有什么区别？ 

  *HashMap和Hashtable都实现了Map接口，因此很多特性非常相似。但是，他们有以下不同点： HashMap允许键和值是null，而Hashtable不允许键或者值是null。 Hashtable是同步的，而HashMap不是。因此，HashMap更适合于单线程环境，而Hashtable适合于多线程环境。 HashMap提供了可供应用迭代的键的集合，因此，HashMap是快速失败的。另一方面，Hashtable提供了对键的列举(Enumeration)。 一般认为Hashtable是一个遗留的类。*

- 数组(Array)和列表(ArrayList)有什么区别？什么时候应该使用Array而不是ArrayList？ 

  *下面列出了Array和ArrayList的不同点： Array可以包含基本类型和对象类型，ArrayList只能包含对象类型。 Array大小是固定的，ArrayList的大小是动态变化的。 ArrayList提供了更多的方法和特性，比如：addAll()，removeAll()，iterator()等等。 对于基本类型数据，集合使用自动装箱来减少编码工作量。但是，当处理固定大小的基本数据类型的时候，这种方式相对比较慢。*

- 什么是Java优先级队列(Priority Queue)？ 

  *PriorityQueue是一个基于优先级堆的无界队列，它的元素是按照自然顺序(natural order)排序的。在创建的时候，我们可以给它提供一个负责给元素排序的比较器。PriorityQueue不允许null值，因为他们没有自然顺序，或者说他们没有任何的相关联的比较器。最后，PriorityQueue不是线程安全的，入队和出队的时间复杂度是O(log(n))。* 

- 如何权衡是使用无序的数组还是有序的数组？ 

  *有序数组最大的好处在于查找的时间复杂度是O(log n)，而无序数组是O(n)。有序数组的缺点是插入操作的时间复杂度是O(n)，因为值大的元素需要往后移动来给新元素腾位置。相反，无序数组的插入时间复杂度是常量O(1)。* 

- Enumeration接口和Iterator接口的区别有哪些？ 

  *Enumeration速度是Iterator的2倍，同时占用更少的内存。但是，Iterator远远比Enumeration安全，因为其他线程不能够修改正在被iterator遍历的集合里面的对象。同时，Iterator允许调用者删除底层集合里面的元素，这对Enumeration来说是不可能的。* 

- Java中Exception和Error有什么区别？ 

  *Exception和Error都是Throwable的子类。Exception用于用户程序可以捕获的异常情况。Error定义了不期望被用户程序捕获的异常。* 

- throw和throws有什么区别？ 

  *throw关键字用来在程序中明确的抛出异常，相反，throws语句用来表明方法不能处理的异常。每一个方法都必须要指定哪些异常不能处理，所以方法的调用者才能够确保处理可能发生的异常，多个异常是用逗号分隔的。*  

- 解释下Serialization和Deserialization。 

  *Java提供了一种叫做对象序列化的机制，他把对象表示成一连串的字节，里面包含了对象的数据，对象的类型信息，对象内部的数据的类型信息等等。因此，序列化可以看成是为了把对象存储在磁盘上或者是从磁盘上读出来并重建对象而把对象扁平化的一种方式。反序列化是把对象从扁平状态转化成活动对象的相反的步骤。* 

- 

   
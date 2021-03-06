# java基础

#### 1. jdk和jre有什么区别？

JDK是 Java 语言的软件开发工具包，它包含了JAVA的运行环境（JVM+Java系统类库）和JAVA工具。
JDK包含的基本组件包括：

1. javac – 编译器，将源程序转成字节码

2. jar – 打包工具，将相关的类文件打包成一个文件

3. javadoc – 文档生成器，从源码注释中提取文档

4. jdb – debugger，查错工具

5. java – 运行编译后的java程序（.class后缀的）

JRE是Java Runtime Environment缩写，指Java运行环境，是Sun的产品。运行JAVA程序所必须的环境的集合，包含JVM标准实现及Java核心类库。

#### 2.==和equals区别

- 基本数据类型 ：byte,short,char,int,long,float,double,boolean。他们之间的比较，应用双等号（==）,比较的是他们的值。
- 引用数据类型：当他们用（==）进行比较的时候，比较的是他们在内存中的存放地址（确切的说，是**堆内存**地址）。

注：对于第二种类型，除非是同一个new出来的对象，他们的比较后的结果为true，否则比较后结果为false。因为每new一次，都会重新开辟堆内存空间。

#### 3.集合底层实现

##### **ArrayList底层实现方式**

ArrayList的底层数据结构就是一个数组，数组元素的类型为Object类型，对ArrayList的所有操作底层都是基于数组的。

##### **LinkedList底层实现方式**

LinkedList是通过双向链表去实现的，既然是链表实现那么它的随机访问效率比ArrayList要低，顺序访问的效率要比较的高。每个节点都有一个前驱（之前前面节点的指针）和一个后继（指向后面节点的指针）

##### **HashMap底层实现方式**

HashMap采用Entry数组来存储key-value对，每一个键值对组成了一个Entry实体，Entry类实际上是一个单向的链表结构，它具有Next指针，可以连接下一个Entry实体，以此来解决Hash冲突的问题。


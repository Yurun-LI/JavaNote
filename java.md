# Java

## 第一章	综述

### Key points

- 数据结构和算法的作用
- 数据结构的概述
- 算法的概述
- 定义
- 面向对象编程
- 软件工程
- 对于C++程序员的Java
- Java数据结构的类库

### 数据结构和算法能起到什么作用?

- 现实世界数据储存

- 程序员工具

- 建模

  

**数据结构**:	对在计算机内存中(有时在磁盘中)的数据的一种安排.

**数据结构**包含:

- 数组
- 链表
- 栈
- 二叉树
- 哈希表
- ...

### **数据结构的概述**

<img src="/Users/liyurun/Library/Application Support/typora-user-images/image-20201204201442991.png" alt="image-20201204201442991" style="zoom:33%;" />

<img src="/Users/liyurun/Library/Application Support/typora-user-images/image-20201204201715108.png" alt="image-20201204201715108" style="zoom:33%;" />

### 算法的概述

三目标:

- 插入一条新数据
- 寻找特定数据
- 删除特定数据

### 一些定义

数据库(database)

记录(record)

字段(field)

关键字

### 面向对象编程

#### 对象简述

对象:一个对象包括==方法==和==字段(数据)==.对象的出现,将计算机中的事物和现实世界的事物联系的更为紧密,而且解决了在过程语言中由全局变量造成的麻烦.

类:任意数目的对象的说明.

创建对象:使用关键词(new)和类的名称连用.

访问对象方法:声明一个类并创建了几个对象后,程序就有可能需要让这些对象相互作用.点运算(.)将一个对象同它的某一个方法(或有时同它的某个字段)连接起来.

#### 一个能运行的面向对象的程序

<img src="/Users/liyurun/Library/Application Support/typora-user-images/image-20201205001130826.png" alt="image-20201205001130826" style="zoom:33%;" />

<img src="/Users/liyurun/Library/Application Support/typora-user-images/image-20201205001224239.png" alt="image-20201205001224239" style="zoom:33%;" />

**BankApp类**:主类,可以理解为main()函数.

**BankAccount**:子类,包括银行账号的字段和方法.

- 字段: balance
- 方法: deposit() & withdrawal() & display()
- 构造函数: BankAccount()

**公有和私有**: public & private

通常一个类中数据字段经常被设为私有,而方法经常是公有的.这样可以保护数据,是指不会被其他类的方法所修改.所有外界的实体要想访问同一个类中的数据,必须使用那个类自己的方法.

#### 继承与多态

**继承**: 由基类拓展或派生形成一个新类,这个拓展类拥有基类的所有属性,并加上几种其他属性.

**多态**: 以相同的办法处理来自不同类的对象.

### 软件工程

软件工程研究的是由许多程序员参与的大型复杂的计算机程序的创建方法.其强调的是程序的整体设计和如何依照最终用户需求而进行设计的问题.软件工程关系着一个软件项目的整个生命周期,包括分析,设计,验证,编码,测试,生产和维护各阶段.

### 对于C++程序员的Java

- 最大不同就是==Java没有指针==

- 与C++用整数类型来表示真/假不同,Java中的boolean是一个独立的类型.

- ==int==大小永远是**32位**
- ==float型变量==(3.14159**F**)
- ==double型变量==无后缀
- ==long型变量==(45**L**)
- etc.

##### **基本变量类型**

<img src="/Users/liyurun/Library/Application Support/typora-user-images/image-20201205005238568.png" alt="image-20201205005238568" style="zoom:33%;" />

##### **输出**

```java
System.out.print(var);  //displays var, no linefeed
System.out.printIn(var);//displays var, then starts new line
```

##### **输入**

如果输入的实际上是字母或者数字,而想要读入的为==String==类,就还得需要将==String==类转换为希望的类型.

且有输入过程的**程序开始**必须包括下条语句:

```Java
import java.io.*;
```

**字符串输入:**

```java
public static String getString() throws IOException
	{
	InputStreamReader isr = new 	InputStreamReader(System.in);
  BufferedReader br = new BufferedReader(isr);
  String s = br.readLine();
  return s;
	}
```

**字符输入:**

​		当程序输入一个字符的时候,为了避免多输入或者输入错误,最安全的方法是通过读入字符串,并通过==charAt()==摘取它的第一个字符:

```java
public static getChar() throws IOExpection
{
  String s = getString();
  return s.charAt(0);
}
```

**整数**:

首先得到==String==类对象并同过转换方法获取==整数==类型

```java
public getInta() throws IOExpection
{
  String s = getString();
  return Integer.parseInt(s);  //或者 parseLong() -->long型
}
```

**浮点型数**:

```java
public getDouble() throws IOExpection
{
  String s = getString();
  Double aDub = Double.valueOf(s);
  return aDub.doubleValue();
}
```

### Java数据结构的类库

Java.util包中包含有诸多向量(一个可扩充的数组),栈,库(dictionary)和哈希表等类型的数据结构.

如果需要使用这些类,必须先加入

```java
import java.util.*;
```

### 小结

- 数据结构是指数据在计算机内存空间中或磁盘中的组织形式

- 正确选择数据结构会使程序的效率大大提高

- 数据结构的例子有数组,栈和链表

- 算法是为了完成特殊任务的过程

- Java中,算法经常通过类的方法实现

- 一些数据结构用途是作为程序员的工具:它们帮助执行算法

- 其他数据结构可以模拟现实世界中的情况,例如城市之间的电话线网

- 数据库是指许多类似的记录组成的数据存储的集合

- 一条记录经常表示现实世界中的一个事物,例如一个汽车零件

- 一条记录被分成字段,每个字段都存储了由这个记录所描述事物的一条特性

- 一个关键字是一条记录的一个字段,通过它可以对数据执行许多的操作,例如,人事记录可以通过LastName字段进行排序

  
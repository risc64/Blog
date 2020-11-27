# Java入门笔记

## 1 基础知识

### 1.1 JDK、JRE、JVM

#### 1.1.1 JDK

Java Development Kit，Java开发工具，包括JRE、javac（编译器）、解释器、Java归档、文档生成器Javadoc等工具。

#### 1.1.2 JRE

Java Runtime Enviroment，Java运行环境，有JVM（Java虚拟机）、核心类库、支持文件组成。

#### 1.1.3 JVM

Java Visual Machine，Java虚拟机，JVM规范、JVM运行实例。JVM执行.class文件，把字节码翻译成平台可以执行的机器码。

### 1.2 解释执行语言、编译执行语言

#### 1.2.1 编译执行语言

将源码一次性编译成特定平台的机器码。执行效率高，可移植性差。如C++

#### 1.2.2 解释执行语言

将源码编译成中间代码，通过解释器在各个平台边解释边执行。执行效率低，移植性好。如Java

### 1.3 基础概念

#### 1.3.1 面向对象

都说物以类聚，面向对象基于分类的思想。比如，正方形、三角形、圆形，都是图形，图形是一个分类，这时候一个边长为4的正方形可以看成是图形类的一个对象。

面向对象是一种编程思想，非常重要，为什么重要?

> 1、面向对象使得计算机语言可以描述现实是世界，比如现实世界的一棵树，我们可以给树挂一个二维码，这个二维码有一个唯一id，有树的种类、树的年龄等。
>
> 2、面向对象使得计算机系统可以分成不同模块（分类思想），模块内是同一类或相关几个类的操作，不同模块之间关联关系小（高内聚、低耦合）,提高系统的可维护性。另外模块化也方便了软件开发过程中分工、并行的实现，缩短研发周期。

封装

将对象属性、方法隐藏起来，提供公共接口访问，提高复用性和安全性。

继承

让一个类获得另一个类的属性、方法。通过继承创建的类称为子类（派生类），被继承的类称父类。比如创建一个圆形类，继承图形类。

多态

一个类实例的方法在不同情形有不同的表现形式。比如图形类画图的方法draw()，子类圆形类调用draw()画出的是圆形，子类正方形调用draw()画出的是正方形。

#### 1.3.2 健壮性

不符合规范的输入，能否有合理的处理方式。比如上传图片接口，上传了word，系统能否提示格式错误。

#### 1.3.3 分布式

一个业务拆分成多个子业务，部署在不同服务器上，不同服务器通过网络连接。

### 1.4 基础语法

#### 1.4.1 数据类型

![image-20201126193846403](https://i.loli.net/2020/11/27/9NPs5rKxe1LiaWz.png)

通常整数用int，小数用double，字符用char或String，布尔型boolean和Boolean

精确计算都会用BigDecimal，例如：

```
/**
* 提供精确的加法运算。
* @param v1 被加数
* @param v2 加数
* @return 两个参数的和
*/
public static double add(double v1,double v2){
    BigDecimal b1 = new BigDecimal(Double.toString(v1));
    BigDecimal b2 = new BigDecimal(Double.toString(v2));
    return b1.add(b2).doubleValue();
}
```

#### 1.4.2 运算符

数值运算：+、-、*、/、%（去余数）和Math类

#### 1.4.3 强制类型转换

![image-20201126195433304](https://i.loli.net/2020/11/27/aFwjgXU5MVkT3vC.png)



#### 1.4.4 字符串

字符截取

```
String h = "hello";
# 截取位置，0到3（不包括3）
String s = h.substring(0, 3);
# s 值为：hel
```

字符拼接

```
String h = "hello";
String s = "word";
String r = h + s;
```

字符相等

```
String h = "hello";
String s = "word";
h.equals(s);
```

空串

```
String s = "";
# s不是空串的判断
if (s != null && s.length() != 0)
```

一些常用方法

```
# 返回index位置的字符
char chatrAt(int index)

# 判断字符串开头或结尾
boolean startWith(String prefix)
boolean endWith(String suffix)

# 获取子串在字符串中的位置
int indexOf(String str)
int lastIndexOf(String str)

# 截取
String substring(int beginIndex)
String substring(int beginIndex, int endIndex)

# 替换
String replace(CharSequence oldString, CharSequence newString)

# 大小写
String toLowerCase()
String toUpperCase()

# 去掉头尾空格
String trim()

```



构建字符串

```
StringBuffer buffer = new StringBuffer();
buffer.append("aaa");
buffer.append("bbb");
String str = buffer.toString();
System.out.println(str);
```

#### 1.4.5 控制语句





#### 1.4.6 数组











## 2 高级特性

### 2.1 面向对象



### 2.2 反射、代理



### 2.3 接口、内部类



### 2.4 异常处理



### 2.5 泛型



### 2.6 集合



### 2.7 事件



### 2.8 并发、多线程






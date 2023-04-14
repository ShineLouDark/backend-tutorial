- [第4章 运算符](#第4章-运算符)
	- [运算符介绍](#运算符介绍)
	- [算术运算符](#算术运算符)
	- [关系运算符(比较运算符)](#关系运算符比较运算符)
		- [逻辑运算符](#逻辑运算符)
		- [赋值运算符](#赋值运算符)
			- [赋值运算符的分类](#赋值运算符的分类)
			- [赋值运算符特点](#赋值运算符特点)
	- [三元运算符](#三元运算符)
		- [基本语法](#基本语法)
		- [使用细节](#使用细节)
	- [运算符优先级](#运算符优先级)
	- [标识符的命名规则和规范](#标识符的命名规则和规范)
		- [标识符命名规范](#标识符命名规范)
	- [关键字](#关键字)
	- [保留字](#保留字)
	- [键盘输入语句](#键盘输入语句)
	- [进制](#进制)
		- [二进制转换成八进制](#二进制转换成八进制)
		- [二进制转换成十六进制](#二进制转换成十六进制)
		- [八进制转换成二进制](#八进制转换成二进制)
		- [十六进制转换成二进制](#十六进制转换成二进制)
	- [原码、反码、补码](#原码反码补码)
	- [位运算符](#位运算符)


# 第4章 运算符

## 运算符介绍

1) 算术运算符
2) 赋值运算符
3) 关系运算符
4) 逻辑运算符
5) 位运算符
6) 三元运算符

## 算术运算符

![](https://raw.githubusercontent.com/timerring/scratchpad2023/main/2023/04/11-18-12-56-1681207973.png)

## 关系运算符(比较运算符)

关系运算符的结果都是boolean 型，也就是要么是true，要么是false

![](https://raw.githubusercontent.com/timerring/scratchpad2023/main/2023/04/11-18-14-16-1681208055.png)

### 逻辑运算符

用于连接多个条件（多个关系表达式），最终的结果也是一个boolean 值。

1) 短路与`&&` ， 短路或`||`，取反`!`
2) 逻辑与`&`，逻辑或`|`，`^` 逻辑异或

### 赋值运算符

#### 赋值运算符的分类

基本赋值运算符 =

复合赋值运算符
+= ，-= ，*= ， /= ，%= 等, 重点讲解一个+= ，其它的使用是一个道理

#### 赋值运算符特点

复合赋值运算符会进行类型转换

byte b = 2; b+=3; b++;

## 三元运算符

### 基本语法

```java
条件表达式? 表达式1: 表达式2;
```

运算规则：

1. 如果条件表达式为true，运算后的结果是表达式1；
2. 如果条件表达式为false，运算后的结果是表达式2；

### 使用细节

1) 表达式1 和表达式2 要为可以赋给接收变量的类型(或可以自动转换)
2) 三元运算符可以转成if--else 语句

## 运算符优先级

1) 运算符有不同的优先级，所谓优先级就是表达式运算中的运算顺序。如右表，上一行运算符总优先于下一行。
2) 只有单目运算符、赋值运算符是从右向左运算的。

![](https://raw.githubusercontent.com/timerring/scratchpad2023/main/2023/04/11-18-28-37-1681208916.png)

## 标识符的命名规则和规范

标识符概念

Java对各种变量、方法和类等**命名时使用的字符**序列称为标识符

标识符的命名规则

1. 由26个英文字母大小写，0-9，或$组成

2. 数字不可以开头。

3. 不可以使用关键字和保留字,但能包含关键字和保留字。

4. Java中严格区分大小写，长度无限制

5. 标识符不能包含空格。int a b = 90;

### 标识符命名规范

1) 包名：多单词组成时所有字母都小写：aaa.bbb.ccc //比如com.hsp.crm
2) 类名、接口名：多单词组成时，所有单词的首字母大写：XxxYyyZzz [大驼峰]
   比如： TankShotGame
3) 变量名、方法名：多单词组成时，第一个单词首字母小写，第二个单词开始每个单词首字母大写：xxxYyyZzz [小驼峰， 简称驼峰法]
   比如： tankShotGame
4) 常量名：所有字母都大写。多单词时每个单词用下划线连接：XXX_YYY_ZZZ
   比如：定义一个所得税率TAX_RATE
5) 后面我们学习到类，包，接口，等时，我们的命名规范要这样遵守,更加详细的看文档.

## 关键字

关键字的定义和特点

定义：被Java 语言赋予了特殊含义，用做专门用途的字符串

特点：关键字中所有字母都为小写

![](https://raw.githubusercontent.com/timerring/scratchpad2023/main/2023/04/11-18-35-38-1681209337.png)

![](https://raw.githubusercontent.com/timerring/scratchpad2023/main/2023/04/11-18-36-01-1681209359.png)

## 保留字

Java 保留字：现有Java 版本尚未使用，但以后版本可能会作为关键字使用。自己命名标识符时要避免使用这些保留字byValue、cast、future、generic、inner、operator、outer、rest、var 、goto 、const

## 键盘输入语句

在编程中，需要接收用户输入的数据，就可以使用键盘输入语句来获取。Input.java , 需要一个扫描器(对象), 就是Scanner

1) 导入该类的所在包, java.util.*
2) 创建该类对象（声明变量）
3) 调用里面的功能

```java
import java.util.Scanner;//表示把java.util下的Scanner类导入 
public class Input { 
	//编写一个main方法
	public static void main(String[] args) {
		//演示接受用户的输入
		//Scanner类 表示 简单文本扫描器，在java.util 包
		//1. 引入/导入 Scanner类所在的包
		//2. 创建 Scanner 对象 , new 创建一个对象,体会myScanner 就是 Scanner类的对象
		Scanner myScanner = new Scanner(System.in);
		//3. 接收用户输入了， 使用 相关的方法
		System.out.println("请输入名字");

		//当程序执行到 next 方法时，会等待用户输入~~~
		String name = myScanner.next(); //接收用户输入字符串
		System.out.println("请输入年龄");
		int age = myScanner.nextInt(); //接收用户输入int
		System.out.println("请输入薪水");
		double sal = myScanner.nextDouble(); //接收用户输入double
		System.out.println("人的信息如下:");
		System.out.println("名字=" + name 
			+ " 年龄=" + age + " 薪水=" + sal);

	}
}
```

## 进制

对于整数，有四种表示方式：
二进制：0,1 ，满2 进1 以0b 或0B 开头。
十进制：0-9 ，满10 进1。
八进制：0-7 ，满8 进1. 以数字0 开头表示。
十六进制：0-9 及A(10)-F(15)，满16 进1. 以0x 或0X 开头表示。此处的A-F 不区分大小写。

```java

//演示四种进制
//
public class BinaryTest { 

	//编写一个main方法
	public static void main(String[] args) {

		//n1 二进制 10
		int n1 = 0b1010;
		//n2 10进制 1010
		int n2 = 1010;
		//n3 8进制 520
		int n3 = 01010;
		//n4 16进制 65793
		int n4 = 0X10101;
		System.out.println("n1=" + n1);
		System.out.println("n2=" + n2);
		System.out.println("n3=" + n3);
		System.out.println("n4=" + n4);
		System.out.println(0x23A); // 570
	}
}
```

### 二进制转换成八进制

规则：从低位开始,将二进制数每三位一组，转成对应的八进制数即可。

案例：请将0b11010101 转成八进制

0b 11(3)010(2)101(5) => 0325

### 二进制转换成十六进制

规则：从低位开始，将二进制数每四位一组，转成对应的十六进制数即可。

案例：请将0b11010101 转成十六进制
0b1101(D)0101(5) = 0xD5

### 八进制转换成二进制

规则：将八进制数每1位，转成对应的一个3 位的二进制数即可。
案例：请将0237转成二进制
02(010)3(011)7(111) = 0b10011111

### 十六进制转换成二进制

规则：将十六进制数每1 位，转成对应的4 位的一个二进制数即可。
案例：请将0x23B 转成二进制
0x2(0010)3(0011)B(1011) = 0b001000111011


## 原码、反码、补码

网上对原码,反码,补码的解释过于复杂，我这里精简几句话:(背下来)

对于有符号的而言:

二进制的最高位是符号位:0表示正数,1表示负数

正数的原码，反码，补码都一样(三码合一)

负数的反码=它的原码符号位不变，其它位取反(0->1,1->0)

**负数的补码=它的反码+1**，负数的反码=负数的补码-1

0的反码，补码都是0

**java没有无符号数，换言之，java中的数都是有符号的**

在计算机运算的时候，都是以补码的方式来运算的

当我们看运算结果的时候,要看他的原码(重点)

## 位运算符

java 中有7 个位运算(&、|、^、~、>>、<<和>>>)

1) 算术右移>>：低位溢出,符号位不变,并用符号位补溢出的高位
2) 算术左移<<: 符号位不变,低位补0
3) \>>>逻辑右移也叫无符号右移,运算规则是: 低位溢出，高位补0
4) **特别说明：没有<<< 符号**


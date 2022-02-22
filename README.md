# AP CSA 终极简答题速通指南
```java
/* @author DylanSun S3C8 */ 
```



## 为什么会有这个指南?

我写 java 写了一段时间了, 然后后来也跑去学了CSA这门课。结果我很多的朋友们似乎对于
CSA中的简答题有一些困惑, 做这些题需要花时间思考, 这对于考试和大家拿5分的伟大理想产
生了严重的冲突。所以为了帮助去美国上学的各位大佬们不要在java里重新踩那些我当年摸爬
滚打的坑, 我决定写这一份CSA速通指南、

这个指南很肝, 很长, 但是所有的知识点都会给你讲通讲透。大家可以一次性看完, 或者Star
这个项目并收藏到以后慢慢看, 建议量力而行吧 :D



## 目录 (你将逐渐理解这一切):

> [基础知识复习](#tag1)

<div id="tag1"></div>

## 基础知识复习

首先来讲讲数据类型, 这是一切程序的基础, 也是我们速通计划的开端. 电脑中所有的数据都是以0和1的二进制
形式存储在内存空间之中, 而数据类型决定了电脑理解这块内存的方式。在 Java 等静态语言之中, 每一个变量
在创建的时候都必须指定其所对应的数据类型。
```java
/**
 * int, 也就是Integer或int32, 是最常见的数据类型, 中文称之为 "整型"。
 * int 一般情况下为 32bits, 最大值为 2147483647, 最小值为 -2147483648
 * int 可以进行加减乘除和取模的运算, 对应操作符为 + , - , * , / , %
 * 也可以通过位操作符进行操作, 如 & , | , ^ , << , >>
 * int 只能够存储整数, 如果将小数转化为int, 小数点后的精度会被抛弃
 * int 可以使用逻辑操作符进行对比 (==, >=, <=, >, <)
 * java int 对应的类型是 Integer
 */ 
int a = 0;   //initialize an integer with a value
int a;       //declare an integer without initializing

/**
 * char, 也就是字符, 是java中另一种非常重要的基础数据类型
 * 每一个char由两个bit构成, 能够表示 \u0000 (0) 到 \uffff (65535) 之间的值
 * char 本身是一个数值, 但是也能够代表一个标准的 Unicode 字符
 *    -  例如 char 'a' 与 char 141 是相同的
 * 大写字母的 char 值小于小写字母的 char 值
 * char 可以进行加减乘除和取模的运算, 对应操作符为 + , - , * , / , %
 * char 可以使用逻辑操作符进行对比 (==, >=, <=, >, <)
 * java char 对应的类型是 Character
 */
char c1 = 'a';    //init a char with a unicode value
char c2 = 69;     //init a char with a numerical value
char c3;          //declare a char without init

/**
 * float 是浮点型, 支持小数点, 在java中特指32位浮点
 * 每一个 float 由 32 bit 构成 (最大最小值比较复杂感兴趣的自己可以搜一下)
 * float 可以进行加减乘除运算
 * float 可以使用逻辑操作符进行对比, 但是不要使用 ==
 * 因为float的存储存在精度问题, 所以对比两个float 的大小是否相等
 * 会通过观察两个float的差是否在可接受的误差范围内, 即
 *    Math.abs(Math.abs(float1) - Math.abs(float2)) < MIN_DIFF
 */
float f1 = 0.09;   //init a float value
float f2;          //declare without init
```
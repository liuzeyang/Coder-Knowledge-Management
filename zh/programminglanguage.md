[TOC]

学习一门语言最痛苦的反而是大量的细节语法，譬如字符串截取、数组或者字典类型的索引之类的。下面要进行讨论的一些语法特性是目前流行的一些语言的总结，可能有些语言尚不支持部分特性，但是要么有些第三方库进行辅助，要么会在未来的版本中添加如下特性。笔者参考的语言包括但不限于：
- Java
- JavaScript
- Python
- Ruby
- PHP
- Swift
- Objective-C
- C/C++
- C#
- Rust*：正在学习

下文的阐述中会以目录方式进行阐述，目录的概览可以参考这篇[文章](http://segmentfault.com/a/1190000003738148)。本篇文章即是对于那篇文章的详细阐述，欢迎大家提出自己的见解，一起来完善。

> 注意：本部分仅仅包含基本语言特性，学习一门语言还有很多其他的部分，但是都暂时摘了出去，请参考笔者该系列其他文章。

# 入门概述(Introduction)

## 版本迭代(Version)

每一门语言的每一次迭代都会引入一些新特性，作为一名合格的程序员一定要随时关注，不是为了一味追新，只是不能墨守成规。就像笔者现在感受到的Swift 2.0、Java 8、NodeJs 4.0、ECMAScript 2015带来的特性变化，会大大方便我们的开发。

## 注释与代码分割

不同语言的注释与代码分割风格大相径庭，笔者最早学习的是C、Java这样看上去灰常严谨的语言，而当笔者学习Matlab、Python、Ruby这样”随意”的语言的时候，内心是崩溃的。有的语言以分号作为代码分割，而Python是利用的换行与缩进进行代码分割（还有SASS）。

## 参考资料

### Tutorial&Docs：入门教程、指导

本部分主要存放部分相关的官方教程，譬如官方的Quick Start以及社区中的部分入门教程。

### Practice&Tips：实践与资源

本部分主要存放社区相关的实践以及资源，譬如Github很著名的awesome-*系列或者Best-Practice系统。

### Forum&Lessons：论坛与视频教程

本部分主要存放该语言相关的著名的论坛地址或者在线教程地址，譬如Coursera或者慕课网这一类型的。

### Blog&News：博客与资讯

本部分主要存放该语言相关的博客或者咨询地址，譬如Java领域的ImportNews、Swift领域的SwiftGG等等。

### Book&Resources：书籍

本部分主要存放该语言相关的书籍地址或者工具地址，譬如Android领域的DevTools这个站点。

# Quick Start

## Installation

本部分主要介绍语言开发环境的搭建以及SDK的安装与管理。譬如利用NVM进行NodeJs的基本环境安装。

## Builder & Dependence Manager：构建与依赖管理

本部分主要介绍该语言的构建工具以及依赖项管理，譬如Java领域的Maven，将笔者从IDE的世界带领到了构建的世界，脱离了IDE的束缚。比较常见的构建工具有Maven、Gradle、[Google-Bazel](http://bazel.io/)、Make、Ant等等。而依赖工具则是更为常见，譬如Npm、Pip等等。

## Deployment：代码部署工具

## IDE：代码开发工作

# 数据结构(Data Structure)

本部分应该算是一门语言的基石，主要涉及某个语言所提供的基本的数据类型与数据结构。

## 变量与常量

本部分主要介绍变量的定义方式与定义规范，变量名的要求、强/弱类型语言区分以及类型声明等。譬如PHP中需要明晰所有的变量以$符号开始，Java中以```Int i ```这种类型在前的方式声明，而Swift中以```var i:Int```这种方式声明。除以之外，在JavaScript与Swift中存在着let与var两种变量声明方式，这两种不同的声明方式对应了不变量与可变量。

### 常量与宏

常量与宏往往作为全局的定义或者配置，譬如C++以及OC中的define关键字，就可以定义某个宏。

#### 系统常量

本部分需要对常用的系统常量有一个了解，譬如PHP中的__dir，就是指代的当前目录。

### 赋值

赋值最简单的理解就是利用```=```号将右侧的值或者指针赋予左侧，不过赋值这部分需要了解的是该语言是否支持析构解包赋值，譬如ES6中的特性：```var a,b = [1,2]```

### 类型/格式判断与转换

本部分主要阐述语言中常用的类型判断方法，譬如Java领域的instanceof关键字、JavaScript领域的typeof关键字等等。另一方面，还要阐述下常见的强制类型转换的方法，就像Swift领域的as关键字。

## 基本类型(Basic)

本部分主要介绍常见的基础数据类型。

### 数值类型

数值类型包括整型、浮点型(如果是强数据类型的化)。

#### 随机数

介绍随机数的生成方式。

#### 科学计算

介绍科学计算的方式，特别是对于Matlab、R、Python这样在统计学与数据科学领域应用较多的，包括常见的科学计算算子等等。

#### 类型转换

介绍数值类型转化为其他类型(特别是String类型，有些语言就没有toString方法，譬如C++)或者数值类型内部转化的方式。

### 空类型

本部分介绍语言中是怎么定义空类型的，常见的空类型有null、nil、undefined等等。

### 布尔类型

不部分介绍语言中的布尔类型，对于非面向对象的语言，往往是true这样的Primitive类型，而OC中则存在着TRUE、YES等等多种形式。

### 可选类型(Optional)

笔者第一次接触到可选类型还是在Google的Guava这个类库中，此后作为特性之一正式加入了Java8。不过笔者窃认为Swift中对于可选类型的封装更为完善，譬如在Swift中以```var str:String?```方式声明的就是一个可选类型，该类型可以优雅地判断是否为空或者为Nil（虽然是因为Swift不会主动将对象赋值为Nil才需要这么做），然后通过```str!```方式即可方便调用。


### 枚举类型(Enum)



## 字符串(String)

字符串是语言中最常使用的语法，没有之一，虽然简单，但是还是很恶心。本部分主要就是阐述常用的字符串的API，往往都是一列一大堆，还长得特别像，所以这边也分了个类。如果是在C这种非对象化的语言中，可以暂时将字符数组看做字符串，不要在意这些细节。

这部分包括字符串的基本比较

### 创建增删

本部分介绍怎么创建以及修改某个字符串。

- 创建添加

  最常见的也是最通用的创建字符串的方式就是以```””```双引号方式创建，不过譬如OC中你一定要加@符号才能真正创建某个字符串对象，这个需要注意。另外，在字符串合并时，譬如C里面要注意使用concat这样的函数，而PHP里面要注意使用```.```运算符而不是```+```运算符。

  - **Format/Template：格式化与模板字符串生成、字符串插值**

  格式化字符串、模板字符串、字符串插值其实是一个意思，简单而言就好像```print("%s","a")```这样，其实print里面是采用变量替换的方式组装了一个新的字符串。在ES6、Swift、PHP中的直观表现就是利用{}或者双引号可以书写变量然后直接将变量的值替换进来。

- 复制

``` 
本部分介绍字符串的复制。
```

- 替换删除

``` 
本部分介绍常见的在字符串中查找某个字符、根据下标删除某个字符等等。
```

- 栈列操作

``` 
本部分介绍常见的push、pop、shift、unshift操作等等。
```

### 索引遍历

- 存在判断

本部分主要介绍如何在字符串中判断某个字符是否存在或者某个字串是否存在，有时候直接可以用contains方法，有时候需要indexOf方法判断。在有些语言，譬如Swift中还支持`hasPrefix`、`hasSuffix`这样的内建的辅助方法。

- 反向索引

  根据某个字符或者某个字串，获得其在字符串中的下标。

- 循环遍历

  怎么去遍历某个字符串。

- 截取分割

``` 
本部分介绍怎么根据某个字符或者正则表达式进行字符串分割，往往分割的结果就是获得一个数组。
```

### 类型编码

- 包括UTF编码、URL编码等


- HTML

``` 
介绍下语言中是否有处理HTML标签的方法，往往是为了防止XSS等，譬如PHP领域的htmlspecialchars、strip_tags等等。
```

- Pinyin

  介绍下语言中是否对于汉字拼音有支持，譬如Java领域比较著名的Pinyin4j。

### 其他操作

- Reverse

  怎么去反转某个字符串，算是一个代码的积累。

- 正则匹配

  正则表达式，不用赘述了，往往用于模式匹配与提取。

- Valid(字符串校验)

​	封装好的类似于正则表达式，用于校验字符串长度、是否为URL、Email等。



## 结构体(Struct)


## 时间日期类型

时间与日期类型也是编程语言领域常用的数据类型，Java8之前的Date、SimpleDateFormat等等也是为人诟病。一般而言，时间与日期类型需要考虑以下几个部分：

### 构造与TimeZone(本地化时间)

本部分介绍怎么根据当前时间构造一个时间对象或者根据输入的指定格式的字符串构造一个时间对象。另外，需要对TimeZone以及本地化时间有一个阐述。

- **TimeFormat(时间格式化)**

``` 
介绍下常用的时间格式话工具、规范，譬如OC领域的NSDateFormatter等等。
```

### TimeComparison(时间比较)&Diff(计算)

主要介绍如何比较两个时间对象以及计算他们之间的差值。

### TimeStamp

介绍怎么从时间对象得到TimeStamp，以及TimeStamp本身的TimeZone。

### Calendar（日历）

日历功能，用于判断某个日期在某月的第几周等等。Java 8中，LocalDate也自带了Calendar功能。

## Indexed Collection:序列类型（Array）

常说的序列类型，包括但不限于数组(Array)、列表(List)、元组(Tuple)。序列类型是编程语言数据类型的重要组成部分。如果是像JavaScript或者PHP这种，只有一种Array类型的，可以直接一章写完。如果是Java这样包含了各种序列类型的，建议是另开一章。序列类型最基本的需要介绍序列的长度获取、空判断以及序列的类型判断。

### 创建增删

- 创建添加
- 复制
- 替换删除
- 栈列操作

### 索引遍历

- 存在判断
- 反向索引
- 循环遍历
- 截取分割

### 类型转换


### 序列操作/Stream API

序列函数在Python、Ruby等语言中早就有了，用起来确实爽气，代码的逼格一下子就上去了。在Java8中也引入了Stream API，不过序列函数并不仅仅包含下面三货，只不过这三个家伙最为出名。

### 其他操作

- 统计查询
- 过滤去重





## Keyed Collections(键值索引类型):字典类型（Dict）/ Map

### 创建增删

- 创建添加
- 替换删除
- 栈列操作

### 索引遍历

- 键类型与存在判断
- 反向索引
- 循环遍历
- 截取分割

### 类型转换

### 其他操作

# 流程控制与异常处理（Control Flow & Error Handling）

## 运算符

### 基本运算符

### 逻辑运算符

### 运算符重载

## 分支选择(Branch)

### if

### switch

## 循环(Loop)

### for

### while

## 控制

### break/continue

### 标签/锚点

## 作用域(Scope)

变量与值存取几乎是所有编程语言中通用的范式，正是这种能够存取以及修改值的能力赋予了程序以状态(State)。本部分主要对于变量的作用域进行一个阐述，一般变量即是指局部变量，但是往往会受到闭包、静态变量(static)、全局变量(global)的影响。

## 迭代器

迭代器（**iterator**）是一种对象，它能够用来遍历标准模板库容器中的部分或全部元素，每个迭代器对象代表容器中的确定的地址。迭代器修改了常规[指针](http://baike.baidu.com/view/159417.htm)的接口，所谓迭代器是一种概念上的抽象：那些行为上像迭代器的东西都可以叫做迭代器。然而迭代器有很多不同的能力，它可以把抽象容器和通用算法有机的统一起来。

迭代器是一个更抽象的概念，任何对象，如果它的类有next方法（**next** python3)和**iter**方法返回自己本身。每个生成器都是一个迭代器，但是反过来不行。通常生成器是通过调用一个或多个yield表达式构成的函数s生成的。同时满足迭代器的定义。当你需要一个类除了有生成器的特性之外还要有一些自定义的方法时，可以使用自定义的迭代器，一般来说生成器更方便，更简单。


## 异常处理（Exception）


### Error(异常定义与类型)

### Throw

### Try-Catch-Finally



# 函数（Function）

## 函数定义

本部分主要介绍在该语言中如何，对于强类型语言，往往返回值在函数定义时即可确定。而对于诸如PHP、JavaScript这样的语言，返回值往往由return语句决定。而对于Python、Swift这样支持元组的语言，往往也支持多个返回值。

### 返回值

### 函数变量

## 参数调用

### 默认参数与外部参数

### 不定参数

### 传值类型：引用传值/复制传值

## 匿名函数/Lambda & 闭包(Closures)

闭包、匿名函数、Lambda这三种东西在有些编程语言里是可以统一而视的，但是在某些编程语言里，譬如JavaScript中，是有区别的。含有自由变量的代码块才被称之为“闭包（closure）”。

> Closures are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created。


## 生成器（Generator/yield）


生成器的概念笔者最早是见于Python中。

## 装饰器(Decorator)

## Currying And unCurrying(函数柯里化与反柯里化)

在计算机科学中，柯里化（英语：Currying），又译为卡瑞化或加里化，是把接受多个参数的函数变换成接受一个单一参数（最初函数的第一个参数）的函数，并且返回接受余下的参数而且返回结果的新函数的技术。这个技术由 Christopher Strachey 以逻辑学家哈斯凯尔·加里命名的，尽管它是 Moses Schönfinkel 和 Gottlob Frege 发明的。这是来自维基百科的名词解释。顾名思义，柯里化其实本身是固定一个可以预期的参数，并返回一个特定的函数，处理批特定的需求。这增加了函数的适用性，但同时也降低了函数的适用范围。笔者在JavaScript与Scala会比较常用这个特性，这里以JavaScript为例说明柯里化的核心思想。

``` javascript
function square(i) {
    return i * i;
}

function dubble(i) {
    return i *= 2;
}

function map(handeler, list) {
    return list.map(handeler);
}

// 数组的每一项平方
map(square, [1, 2, 3, 4, 5]);
map(square, [6, 7, 8, 9, 10]);
map(square, [10, 20, 30, 40, 50]);
// ......

// 数组的每一项加倍
map(dubble, [1, 2, 3, 4, 5]);
map(dubble, [6, 7, 8, 9, 10]);
map(dubble, [10, 20, 30, 40, 50]);
```

譬如上述代码中，我们使用了几个元函数的组合来达成某个复杂的操作。创建了一个map通用函数，用于适应不同的应用场景。显然，通用性不用怀疑。同时，例子中重复传入了相同的处理函数：square和dubble。应用中这种可能会更多。当然，通用性的增强必然带来适用性的减弱。但是，我们依然可以在中间找到一种平衡。

``` javascript
function square(i) {
    return i * i;
}

function dubble(i) {
    return i *= 2;
}

function map(handeler, list) {
    return list.map(handeler);
}

var mapSQ = currying(map, square);
mapSQ([1, 2, 3, 4, 5]);
mapSQ([6, 7, 8, 9, 10]);
mapSQ([10, 20, 30, 40, 50]);
// ......

var mapDB = currying(map, dubble);
mapDB([1, 2, 3, 4, 5]);
mapDB([6, 7, 8, 9, 10]);
mapDB([10, 20, 30, 40, 50]);
// ......
```



# 模块(Modules) / 组件(Components)

## 命名空间

# 类与对象(Class)

## 定义

### 可见域

包括public、private、protected这几个关键字不同的作用以及不同语言里不同的声明方式。static final

### 属性(Properties)

### 方法(Methods)

## 对象

### 实例化

#### 单例模式

### this
### 类型判断

## 继承

### 运算符重载

## 抽象类、接口/协议与委托（Delegate）
### 注解(Annotation)



## 内部类

### 静态内部类

### 成员内部类(普通内部类)

### 局部内部类(定义在代码块中)

### 匿名内部类

## 反射（Reflect）与类装载

### Immutable:不可变对象

# IO




# 其他知识点目录规范（Directory For Programming Language）

此部分主要是阐述了某个语言/框架所包含的内容和应该怎么将需要学习的东西进行分类，这边以Java作为示范。

## Advanced



### 泛型编程

关于泛型的理解可以总结下面的一句话，它是把数据类型作为一种[参数传递](http://baike.baidu.com/view/2691131.htm)进来。 

### 内存管理

本部分因为篇幅所限(总不能在一篇笔记里把所有东西撸一遍)

### 序列化与反序列化

序列化与反序列化简单来说就是把某个Object或者复杂数据类型转化为某个字符串(Json)或者某个数据流。本部分一方面主要介绍语言内置的序列化方式，譬如Java的Serialization，不要管什么ProtoBuf、FlatBuffer、Thrift等等。另一方面介绍该语言常用的Json编译与解析框架(用的多，没办法)。就像Java领域的FastJson。





### 编程规范与代码风格



### Algorithms

常见的算法与高级数据结构实现



- Advanced:存放编程规范、设计模式、应用架构等相关内容

  - 设计模式
  - 编程规范
    - API 设计规范
  - 应用架构

- UI:界面相关内容
- Network:存放网络、Socket相关内容
  ## Storage:存放文件系统、数据库等存储相关内容​

### Cache

​	 on-heap Cache

​	 off-heap Cache
​### DataBase

#### KeyValue

​#### Relational

##### ORM

##### Sharding Support(数据库分片支持)


​#### Document

​### FileSystem

## TestRelease:存放测试发布相关内容
### Debug：调试
### Log：日志
### Monitor：运行状态监控


## SysProc:存放系统进程相关内容



### AOP(切面编程)



### Concurrence(并发)
#### Thread：线程基本知识

#### Thread Communication:线程通信

#### Asynchronous Pattern

主要介绍CallBack、Promise/Future/Defer、Generator、Async的一些实现与用法

#### Asynchronous Data Flow：消息总线类型的，常见的方式有EventBus

#### Reactive(Actor):响应式开发

### Synchronous(同步) & ThreadSafety(线程安全)

#### Lock(锁)

#### Built-in ThreadSafe DataStructure

##### Atomic Variables(原子变量)

##### Collections(集合类型)

#### Built-In ThreadSafe DataStructure(内置的线程安全的数据结构)



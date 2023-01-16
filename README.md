# go语言的基础学习~用java,c去理解go|青训营笔记

这是我参与**「第五届青训营 」**伴学笔记创作活动的第1天

## go简介

Go 是一门新语言。虽然它借鉴了现有语言的思想，但它具有不寻常的特性，使有效的 Go 程序在性质上不同于用其亲戚编写的程序。将 C++ 或 Java 程序直接翻译成 Go 不太可能产生令人满意的结果——Java 程序是用 Java 而不是 Go 编写的。另一方面，从 Go 的角度思考问题可能会产生一个成功但完全不同的程序。换句话说，要写好 Go，重要的是要了解它的属性和习语。了解 Go 编程的既定约定也很重要，例如命名、格式化、程序构造等，这样您编写的程序将很容易被其他 Go 程序员理解。

## go环境|编译器

关于go的开发环境，我个人目前知道的有vscode、Goland、IntelliJ IDEA。我推荐是使用vscode进行编译因为免费和只需要安装插件即可用，其次如果是非常萌新的同学来学习语言那么我的建议是用golan来进行编译，因为此编译方便，可以直接在编译器里面进行点击运行和IDEA是非常类似的（但是注意这个是免费使用30天之后，之后使用是要收取费用的，若你是学生那么可以申请学生的优惠政策）。我个人目前使用的是IDEA因为我已经用习惯了，可以进行go后端服务器的整个项目部署。

下列依次介绍各个编译器。

### Goland

Goland 是由 JetBrains 公司开发的一个新的商业 IDE，旨在为 Go 开发者提供的一个符合人体工程学的新的商业 IDE。Goland 整合了 IntelliJ 平台（一个用于 java 语言开发的集成环境，也可用于其他开发语言），提供了针对Go语言的编码辅助和工具集成。

### VS code

vscode是一种简化且高效的代码编辑器，同时支持诸如调试，任务执行和版本管理之类的开发操作。它的目标是提供一种快速的编码编译调试工具。然后将其余部分留给IDE。vscode集成了所有一款现代编辑器所应该具备的特性，包括语法高亮、可定制的热键绑定、括号匹配、以及代码片段收集等。

### IntelliJ IDEA

IDEA 全称 IntelliJ IDEA，是[java](https://baike.baidu.com/item/java/85979?fromModule=lemma_inlink)[编程语言](https://baike.baidu.com/item/%E7%BC%96%E7%A8%8B%E8%AF%AD%E8%A8%80/9845131?fromModule=lemma_inlink)的[集成开发环境](https://baike.baidu.com/item/%E9%9B%86%E6%88%90%E5%BC%80%E5%8F%91%E7%8E%AF%E5%A2%83/298524?fromModule=lemma_inlink)。IntelliJ在[业界](https://baike.baidu.com/item/%E4%B8%9A%E7%95%8C/2870119?fromModule=lemma_inlink)被公认为最好的[Java](https://baike.baidu.com/item/Java/85979?fromModule=lemma_inlink)开发工具，尤其在智能代码助手、代码自动提示、[重构](https://baike.baidu.com/item/%E9%87%8D%E6%9E%84/2182519?fromModule=lemma_inlink)、[JavaEE](https://baike.baidu.com/item/JavaEE/3066623?fromModule=lemma_inlink)支持、各类版本工具([git](https://baike.baidu.com/item/git/12647237?fromModule=lemma_inlink)、[svn](https://baike.baidu.com/item/svn/3311103?fromModule=lemma_inlink)等)、[JUnit](https://baike.baidu.com/item/JUnit/1211849?fromModule=lemma_inlink)、[CVS](https://baike.baidu.com/item/CVS/405463?fromModule=lemma_inlink)整合、代码分析、 创新的[GUI](https://baike.baidu.com/item/GUI/479966?fromModule=lemma_inlink)设计等方面的功能可以说是超常的。IDEA是[JetBrains](https://baike.baidu.com/item/JetBrains/7502758?fromModule=lemma_inlink)公司的产品，这家公司[总部](https://baike.baidu.com/item/%E6%80%BB%E9%83%A8/5289033?fromModule=lemma_inlink)位于[捷克共和国](https://baike.baidu.com/item/%E6%8D%B7%E5%85%8B%E5%85%B1%E5%92%8C%E5%9B%BD/418555?fromModule=lemma_inlink)的首都[布拉格](https://baike.baidu.com/item/%E5%B8%83%E6%8B%89%E6%A0%BC/632?fromModule=lemma_inlink)，开发人员以严谨著称的[东欧](https://baike.baidu.com/item/%E4%B8%9C%E6%AC%A7/7149362?fromModule=lemma_inlink)[程序员](https://baike.baidu.com/item/%E7%A8%8B%E5%BA%8F%E5%91%98/62748?fromModule=lemma_inlink)为主。它的[旗舰版](https://baike.baidu.com/item/%E6%97%97%E8%88%B0%E7%89%88/1412903?fromModule=lemma_inlink)还支持[HTML](https://baike.baidu.com/item/HTML/97049?fromModule=lemma_inlink)，[CSS](https://baike.baidu.com/item/CSS/5457?fromModule=lemma_inlink)，[PHP](https://baike.baidu.com/item/PHP/9337?fromModule=lemma_inlink)，[MySQL](https://baike.baidu.com/item/MySQL/471251?fromModule=lemma_inlink)，[Python](https://baike.baidu.com/item/Python/407313?fromModule=lemma_inlink)等。[免费版](https://baike.baidu.com/item/%E5%85%8D%E8%B4%B9%E7%89%88/1817376?fromModule=lemma_inlink)只支持Java,[Kotlin](https://baike.baidu.com/item/Kotlin/1133714?fromModule=lemma_inlink)等少数语言。

## go基础入门

### 简单介绍

-   go语言的主要一些特征如下：
-   高性能，高并发
-   语法简单。
-   丰富标准库。
-   完善的工具链。
-   静态链接。
-   快速编译。
-   跨平台。
-   垃圾回收。

### 基础语法

基础语法结构包括这几个部分

包声明、引入包、函数、变量、语句表达式、注释

例如下列图片展示最基本的一个语句，下面的图片和java做一个对比就很容易懂了只是go语言没有java类的概念，引入一个fmt对应java，System的效果是一样的道理。

| <img align="center" src="https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e020a6aa8f2f44f0992063c1a910a500~tplv-k3u1fbpfcp-watermark.image?"> | <img align="center" src="https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/caa91ffbe33c4825bc6f5957f03e8631~tplv-k3u1fbpfcp-watermark.image?"> |
| ------------------------------------------------------------ | ------------------------------------------------------------ |

且声明变量可以用如下的代码，最具有特色的就是最后一行代码，这样声明了其实可以直接赋值语句，这样go也会自动识别出来是哪一种的数据类型

```go
var a = "initial"
var b, c int = 1, 2
var d = true
var e float64
f := float32(e)
```

### 数组

go语言的数组格式如下

```go
var a [5]int
a[4] = 100
fmt.Println("get:", a[2])
fmt.Println("len:", len(a))
```

就类似于很多的数组语言这里不再说明，其次这个数组是固定的数组，大小不可以改变如果想要用动态的数组例如java中的ArrayList那么就使用如下的数组（语言切片：slice）

```go
	s := make([]string, 3)
	s[0] = "a"
	s[1] = "b"
	s[2] = "c"
	fmt.Println("get:", s[2])   // c
	fmt.Println("len:", len(s)) // 3
	s = append(s, "d")
	s = append(s, "e", "f")
```

其中还有重要的key value的数组语句如下对应着java中的hashmap

```go
m := make(map[string]int)
m["one"] = 1
m["two"] = 2
fmt.Println(m)           // map[one:1 two:2]
fmt.Println(len(m))      // 2
fmt.Println(m["one"])    // 1
fmt.Println(m["unknow"]) // 0
```

### 条件语句

go语言的条件语句和其他的语言的格式有所不同区别就在于没有大括号

且提供了如下的一些条件语句

<img align="center" src="https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ae978bf61afa42b1a79ca07ed28fb4a5~tplv-k3u1fbpfcp-watermark.image?">

和其他语言的原理几乎是类似的，就是例如Java中条件语句一般如

```java
if (true){
    System.out.println("hello");
}
```

go语言的条件语句如下

```go
if 7%2 == 0 {
   fmt.Println("7 is even")
} else {
   fmt.Println("7 is odd")
}
```

没有小括号引用

例如switch语句是差不多的，只是go语言可以这样写

```go
switch {
case t.Hour() < 12:
   fmt.Println("It's before noon")
default:
   fmt.Println("It's after noon")
}
```

### 循环

go语言循环就只能用for进行一系列的循环，且循环条件里面可以用一些函数（range）来增强逻辑关系，其中的range就是来限定for循环的范围，如下代码

```go
for i, num := range nums {
   sum += num
   if num == 2 {
      fmt.Println("index:", i, "num:", num) // index: 0 num: 2
   }
}
```

比其他的语言更加的快捷和方便的实现循环逻辑，其中当代码中for后面如果没有表达式来进行一种限定，那么他就会无限的循环该代码块实现循环逻辑。

### 函数

go语言的函数跟其他语言不同的是，可以有多个返回值且对比java不需要设置返回类型，go语言可以自己识别返回值的数据类型如下代码

```go
func exists(m map[string]string, k string) (v string, ok bool) {
   v, ok = m[k]
   return v, ok
}
```

### 结构体

go语言有结构题这一说发 就跟c语言非常类似了，如下代码

```go
type user struct {
   name     string
   password string
}
```

你可以把它看作一个java的实体集类这样用java 的角度去理解更加的易懂

### erorr

go语言的erorr实际上就是java语言的try catch来进行错误的抓取，来进行异常的抛出或者处理具体代码如下

```go
u, err := findUser([]user{{"wang", "1024"}}, "wang")
if err != nil {
   fmt.Println(err)
   return
}
```

这里做一个充分的解释说明finduser函数赋值给u，此时可能会有一些格式转换的错误或者类似于java抓取字节流传输时可能遇到的错误，如果error不等于空就如这个if条件语句于洋那么就会打印错误且终止程序

## proxy

go语言的代理，启动微服务功能功能类似于java的socket直接上代码演示

```go
server, err := net.Listen("tcp", "127.0.0.1:1080")
if err != nil {
   panic(err)
}
for {
   client, err := server.Accept()
   if err != nil {
      log.Printf("Accept failed %v", err)
      continue
   }
   go process(client)
}
```

我是按照java去一步一步理解的，熟悉Java的同学就可以来按照java思维来理解哦，具体表达我怕出错所以就不过多赘述

## 个人总结

go语言确实比许多语言更加容易上手且有很多的库可以进行调用，性能方面也比其他语言要好的很多且代码的复杂度很小，还有一些go语言的代理，请求等等也是比较方便的

## 引用

-   [go官网之go语言介绍](https://golang.google.cn/doc/effective_go#introduction)
-   [go语言的菜鸟教程](https://www.runoob.com/go/go-tutorial.html)

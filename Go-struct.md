# 面向对象Class类的底层实现从某些方面说就是结构体，对象的引用就是指针，只是语言把他们封装起来了而已。

Golang的Struct结构体（源于C语言，但又有别于C）的灵活性：
go语言中并没有像C++，Java语言中这类的Class，它只含有像C语言中的结构体，用结构体和指针等特性，完成一个类的作用，很巧妙的使用了指针和结构体，不仅是go的面向对象，包括go语言中的map等操作都是借助了结构体。其实，说白了，C++、Java等面向对象的语言中，类的底层实现就是结构体，对象的引用就是指针，只是语言把他们封装起来了而已。很多人刚接触面向对象很不理解这些东西也应该缘于此。
或者说，面向对象的封装在某种意义上是以牺牲灵活特性的为代价的一种抽象简化。

所有高级语言(PHP、Java、Python、JavaScript等等...)的数组Array、字典map、Slice切片、Json等结构类型往往只是叫法不一样，多少都源于C系或者受到C系的Struct结构体思想的影响,在某些特定领域内，做了一些针对性的解决方案。

PHP就是c语言实现的一套高级“程序”语言，只不过是这套“程序化的语言”的规范和语法等机制可以用来快速做web领域的事情，通过解释器，转成底层语言完成代码的最终执行。

这也印证了很多答案往往追根溯源都在计算机数据结构基础里没有捷径可以走。

### 编程的世界应该是丰富多彩的,不拘泥于任何一种思维模式。

## golang struct注意事项：

对于struct类型来说，字段的先后顺序是非常关键的。如果两个struct类型包含了完全相同的字段，但是排列顺序不同或者进行了部分合并，那么这两个struct就是不同的类型！

如果struct字段是大写字母开头，那么该字段就是导出的（包外可见），这也符合Go语言的可见性规则。因此一个struct可以同时包含导出和未导出的变量。
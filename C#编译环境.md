# C#编译环境

---

- 拓展1：Visual Studio
- 拓展2：.Net/.Net framework
- 拓展3：.net与Java的对比

# Visual Studio

---

一般指Microsoft Visual Studio，其包括了开发过程中的UML工具、代码管控工具、集成开发环境 **IDE** 。所写代码可用于微软支持的所有平台。

- ​

# .Net/.Net Framework

---

## CLI  **通用语言基础架构**

Common Language Infrastructure，简称CLI 。是一个开放的技术规范。

通用语言基础架构定义了构成.NET Framework基础结构的可执行码以及代码的运行时环境的规范，它定义了一个语言无关的跨体系结构的运行环境，这使得开发者可以用规范内定义的各种高级语言来开发软件，并且无需修正即可将软件运行在不同的计算机体系结构上。

对CLI的实现（略）

- **Microsoft .NET Framework - 微软提供的面向Windows系统的实现，提供了各种各样的程序库，工具等。**
- Microsoft Silverlight - 微软提供的一个跨平台实现，能同时在Windows和Macintosh操作系统上运行。
- .NET Compact Framework - 微软提供的面向便携式系统的商用实现。
- Microsoft XNA - 微软提供给游戏开发人员使用的一个CLI，面向的是XBOX和Windows Vista。
- Rotor - Microsoft Shared Source CLI（Rotor）微软开发出来的一个在Window,Mac OS X和FreeBSD上运行的一个CLI实现，但微软并没有授权用Rotor开发商业程序，只是一个学习工具。
- Mono - 由Novell赞助开发的开源实现，它能够应用于Linux，Mac OS等多种操作系统。
- dotGNU - dotGNU项目也是一个开源并且自由的实现。

## _.NET Framework_ 是微软公司的 **系统框架** ，是用于Windows的新托管代码 **编程模型** 。是对CLI的一种实现。

NET Framework包括了三大部分：

1. 第一个部分是 **Common Language Runtime** ( **CLR，** 所有.NET 程序语言公用的执行时期组件)，
2. 第二部分是共享 **对象类别库** (提供所有NET 程序语言所需要的基本对象)，
3. 第三个部分是重新以 **组件** 的方式写成的(旧版本则是以asp.dll提供ASP网页所需要的对象)。
  1.  **公共语言运行** 环境是NET Framework的基础。可以将 **运行库** 看作一个在<执行时管理代码>的 **代理** 。它提供内存管理、线程管理和远程处理等核心服务，并且还强制实施严格的类型安全以及可提高安全性和可靠性的其他形式的代码准确性。
  2.  NET Framework的另一个主要组件是 **类库** ，它是一个综合性的面向对象的可重用类型集合，可以使用它开发多种应用程序，这些应用程序包括传统的命令行或图形用户界面(GUI) 应用程序，也包括基于所提供的最新创新的应用程序(如Web窗体和XML Web services)。

   **代码管理的概念是运行库的基本原则** 。托管代码是指用来构成运行库的代码，而不以运行库为目标的代码称为非托管代码。 **同时，NET Framework可由非托管组件承载。** 这些组件将公共语言运行库加载到它们的进程中并启动托管代码的执行。

  从而创建一个可以同时利用托管和非托管功能的软件环境。NET Framework不但提供若干个运行库宿主，而且还支持第三方运行库宿主的开发。

NET Framework的功能

1. 软件向多样化的移动组件发展，并根据这种事实提供保护。在一个细化的、可扩展的策略和许可系统下，用户能够运行功能强大的代码，而同时减少相关的风险。在没有运行时对用户作出信任决定时，管理员可以在各个级别创建强壮的安全策略。策略是完全可定置的。
2. 它支持C#开发网页程序，他运行的服务器是IIS，这种开发模式又称之为 **ASP.net** 。

  NET Framework提供了应用程序模型及关键技术，让开发人员容易以原有的技术来产生、布署，并可以继续发展具有高安全、高稳定，并具高延展的 [Web Services](http://baike.baidu.com/link?url=gqduLCpsvrW-y8GJ8fUi-Y-eRNczQ22fCWicf6fWVUDMXTIRB07TzWpWeKSpXuS1Qh-K4rJgRmnY_l7Zypjt1scK-iqIHYALHt3w5WdnK43#2) 。

  对于NET Framework而言，所有的组件都可以成为Web Services，Web Services只不过是另一种型态的组件罢了。NET Framework以松散的方式来栓锁Web Services这种型态的组件。这样的结果让开发人员非常容易的发展出强而有力的Web 服务组件，提高了整体的安全及可靠性，并且大大的增加系统的延展性。

3. Net FrameWork是微软提供的一整套支持C系列各种语言的API和各种丰富的资源框架。可以帮助开发者快速便捷轻松的开发出复杂度较高的高级程序和网页.

## .NET平台编译过程（如右图）

1. CLI是标准。
2. .NET Framework是对CLI标准的实现形式之一。
3. CLR是.NET Framework里面的虚拟机。

## 区别：CLI与CIL

 **CIL，公共中间语言（Common Intermediate Language）** 

CIL，简称微软中间语言（MSIL）或者中间语言（IL）。

 **过程** ：CIL是编译器将.NET代码编译成公共语言运行时（CLR）能够识别的中间代码。它是一种介于高级语言（例如C#）和CPU指令之间的一种语言 **。当用户编译一个.NET程序时，编译器（例如VisualStudio）将C#源代码编译转换成中间语言 (MSIL)，它是一种能够被CLR转换成CPU指令的中间语言** 。当执行这些中间语言时，CLR提供的实时（JIT）编译器将它们转化为CPU特定的代码。

 **CLI，公共语言基础架构（Common Language Infrastructure）** 

CLI是一个开放的技术规范。

通用语言基础架构定义了构成.NET Framework基础结构的可执行码以及代码的运行时环境的规范，它定义了一个语言无关的跨体系结构的运行环境，这使得开发者可以用规范内定义的各种高级语言来开发软件，并且无需修正即可将软件运行在不同的计算机体系结构上。CLI有时候会和CLR混用。但严格意义上说，这是错误的。因为CLI是一种规范，而CLR则是对这种规范的一个实现。

![](https://static.notion-static.com/9fd3d63785934245ae83f0831edb0f65/681873-20151205145611580-1180801416AA.png)

 **实际意义** ：.NET的世界中可能出现下面的情况一部分代码可以用C++实现，另一部分代码使用C#或VB.NET完成的，但是最后这些代码都将被转换为中间语言。又由于公共语言运行库支持多种实时编译器，因此同一段中间语言代码可以被不同的编译器实时编译并运行在不同的CPU结构上。

---

 **综上；一个.net平台包括：C#等语言的编译器/CLI/类库** 。

当我们在开发一个项目时，可任意使用.net 平台所支持的各种语言(C#、F# 和 Visual Basic .NET)。在编译器(如Visual Studio)中被编译成公共中间语言(Common Intermediate Language)。这一步骤实现跨语言编程。对于CLI有各种各样的实现方式，但都包含了公共语言运行库CLR。CIL中间语言可以在CLR编译下运行在不同的CPU上，实现跨平台编程。

## <跨语言可互操作>相关规范

 **CTS，通用类型系统（Common Type System）** 

CTS是一种类型系统和语言规范，它能够确保CLR能够识别和处理的类型，所有.NET开发语言中的类型，无论时VS.NET类型还是C#.NET类型最终都会被编译成CLR能够识别的CTS类型，因此CTS是.NET平台类型的抽象。例如VB.NET中的integer类型和C#中的int类型都编译成CTS的System.Int32类型。如果某种语言编写的程序能够在CLR上运行，并不能说明这种语言完全符合CTS的规范。例如使用C++编写的代码，部分代码并不符合CTS规范，在编译时把这部分不符合CTS的代码会被编译成原始代码本地CPU指令而非中间代码。

 **CLS，公共语言规范（Common Language Specification）** 

CLS是CTS的一个子集，所有.NET语言都应该遵循此规则才能创建与其他语言可互操作的应用程序，但要注意的是为了使各语言可以互操作，只能使用CLS所列出的功能对象，这些功能统称为与CLS兼容的功能，它是在.NET平台上运行语言的最小规范，正因为.NET上不同语言能够轻松交互一样，例如C#编写程序时可以直接引用并使用VB.NET编写的类库。为了达到这样的交互，才制定出CLS规范，在.NET框架本身提供的所有类库（并非所有）都是与CLS兼容的，在查看MSDN文档时，不兼容的类和方法都被特别标记为不兼容，例如C#中的System.UInt32就标记为”此API不兼容CLS。兼容 CLS的替代API为 Int64。“，这说明并不是所有的语言(例如VB.NET或J#)都支持无符号的数据类型，但这种数据类型与CLS不兼容的。

## <相关类库>

 **BCL，基础类库（Base Class Library）** 

BCL是一个公共编程框架，称为基类库，所有语言的开发者都能利用它。

是CLI（Common Language Infrastructure，公共语言基础结构）的规范之一，主要包括：执行网络操作，执行I/O操作，安全管理，文本操作，数据库操作，XML操作，与事件日志交互，跟踪和一些诊断操作，使用非托管代码，创建与调用动态代码等，粒度相对较小，为所有框架提供基础支持。

 **FCL，框架类库（Framework Class Library）** 

FCL提供了大粒度的编程框架。

它是针对不同应用设计的框架 ，FCL大部分实现都引用了BCL，例如我们常说的开发框架：ASP.NET、MVC、WCF和WPF等等，提供了针对不同层面的编程框架 。

## [上述.NET名词解释原链接](http://www.cnblogs.com/cn-chenhao/p/5001534.html)

# Java开发与.Net开发对比

---

## Java开发工具

JDK : Java Development ToolKit(Java开发工具包)。

 **外语首字母缩写：SDK、外语全称：Software Development Kit** 

JDK是整个JAVA的核心，包括了Java运行环境（Java Runtime Envirnment），一堆Java工具（javac/java/jdb等）和Java基础的类库（即Java API 包括rt.jar）。

JDK有以下三种版本：

J2SE，standard edition，标准版，是我们通常用的一个版本J2EE，enterpsise edtion，企业版，使用这种JDK开发J2EE应用程序J2ME，micro edtion，主要用于移动设备、嵌入式设备上的java应用程序。我们常常用JDK来代指Java API，Java API是Java的应用程序接口，其实就是前辈们写好的一些java Class，包括一些重要的语言结构以及基本图形，网络和文件I/O等等 ，我们在自己的程序中，调用前辈们写好的这些Class，来作为我们自己开发的一个基础。当然，现在已经有越来越多的性能更好或者功能更强大的第三方类库供我们使用。

JRE:Java Runtime Enviromental(java运行时环境)。

也就是我们说的JAVA平台，所有的Java程序都要在JRE下才能运行。包括JVM和JAVA核心类库和支持文件。与JDK相比，它不包含开发工具——编译器、调试器和其它工具。

JVM：Java Virtual Mechinal(JAVA虚拟机)。

JVM是JRE的一部分，它是一个虚构出来的计算机，是通过在实际的计算机上仿真模拟各种计算机功能来实现的。JVM有自己完善的硬件架构，如处理器、堆栈、寄存器等，还具有相应的指令系统。JVM 的主要工作是解释自己的指令集（即字节码）并映射到本地的 CPU 的指令集或 OS 的系统调用。Java语言是跨平台运行的，其实就是不同的操作系统，使用不同的JVM映射规则，让其与操作系统无关，完成了跨平台性。JVM 对上层的 Java 源文件是不关心的，它关注的只是由源文件生成的类文件（ class file ）。类文件的组成包括 JVM 指令集，符号表以及一些补助信息。

## Java的编译与执行

1. 保存->产生Hello.java
2. 编译(工具:javac编译器把Java源程序编译成字节码)->产生Hello.class类文件

  cmd：javac [Hello.java](http://hello.java) 

3. 执行(工具:java解释器从类文件执行Java应用程序)

  cmd：java Hello （注意无需加.class）
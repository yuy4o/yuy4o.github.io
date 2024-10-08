---
title: Python General
author: yuyao
date: 2024-09-14 23:39:20 +0800 
categories: [Projects, python]
tags: [python]
---

### 静态类型语言 vs 动态类型语言

静态类型语言编译为什么要转换成机器码，但动态类型语言不需要转成机器码？

静态类型语言和动态类型语言在编译和执行模型上的差异主要源于它们的设计目标、类型系统和运行时环境。以下是两者在编译和执行时的区别及原因：

静态类型语言编译成机器码的原因：

性能优化：静态类型语言通常在编译阶段进行类型检查和优化，从而生成高效的机器代码。这种机器代码可以直接由计算机的处理器执行，具有较高的执行效率。

类型安全：在编译阶段进行类型检查，确保在运行时不会出现类型错误。编译器在这个阶段将类型信息转换为机器码，这样运行时环境就不需要再进行类型检查。

避免解释开销：编译为机器码后，可以避免在运行时解释代码所需的开销，提升了性能。这对于要求高性能的应用（如游戏开发、系统编程）尤其重要。

典型的静态类型语言：C、C++、Java、Go等语言，它们在编译后生成独立的可执行文件，这些文件可以直接在目标平台上运行。

动态类型语言直接解释执行的原因：

灵活性：动态类型语言在设计上允许变量的类型在运行时被更改，因此它们需要在执行时对类型进行检查。这种动态检查提供了更大的灵活性，但也意味着不能事先编译为高效的机器码。

快速开发：动态类型语言通常用于快速原型开发和脚本编写，开发者可以迅速编写和测试代码，省去编译的过程，提高开发效率。

可以编译的动态语言：

尽管动态类型语言通常不编译成机器码，但一些动态语言（如 JavaScript 和 Python）可以使用 JIT（即时编译）技术或其他编译工具将代码编译为中间表示（字节码），以提高性能。

例如，Python 可以将代码编译为字节码，在 Python 虚拟机上运行，而 JavaScript 引擎也可以在运行时将代码编译为机器码。

总结

静态类型语言通常在编译阶段生成高效的机器码，以获得更好的性能和类型安全。编译器在此阶段进行全面的检查和优化，生成可以在目标平台上高效执行的可执行文件。

动态类型语言主要通过解释器直接执行代码，允许更大的灵活性和快速开发，但相对而言性能较低，且在运行时进行类型检查。

因此，静态类型语言和动态类型语言在编译和执行的差异主要体现在性能需求、类型系统、开发方式和运行时环境上。


### 函数结尾 `pass` vs `return`


### 系统路径

当前文件的绝对路径： `os.path.abspath(__file__)`

当前文件所在的目录： `os.path.dirname(os.path.abspath(__file__))`

当前的工作目录（即从哪个目录启动运行 Python 解释器的目录）执行脚本的目录： `os.getcwd()`

相对路径： `os.path.relpath(os.path.abspath(__file__), os.getcwd())`
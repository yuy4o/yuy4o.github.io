---
title: Sublime Text配置Build System（MacOS ARM64）
author: yuyao
date: 2023-04-29 01:26:40 +0800 
categories: [System, software]
tags: [sublime]
---

![sublime.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/230429sublime.webp)

最近发现Sublime Text作为一款编辑器真的好用。虽然没有VS code功能繁多，但简洁朴素，体量轻便。只要不是做什么工程项目（用JetBrains或者VS），写写Python, C++的代码片段(Snippet)完全够用，美中不足的是不支持Jupyter Notebook（在苹果M1芯片上未找到解决方案）。以下是今天摸索出的C++和MPI的配置文件，针对`MacOS ARM64`。

### C++11.sublime-build

```c++
{   
    "cmd": ["g++", "${file}", "-o", "${file_path}/${file_base_name}"],
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c++",
    "variants":
    [
        {
            "name": "Compile",
          	// 可根据需要设置g++ -std=c++17, c++2a等
            "cmd": ["zsh", "-c", "g++ -std=c++11 '${file}' -o '${file_path}/${file_base_name}'"] 
          	// 可编译后打开终端，在终端查看结果
            // && open -a Terminal.app '${file_path}/${file_base_name}'
        },
        {
            "name": "Run",
            "cmd": ["zsh", "-c", "'${file_path}/${file_base_name}'"]
        }
    ]
}
```

### MPI.sublime-build

```c++
{    
    "cmd": ["mpic++","mpiexec", "-n", "${file}", "-o", "${file_path}/${file_base_name}"],
    "file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
    "working_dir": "${file_path}",
    "selector": "source.c++",
    "variants":
    [
        {
            "name": "Complile",
            "cmd": ["zsh", "-c", "mpic++ '${file}' -o '${file_path}/${file_base_name}'"]
        },
        {
            "name": "Run",
            // 此处设置默认线程数为4
            "cmd": ["zsh", "-c", "mpiexec -n 4 '${file_path}/${file_base_name}'"]
        }
    ]
}
```
`Page Screenshot`
![screenshot.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/230429screenshot.png)

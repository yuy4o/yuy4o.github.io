---
title: Ubuntu安装Mojo
author: yuyao
date: 2023-11-30 17:45:40 +0800
categories: [System, software]
tags: [mojo]
---

## 运行环境
- Ubuntu 22.04（要求Ubuntu 20.04或之后）
- Python 3.10（要求Python 3.8 - 3.10）
- x86-64 CPU，最小4G RAM
- g++ 或 clang++ 编译器

## 安装步骤

1. **安装 Modular CLI**

    `curl https://get.modular.com | sh - && modular auth mut_cccd224218bb423e8786415077b8cb7e`

    ![cli.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130cli.png)

2. **安装 Mojo SDK**

    `modular install mojo`

    - 可能出现问题1：modular: error: failed to run python

        ![error1.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130error1.png)

    - 解决1：`sudo apt install python3.10-venv`

        ![soln1.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130soln1.png)

    - 可能出现问题2：modular: error: failed to run python

        ![error2.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130error2.png)

    - 解决2：多次尝试 `sudo apt install python3.10-venv`

    **每次 `modular install mojo` 运行失败，运行 `modular clean` 清除**

3. **成功安装**

    ![success.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130success.png)

4. **配置路径及"Hello, world!"**

    If you are using ZSH (default on macOS), run the following commands:

    ```shell
    echo 'export MODULAR_HOME="$HOME/.modular"' >> ~/.zshrc

    echo 'export PATH="$HOME/.modular.modular/pkg/packages.modular.com_mojo/bin:$PATH"' >> ~/.zshrc

    source ~/.zshrc
    ```

    If you are using bash, run the following commands:

    ```shell
    BASHRC=$( [ -f "$HOME/.bash_profile" ] && echo "$HOME/.bash_profile" || echo "$HOME/.bashrc" )

    echo 'export MODULAR_HOME="$HOME/.modular"' >> "$BASHRC"

    echo 'export PATH="$HOME/.modular/pkg/packages.modular.com_mojo/bin:$PATH"' >> "$BASHRC"

    source "$BASHRC"
    ```
    **修改路径时，"$HOME/.modular"比如是 "/home/yuy4o/.modular"，不可写成 "~/.modular"，source时可能识别不出 ~**

    ![demo.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130demo.png)


## 附录

[Mojo使用文档](https://docs.modular.com/mojo/)

[官方教程链接](https://developer.modular.com/download)

[个人参考链接1](https://www.ewbang.com/community/article/details/961944197.html)

[个人参考链接2](https://www.bilibili.com/read/cv26616475/)
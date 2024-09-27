---
title: Linux General
author: yuyao
date: 2024-04-22 15:46:16 +0800 
categories: [System, software]
tags: [linux]
---

## Linux 发行版本

Linux 发行版（Linux distributions）是基于 Linux 内核的操作系统的不同版本，它们在系统管理、用户界面、默认软件和包管理等方面有所不同。以下是不同 Linux 发行版之间的关系及分类：

**1.Linux 内核**

所有 Linux 发行版都基于 Linux 内核，这是 Linux 操作系统的核心。内核负责管理硬件资源、提供系统调用和执行用户程序

Linux 内核使用 GNU GPL 许可证，这要求衍生作品也必须开源。相应地，FreeBSD 使用 BSD 许可证，这种许可证允许将代码用于专有软件，并且不要求衍生作品也必须开源

**2.主要发行版家族**

Linux 发行版可以按照不同的标准进行分类，这些标准通常包括包管理系统、桌面环境、目标用户群体等。以下是一些主要的发行版家族及其代表性发行版：

*a. Debian 家族*

Debian：一个稳定、广泛使用的发行版，重视系统的稳定性和可靠性。它使用 .deb 包和 dpkg 包管理系统

Ubuntu：基于 Debian 的发行版，旨在提供用户友好的体验。Ubuntu 每六个月发布一个新版本，并且有多个变体，例如 Ubuntu Desktop、Ubuntu Server 和 Ubuntu LTS（长期支持）

Linux Mint：基于 Ubuntu（有时基于 Debian），专注于易用性和桌面体验，提供多种桌面环境，如 Cinnamon 和 MATE

*b. Red Hat 家族*

Red Hat Enterprise Linux (RHEL)：企业级发行版，提供稳定的支持和维护，主要用于商业环境。使用 .rpm 包和 yum 包管理系统

CentOS：基于 RHEL 的免费版本，提供与 RHEL 相同的源代码，但没有官方支持。CentOS 8 已经被 CentOS Stream 取代，后者是 RHEL 的滚动更新版本

Fedora：由 Red Hat 资助的社区驱动发行版，旨在提供最新的软件和技术。是 RHEL 的上游开发版本，也使用 .rpm 包和 dnf 包管理系统

*c. SUSE 家族*

openSUSE：一个社区驱动的发行版，提供稳定的版本和滚动更新的版本（openSUSE Leap 和 openSUSE Tumbleweed）。使用 .rpm 包和 zypper 包管理系统

SUSE Linux Enterprise Server (SLES)：企业级发行版，提供商业支持和长期维护

*d. Arch 家族*

Arch Linux：一个以简约为原则的发行版，提供最新的软件和用户控制的安装体验。使用 pacman 包管理系统

Manjaro：基于 Arch 的发行版，提供更易用的安装和用户体验，同时保留了 Arch 的灵活性

*e. Gentoo 家族*

Gentoo：一个源代码发行版，允许用户根据自己的需求编译和优化软件。使用 Portage 包管理系统

Calculate Linux：基于 Gentoo 的发行版，提供了开箱即用的桌面和服务器环境

**3.发行版间的关系**

衍生版（Derivatives）：许多发行版是其他发行版的衍生版。例如，Linux Mint 是 Ubuntu 的衍生版，Kali Linux 是 Debian 的衍生版

社区和企业支持：一些发行版，如 Fedora 和 CentOS，作为 Red Hat 的开发版本和社区版本，具有紧密的关系。Debian 和 Ubuntu 之间的关系也是非常显著，Ubuntu 基于 Debian 并继承了其许多特性

包管理系统：不同 Linux 发行版使用不同的包管理系统。例如，Debian 和 Ubuntu 使用 APT（Advanced Package Tool） 和 dpkg，Red Hat 和 Fedora 使用 RPM（Red Hat Package Manager） 和 dnf（或 yum），Arch 使用 pacman，而 Gentoo 使用 Portage（FreeBSD 使用 Ports Collection 系统和 pkg 包管理器）

**4.选择适合的发行版取决于个人需求和使用场景**

用户友好性：如果你是新手，可以考虑 Ubuntu、Linux Mint 或 Fedora

企业环境：RHEL 和 SLES 提供了企业级支持，适合商业环境

高级用户和开发者：Arch Linux 和 Gentoo 提供了高度的自定义和控制

[最全Linux的发行版简介，一文读懂各发行版之间的联系和区别](https://cloud.tencent.com/developer/article/1114589)

[浅谈Linux下dpkg、apt-get、yum和rpm命令的区别](https://cloud.tencent.com/developer/article/1759038)

[维基-Linux发行版列表](https://zh.wikipedia.org/wiki/Linux%E5%8F%91%E8%A1%8C%E7%89%88%E5%88%97%E8%A1%A8)

[维基-Linux发行版](https://zh.wikipedia.org/wiki/Linux%E5%8F%91%E8%A1%8C%E7%89%88)

![240421linuxpkg](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/240421linuxpkg.png)

[DistroWatch.com](https://distrowatch.com/)

[Rpmfind mirror](https://www.rpmfind.net/)

## Community

[LINUX DO](https://linux.do/)

[Linux迷](https://www.linuxmi.com/)

[Linuxeden](http://www.linuxeden.com/) 

<!-- [Linuxeden <font color="red" face="Times New Roman" size=1>网址换http</font>](https://www.linuxeden.com/) -->

[Linux中国](https://linux.cn/)

[Linuxfans](http://www.linuxfans.org)

## Course

[计算机教育中缺失的一课](https://missing-semester-cn.github.io/)

[linuxcommand.org](https://linuxcommand.org/)
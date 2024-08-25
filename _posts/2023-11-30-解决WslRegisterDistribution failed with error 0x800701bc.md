---
title: 解决WslRegisterDistribution failed with error 0x8007019e
author: yuyao
date: 2023-11-30 01:03:40 +0800 
categories: [System, software]
tags: [wsl]
---

![wsl.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130wsl.png)

### 问题：安装并打开Ubuntu 22.04.2 LTS 报错 WslRegisterDistribution failed with error: 0x8007019e

![question.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130question.png)

### 步骤一：完善电脑设置

`控制面板` - `程序` - `程序和功能` - `启用或关闭Windows功能`，如下图，`Hyper-V` 和 `虚拟机平台` 不需要打开，只要打开 `适用于Linux的Windows子系统` 即可使用WSL。`Hyper-V` 是微软开发的虚拟化平台，WSL作为 Linux内核和 `Hyper-V` 没有依赖关系。对于Docker Desktop，`Hyper-V` 或 `WSL2` 都可作为其后端，`WSL2` 性能会更好

![check.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130check.png)

### 步骤二：安装WSL更新包

You can fix this issue by install this package: https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi

More detail here:

https://learn.microsoft.com/zh-cn/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package

### 问题解决
![result.png](https://raw.githubusercontent.com/yuy4o/yuy4o/main/figures/231130result.png)


## 资料来源

https://learn.microsoft.com/en-us/answers/questions/1152199/wslregisterdistribution-failed-with-error-0x800701

https://www.bilibili.com/video/BV1cP41137bV/?spm_id_from=333.337.search-card.all.click&vd_source=890879be0041154ef8107bc3fadcc7c4


## [个人视频总结](https://www.bilibili.com/video/BV1yK42147E5/?spm_id_from=333.999.0.0)
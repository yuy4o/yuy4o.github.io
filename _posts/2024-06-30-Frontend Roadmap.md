---
title: 【转】Frontend Roadmap
author: yuyao
date: 2024-06-30 22:58:40 +0800
categories: [Trends, exp]
tags: [repost]
---
> 如有侵权，请联系 `yuyao.jiang22@gmail.com` 删除。

鱼皮哥的今晚前端路线不是很详细，所以本文诞生了，很长时间没发文了，诸君共勉！

注意本文适合纯前端乃至想要进阶全栈的同学，我会尽量把各个关键点列出

## 基础阶段

+ HTML：**HTML4**到**HTML5**，一些新特性要了解，比如`contenteditable`属性
+ CSS：**CSS**方面比较关键，分几个节点
  + 第一个阶段：熟悉基本语法到**CSS3**
  + 第二个阶段：学会运用预处理器如**Less**，**Sass**，学会**CSS Module**（普通实习够了）
  + 第三个阶段：学会原子化CSS如**TailwindCSS**，**UnoCSS**（进阶）
  + 第四个阶段：学会运用后处理器**PostCSS**，运用各个插件（进阶）
+ JavaScript：**JavaScript**主要为如下
  + 基本语法，操作DOM，BOM等
  + **ES6+**后的语法
  + 正则表达式
  + 设计模式（**发布订阅**模式建议学好，很常用，其他如单例模式了解即可）
  + **TypeScript**：JS的超集，我的建议是在学完js后就先了解好ts的基本语法，对以后有帮助
  + Canvas（可选，有2D和3D）
+ 数据结构和算法：学好这个对后面的源码部分有帮助
  + 数组：队列，链表，哈希表等等
  + 排序：双指针，**二分**（比较重要）等等
+ 数据交互：这块就是和后端交流最多的地方了，也分阶段
  + （基本）Ajax：学好最基础的交互方法
  + （基本）**Axios**：Ajax的封装常用库，分几个小阶段
    + 掌握基本用法
    + **进阶**就是你用Ajax自己封装出一个简单的Axios
    + **更进一步**就是二次封装axios，这点在项目中很多
  + （基本）Fetch：建议掌握
  + （进阶）WebSocket，SSE
  + （**必备**）网络模式，HTTP协议，TCP三次握手四次挥手等，就是计算机网络部分，部分大公司很看重

## 提升阶段

+ 包管理工具，目前较多，基本只需了解命令，进阶的话需要了解工作区等概念
  + **npm**（node官方）
  + cnpm（不推荐了现在）
  + yarn（一般）
  + **pnpm**（推荐，在速度方面很快且在后续的Monorepo项目中运用多）
+ 工程化：即构建工具一类，目前来说你想学深必须学好这里，如果很急的话暂时可以跳过，但不急的话建议先学懂这块再去学框架会更好
  + **Webpack**：老牌常用的工具，进阶就是会定制插件
  + **Vite**：新生代，构建很快，进阶就是会定制插件
  + Gulp：不推荐了
  + EsBuild：可选
  + SWC：可选
  + **Babel**：让我们使用新语法和 api，babel 会在编译中转为目标环境的支持的语法（进阶必学）
+ 项目管理：**Git**，学会多提交github代码，这里不多表述
+ 框架：主要分几个
  + **React**：生态丰富，主要学好**hooks**，函数式编程已成主流，基本的库如下
    + **React-Router**：路由
    + **Redux**：状态管理，也有其替代如**Zustand**也用的多
    + **Antd**：UI库，我的建议是学的时候可以自己尝试用原生写一个类似的组件，因为企业中的需求很多不一样，需要自己定制一些UI组件库（后面UI库单独列一下）
    + 进阶的一些如动画库 react-transition-group，可以根据需求寻找
  + **Vue**：生态丰富，现在Vue2版本虽然停止维护，但还是建议学，很多面试会问Vue2和Vue3的区别
    + **Vue-Router**：路由
    + **Vuex**：状态管理，有**Pinia**替换
  + Angular：老牌，但国内用的少，需要掌握 Rxjs
  + Solid：新生，国内用的少
+ UI组件库单独：
  + PC端
    + Element UI
    + Ant Design
    + IView
  + H5端
    + Vant（用的最多）
    + Muse UI
  + 小程序：（一般来说大前端包括小程序）
    + Vant和iview

## 进阶阶段

一般来说你学会前面的时候，运用好框架做好项目就可以实习了，这时候只要基础好基本没问题

下面的内容就是进阶部分了，一般来说在实习不会问，源码方面大公司问的多，普通实习的同学了解即可

+ **SSR**服务器渲染：有利于SEO搜索引擎优化，一般是**进阶学习**
  + NuxtJS（运用在Vue框架）
  + NextJS（运用在React框架）

+ 小程序：大部分公司都是前端写小程序，所以有必要还是学一下，实习的话一般不需要

  + 原生小程序（不推荐）
  + **Uniapp**
  + **Taro**

+ 跨端：如安卓，iOS

  + **Uniapp**：用的挺多
  + Flutter：这个可选，因为需要学习一门新的语言dart，所以难度较高
  + **HTML5 Plus**：挺常用的
  + **Hybrid**：很常用，可以嵌入到原生安卓和ios开发
  + **ReactNative**：React的跨端，学过react的话上手难度很低，很不错

+ **源码**：这块很多问的大多都是框架的底层，很多大公司会问，建议多看网上八股和看源代码

  + Vue：如v2和v3底层实现，diff算法等等
  + React：如fiber架构，hooks的区别等

+ 可视化：可选，一些公司用，技术如Echarts，DataV，Ucharts等

+ 微前端：可选，进阶学，大公司一般有用

  + 乾坤（阿里）
  + macro APP（京东）
  + 无界（腾讯）

+ **服务器**：想要进阶的必备

  + Linux的基础
  + Nginx基础，Nginx的插件，lua语言
  + **Pm2**: 很常用的服务器库，**进阶必备**

+ **技术方案**：各个需求的整合

  + 主题切换：如白天黑夜

  + 数据埋点和服务监控：大公司非常常用！

  + 性能监控和指标分析：作为高级工程师必须考虑好性能问题

  + **monorepo**：该项目想要用到另一个项目的东西，就需要这个技术了，目前pnpm方案很不错

    > 很大一部分你所熟知的项目都是该架构，如 React框架

  + 国际化：如果需要发布在外国，就需要该技术的支持了

+ **NodeJS**：它是贯穿整个项目的基石，各个包各个库都是通过node来运作，作为JavaScript的运行时，它的重要性无可置疑

  + 包管理工具，上面已有概述

  + 核心模块：如process，**child_process**，net，os，util等

  + Express：前端变全栈的基石

    + **Koa**：集成框架，流行度高
    + Egg：不推荐，毕竟该项目业务团队都没了
    + **Nest**：很流行的框架，尤其在国外用的很多

  + **Mysql**：学会数据库才知道后端，所用技术为**mysql2**

  + **ORM**：调用数据库的集成框架

    + Knex：新手上手
    + Prisma：最常用的框架，集成了多种数据库

  + **Redis**：内存数据结构存储系统，很常用，使用技术为**ioredis**

  + **lua**：一种轻量级、高效、可嵌入的脚本语言，在**自动化**方面很常用

  + **serverLess**：无服务器架构模式，建议学

  + **爬虫**：没想到吧，node也可以做爬虫相关的，所用技术为**puppeteer**

  + 学无止境，node还有定制脚手架，定制命令行交互，甚至可以做嵌入式！

## 学无止境阶段

 这个阶段一般来说就是选择自己感兴趣的了，学习的路线远不止这些，各类技术层不出穷

我只介绍一部分仅供扩展视野

+ SSG技术：静态站点生成

  + **VitePress**：很常用的SSG技术框架
  + Next：支持SSG
  + Rspress：字节开源的基于rust的ssg框架

+ 桌面开发：

  + **Electron**：常用的跨桌面端开发框架
  + NW.js：以前常用的框架
  + **Tarui + Rust**：新生代构建

+ **Web**系列：目前来说很多地方都有用，但只有用到的时候才学

  + WebGL：专门做图形绘制和渲染的

    + **three.js**框架：3D渲染
    + openGL：需要学**着色器**语言，学习图形学
    + 数学：做图形绘制需要用到数学的向量、矩阵、三角函数等等

  + WebRTC：该技术主要用于**音视频通话**，浏览器录屏等

  + Web Socket：主要用于**聊天室**等等

  + Web Worker：允许我们在 js 主线程之外开辟新的 Worker 线程，并将一段 js 脚本运行其中，它赋予了开发者利用 js 操作**多线程**的能力。

  + Web SQL、IndexDB：存储大量客户端数据，推荐IndexDB

  + Web Components：用于构建可复用用户组件的技术

  + Web Assembly：简称wasm，一种通用字节码技术，它可以将其他编程语言（如 Go、Rust、C/C++ 等）的程序代码编译为可在**浏览器环境**直接执行的字节码程序。

    > 想不到吧，浏览器也可以跑C和C++这种代码

  + Web GPU：用于在 Web 应用程序中访问 **GPU** 的功能，js也能调**硬件**！

  + Web View：跨端中为什么h5可以做呢，就是运用它，可以在原生中通过网络引入h5从而嵌入

  + Web AR：通过传感器等实现智能交互等

  + Web Serial：允许网站从串行设备通过脚本读取和写入的方式微控制器、3D 打印机和其他串行设备等设备进行通信的一套 API，通过它我们就可以和**单片机**通信了！神奇不！

  + Web Containers：基于wasm的系统，可在浏览器端启动**nodejs**环境！

+ JavaScript运行时：新生代有**bun**包子技术

+ 区块链：Web3JS技术

+ 游戏开发：Cocos，虚幻五

+ 嵌入式开发：Ruff js

+ 人工智能：TensorFlow和face-api

  以上知识仅供参考，有可能打错了嘿嘿，学习的路线永无止境，加油吧同志们！
---
layout: post
title:  "项目经历"
date:   2022-08-26 15:34:36 +0800
categories: jekyll update
---



# 项目经验 


<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [项目经验](#项目经验)
  - [**1.跨平台即时通讯系统（Go，C#，JS，Kotlin，Gin，Vue）**](#1跨平台即时通讯系统gocjskotlinginvue)
    - [1.1 简介](#11-简介)
    - [1.2 技术细节](#12-技术细节)
    - [1.3 功能演示](#13-功能演示)
    - [1.4 项目仓库](#14-项目仓库)
  - [**2.线上预约陪诊系统（Java，JS，micro-service，Vue）**](#2线上预约陪诊系统javajsmicro-servicevue)
    - [2.1 简介](#21-简介)
    - [2.2 技术细节](#22-技术细节)
    - [2.3 功能演示](#23-功能演示)
    - [2.4 项目仓库](#24-项目仓库)
  - [**3.FeedManger Rss订阅管理系统（ASP.NET Web Forms，EF，C#，HTML，JavaScript）**](#3feedmanger-rss订阅管理系统aspnet-web-formsefchtmljavascript)
    - [3.1 简介](#31-简介)
    - [3.2 技术细节](#32-技术细节)
    - [3.3 功能演示](#33-功能演示)
    - [3.4 项目仓库](#34-项目仓库)
  - [**4.Android端数独小游戏（Android，Java）**](#4android端数独小游戏androidjava)
    - [4.1 简介](#41-简介)
    - [4.2 技术细节](#42-技术细节)
    - [4.3 功能演示](#43-功能演示)
    - [4.4 项目仓库](#44-项目仓库)
  - [**5.BitChat-C语言聊天室（C，tcp/socket，mysql，linux）**](#5bitchat-c语言聊天室ctcpsocketmysqllinux)
    - [5.1 简介](#51-简介)
    - [5.2 技术细节](#52-技术细节)
    - [5.3 功能演示](#53-功能演示)
    - [5.4 项目仓库](#54-项目仓库)
  - [**6.pipe cpu（Verilog，FPGA）**](#6pipe-cpuverilogfpga)
    - [6.1 简介](#61-简介)
    - [6.2 技术细节](#62-技术细节)
    - [6.3 功能演示](#63-功能演示)
    - [6.4 项目仓库](#64-项目仓库)
  - [**7.操作系统实验（C，Linux，Windows，OS）**](#7操作系统实验clinuxwindowsos)

<!-- /code_chunk_output -->




## **1.跨平台即时通讯系统（Go，C#，JS，Kotlin，Gin，Vue）**
本科毕业设计
###  1.1 简介
本课题使用WebSocket和SignalR来实现一个简单的跨平台实时通讯应用。该应用允许用户在Web浏览器或Android App上进行实时聊天，支持私聊，群聊，广播，发送文本及图片消息以及传输文件。同时课题也实现了一套流式数据传输的演示程序，以模拟物联网系统中需要处理流式数据的应用场景，如智慧医疗系统中对患者生命体征数据的监控。
###  1.2 技术细节
- 语言及框架：
    - C#，Go，Kotlin，JavaScript
    - .NET WebAPI，Gin，Vue，Gorm，MySQL，JWT
- 服务器搭建：
    - 采用前后端分离的架构构建。
    - 服务器使用.NET Web API框架（结合SignalR组件）和Go语言的开源库Gorilla/Websocket两种技术方案分别实现。
    - 使用MySQL存储用户信息，使用JWT进行身份认证与鉴权。
- 客户端实现：
    - Web端使用Vue框架开发，Android使用Kotlin语言开发。
    - 在Web端针对基于SignalR的服务器和基于Go（WebSocket）的服务器分别设计封装了两套不同的通信接口。
    - Web端使用SignalR的JS语言支持与服务器（基于SignalR）通信。使用原生HTML5原生Websocket支持与服务器（基于Go）通信。
    - Android使用Kotlin开发，使用SignalR的Java语言支持与服务器（基于SignalR）通信。

###  1.3 功能演示
- [实时通信系统功能演示视频（点击跳转）](https://www.bilibili.com/video/BV17W4y1t73n)
    <iframe src="//player.bilibili.com/player.html?aid=942472997&bvid=BV17W4y1t73n&cid=814360620&page=1&high_quality=1&danmaku=0" allowfullscreen="allowfullscreen" width="100%" height="500" scrolling="no" frameborder="0" sandbox="allow-top-navigation allow-same-origin allow-forms allow-scripts"></iframe>


- 聊天室：<br>
![聊天室演示图][pic-1.3.1]<br>
- 图片消息：<br>
![图片消息演示图][pic-1.3.2]<br>
- 文件传输：<br>
![文件传输演示图][pic-1.3.3]<br>
- 流式数据传输：<br>
![流式数据传输演示图][pic-1.3.4]<br>

###  1.4 项目仓库
- .NET服务器：<br>
<https://github.com/HaoyuanMa/IM-Api>
- Go服务器：<br>
<https://github.com/HaoyuanMa/IM-Api-go>
- Web客户端：<br>
<https://github.com/HaoyuanMa/IM-Front-Web>
- Android客户端：<br>
<https://github.com/HaoyuanMa/IM-Front-Android>
- 流式数据生成demo：<br>
<https://github.com/HaoyuanMa/IM-DataStreamGenerator-CSharp><br>
<https://github.com/HaoyuanMa/IM-DataStreamGenerator-go>

---

## **2.线上预约陪诊系统（Java，JS，micro-service，Vue）**
微服务应用课程设计
###  2.1 简介
一个线上预约陪诊系统，用户可通过H5小程序预约陪诊员上面进行陪诊服务。后端服务器使用Java开发，前端基于Vue开发面向用户的H5应用及面向管理员的后台系统。
###  2.2 技术细节
- 语言及框架/工具：
    - Java，JavaScript
    - SpringCloud，MyBatis，OpenFeign，Vue，MySQL，JWT
    - Nacos，SpringCloud GateWay，Docker
- 服务器：
    - 根据不同的业务场景，将系统划分成订单管理，用户中心等不同微服务，使用Docker部署各服务。
    - 使用Nacos作服务注册与配置中心，使用SpringCloud Gateway作网关，不同服务间使用OpenFeign通信。
    - 使用MySQL存储订单，用户，陪诊员等数据。
    - 使用开源工具[renren-generator](https://gitee.com/renrenio/renren-generator)通过数据库结构快速生成订单，用户等数据查询接口模板代码，加快开发速度。
- 客户端/后台管理系统：
    - H5应用基于开源商城项目[众邦科技/CRMEB-H5](https://gitee.com/ZhongBangKeJi/CRMEB-H5)。根据陪诊服务场景对开源项目代码进行删减，修改，重构以实现对应的业务逻辑。
    - 后台管理系统使用开源工具[renren-fast-vue](https://gitee.com/renrenio/renren-fast-vue)快速构建。

###  2.3 功能演示
- 系统架构：<br>
![系统架构图][pic-2.3.0]<br>
- 客户端截图：<br>
![客户端截图][pic-2.3.1]<br>
- 后台管理系统：<br>
![后台管理系统截图][pic-2.3.2]<br>
- nacos配置：<br>
![nacos配置中心截图][pic-2.3.3]<br>
![nacos注册中心截图][pic-2.3.4]<br>

###  2.4 项目仓库
- 服务器：<br>
<https://github.com/HaoyuanMa/micro-service-server>
- 客户端：<br>
<https://github.com/HaoyuanMa/micro-service-front>
- 后台管理系统：<br>
<https://github.com/HaoyuanMa/micro-service-admin>

---

## **3.FeedManger Rss订阅管理系统（ASP.NET Web Forms，EF，C#，HTML，JavaScript）**
移动互联课程作业
###  3.1 简介
一个向用户提供RSS订阅管理的网站系统。支持用户添加RSS订阅，并对其管理，如取消订阅，为订阅分类等。同时也支持对订阅中的具体文章或任意文章链接进行收藏等操作。
###  3.2 技术细节
- 语言框架：
    - C#，JavaScript，HTML，CSS
    - ASP.NET，SQL Server，jQuery，Bootstrap
- 使用ASP.NET Web Forms开发模式，对模板代码进行修改已完成自己的业务需求。
- 使用IIS部署网站。

###  3.3 功能演示
- 订阅列表：<br>
![订阅列表][pic-3.3.0]<br>
- 收藏夹：<br>
![收藏夹][pic-3.3.1]<br>
- 添加订阅/收藏非订阅中的文章：<br>
![订阅管理][pic-3.3.2]<br>

###  3.4 项目仓库
<https://github.com/HaoyuanMa/FeedManager>

----

## **4.Android端数独小游戏（Android，Java）**
Android开发课程作业
###  4.1 简介
一个Android平台的数独小游戏，共24到数独题目，游戏界面对于玩家填入的正确数字以蓝色字体显示，若存在冲突，以红色字体提醒。完成数独后，计算用时以提供一个简单的排行榜。
###  4.2 技术细节
- 语言框架：
    - Java，Android，SQLite
- 技术细节
    - 设计引导页面，App启动后显示封面图三秒后跳转至主页面。
    - 设计SudoView（继承自View）绘制游戏页面，并实现对应的填数逻辑。设计KeyDialog（继承自Dialog）绘制玩家填数时显示的输入pad，同时实现相关逻辑。
    - 设计Game类封装游戏逻辑，使之与视图显示及用户交互逻辑上解耦。
    - 使用SQLite存储玩家解题用时。

###  4.3 功能演示
- 引导界面/主页面：<br>
![主页面][pic-4.3.0]<br>
- 游戏页面：<br>
![游戏页面][pic-4.3.1]<br>
- 完成游戏/排行榜：<br>
![排行榜][pic-4.3.2]<br>

###  4.4 项目仓库
<https://github.com/HaoyuanMa/sudoku>

----

## **5.BitChat-C语言聊天室（C，tcp/socket，mysql，linux）**
小学期实践作业
###  5.1 简介
小组协作开发，我负责服务器端，主要实现返回好友列表，处理在线状态，转发消息等功能。
###  5.2 技术细节
- 语言框架：
    - C，MySQL，Linux
- 依据C/S模式工作原理，服务器对端口进行监听，与客户端连接后，新建一个线程进行接受数据。
- 自定义传输协议（字符串），根据字符串首位标识符确定客户端的请求类型，并调用对应函数处理数据。

###  5.3 功能演示
- 登录页面/主页面：<br>
![主页面][pic-5.3.0]<br>
- 聊天页面：<br>
![聊天页面][pic-5.3.1]<br>

###  5.4 项目仓库
<https://github.com/HaoyuanMa/BitChat>

----

## **6.pipe cpu（Verilog，FPGA）**
计算机组成原理课程设计
###  6.1 简介
一个基于FPGA的简单的五级流水线CPU，支持基本的运算，跳转，数据存储与传送等基本指令，解决了流水线cpu中的控制相关和数据相关的问题。
###  6.2 技术细节
- 语言框架：
    - Verilog，FPGA，时序电路仿真
- 根据五级流水的五个阶段（取指，译码，执行，执行，访存，写回），将整个cpu分为五个子模块分别编码实现，然后封装在顶层模块里。
- 在五个子模块中又分别对alu（运算模块），cu（控制模块），bru（跳转处理模块）等更小的子模块进行封装。
- 由于流水执行，跳转指令在译码阶段被识别时，下一条指令已经取指开始执行，如不处理，会导致寄存器值被更改，即控制相关问题。采用在跳转指令后插入空指令的方法处理控制相关。
- 下一条指令读寄存器时，前三条指令还未进行写回，如不处理，所读取的内容将不是最新的，即数据相关问题。采用数据前推的方式解决。
- 由于LW指令改写寄存器的写入数据在访存阶段才能确定，因此单纯的数据回推无法解决相关问题，需要在指令后插入一条空指令。为了简化设计，对于所有LW指令，无论是否出现数据相关，均在其后插入空指令。
- 通过汇编工具将指令翻译成二进制数字，然后输入cpu进行仿真。

###  6.3 功能演示
- cpu架构：<br>
![cpu架构图][pic-6.3.0]<br>
- 仿真结果：<br>
![仿真结果][pic-6.3.1]<br>
![仿真结果][pic-6.3.2]<br>
![仿真结果][pic-6.3.3]<br>

###  6.4 项目仓库
<https://github.com/HaoyuanMa/pipe-cpu-verilog>

----

## **7.操作系统实验（C，Linux，Windows，OS）**
包括以下四个实验：

- **copy**
    - 分别在windows和linux下完成一个目录复制命令mycp，包括目录下的文件和子目录。复制后，不仅权限一致，而且时间属性也一致。linux下要求支持软链接。
    - 实验报告：[copy实验报告](https://github.com/HaoyuanMa/os-experiment/tree/main/copy/)
<br>

- **time**
    - 在windows和linux下分别实现mytime命令，通过命令行参数接受要运行的程序，创建一个独立的进程来运行该程序，并记录程序运行的时间。
    - 实验报告：[time实验报告](https://github.com/HaoyuanMa/os-experiment/tree/main/time/)
<br>

- **memory-monitor**
    - 设计一个内存监视器，能实时地显示windows系统中内存的使用情况，包括系统地址空间的布局，物理内存的使用情况；能实时显示某个进程的虚拟地址空间布局和工作集信息等。
    - 实验报告：[memory-monitor实验报告](https://github.com/HaoyuanMa/os-experiment/tree/main/memory-monitor/)
<br>

- **consumer-and-producer**
    - 分别在windows和linux下模拟实现下列内容：
        - 一个大小为3的缓冲区，初始为空
        - 2个生产者
            - 随机等待一段时间，往缓冲区添加数据，
            - 若缓冲区已满，等待消费者取走数据后再添加
            - 重复6次
        - 3个消费者
            - 随机等待一段时间，从缓冲区读取数据
            - 若缓冲区为空，等待生产者添加数据后再读取
            - 重复4次

    - 实验报告：[consumer-and-producer实验报告](https://github.com/HaoyuanMa/os-experiment/tree/main/consumer-and-producer/)

### 代码仓库
https://github.com/HaoyuanMa/os-experiment/

----

[pic-1.3-0]: https://images.wait4echo.love/Works/im/wl-im-videoPoster.png
[pic-1.3.1]: https://images.wait4echo.love/Works/im/wl-im-chatRoom.png
[pic-1.3.2]: https://images.wait4echo.love/Works/im/wl-im-picMsg.png
[pic-1.3.3]: https://images.wait4echo.love/Works/im/wl-im-fileTransfer.png
[pic-1.3.4]: https://images.wait4echo.love/Works/im/wl-im-streamMonitor.png

[pic-2.3.0]: https://images.wait4echo.love/Works/micro-service/wl-ms-microServiceArch.png
[pic-2.3.1]: https://images.wait4echo.love/Works/micro-service/wl-ms-microServiceShow0.png
[pic-2.3.2]: https://images.wait4echo.love/Works/micro-service/wl-ms-microServiceShow1.png
[pic-2.3.3]: https://images.wait4echo.love/Works/micro-service/wl-ms-nacosConfig.png
[pic-2.3.4]: https://images.wait4echo.love/Works/micro-service/wl-ms-nacosRegister.png

[pic-3.3.0]: https://images.wait4echo.love/Works/feed-manager/wl-fm-mainPage.png
[pic-3.3.1]: https://images.wait4echo.love/Works/feed-manager/wl-fm-sideBar.png
[pic-3.3.2]: https://images.wait4echo.love/Works/feed-manager/wl-fm-addRss.png

[pic-4.3.0]: https://images.wait4echo.love/Works/sudoku/wl-sudoku-main.png
[pic-4.3.1]: https://images.wait4echo.love/Works/sudoku/wl-sudoku-game.png
[pic-4.3.2]: https://images.wait4echo.love/Works/sudoku/wl-sudoku-rank.png

[pic-5.3.0]: https://images.wait4echo.love/Works/bit-chat/wl-bc-main.png
[pic-5.3.1]: https://images.wait4echo.love/Works/bit-chat/wl-bc-chat.png

[pic-6.3.0]: https://images.wait4echo.love/Works/pipe-cpu/wl-pc-arch.png
[pic-6.3.1]: https://images.wait4echo.love/Works/pipe-cpu/wl-pc-sim0.png
[pic-6.3.2]: https://images.wait4echo.love/Works/pipe-cpu/wl-pc-sim1.png
[pic-6.3.3]: https://images.wait4echo.love/Works/pipe-cpu/wl-pc-sim2.png
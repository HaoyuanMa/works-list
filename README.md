---
layout: post
title:  "项目经历"
date:   2022-08-26 15:34:36 +0800
categories: jekyll update
---


# 项目经验 
[在博客中查看:](https://haoyuanma.github.io/works-list/)<br>

<https://haoyuanma.github.io/works-list/>

---

<!-- vscode-markdown-toc -->
* 1. [**跨平台即时通讯系统（Go，C#，JS，Kotlin，Gin，Vue）**](#GoCJSKotlinGinVue)
	* 1.1. [简介](#)
	* 1.2. [技术细节](#-1)
	* 1.3. [功能演示](#-1)
	* 1.4. [项目仓库](#-1)
* 2. [**线上预约陪诊系统（Java，JS，micro-service，Vue）**](#JavaJSmicro-serviceVue)
	* 2.1. [简介](#-1)
	* 2.2. [技术细节](#-1)
	* 2.3. [功能演示](#-1)
	* 2.4. [项目仓库](#-1)
* 3. [**next**](#next)
	* 3.1. [简介](#-1)
	* 3.2. [技术细节](#-1)
	* 3.3. [功能演示](#-1)
	* 3.4. [项目仓库](#-1)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->



##  1. <a name='GoCJSKotlinGinVue'></a>**跨平台即时通讯系统（Go，C#，JS，Kotlin，Gin，Vue）**
本科毕业设计
###  1.1. <a name=''></a>简介
本课题使用WebSocket和SignalR来实现一个简单的跨平台实时通讯应用。该应用允许用户在Web浏览器或Android App上进行实时聊天，支持私聊，群聊，广播，发送文本及图片消息以及传输文件。同时课题也实现了一套流式数据传输的演示程序，以模拟物联网系统中需要处理流式数据的应用场景，如智慧医疗系统中对患者生命体征数据的监控。
###  1.2. <a name='-1'></a>技术细节
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
###  1.3. <a name='-1'></a>功能演示
- [实时通信系统功能演示视频（点击跳转）](https://www.bilibili.com/video/BV17W4y1t73n)
[![video][pic-1.3-0]](https://www.bilibili.com/video/BV17W4y1t73n)



- 聊天室：<br>
![聊天室演示图][pic-1.3.1]]<br>
- 图片消息：<br>
![图片消息演示图][pic-1.3.2]<br>
- 文件传输：<br>
![文件传输演示图][pic-1.3.3]<br>
- 流式数据传输：<br>
![流式数据传输演示图][pic-1.3.4]<br>
###  1.4. <a name='-1'></a>项目仓库
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

##  2. <a name='JavaJSmicro-serviceVue'></a>**线上预约陪诊系统（Java，JS，micro-service，Vue）**
微服务应用课程设计
###  2.1. <a name='-1'></a>简介
一个线上预约陪诊系统，用户可通过H5小程序预约陪诊员上面进行陪诊服务。后端服务器使用Java开发，前端基于Vue开发面向用户的H5应用及面向管理员的后台系统。
###  2.2. <a name='-1'></a>技术细节
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
###  2.3. <a name='-1'></a>功能演示
- 系统架构：<br>
![系统架构图][pic-2.3.0]<br>
- 客户端截图：<br>
![客户端截图][pic-2.3.1]<br>
- 后台管理系统：<br>
![后台管理系统截图][pic-2.3.2]<br>
- nacos配置：<br>
![nacos配置中心截图][pic-2.3.3]<br>
![nacos注册中心截图][pic-2.3.4]<br>

###  2.4. <a name='-1'></a>项目仓库
- 服务器：<br>
<https://github.com/HaoyuanMa/micro-service-server>
- 客户端：<br>
<https://github.com/HaoyuanMa/micro-service-front>
- 后台管理系统：<br>
<https://github.com/HaoyuanMa/micro-service-admin>

---

## **FeedManger Rss订阅管理系统（ASP.NET Web Forms，EF，C#，HTML，JavaScript）
移动互联课程作业
### 简介
一个向用户提供RSS订阅管理的网站系统。支持用户添加RSS订阅，并对其管理，如取消订阅，为订阅分类等。同时也支持对订阅中的具体文章或任意文章链接进行收藏等操作。
### 技术细节
- 语言框架：
    - C#，JavaScript，HTML，CSS
    - ASP.NET，SQL Server，jQuery，Bootstrap
- 使用ASP.NET Web Forms开发模式，对模板代码进行修改已完成自己的业务需求。
- 使用IIS部署网站。
### 功能演示
- 订阅列表：<br>
![订阅列表][pic-3.3.0]<br>
- 收藏夹：<br>
![收藏夹][pic-3.3.1]<br>
- 添加订阅/收藏非订阅中的文章：<br>
![订阅管理][pic-3.3.2]<br>
### 项目仓库
<https://github.com/HaoyuanMa/FeedManager>

----

##  **Android端数独小游戏（Android，Java）**
Android开发课程作业
### 简介
一个Android平台的数独小游戏，共24到数独题目，游戏界面对于玩家填入的正确数字以蓝色字体显示，若存在冲突，以红色字体提醒。完成数独后，计算用时以提供一个简单的排行榜。
### 技术细节
- 语言框架：
    - Java，Android，SQLite
- 技术细节
    - 设计引导页面，App启动后显示封面图三秒后跳转至主页面。
    - 设计SudoView（继承自View）绘制游戏页面，并实现对应的填数逻辑。设计KeyDialog（继承自Dialog）绘制玩家填数时显示的输入pad，同时实现相关逻辑。
    - 设计Game类封装游戏逻辑，使之与视图显示及用户交互逻辑上解耦。
    - 使用SQLite存储玩家解题用时。
    
### 功能演示
- 引导界面/主页面：<br>
![主页面][pic-4.3.0]<br>
- 游戏页面：<br>
![游戏页面][pic-4.3.1]<br>
- 完成游戏/排行榜：<br>
![排行榜][pic-4.3.2]<br>
### 项目仓库
<https://github.com/HaoyuanMa/sudoku>



[pic-1.3-0]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/628cfa92-ca9b-430a-92da-7c533fb98834.png
[pic-1.3.1]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/ea520e51-4294-4b9a-a601-43c6d8221aa6.png
[pic-1.3.2]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/ce000332-4e71-41b5-86f7-525382cbf046.png
[pic-1.3.3]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/e8261b77-42b2-425f-8afe-382559d5677e.png
[pic-1.3.4]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/82f97639-a929-4e4d-851a-ed617c532ae1.png

[pic-2.3.0]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/6a53e09c-d00a-4165-ac13-bfdd5d56df70.png
[pic-2.3.1]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/b4706df5-f348-49bd-a7e3-f24368b8a185.png
[pic-2.3.2]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/901482dd-2bd4-4dac-a14a-457902558a6c.png
[pic-2.3.3]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/a861fc72-36a1-4853-b193-d664601138ef.png
[pic-2.3.4]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/dd9802ea-dbdf-48a2-abde-b16841b6685d.png

[pic-3.3.0]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/f52f1930-4637-476c-8888-b9b7b889af88.png
[pic-3.3.1]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/005514d1-07d4-4153-b801-9d462abba4dc.png
[pic-3.3.2]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/e6f8beb4-463e-41b0-9fd4-f58e728e7abb.png

[pic-4.3.0]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/e0fe6b57-7883-4a95-9dc0-4dd550be14e8.png
[pic-4.3.1]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/8a0356c4-ce40-48a8-a28c-c3320bba02d7.png
[pic-4.3.2]: https://vkceyugu.cdn.bspapp.com/VKCEYUGU-1682933a-c290-4a19-a517-c44d14df20fc/8d85d907-37fd-461a-965c-034e0e17e7cf.png

----
---
layout: post
title:  "项目经历"
date:   2022-08-26 15:34:36 +0800
categories: jekyll update
---

# 项目经验 
[在博客中查看:]()<br>

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
[![video](/images/IM/videoPoster.png)](https://www.bilibili.com/video/BV17W4y1t73n)

- 聊天室：<br>
![0](/images/IM/chatRoom.png "聊天室")<br>
- 图片消息：<br>
![1](/images/IM/picMsg.png "图片消息")<br>
- 文件传输：<br>
![2](/images/IM/fileTransfer.png "文件传输")<br>
- 流式数据传输：<br>
![3](/images/IM/streamMonitor.png "流式数据传输")<br>
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
    - SpringCloud，OpenFeign，Vue，MySQL，JWT
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
![0](/images/micro-service/microServiceArch.png "系统架构")<br>
- 客户端截图：<br>
![1](/images/micro-service/microServiceShow0.png "H5-APP")<br>
- 后台管理系统：<br>
![3](/images/micro-service/microServiceShow1.png "后台管理")<br>
- nacos配置：<br>
![4](/images/micro-service/nacosConfig.png "配置中心")<br>
![5](/images/micro-service/nacosRegister.png "微服务注册")<br>

###  2.4. <a name='-1'></a>项目仓库
- 服务器：<br>
<https://github.com/HaoyuanMa/micro-service-server>
- 客户端：<br>
<https://github.com/HaoyuanMa/micro-service-front>
- 后台管理系统：<br>
<https://github.com/HaoyuanMa/micro-service-admin>
---
##  3. <a name='next'></a>**next**

###  3.1. <a name='-1'></a>简介

###  3.2. <a name='-1'></a>技术细节

###  3.3. <a name='-1'></a>功能演示

###  3.4. <a name='-1'></a>项目仓库

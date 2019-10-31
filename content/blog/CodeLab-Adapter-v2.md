---
title: "CodeLab Adapter v2"
author: 种瓜
date: 2019-08-26
tags: ["programming"]
---

<img class="img-responsive" src="/img/water_727df488.png" />

>  Water as a first principle -- Thales

>  The Big Idea is Messaging -- Alan Kay

# 大纲

本文将讨论以下话题:

- 关于 CodeLab Adapter v2
  - 从 CodeLab Adapter 说起
  - v2 相对于 v1 做了哪些改进
- CodeLab Adapter v2 可以用来做些什么有趣的东西
- CodeLab Adapter v2 的开放计划

<!--more-->

# 关于 CodeLab Adapter v2

> talk is cheap, show me the <s>code</s> demo

我们先来看几个由 CodeLab Adapter v2 驱动的例子。

### Jupyter/Python & Scratch

<video width=600px src="http://scratch3-files.just4fun.site/jupyter_scratch.mp4" controls="controls"></video>

使用 CodeLab Adapter v2，用户可以在 Jupyter 中编写 Python 代码，并与 Scratch 互操作。

### 谁动了我的糖果

<video width=600px src="http://scratch3-files.just4fun.site/toio_candy.mp4" controls="controls"></video>

使用 CodeLab Adapter v2 的物体追踪插件(OpenCV)实时检测物体，将数据传递给 Scratch，最终在积木里编写程序逻辑，进而让 toio 小方块拥有视觉能力！

CodeLab Adapter v2 可以将任何 Python 程序整合到自身中。这个例子展示了 SmallTalk 的理念：用环境增强环境内的物体。

### I am reading!

当你妈妈进入房间的时候，只见你在聚精会神地阅读《理想国》，只是不知为何你喜欢用《权利的游戏》的片头曲作为背景乐。

<video width=600px src="http://scratch3-files.just4fun.site/python_neverland.mp4" controls="controls"></video>

这个例子展示的是“当有人推门时，屏幕自动切换到阅读界面”，在 10 行 Python 代码内，为整个生活空间编程。CodeLab Adapter v2 让 Python 入门充满趣味。

### cube symphony

<video width=600px src="http://scratch3-files.just4fun.site/cube%20symphony.mp4" controls="controls"></video>

用实体与空间交互，将桌面的物体当作系统 UI，实现类似[Dynamicland](https://dynamicland.org/)空间里交互效果。

这个程序目前有两个版本:Python 版和 Scratch 版，都由 CodeLab Adapter v2 驱动。

### 从 CodeLab Adapter 说起

CodeLab Adapter 是由[CodeLab](https://www.codelab.club/)构建的基础项目，致力于连接万物，无论是软件还是硬件，无论是 AI、开源硬件、现实世界的物体、还是虚拟世界的动画角色，在 CodeLab Adapter 的驱动下，皆可彼此互动。

目前，我们在 CodeLab Neverland 中使用 CodeLab Adapter。CodeLab Neverland 是一个由 CodeLab Adapter 驱动的可编程空间，也是我们的办公室和活动室，空间里的一切事物皆可编程。

在 CodeLab Adapter 驱动的空间里，你可以与万物沟通，你可以让神经网络识别出你的身体部位，进而制作一个体感游戏, 或是通过算法让整个空间变得智能。你可以在朋友生日那天，在 Ta 进门的一刻，将手中的魔杖一挥，在空中划一个字母 L 的轨迹，瞬间，点亮房间里五彩的灯光。在这儿，你将轻松做出这样的魔杖。

<video width=300px src="http://scratch3-files.just4fun.site/wand.mp4" controls="controls"></video>

<video width=300px src="http://scratch3-files.just4fun.site/tello_leapmotion.mp4" controls="controls"></video>

更多的[演示案例](/user_guide/gallery/)。

CodeLab Adapter 的一个典型用例，是将任何有趣的东西接入 Scratch3.0，接入之后你便能用 Scratch3.0 的积木来操控它，让它与任何接入 Scratch3.0 的物体互动。无论是来自现实世界的物体，还是来自虚拟世界的 AI 或动画角色，都能彼此互动，我们不想针对某个硬件产品发布一个客户端，我们相信创意来自广泛的连接，我们致力于做一个中立的东西，将 Scratch3.0 连接到更广阔的领域，我们想做到[宽围墙](http://learn.media.mit.edu/lcl/weeks/week5/)。

CodeLab Adapter 是一个跨平台跨语言的通用工具，你可以在多个平台上,将多种编程语言作为它的 client， 详情参考[Architecture](/dev_guide/Architecture/)。除了 Scratch3.0，CodeLab Adapter 目前也支持 Blockly、 Python、Javascript、SmallTalk，更多的编程语言支持目前正在开发中。

### v2 相对于 v1 做了哪些改进

CodeLab Adapter v2 是 CodeLab Adapter 的最新版本。

我们为此付出了巨大努力。 相比于 v1，v2 作出的主要改进包括以下方面:

- 优化消息结构
- 分离 UI 与内核
  - 可以作为 Python 库使用
  - 方便与 Electron 等工具集成
- 将内部功能服务化
  - 允许用户自定义 UI
- 使用 web UI
- 配套的调试工具
- 分布式优先
  - 云端 AI
  - 支持移动端
- 提供 Python Client
  - 提供教学例子
  - 允许以多种方式扩展 CodeLab Adapter
- 支持扩展 gateway
  - 默认构建了 MQTT gateway，websocket gateway
  - 允许用户自行构建 gateway：Arduino、socket...
- 降低开发门槛
  - 更加一致和易用的 API
- 增强可定制性
  - https 证书
  - 静态资源

接下来逐项陈述.

#### 优化消息结构

从 CodeLab Adapter[架构图](https://adapter.codelab.club/dev_guide/Architecture/)中可以看出，CodeLab Adapter 本质上是一个消息系统，它的核心设计理念是: Everything Is Message(EIM), 这个想法来自 SmallTalk 的设计理念:

> Everything is an object, and objects communicate only by sending each other messages.

在 v2 中，我们设计了更为通用的消息结构，新的消息结构使得系统的一致性提高，复杂性降低。待我们将核心部分开源之后，再来对这部分做深入讨论。

目前所有的 message topic 都在这儿: [codelab_adapter_client](https://github.com/Scratch3Lab/codelab_adapter_client_python/blob/master/codelab_adapter_client/topic.py), CodeLab Adapter v2 的所有行为都可用这些 topic 的语义来描述。

CodeLab Adapter v1 的消息结构记录在[这儿](https://github.com/Scratch3Lab/codelab_adapter_extensions/wiki/%E6%B6%88%E6%81%AF%E7%BB%93%E6%9E%84)。

v2 的消息结构目前还在梳理中，之后也会更新到 wiki 上。

#### 分离 UI 与内核

v2 将内核(core)与 UI 做了分离，出于以下目的考虑:

- 将两者解耦，提高开发效率，减少调试的困难
- 支持多种 UI，允许开发者定制自己的 UI
- 支持 headless 模式，方便集成到其他程序中
  - 诸如与 Electron 等工具集成
- 作为 Python 库单独发布

基于新的消息结构，CodeLab Adapter 的各个部分是对等的，无论是 GUI 、 Extension 还是系统的其他部分，它们都只是在 send/receive 消息，所以分离内核(core)与 UI 就是一件简单的事情，我们甚至允许内核(core)与 UI 运行在不同的设备上。

#### 将内部功能服务化

分离 UI 与内核之后，我们将内核中的所有功能，都变为了服务，可以通过消息与内核中的服务交互，诸如:

- 获取插件信息
- 更新插件
- 下载插件
- 启停插件
- 接收和发布通知(错误信息等)
- REST API
- 将消息发往特定 gateway
- 退出程序
- ...

以启停插件为例，可以参考[scratch3_eim](https://github.com/Scratch3Lab/scratch3_eim/blob/v2/index.js#L351)

#### 使用 web UI

v2 默认使用 web UI。

此前有过两个版本的 UI，分别基于 Tkinter 和 PyQt5，如下图所示。

<img width=250 src="/img/tui_064332a6.png"/>

<img width=250 src="/img/qtui_7f67c7f8.png"/>

Tkinter 的组件不大好看。Qt 是目前最强大的 UI 库，但存在一些跨平台的不一致性，诸如有用户反馈在某些 windows 版本下字体排版很奇怪，此外 Mac 下 PyQt5 的线程会自动休眠。只要投入足够多的时间，当然可以解决这些兼容性问题，但似乎不大划算。

web 技术的跨平台能力是最好的，而且基于 html 和 css 的布局技术，足够简单和灵活，所以我们最终决定采用 web UI 作为默认的 UI。由于 web 开发者众多，也方便更多开发者能参与进来改进它。

由于我们已经将内部功能服务化，所以所有的功能都可以在 Web UI 上使用。开发者可以自行构建新的 UI。以下是极简版的 demo UI， 只用到了 HTML：

<img width=250 src="/img/webui_0cdd2618.png" />

#### 配套的调试工具

v2 携带了一组调试工具，方便开发者用于构建新的[CodeLab Adapter Extension](https://github.com/Scratch3Lab/codelab_adapter_extensions)。

既包含基于 web 的调试工具:

- webdebug
- web_log_page

又包含基于命令行的调试工具:

- codelab-message-monitor
- codelab-message-trigger

<img width=600 src="/img/shelldebug_3ca7313d.png"/>

此外我们还提供了 MQTT 调试工具: [codelab_adapter_mqtt_client](https://github.com/Scratch3Lab/codelab_adapter_mqtt_client).

这些工具是我们自己在构建 CodeLab Adapter v2 时，爱吃的狗粮，也分享出来给大家。

#### 分布式优先

CodeLab Adapter v2 是一种分布式设计。

我们出于以下的理由这样做:

- 让云端和本地可以轻松建立连接，让云端的 AI 能力可以轻松为用户使用，也方便云端产品可以轻易接入教育体系，只需要写一个 CodeLab Adapter extension 即可。
- 让分布式的节点可以协同工作，典型用途包括教室里只需要有一个强大服务器，所有轻量级的学生端(诸如树莓派或 chromeOS)都可以得到这种计算力，来做 AI 之类的项目。
- 支持移动端设备。分布式的架构允许把硬件能力跑在树莓派或路由器上，而用户在 iPad 免费得到这种连接能力，无需构建单独的的 APP。

拿前头展示过的一个例子来说:

<video width=600px src="http://scratch3-files.just4fun.site/python_neverland.mp4" controls="controls"></video>

在这个例子中， 用户在电脑上，使用 Python 编程，却可以与 Neverland 整个空间交互，驱动 Neverland 的程序跑在树莓派中。如此一来用户的客户端无需任何配置，即可进入编程教学。

此外也方便在浏览器上做教学（跨平台），方便集成到任何网站中(诸如使用 brython（浏览器中的 Python）). 你可以认为 CodeLab Adapter 拓展了 web 的能力，你依然可以得到 web 的任何好处，可以与自己的云打通，它兼容你的任何架构。

因为没有任何客户端依赖，极大节省了课前配置的时间。

#### 提供 Python Client

上头的例子，便使用了我们提供的 Python Client：[codelab_adapter_client_python](https://github.com/Scratch3Lab/codelab_adapter_client_python)，利用 Python Client，你可以免费得到若干案例用于教学和演示，也可以模仿我们的案例设计你自己的教学内容，或者构建新的 extension，将你的业务整合进来。 我们会持续推出有趣的案例，在 CodeLab，这些案例都属于 realworld(类比于《Mindstorms》的 microworld)。

同时我们也构建了 [codelab_adapter_client_nodejs](https://github.com/Scratch3Lab/codelab_adapter_client_nodejs)、[codelab_adapter_mqtt_client](https://github.com/Scratch3Lab/codelab_adapter_mqtt_client)

之后会陆续放出 ruby client，smalltalk client...

利用 CodeLab Adapter v2，开发者可以用任何喜欢的编程语言来拓展 Scratch。

#### 可扩展的 Gateway

在 CodeLab Adapter v2 内部，我们将消息通道作为 gateway，它本质上是一个分布式节点(node)。只是收发消息，真正重要的是消息的结构以及它对应的语义功能。

消息是一种极强的逻辑构造，利用消息你可以构建一个编程语言(SmallTalk)或者操作系统。

CodeLab Adapter v2 与 Scratch 通信其实基于我们的 websocket gateway，与 MQTT 通信基于 MQTT gateway，这种高度的一致性，使其简易和清晰，也让 v2 易于迭代更新,v1 的复杂性是我过去一段时间痛苦的来源。

#### 降低开发门槛

降低开发门槛是我们在 v2 中做的核心考虑之一。这也是我们做前头这些工作动机之一。

为了方便开发者上手，我们近期正在构建 v2 的文档，以及开放 v2 的相关插件。

v2 的内核我们也计划开放它。

### 增强可定制性

由于 v2 计划开源，所以我们希望提高软件的可定制性，方便开发者能够很轻松地 fork 它，赋予它新的能力，将其集成到自己的系统中。我们试图将更多的配置放在用户目录下，而不是软件内部。

# CodeLab Adapter v2 可以用来做些什么有趣的东西

CodeLab Adapter v2 实际上接近一个分布式系统，有灵活的扩展能力，有强劲的消息内核，在 4 核机器上，每秒能处理 2000 万条消息。所以你可以将其用于很多领域：物联网、物理计算、空间编程...

CodeLab 的初心是让其成为编程教育的基础设施。使用 CodeLab Adapter v2，我们可以快速构建一个万物互联的 Playground 或者一个 AIoT Lab，它可能类似于[Dynamicland](https://dynamicland.org/)或者 CodeLab Neverland。

当然，你也可以将其视为灵活、可扩展、跨平台的 Scratch Link。或者将其视为特定硬件图形化编程工具的开放版本。

如果认同 Seymour Papert 在《Mindstorms》提到的 microworld；

如果你认同 Alan Kay 提到的：real playing；

如果你是 Dynamicland 的粉丝；

那么，CodeLab Adapter v2 便是为你打造的，因为正是这些理念驱使我们构建它。

我们希望实现约翰·杜威提倡的:

> educaition as life

如果你想亲眼看到 CodeLab Adapter v2 可以构建出什么有趣的东西，欢迎到 Neverland 参观: 预约报名地址是:[CodeLab Neverland 参观报名表](https://jinshuju.net/f/YEJGfB)。

# 开放计划

CodeLab Adapter v2 的开源计划分为 3 个阶段:

1. 本周我们将开放出所有的 extension 和 server。这些 extension 和 server 是 CodeLab Adapter 抵达万物的触角。
2. 我们计划在[Maker Faire Shenzhen](http://www.shenzhenmakerfaire.com/)开幕的那天(2019.11.09)对企业和组织开放早期成员资格申请，以此向 Maker Faire 致敬。
3. CodeLab 与早期成员一起商讨可能的社区形态以及方向，半年后正式向社区开放所有源码。

源码的第一个开放版本我们已经想好了名字: Thales。

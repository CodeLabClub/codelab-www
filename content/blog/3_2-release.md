---
title: 发布 CodeLab Adapter 3.2
author: CodeLab
date: 2020-05-10
tags: ["codelab"]
---

<img class="img-responsive" src="https://adapter.codelab.club/img/42b96f90be7f9884c9702fc5cd5279fb.png" />


> Playful Programming Centre

# 前言

距离 [CodeLab Adapter 3.0 发布](https://www.codelab.club/blog/3-release/)过去了 3 周有余，期间收到许多用户的邮件反馈，大家热心给出了改进建议和 bug 报告。

这段期间，根据大家的反馈迭代了若干个小版本，也为一些用户单独构建了一些版本，以服务于他们独特的用途。

3.2 是一个大版本，汇集了我们这段时间来的所有改进。

<!--more-->

今后，每当发布大版本，我们会在博客里发一篇文章说明重大变更。(沿袭 [Open edX](https://open.edx.org/) 社区类似的做法。)

至于常规版本的迭代日志，可参考[changelog](https://adapter.codelab.club/changelog/)。

# 先睹为快

CodeLab Adapter 3.2 的改进，主要围绕以下方面:

-   **新增扩展**
-   **让连接无处不在**
-   **提升 Windows 平台的使用体验**
-   **增强自省能力**
-   **完善插件体系**


以下逐条陈述。

## 新增扩展

CodeLab Adapter v3 是一个高度可扩展的开放系统。将一个新的体系接入 CodeLab Adapter， 有时只需几分钟时间！

在 3.2 中，新增了以下扩展:

-   [Stage](https://adapter.codelab.club/extension_guide/stage/)
-   [RaspberryPi GPIO](https://adapter.codelab.club/extension_guide/rpi_gpio/)
-   [Minecraft](https://adapter.codelab.club/extension_guide/minecraft/)
-   [Sonic Pi](https://adapter.codelab.club/extension_guide/sonicPi/)
-   [MQTT Broker](https://adapter.codelab.club/extension_guide/MQTT_Broker/)
-   [MQTT Adapter](https://adapter.codelab.club/extension_guide/MQTT_adapter/)
-   [Calypso](https://adapter.codelab.club/extension_guide/Calypso/)

其中 RaspberryPi，Minecraft，Sonic Pi 拥有巨大生态，用户社区从千万到百万级别不等。

### [Stage](https://adapter.codelab.club/extension_guide/stage/)

Stage 指 Scratch 的舞台区。

![](https://adapter.codelab.club/img/307a089f4fc36348702fe4d98958ce30.png)

Adapter/Scratch Stage 插件允许将 Scratch 舞台区的图像（舞台或者摄像头图像）以 base64 的格式发往 Adapter。如此一来，你就可以构建 Adapter node/extension ，用作自定义图像处理程序！可以使用 神经网络 / OpenCV ... 来处理舞台区的内容，一切都由你决定，识别的结果将返回给 Scratch。

其他的用例，包括构建一个自动保存舞台状态的插件；或者构建自拍/美颜插件：）

需要配合 Scratch `图像识别` 插件中的积木一起使用。

![](https://adapter.codelab.club/img/999e46633d51f05d58c863c698fcb109.png)

### [RaspberryPi GPIO](https://adapter.codelab.club/extension_guide/rpi_gpio/)

![](https://adapter.codelab.club/img/cb459aec0fc8b001c8f1f9e32b10d8f2.png)

树莓派是全球最流行的开源硬件之一，在疫情期间，更是被广泛使用，哥伦比亚将其用于制作呼吸机，有些硬件黑客则使用树莓派 DIY 口罩制作机，将自动生产的口罩赠送给附近医院。

树莓派通过 GPIO 引脚驱动物理/电器设备，所以 DIY 经常会用到 GPIO 。操作树莓派 GPIO 的工具里，[gpiozero](https://gpiozero.readthedocs.io/en/stable/index.html)尤为出色，因其具有很好的可理解性（图形化未必意味着更好的可理解性），Python 之父也是 gpiozero 的粉丝。

为了充分利用 gpiozero，我们只对它做一层薄薄的包装(REPL), 使其在 Scratch 中可用，更多的自由度则留给了你。

树莓派高度灵活，难以积木化它的所有特性，那样并不会提高可理解性。 我们希望用户灵活使用 Python 去增强 Scratch ，更好的扩展模式可以参考[Python eval kernel](https://adapter.codelab.club/extension_guide/extension_python_kernel/)。

当然， 一些功能是可以积木化的，期待你来提交 PR。

### [Minecraft](https://adapter.codelab.club/extension_guide/minecraft/)

![](https://adapter.codelab.club/img/WechatIMG1431.jpeg)

Minecraft（我的世界）是一款开放世界沙盒游戏，拥有惊人的自由度，它是有史以来最畅销的电子游戏，在儿童中尤其流行。

由于 COVID-19，提前结束这个学期后，MIT 学生在 Minecraft 上重建了 MIT 整个校园。校方还[报道了这事](http://news.mit.edu/2020/building-and-reconnecting-mit-minecraft-0407)。

![](https://adapter.codelab.club/img/ba660a0566b0e83a643e88da376f3140.png).

Minecraft 插件将 Minecraft 接入 Adapter ，使游戏中的世界可以与现实世界随意互动！ 可以将 Scratch、乐高、 AI、 实物，以及任何你喜欢的东西都接入到游戏中，与游戏角色互动。

我们制作了一个入门 Demo:[Scratch-mcTurtle](https://scratch3v3.codelab.club?sb3url=https://adapter.codelab.club/sb3/Scratch-mcTurtle.sb3)， 你可以从这里起步。它是一个运行在 Minecraft 世界里的 Turtle，将出现在主角周围， 推荐你飞到空中(空格)去看它的运行轨迹。

<video src="https://adapter.codelab.club/video/1588665494072465.mp4" controls="controls"></video>

如果你想做更多有趣的事，建议阅读[minecraft](stuffaboutcode.com/p/minecraft.html), 我们鼓励你去修改[插件源码](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/nodes_v3/node_minecraft.py)，去支持更多的对象。欢迎把你的修改结果提交到 CodeLab 源码仓库，分享给社区里的其他人用。

### [MQTT Broker](https://adapter.codelab.club/extension_guide/MQTT_Broker/)

@云天 在 国内最大的 maker 社区 -- dfrobot 社区里分享了十来篇采用 CodeLab Adapter 构建项目的案例, 一些有趣的案例如:

<video src="https://adapter.codelab.club/video/1589111397669473.mp4" controls="controls"></video>

将 OpenCV 接入 CodeLab Adapter，与家居互动，挥手时显示运动区域的光晕，颇有钢铁侠的味道。

<video src="https://adapter.codelab.club/video/1589111360787294.mp4" controls="controls"></video>

使用 CodeLab Adapter 连接 Google Teachable Machine 和 Microbit，训练了一个口哨汤勺开关

他在 懒人系列之视控灯 项目里写道:

> CodeLab Scratch3+CodeLab Adapter+Python 完美搭配。以前我要实现类似功能，要通过一个中间者 MQTT，比如本地的像 Siot。

CodeLab Adapter 的典型用途之一确实是 构建复杂连接的项目时，部分替代 MQTT。

但 MQTT 有其独特的价值，所以在 Adapter 3.2 中，有两个插件围绕 MQTT 。

MQTT Broker 插件允许你在本地轻松启动一个轻量级 MQTT Broker，这是一颗强劲的心脏。 轻量级，却高性能，采用 Adapter 内置的 [hbmqtt](https://hbmqtt.readthedocs.io/en/latest/index.html)， 基于协程的并发能力，足以让你在树莓派上支撑起整个学校的物联网。

一个典型的使用场景是将各类支持 mqtt client 的硬件，接入 Adapter（你需要写一个 extension, 不过我们已经构建了一个:[MQTT_adapter](https://adapter.codelab.club/extension_guide/MQTT_adapter/) ），方便你将 esp32、esp8266、掌控板等设备接入 Adapter 。

### [MQTT Adapter](https://adapter.codelab.club/extension_guide/MQTT_adapter/)

MQTT Adapter 插件负责桥接 mqtt 与 Scratch/Adapter， 它展示我们在易用性上所做的努力。

原理很简单，它将来自 mqtt 的消息(mqtt topic:`to_scratch`)，转发到 eim 中，将 eim 中的消息转发到 mqtt(mqtt topic:`from_scratch`)。

### [Calypso](https://adapter.codelab.club/extension_guide/Calypso/)

![](https://adapter.codelab.club/img/5e2d27904616c6f685c439d933fa2ced.png)

[Calypso](https://calypso.software/) 是 CMU 大学七年来对儿童如何学习基于规则的机器人编程的研究成果。由[David S. Touretzky](https://en.wikipedia.org/wiki/David_S._Touretzky)博士构建，他是 CMU 计算机科学和神经认知基础中心的研究教授。此外，Touretzky 一直活跃在互联网，主张言论自由。

[Calypso](https://calypso.software/)目前用于为 Cozmo 编程。被广泛用于 AI 教育项目.

<video src="https://adapter.codelab.club/video/1589111342575217.mp4" controls="controls"></video>

当 Cozmo 看到我表情悲伤时，将帮我升起窗帘: "Give you some sunshine"。

Cozmo 说 oh you are sad ，give you some sunshine。《Give Me Some Sunshine》是《三傻大闹宝莱坞》里的插曲。

这个例子很好展示了 设备与环境的互动。这种与环境的连接能力，允许大量有想象力且有温度的事情发生。更多理念，参考[CodeLab 可编程空间 背后的理念与设计原则](https://www.codelab.club/blog/design-principles-behind-neverland/)。

## 让连接无处不在

Adapter 3.0 拥有强大的连接能力。

v3.2 在连接方面的主要工作是使其高度易用。

[Adapter Node](https://adapter.codelab.club/dev_guide/Adapter-Node/) 虽然能够将整个 Python 生态 接入到 Adapter 中， 但对于许多入门者，却可能缺乏 Python 相关的技能。

v3.2 使连接开箱可用，对于入门者，Ta 可以快速将自己感兴趣的系统，接入 Adapter 中；对于高阶用户，推荐使用[Adapter Node](https://adapter.codelab.club/dev_guide/Adapter-Node/)，几乎拥有无限的自由。

> 让简单的事情保持简单，让困难的事情变得可能 -- Alan Kay

v3.2 中 Adapter 默认接收 EIM 消息请求，请求地址为:

`https://codelab-adapter.codelab.club:12358/api/message/eim?message=hi`

它只是简单 HTTP 请求，可以从任何地方发起！拥有和 web 生态一样的简单性。这个简单的接口带来了类似 IFTTT 的简单和灵活。你可以将任何 event 通知给 Adapter。

前边有两个案例，是基于这个接口做的：

[Calypso](https://adapter.codelab.club/extension_guide/Calypso/) 以及 Kano 魔杖。以下是 Kano 魔杖的案例：

<video src="https://adapter.codelab.club/video/1576905337206766.mp4" controls="controls"></video>

更有想象力的事情是，使用 Ngrok 之类的工具，将该接口暴露到公共互联网，如此一来，我们甚至可以在教学直播中，让远方的学生与演播厅的整个可编程空间互动，可以是多人！

前边的场景不过也是一种**连接**罢了，虽然可能跨越半个地球。 

Adapter 专注在连接，并使其简易。

尤其值得一提的是，我们充分考虑了安全性，即便暴露到公共网络，它也是安全的！

## 提升 Windows 平台的使用体验

由于许多用户在使用 Windows 平台，而我自己则主要在用 MacOS 和 Linux，之前忽视了 Windows 平台下的使用体验。

@Hanson 同学在使用 CodeLab Adapter 过程中，不只在班级博客中写了推荐文章:[使用 Codelab-Adapter 扩展 Scratch](https://rcfclass7.wordpress.com/2020/04/24/%e4%bd%bf%e7%94%a8codelab-adapter%e6%89%a9%e5%b1%95scratch/)（文章中对 Adapter 架构的理解非常精确），还给出了许多反馈和建议, 这些改进建议，多数在 3.2 中付诸实施。

其中最大的一项改进是:

> HCI 运行时启动的 python 命令行程序可以改为.pyw 的隐藏程序

将 Node 作为隐藏程序，不只是 @Hanson 同学提出，其他用户也多次提出，在 3.2 中，这项工作已完成。

容我吐槽下 Windows，忍无可忍，在源码注释中竖了中指 🖕️，不准备删除：） Windows 拙劣得惊人。 在其中编程，仿若在泥塘与巨兽搏斗。推荐大家使用 Ubuntu系统，Ubuntu 是免费的，不需要重新购买计算机，直接安装 Ubuntu 即可使用。

## 增加自省能力

我们在[发布 CodeLab Adapter 3.0](https://www.codelab.club/blog/3-release/) 讨论**自省**时说到

> 自省的意思是说事物理解它自身的状态，当我们说一个事物 智能 的时候，很多时候和它的自省能力有关。

3.2 进一步增强 Adapter 的自省能力，于是我们可以做到一些智能的行为，诸如在程序启动时，自动更新最新的 Adapter Client，这样使用 Adapter Node 时，无需再操心环境依赖问题。

这也是 3.2 对易用性的最大改进之一。

导致这项改进的背景是，Cozmo 社区的许多用户，是没有技术背景的奶爸，他们使用 CodeLab Adapter 来驱动孩子们喜欢的 Cozmo，让他们在 Scratch 里同时驱动 Cozmo 和 Vector:

<video src="https://adapter.codelab.club/video/where-did-the-human-go.mp4" controls="controls"></video>

但他们经常会对文档中一些我们(工程师们)认为非常基础的概念产生疑惑，诸如 pip 是什么，命令行怎么打开，他们给我发邮件，他们感到困惑的地方，让我有点惊讶。

但我们要承认，对创造感兴趣的并非都是工程师，如何让非技术背景的用户更加易于使用，是我们不断增强 Adapter 自省能力的原因。通过增加自省能力，来自动化完成一些需要手动操作的技术活。

## 完善插件体系

3.2 中，对插件体系有 2 大改进：

### 插件市场

![](https://adapter.codelab.club/img/57c8980da375649292ff3fc158e71bae.png)

插件市场现在同时支持 Node 和 Extension，用户可以将自己创建的插件，分享给社区用户。而且我们允许 Node 托管在互联网的任何区域！

### 可扩展的插件 Meta 信息

3.2 中，我们使用静态分析(ast) 从 Node/Extension 中动态提取 meta 信息。这些信息用于为插件排序，以及为 UI 提供插件附属信息。其中关于添加图标和描述信息的想法，来自Longan团队的产品经理@yuchen，目前3.2中已经实现。

![](https://adapter.codelab.club/img/a884c24a566089e8d87ce339fab0efdd.png)

此外， 第三方公司在构建自己的扩展时，可以随意自定义信息给自定义的前端 UI 使用，这样一来具有极高的灵活度。

这是我第一次写静态分析相关的代码。把代码当数据来操控的想法实在太有意思了！它给人一种无所不能的快乐。

把代码当数据来操控的想法在 LISP 社区很盛行，但在学习 LISP 的时候（《SICP》和《The Little Schemer》）围绕这个话题读了不少资料，却总有一种隔阂感，后来 Seymour 和蒙台梭利关于“实践”的论点打动我，便习惯了 learning by doing。由于近期希望在代码运行之前提取 Meta 信息，如此一来对代码的静态分析，就成为眼前事，那些能够方便解析和操控静态代码的工具和语言(hylang)，像 ast，之前觉得复杂而冗长，这两天却呈现出前所未有的趣味。

ast 模块的 api 惊人地优美。这些 api 在我之前看来，是一堆与我无关的结构，只能凭借记忆和无聊的练习去反复适应它。当我最近试着手动处理代码结构，处处碰壁，再次看到 ast，惊为天人。这时，理解只是轻松的副产物。或许可以作为 seymour 关于“建构主义”所做讨论的案例注脚。


# 其他改进
其他的改进，如:

-   日志滚动存放 30 天，逾期清除，避免占用太多计算机存储空间
-   Adapter退出时，UI 弹出(alert)提醒，而不是显示断开加载中(之前有几位用户对此感到困惑)
-   软件启动时，使用线程自动检查环境信息，并提取到全局
-   将一些辅助函数移往 adapter client，使得构建 Node 更为容易。
-   ...

不在此一一列出，我们近期将一起更新到changelog里。

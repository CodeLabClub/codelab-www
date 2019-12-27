---
Date: 2019-11-16
title: "CodeLab Adapter 深度连接 micro:bit 生态"
Slug: codelab-adapter-microbit-deep-connect
tags: ["microbit","Scratch","Python","kit"]
author: "种瓜"
categories: ["少儿编程"]
---

<img class="img-responsive" src="/img/magic.png" />


# 前言

因为开放性和出色的基础工作，micro:bit 现在拥有无与伦比的生态。

上周参加了[Maker Faire shenzhen](http://www.shenzhenmakerfaire.com/)，现场有各类新的 STEM 教育套件，大多数基于 micro:bit:  DIY 编程套件、类乐高编程套件、各类拓展板、麦克纳姆轮遥控车、可穿戴手表、循迹小车、平衡小车、机械臂...

去淘宝上搜一搜，琳琅满目。

时间回退到几年前，Maker Faire 上的编程/STEM 套件，几乎被 arduino 统治。去年，两者不相伯仲，而今年，micro:bit 生态已经明显胜出。micro:bit 似乎正处于 STEM 编程套件领域的中心。

<!--more-->


micro:bit在教育开源硬件/STEM 编程套件领域，与 RaspberryPi(树莓派)、Arduino 鼎足而三。

生态的繁荣带来的一个显著现象是同质化严重，功能相似的拓展板(甚至电路结构都相似)、配色和尺寸完全一致的乐高兼容积木、除了 Logo 其他基本一样的编程平台...

严重的同质化几乎可以视为一个领域蓬勃发展的标志，这点我们在 IoT 和 AI 领域也可以看出来。

市场给出了明确的需求信息，各家公司纷纷涌入其中。这当然是一件好事。对于消费者而言，有更多选择，而不至于被一家公司绑架。对产商而言，喜忧参半吧，如果我是硬件产商，我会开心多一些，尽管竞争激烈，但市场信号明确，意味着只要在产品上打磨得足够好，便有机会。

并非所有努力都有回报，许多时候不可抗力太多，市场需求当然算重要的一种不可抗力。这便是我说“开心多一些的原因”，乐于参与这种 努力就有回报 的竞争里。

构建足够有 想象力/差异化 的编程平台/内容，又恰好属于我有些把握的领域。

# 与 micro:bit 建立连接

## Scratch 社区的做法

Scratch 社区在发布 3.0 版本的时候，一个重要的工作就是兼容 micro:bit。Scratch 团队似乎也认为 micro:bit 未来会是最重要的教育开源硬件生态（至少是之一）。

Scratch 团队采用的策略是构建一个[Scratch-Link](https://github.com/LLK/scratch-link)，使用它将 Scratch 与外部设备连接(主要是乐高)), 然后为 micro:bit 构建一个兼容于 Scratch-Link的固件。

Scratch 的做法是可以理解的，Scratch 的核心是交互式编程(Scratch 的许多设计理念来自 Smalltalk)，而不是灌入式编程，所以他们为树莓派写了固件，来服务于交互式编程。关于这点我在[两种硬件编程风格的比较](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/hardware-programming-style/)里做了详尽讨论。

目前 scratch 开放了[Scratch-Link 的源码](https://github.com/LLK/scratch-link)，但 micro:bit 的源码目前尚未开源。

如果你对交互的细节感兴趣，可以阅读我的这篇分析文章: [分析 scratch3.0 与 micro:bit 的通信](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3-microbit-analysis/)

### Scratch Link 的问题

Scratch Link 目前存在一些问题：

-   对系统环境有严格要求
    -   Windows 10 version 1709+
    -   macOS 10.13+
    -   Bluetooth(4.0+)
-   不支持 Window7，许多学校/机构/家庭用户在使用 Windows7
-   不支持 Linux, 无法支持许多学习者/教育机构使用的树莓派
-   可扩展性不足, 只支持在 Scratch 中编写基于 BLE 的硬件拓展
-   使用 C#和 Swift，需要维护 2 套代码

因为存在这些问题，我对 Scratch Link 颇有微词，自行构建了[CodeLab Adapter](https://adapter.codelab.club/)，我想把 Alan Kay 在构建 smalltlak 怀有的创见带到 Scratch 社区。为此，今年四月份还专门去了一趟 MIT Media Lab，与 Scratch 团队交流。

[CodeLab Adapter](https://adapter.codelab.club/)早期的名字叫`scratch-adapter`，它最初的目的是提供一种更加灵活的方式来增强 Scratch，关于这部分的思考和交流，做了记录:

-   [为 Scratch3.0 设计的插件系统(上篇)](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3-plugin-1/)
-   [为 Scratch3.0 设计的插件系统(下篇)](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3-plugin-2/)
-   [美国之行](https://blog.just4fun.site/post/%E9%9A%8F%E7%AC%94/usa-travel/)
-   [CodeLab 近况_03](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/codelab-recent-situation-03/#mit-media-lab)

后来发现[CodeLab Adapter](https://adapter.codelab.club/)并不限于增强 Scratch，它已经成为:

> 致力于连接万物，无论是软件还是硬件，无论是 AI、开源硬件、现实世界的物体、还是虚拟世界的动画角色，在 CodeLab Adapter 的驱动下，皆可彼此互动。 目前，我们在 CodeLab Neverland 中使用 CodeLab Adapter。CodeLab Neverland 是一个由 CodeLab Adapter 驱动的可编程空间，空间里的所有事物皆可编程。

于是便改了名字。

目前我们为它构建了 [34+编程语言的交互例子](https://adapter.codelab.club/dev_guide/system_command/)，Scratch 仅是其中的一门语言。

## CodeLab Adapter 连接 micro:bit

抛开前头的问题不说，Scratch Link 采用蓝牙与 micro:bit 通信，还存在一个稳定性的问题，蓝牙时常会断开，在一个教室中，有许多蓝牙设备时尤其如此(信道拥挤)。这让初学者提心吊胆，时常得担忧掉线问题，十分打断思路。

于是 CodeLab Adapter 用户(他们服务于课堂)催着我们构建了基于 usb 版本的固件，功能与 Scratch micro:bit 类似，但稳定性要好很多，适合教学使用，这部分的源码我们都已经公开:

-   [extension_usb_microbit.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v2/extension_usb_microbit.py)
-   [usbMicrobit_for_adapter.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/firmware/usbMicrobit_for_adapter.py)

相关文档在这儿: [micro:bit Tutorial](https://adapter.codelab.club/extension_guide/microbit/)。

这个插件一直在稳定使用，CodeLab 在做活动时使用它；一些公司在教育机构里使用它；有些学校在课堂上使用它。

### Think Bigger

前头方案尽管兼容性、可扩展性和稳定性足够好，但依然有其局限性，我自己最不满意的是它并未与 micro:bit 生态做深度连接。只是通过开发者构建固件来建立连接。

这会带来的一个问题是，我们在 Maker Faire shenzhen 上看到如此众多的厂商生产的丰富 microbit 拓展套件、琳瑯满目的传感器和执行器，他们都有各自的编程包(主要是 MakeCode extension)，如果不能无缝兼容到 CodeLab Adapter 中，多可惜。

而一旦兼容之后，我们可以做些真正有想象力的事，孩子们在入门时使用简易的套件构建丰富的玩具，而他们一旦希望做更多探索，我们就可以把他们的玩具接入到真是世界中：他们可以在门口放一个橘子，将其用作门铃；将玩具套件里超声波积木接入到家庭安防系统中；使用红外玩具积木构建非接触时开关；通过连接一切，便可以利用玩具来解决真实的生活问题。模糊玩耍和实际发明之间的界限。

> Education as life.

此外，这种深度的连接带来的另一个好处是，我们可以将 CodeLab Adapter 生态中的所有能力带给这些玩具，无论是脑电波、眼动仪还是 AI。

# 深度连接

怎么做呢？

## 思路

我们先想来梳理一下目标。

我们希望:`与micro:bit生态中的所有厂商的所有拓展套件连接`。

乍看起来是个无法完成的目标，micro:bit 生态中的许多拓展套件都还没有生产出来，而且我们也不知道它们来自哪个国家、哪家公司，怎么能知道可否建立连接？

胡乱对未来下断言，是政客的伎俩，是情侣的冲动，却不是开发者的美德。

我们接下来说说为何这个目标并非遥不可及。这其中的关键词是开放性、最佳实践、技术生态/社区。

《大教堂与集市》中论述了开源社区与开放市场拥有极为相似的结构。这也是开源社区取得胜利的经济学原理。

市场通过自由竞争，为资源找到最优配置方式，哈耶克在它的书里（《自由宪章》、通往奴役之路...）里不厌其烦地论述这点。

> 那些因为发现了如何对变化作出适当反应从而成功的个人所确立的范例，一定会为其余的人所仿效 --《自由宪章》

目前在 micro:bit 生态中获得成功的范例似乎已经为大家所领悟:

-   开放
-   兼容[MakeCode](https://makecode.microbit.org/)
-   兼容[python](https://python.microbit.org/)

我们在 Maker Faire shenzhen 上看到的`同质性`, 部分原因正来自对成功范例的模仿。目前的成功范例中，最大的共性就是支持[MakeCode](https://makecode.microbit.org/)。

因此，他们便有了相似的模式和约束条件。如此一来，我们就可以有把握地说，micro:bit 生态中无论是现在还是未来流行的套件，我们都可以兼容它。

于是我们只需要对 MakeCode 和 python 做好兼容，几乎就能兼容整个 micro:bit 生态。

有怀疑精神的读者要说了，未来有比 MakeCode 更好的的平台出现，怎么办呢，关于这点我们可以邮件里讨论，我自己目前是有答案了，我很有把握 CodeLab Adapter 能极快接入其中，因为其中有些模式我们现在是可以清楚看到的。

### 技术层面

技术层面，思路很简单: 构建 gateway, 让两个彼此不相关的领域，彼此 talk(双向沟通)。我们此前也是这么桥接 mqtt 的: [extension_mqtt_gateway.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v2/extension_mqtt_gateway.py)。

因为 CodeLab Adapter 背后的哲学是`Everything is message`，所以构建这样的连接轻而易举。

我们将一块 micro:bit 接入电脑，用作中转站(类似 usb dongle)，用于在 CodeLab Adapter 和任何 microbit 套件做中转站。这里的一个背景知识是，任何的 microbit 直接可以通过 radio(简易的无线连接) 方便地彼此通信。

在这个思路中，获得的一个意外收获是: 能让任何电脑与 microbit 无线连接！即便没有蓝牙！

#### MakeCode

MakeCode 是微软构建的一个可视化编程平台，方便用来为 microbit 这类小设备编写固件。MakeCode 几乎是可视化编程领域的 IDE，它做了许多贴心而令人惊艳的工作。

> 除了网站编辑器的熟悉功能外，您可以通过连接 USB 进行编程（无需拖放文件到 micro:bit 驱动器上），并可直接读取您的 micro:bit 序列数据，用于数据日志及其他有趣的实验！

## 实现

我们先来实现 radio_microbit_adapter 固件，固件烧录进 micro:bit，将其用作 gateway。它的职责是桥接外部的 micro:bit 设备/套件和 CodeLab Adapter，该固件与 CodeLab Adapter radio extension 配合使用。

以下是 radio_microbit_adapter 的部分代码:

![](/img/radio_microbit_adapter.png)

CodeLab Adapter radio extension 的源码很简单，实际上是对我们先前的插件[extension_usb_microbit.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v2/extension_usb_microbit.py)做的插件，我大约花了 5 分钟完成。

## 使用

接下来我们来看看如何使用 radio_microbit_adapter 插件，来深度接入到 microbit 生态中的任何产品上。

我们从淘宝上买一个套件，随便挑一个购买的人较多的、好看的、不要太贵的。

![](/img/dadabit.png)

使用这个类乐高编程套件，我们可以构建各种东西，而且他们全都由 micro:bit 驱动!

![](/img/dadabit_demo.png)

来搭一个`投石器`玩。

![拼搭结果](/img/catapult.jpeg)

先来看下投石器的程序，和大多数套件一样，该套件也使用 MakeCode 作为其编程工具。

![投石器程序](/img/fire_microbit_origin.png)

### 接入！
接下来让我们将其接入 CodeLab Adapter。

让我们在 MakeCode 中对投石器的驱动程序做一些微调：

![投石器程序](/img/fire_microbit.png)

几乎没有什么变动！

接入CodeLab Adapter之后，我们就可以与CodeLab Adapter生态中的所有事物互动啦!

![](https://adapter.codelab.club/img/adapter_party.jpeg)

让我们写个程序，使用魔杖控制投石器:

![投石器程序](/img/catapult_scratch.png)

来看看效果:

<video width=80% src="/img/wand_catapult_demo.mp4" controls="controls"></video>

让我们构思一个完整一些的场景:

Fire！

<video width=80% src="/img/wand_catapult.mp4" controls="controls"></video>

# 总结

总结以下，通过深度连接 micro:bit 生态，我们能做什么，我想到以下三点:

1. 为 micro:bit 社区引入 CodeLab Adapter 的所有能力: AI、IoT、开源硬件、脑电波、眼动仪...

2. 为 CodeLab Adapter 引入 micro:bit 生态里的无数内容和套件

3. 最后为 scratch 生态引入以上两者。


# 参考

-   [adapter micro:bit extension](https://adapter.codelab.club/extension_guide/microbit/)
-   [microbit.org](https://microbit.org/zh-CN/code/)
-   [Scratch3.0、micro:bit 与 Windows7](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3-microbit-windows7/)
-   [分析 scratch3.0 与 micro:bit 的通信](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3-microbit-analysis/)
-   [Scratch-Link](https://github.com/LLK/scratch-link)

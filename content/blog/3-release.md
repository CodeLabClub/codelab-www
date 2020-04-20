---
title: 发布 CodeLab Adapter 3.0
author: CodeLab
date: 2020-04-17
tags: ["codelab"]
---

> real playing -- Alan Kay

# 目标与理念

[CodeLab Adapter](https://adapter.codelab.club/) 是 [CodeLab](https://www.codelab.club/) 为编程教育构建的基础设施。

CodeLab Adapter 3.0 的目标是成为继 [Scratch](https://scratch.mit.edu/)/[Etoys](http://www.squeakland.org/) 之后，最有趣的编程学习启动平台。追随 [Alan Kay](https://zh.wikipedia.org/zh-hans/%E8%89%BE%E4%BC%A6%C2%B7%E5%87%AF) "real playing" 的理念。

CodeLab Adapter 经过之前两个大版本的迭代，历时两年多，我们对问题域有了更清晰的认识: 关于如何为编程入门、 AI 教育、 开源硬件、空间编程... 提供一个理想的环境, 在这个环境中，创造成为一件稀疏平常的事情， 而不是先与糟糕的编程环境来个殊死搏斗。 这个问题背后是一个更大的母题， 它正是 Seymour Papert/Alan Kay/Marvin Minsky/Bret Victor 以及 Smalltalk 社区 同时关注的一个问题: 计算机如何为创造精神提供支持？

对这个问题的理解，我们受以上先驱的强烈影响。 CodeLab Adapter 3.0 正是这些影响下的最近产物。

<!--more-->

# 先睹为快

CodeLab Adapter 3.0 的升级主要围绕 **简易** 、**灵活**、**健壮** 三大特性，以下逐条陈述。

## 简易

### 彻底采用 Web UI

![Web UI](https://adapter.codelab.club/img/c5b2b84e3b0ab411e7d7342104c5bba3.png)

3.0 彻底放弃了之前的桌面 UI (它们曾分别基于 [guizero](https://github.com/lawsie/guizero) 和 PyQt5(主要由 CodeLab 志愿者 @liheng @Bilikyar 设计，由 @wangshub 实现) )。

彻底采用 Web UI 之后提升了 3 个方面的 **简易性** :

1. 对于用户而言，所有的控制都在浏览器的一个界面中。用户无需在浏览器和 GUI 之间切换。对易用性的关注并移除无关的干扰元素，主要受到 @曾老师 的影响。
2. 对于开发者/第三方公司而言，由于一切都从 Web UI 控制, 意味着 CodeLab Adapter 只是纯服务，由 websocket/REST 接口完全控制，如此一来，它可以与任何软件(如 Electron)或 web 网站进行集成，这让它可以配合任何编程语言使用，学习者在一开始就可以做些真实而有趣的事。由于 Web UI 只是 html 和 js，所以可以由第三方公司任意定制！目前 Longan 项目将其用于扩展 **machine learning for kids** 和 龙眼盒(用于空间编程), 让 AI 和物联网 变得更有趣。
3. 简化 CodeLab Adapter 的 UI 体系，跨平台将变得容易，因为没有任何系统 UI 依赖，它可以轻松运行在所有主流操作系统上，甚至包括安卓！我们也支持了 headless 模式，headless 模式对集成到其他软件至关重要，CodeLab Adapter 3.0 可以方便集成到硬件产品里。

### 增强反馈

这是之前许多用户在有邮件里提到的功能增强需求， 用户希望在使用时，收到清晰明确的反馈信息，诸如

-   CodeLab Adapter 是否已经成功接入 Scratch

![](http://adapter.codelab.club/img/8411bbdd83b202de10e04fab510a8f1e.png)

-   硬件设备(诸如 micro:bit, Arduino, Cozmo)是否已经连接成功

![](http://adapter.codelab.club/img/e18c522106b8f904795a1e092aee6cf8.png)

-   环境依赖不满足或者设备掉线之类的提示信息

![](http://adapter.codelab.club/img/9854c0e4addbf48bcf438fca45b5cd6d.png)

以及更多的信息提示，这对于诊断问题和自助使用很重要。

### 自省

自省的意思是说事物理解它自身的状态，当我们说一个事物 **智能** 的时候，很多时候和它的自省能力有关。

CodeLab Adapter 拥有自省能力，它理解自身内部以及自身所处环境的状态，并将这些信息反馈给使用者。

以下是 CodeLab Adapter 报告的运行时信息，以及它所处环境的信息 (你可以在 Web UI 右边栏菜单里打开它)。

![env](https://adapter.codelab.club/img/5d00c1e6ee237fe95671d791a54805e5.png)

自省信息有多种用途，诸如服务于 Python 教育或者插件开发者。如果你希望让 Python 做些真实世界里的事情，处理你的照片或者自动化你的 word 文档。那么你就很难使用基于云端的环境来做。此时用户需要在本地安装 Python。CodeLab Adapter 将让 Python 入门教育变得容易，对于入门者，在命令行里安装依赖库，是令人生畏的。

由于有了自省能力，假设我们想为用户构建一个 jupyterlab 插件，当发现用户本地没有安装 Python，则给 Ta 安装引导提醒，如果发现 Ta 已经安装了 Python，但没有安装 jupyterlab，我们可以利用环境自省信息，在插件里决策，帮助用户安装 jupyterlab , 安装完成后运行它，这个假想的插件，我们已经完成，你可以拿到它的源码，以便于构建你自己的插件，为用户打造新的学习环境。

<video src="https://adapter.codelab.club/video/1587120471271045.mp4" controls="controls"></video>

所有这一切在 CodeLab Adapter 里，只需要写 100 行不到的代码，跨所有平台！源代码在这儿: [extension_jupyterlab.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v3/extension_jupyterlab.py)。

### 更多开箱可用的开源硬件

目前最流行的三大开源硬件是:

-   micro:bit
-   Raspberry Pi
-   Arduino

CodeLab Adapter 对 micro:bit 的支持是开箱可用的。

CodeLab Adapter 可运行在树莓派上。

但对 Arduino 的支持颇为曲折，一方面，是重视程度不够，我们认为 micro:bit 是未来，它正在替代 Arduino，至少在教育领域如此。但 Arduino 在全球依然拥有海量的用户和庞大生态，许多用户在邮件和 Github 里提议我们为 Arduino 构建驱动，在 3.0 版本中，这项工作终于完成，做到了开箱可用, 我们依赖于开源社区的许多已有工作, 我们把教程和感谢信息都放在[文档页](https://adapter.codelab.club/extension_guide/arduino_UNO/)里了。

至此，对全球 3 大开源硬件的支持已经完成。

未来我们会持续加入更多的开源硬件支持，如 esp8266 等。

# 灵活

3.0 中，为灵活性所做的工作主要包括以下几个:

-   重构消息结构
-   重构插件系统
-   插件市场

分别论述。

### 重构消息结构

在 3.0 中，我们基于著名开源项目 -- [Jupyter](https://jupyter.org/)的消息结构，重构了 CodeLab Adapter 的消息结构。当然关于消息系统的实现机制，我们没有采用 Jupyter 的策略，而是受 Dynamicland 影响，采用 "one world" 的概念，所有事件发生在一个消息通道里，一切都是异步消息，同步消息只是异步消息的一个特例，这点和 ROS 的策略相同。关于同步异步的细节，参考 [EIM 插件源码](https://github.com/CodeLabClub/scratch3_eim)。

> 世界是事实的总和，而非事物的总和 --维特根斯坦《逻辑哲学论》

在 CodeLab Adapter 中，所发生的一切都是消息。所有发生的事都被描述为事件( event )，之后异步地软件世界里传播它。每条消息的逻辑结构为:

-   parent_header
-   header
    -   version
    -   message_id
    -   message_type
    -   token
    -   username
    -   sender
    -   node_id
-   content

### 重构插件系统

重构了插件系统，这是 3.0 最大的改进之一，对于开发者来说可能没有之一。

在 2.0 中, 有以下 4 种方式来扩展 CodeLab Adapter :

1.  [EIM](https://adapter.codelab.club/extension_guide/eim/)
    -   [eim_monitor](https://adapter.codelab.club/extension_guide/eim_monitor/)
    -   [eim_trigger](https://adapter.codelab.club/extension_guide/eim_trigger/)
2.  [Adapter extension](https://adapter.codelab.club/dev_guide/helloworld/)
3.  [Adapter Node](https://adapter.codelab.club/dev_guide/Adapter-Node/)
4.  [跨语言支持](https://adapter.codelab.club/dev_guide/system_command/)

其中 **3.Adapter Node** 允许将 Python 生态里的海量的第三方库接入到 CodeLab Adapter 里, 这也是开发者最喜欢的一种接入方式。在 3.0 中，我们将 **Adapter Node** 与 **Adapter Server** 合并，这意味着 **任何** 的 Python 程序都可以成为 CodeLab Adapter 的插件！如此一来写一个 AI 拓展就是轻而易举的事，因为大多数的 AI 项目都发生在 Python 社区！而且允许你使用 CodeLab Adapter API 来控制这些自定义插件，甚至，我们在下文里会提到，你可以发布到插件市场，供用户下载使用！具体细节，可以看 3.0 里已有的 node， 它们的源码都在[nodes_v3](https://github.com/CodeLabClub/codelab_adapter_extensions/tree/master/nodes_v3)目录里。

将一款自研硬件或一个 AI 服务引入 Scratch，进而作为教育产品发布，不再需要经历过去漫长的周期，发布一款 CodeLab Adapter 插件即可。CodeLab 将大疆(DJI)的 RoboMaster EP 接入 Scratch 用了不到一个 10 分钟的时间，所有的源码不超过 100 行，源码在这里:[extension_RoboMaster.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v3/extension_RoboMaster.py)。

<video src="https://adapter.codelab.club/video/1587120578222179.mp4" controls="controls"></video>

一旦一款新设备接入进来，它将得到其他许多好处 -- 获得与体系里任何事物连接的能力: 所有主流编程语言，主流 AI 应用(语音/视觉)，所有主流开源硬件，以及与玩家已有的有趣产品(cozmo/toio/乐高)连接并互动。让它们彼此增强，扩大创造的可能性和可玩性，而不局限在任何单一厂商设备已有的能力里。

此外，市面上最好的 Python 学习环境[Jupyterlab 已成为内置的插件](https://adapter.codelab.club/extension_guide/jupyterlab/)，你甚至可以使用 Adapter Jupyterlab 插件来阅读和修改它本身的代码！CodeLab Adapter 3.0 也将负责 Python 的环境管理，能帮你完成 JupyterLab 本身的安装之类的事情，不需要进入不友好的命令行，这对于减少入门者掉眼泪很有帮助。

此外值得一提的是，插件发布者，在插件里可以附带插件的文档信息，它可以链接到任何第三方网站里。这也是我们为了提高易用性而做的努力，并且以开放的方式来做。

![](https://adapter.codelab.club/img/1efc4c2cf4dcba42d009f78f4343e8f0.png)

### 插件市场

这是用户多次反馈的另一个问题，他们希望有一个统一的插件市场，可以方便下载到新的插件，就像我们在 vscode 或 sublime text 里的体验的那种插件系统，有个体面的 UI，而不是使用 curl 或者 wget 去 github 里手动下载。

![](https://adapter.codelab.club/img/4c48b29253b1923ce61ba104e5ef21fa.png)

作为演示我们下载了插件市场里的一个番茄工作法插件，这个插件的功能很简单(源码也是公开的): 每 25 分钟提醒编程者起来看看窗外风景。

![](https://adapter.codelab.club/img/06be05f915263f36d4663074d6147cb5.png)

下载完成之后，不需要重启软件，即可在 Scratch 和 Web UI 中看到新下载的插件，点击运行它：每 25 分钟，你就会收到一条信息提示你做个短途休息。

![](https://adapter.codelab.club/img/b6d455988e421b05e1aa9eb593957c6a.png)

值得注意的是, Scratch 里的积木也是实时更新的，它与 Adapter 实时同步，没有中断和刷新！

![](https://adapter.codelab.club/img/117126c46882c9d1122868519d0ad066.png)

为了追求连贯的编程体验，一切都是动态的！这是我们从 Smalltalk 和 Lively 那儿得到的观念：提供一个活的编程环境(Live Programming)。

利用这个特性，你可以做非常多有趣的事，[这些源码](https://github.com/CodeLabClub/scratch3_eim/blob/v3/index.js#L535)，我们都开放在 Github 了，

Scratch 内积木的动态机制，主要由 @shenyu 完成。

# 健壮

3.0 修复了很多之前版本的稳定性问题，这些都在源码中记录了。

其中最重要的一点值得一提，CodeLab Adapter 的心脏是消息系统，其他的一切都建立在它们之上。

此次的版本我们重点对此做了加固和保护，使其不大可能崩溃，即便消息本身错误或不完整的，消息内核也不会崩溃，它会向你指出问题所在。这样一来，错误就被限制在外围插件中，而 CodeLab Adapter 的内部组件也是插件！所以理论上，它将随着时间演化，越来越坚固。

# 开始使用

CodeLab Adapter 3.0 的[下载地址](https://adapter.codelab.club/user_guide/install/)与之前相同，它是免安装的。运行之后，记得更新插件。

有任何问题，欢迎与我们联系。

# 写在后边

## CodeLab Adapter 3.0 与 Scratch 3.0

Scratch 最初来自 Smalltalk 社区。尽管 Scratch 3.0 改由 JavaScript 实现（为了更好地支持网络社区），但其编程风格和体系设计依然保持 Smalltalk 风格， 消息(message)和对象/角色 是其一等公民，也是它的思考方式。 这也正是熟悉传统编程语言的开发者/教育者，觉得 Scratch 非常奇怪的一个原因。

以 C 或 Java 的风格理解和教学 Scratch ，会觉得使用它是一种将就, 带着疲弱感, 希望快快从中逃离，进入`真正`的编程世界里( Python/C/C++... ), 人们无法发挥它继承自 Smalltalk 的灵活性，这令人遗憾，但正是今天围绕编程入门教育的现状。

Scratch 全球社区有 5430.8 万用户, 还不包括国内各类 Scratch 的改编版的用户。如何赋予这个人群更强大的力量，让它们在其中理解 AI、物联网、开源硬件... 所有这些在 Scratch 创建之初，并未被考虑进来。这些东西，我们认为对于未来社会的公民至关重要，这正是今天各国教育看中 STEM 和编程教育的原因之一。如何将这些新事物与孩子们已经熟悉的工具 -- Scratch 结合起来，让新的知识从已经掌握的知识中自然生长出来，而不是造成更多割裂，是 CodeLab Adapter 最初的目标之一。 当然，今天 CodeLab Adapter 已经独立于 Scratch 可以支持其他 34+ 编程语言。

由于 CodeLab Adapter 最初是为增强 Scratch 3.0 ，所以 2019.04.06 我们前往 MIT Scratch Team 与他们分享了我们在这方面的工作（我们在之前的博客里有记录此次行程）。

![](https://adapter.codelab.club/img/codelab_mit.jpg) <!--Scratch mit-->

和 Scratch 3.0 类似，虽然在软件体系设计上，大量从 Smalltalk 汲取营养，但其实现语言，并未采用 Smalltalk, 对于 CodeLab Adapter， 实现语言是 Python 。原因是 Python 生态在今天高度成熟，允许我们以最小的代价实现它。而 Smalltalk 更偏向研究和学习，对于工程实践，生态很小，

由于两者的核心都是消息和对象，都是 Smalltalk 风格，它们背后的隐喻和思考方式是相似的，这点对于学习者的意义在于，Ta 们在不需要切换心理模型的情况下，可以扩展自身能力的范围。

在 CodeLab Adapter 3.0 中，我们将更多外部世界的能力引入 Scratch，同时我们重构了整个插件体系， 允许第三方公司像我们一样能够轻松扩展它以匹配自己的业务模型。

# 致敬

CodeLab Adapter 3.0 受到以下项目启发:

-   Smalltalk
-   Dynamicland
-   ZeroMQ
-   Jupyter
-   Lively
-   ROS
-   Cozmo/Vector SDK

关于系统设计方面，致敬 Alan kay，3.0 做了大量调整。所有这些变化之所以能够连贯地进行，而不至于坍塌，是因为它本质上一个消息系统，这正是 Alan Kay 一直坚持的更好"旧"事物，消息系统拥有惊人的灵活性，这类系统在演化过程中，并不是在重塑某种结构，更恰当的隐喻是，它像生物一样生长。

正是 Alan Kay [关于`面向对象`的异端见解](http://lists.squeakfoundation.org/pipermail/squeak-dev/1998-October/017019.html)， 让我们得以如此愉快地编程。

此外， 年初的 Dynamicland 之行，对我们的影响也很大 ，我们在[奥克兰的一间屋子里](https://blog.just4fun.site/post/%E7%BC%96%E7%A8%8B/the-next-big-thing-is-a-room/)亲眼见识了真正伟大的项目，如 Alan Kay 所说，Bret 在 Dynamicland 里延续恩格尔巴特的理想。今天如果有什么地方像 80 年代的施乐实验室一样令人惊叹和热血沸腾，Dynamicland 肯定是其一(如果不是唯一的话) -- 奥克兰街角处的一间屋子，午后透窗的阳光和 Bret 本人一样安静，像一个赶工的忙碌木匠。

感谢 志愿者 @Finn 和 @实习生 David 的同行和一路讨论。

Dynamicland 对 "one world" 的坚持是奇怪的，仿佛在使用全局变量之类的东西。那其实是消息。

我们从 Dynamicland 带回了一些他们的资料，资料里提到今年年底， Dynamicland 将离开实验室， CodeLab 希望在国内第一个实践它，并将其核心系统 realtalk 接入到 CodeLab Adapter 。 在 3.0 中，我们之所以致力于提升灵活性并扩展消息结构， 是为今年年底，接入 Dynamicland 作准备。

## 后记

写完这篇东西，以及发布完软件新版本，如释重负。

原本计划上周发布它，拖了一周，有点抱歉，简单做个解释。

围绕这个项目，前后思考了 2 年有余，关于 messaging 的许多问题，也持续困扰了我两年多，这些问题有时让人恼火，有时让人沮丧，有时令人热血沸腾（它发生在洗澡、爬山或睡醒时），但从不让人平静。它有时造成睡眠不好，神经衰弱，尤其在每次重构的时候，对之前自己的愚蠢都感到触目惊心。

由于疫情，有大把时间读其他采用了消息的优秀项目源码。这段时间，大体上读完 Jupyter、ROS1/ROS2 client 源码、Vector SDK 源码、Pieter Hintjens 混合了吐槽和奇妙洞见的 ZeroMQ 引导、以及 Smalltalk 几位作者的早期论文，把过去积累的困惑差弄懂了许多，但造成的问题是，想不停推翻之前写的东西。

原本计划上周发布，发布前发现很多地方需要重写，一开始试图安慰自己说那些可以在以后的迭代里做，可越想越不对，有些体系设计缺陷，如果不现在处理，以后的代价会很大。原本想假装没看见，以后的烦恼留给以后，想快点发布它，好睡个好觉。但第二天一早醒来问题还在那里。上周有一天，早上 6 点多醒来，决定把几个大的模块彻底重写，因为里边有几个严重问题，包括消息 channel 的命名，而糟糕的命名又会混淆概念，让体系越来越混乱。那天在屏幕前待太久，导致这一周视力还有点问题， 希望快点恢复。

好歹它现在完成了, 接下来软件肯定还会有很多 bug，但我相信不会是结构性的问题，新的问题，可以在迭代中优化，期待你的反馈，让我们在迭代里一起改进它。

最后希望，我们的工作，为你带来乐趣 :)

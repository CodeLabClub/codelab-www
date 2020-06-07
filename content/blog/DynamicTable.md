---
Date: 2020-05-31
title: "CodeLab DynamicTable: A Seeing World"
Slug: CodeLab-DynamicTable-A-Seeing-World
tags: ["CodeLab"]
author: CodeLab
categories: ["CodeLab"]
---

<img class="img-responsive" src="http://adapter.codelab.club/img/WechatIMG1946.jpeg" />

> 当心灵和手不默契，艺术将不存在 -- 达·芬奇

> 在设计这样一个系统时，我们使用的一个隐喻是乐器，比如长笛，它是用户拥有的，并对用户的愿望作出即时和一致的响应。想象一下，在吹出一个音符和听到它之间的一秒钟的延迟是多么荒谬！ --Alan Kay & Adele Goldberg 《Personal Dynamic Media》

<!--more-->

# 是什么东西？

CodeLab DynamicTable 是个什么东西？

老实说, 在开始写这篇文章的时候，我并不确切知道它是个啥。

所以打算先从 DynamicTable 出现的背景说起，溯本求源，有时能帮我们看清事物。

我们在 CodeLab 里构建了一个可编程空间(Neverland)，许多人对这里头发生的事情感兴趣，每周我们会接待若干访客。由于这个空间被设计成[高度开放和动态(Dynamic)的系统](https://www.codelab.club/blog/design-principles-behind-neverland/)，它试图连接一切，在交流的时候，访客们很容易把自己的想象植入进来，讨论他们由所见事物引发的联想。

脑洞通常产生于不同背景的访客到来的时候，其中有些脑洞，特别令人振奋，我们便在当天就把脑洞制作了出来，而这些新构建出来的事物，又常常成为下一个访客进一步想象的基础。

<!--这些联想中，有些是人们之前试图想做的事情(如@Rick多年来对可编程空间的想象)，有些是人们深受(STEM教育从业者)。
不同背景的人看到的东西和想象的应用场景似乎完全不同，这让我们一开始很惊讶。
-->

DynamicTable 是这个不断循环的过程的产物。

它与以下 人/事/物/书 相关。

-   今年 1 月份拜访了 [Dynamicland](https://dynamicland.org/)， 深受触动，我们准备复现一些在[Dynamicland](https://dynamicland.org/)见到的惊人事物。Dynamicland 认为 **笔、剪刀和订书机是真正的强大工具**。
-   Seymour 在《Mindstorms》第五章里提到 microworld 的概念: 每个 microworld 都可以成为一个可以探索的、可以操作的环境。
-   Alan Kay 和 Adele Goldberg 在[Personal Dynamic Media](http://www.newmediareader.com/book_samples/nmr-26-kay.pdf)提到 "在设计这样一个系统时，我们使用的一个隐喻是乐器，比如长笛，它是用户拥有的，并对用户的愿望作出即时和一致的响应。想象一下，在吹出一个音符和听到它之间的一秒钟的延迟是多么荒谬！"
-   我们把早期构建的几个 demo（目前都放在 [CodeLab blog](https://www.codelab.club/blog/) 上）分享出来，希望有一个名字来描述它们，@liyi 提出使用 DynamicTable 描述 CodeLab 在桌子上做的各种编程实验。
-   @Rick 第三次来访时，看到我们在桌子上的实验项目: [桌面纸片编程](https://www.codelab.club/blog/mini-vm/)，受此触动，大开脑洞。当天制作的[spelling](https://www.codelab.club/blog/spelling/) 和[如何画一只会跑的独角兽 🦄](https://www.codelab.club/blog/how-to-draw-a-running-unicorn/)都来自 @Rick 的脑洞。
-   而触动 @Rick 的桌面纸片编程，则由于一些孩子的来访。他们的父母提出这样一个问题: "能否在没有屏幕的情况下为 CodeLab 空间里的所有事物编程呢？ 因为近期的网课，孩子长期对着屏幕，导致视力下降。" 作为回应，我们在桌子上制作了使用物理积木为空间里的一切编程。
-   @jinlei 在看了 @Rick 的脑洞产物: [spelling](https://www.codelab.club/blog/spelling/)之后，十分兴奋，提到这种桌面交互式的环境可以在多门学科里应用，允许设计的内容形式是极其丰富的！在这个讨论之后，我们制作了[我们想要一个答案](https://www.codelab.club/blog/the-answer-to-everything/)和[皮卡与皮卡丘的区别](https://www.codelab.club/blog/the-difference-between-pickup-truck-and-pikachu-in-chinese/)，作为中文词汇游戏和数学四则运算的原型
-   [我们想要一个答案](https://www.codelab.club/blog/the-answer-to-everything/)的制作与 @liyi 也有关，@liyi 在看到[spelling](https://www.codelab.club/blog/spelling/)之后，想到他在东京的松下智能展厅里看到的交互式数学游戏(@liyi 本科学的是数学，对数学感兴趣)，他提到说这样的交互式环境，将让数学变得有趣，@liyi 构想了 DynamicTable 如何用于复现松下的数学游戏 。在复现这个案例之前，我们先做了一个更简单的数学 demo: [我们想要一个答案](https://www.codelab.club/blog/the-answer-to-everything/). 这个案例的名字来自@liuqing，她制作了视频里的卡片和视频本身。@jinlei 为这个项目起的名字则是 DynamicTable4Math。视频里 42 的梗是我想出来的，我对这个梗洋洋得意，所以在我自己的博客上，给这个案例起的名字是[42](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/42/)。这种协作方式和脑洞的交叉融合，是 CodeLab 日常发生的事情。我们相信，这也是开放的创造环境的自然产物。
-   @种瓜 制作了大多数的想法的原型。
-   @David 曾是 CodeLab 的实习生。也是目前最理解 Dynamicland 的人之一，他站在 Dynamicland 视角，对 DynamicTable 原型背后的技术架构和设计原则给出了许多建议。他指出了原型中关于`指向`问题的不足，也提出一些目前尚未实现但真正具有想象力的想法(诸如代码的可视性，把程序附到事物上)，@David 之前的兴趣是量子力学，经历了 Alan Kay/Bret/明斯基/Seymour 之后，目前他的看法是 "想象能力在计算机领域能得到更好的发挥"
-   [编程少年 1+1 访谈](https://www.codelab.club/blog/interview-01/)的受访者@Hanson, 提问说“能否在网上搜索某个关键词，然后在 Scratch 里播放视频片段”，这个问题导致了我们增强了 Scratch 与视频/动画的互操作。最终由 @shenyu 为 Scratch 引入了了外部的图片帧，而这个东西是[使用 CodeLab DynamicTable 解释动画原理](https://blog.just4fun.site/post/dynamictable-and-animation/) 原型的基础。这部分的文档，我们会尽快补上。
-   [编程少年 1+1 访谈](https://www.codelab.club/blog/interview-01/)的另一位受访者@在梦里，在看了 DynamicTable 的几个 demo 后，发现它"似乎无法使用 Teachable Machine 实现"，于是提问说 "是否可以通过输入几个训练图像，自动生成模型，然后识别图像中是否包含模型的图像类型，甚至位置"。@在梦里的问题非常精彩，实际上@Dynamicland 今年的核心目标之一正是这个！Github 上有一个博士论文的相关源码，做的也是这件事(我已经把源码分享给了@在梦里，由于涉及到深度学习，@在梦里近期在学习深度学习)。我们目前也正在基于前头提到的开放源码，实施这个想法。
-   访客 @zhangxuewu 提到基于 OCR 来识别实物文本，我们之前做过基于 OCR 的实验，发现不如 ArUco marker 稳定，目前在使用 ArUco marker 作为实物标识之一。
-   @Finn / @jackson / @yuanchi / @yuchen 讨论该项目的硬件构成，以及如何将其产品化。
-   @jinlei 联想到了一些更有趣意思的交互形式，我们还未实现出来，如 storytelling 等，未来会继续基于这些脑洞，构建新的原型。

CodeLab DynamicTable 是一个混合了许多人想象力的集体产物。我们在这篇文章里阐述它，也以此欢迎 @yub 的加入，明天 @yub 将正式入职 CodeLab，随着 @yub 的加入，我们将开始规划和运营 CodeLab 的线上开放社区，更多的集体脑洞、相互启发和学习、想象力的交叉融合将不止发生在 CodeLab Neverland 里。

# 展示原型 Demo

接下来展示一些原型 Demo，通过这些原型，先对 DynamicTable 建立其直观感受，我们将在其后，说明 DynamicTable 究竟是什么。

[Smalltalk 背后的设计原则](https://blog.just4fun.site/post/%E7%BC%96%E7%A8%8B/design-principles-behind-smalltalk/) 提到构建 Smalltalk 遵循的工作周期:

-   在当前系统内构建一个应用程序（进行观察）
-   根据经验，重新设计语言（形成一种理论）
-   基于新设计构建新系统（做出可测试的预测）

循环这个周期。

我们目前也大体上遵循这个工作周期（只是没有设计自己的编程语言，选择 Scratch ，并对其进行改进），这便是我们在清楚定义 DynamicTable 之前，在当前系统内构建许多应用程序的原因。

### 拍案惊球

<video width=40% src="https://adapter.codelab.club/video/%E6%8B%8D%E6%A1%88%E6%83%8A%E7%90%83.mp4" controls="controls"></video>

### 探索二进制

<video width=80% src="https://adapter.codelab.club/video/二进制.mp4" controls="controls"></video>

### 桌面泡泡龙

<video width=40% src="https://adapter.codelab.club/video/toio泡泡龙.mp4" controls="controls"></video>

### 看到机器人内部状态

<video width=80% src="https://adapter.codelab.club/video/1576905372587643.mp4" controls="controls"></video>

### COVID-19: 交互式可探索的环境

<video width=80% src="https://adapter.codelab.club/video/1589296982429059.mp4" controls="controls"></video>

<video width=80% src="https://adapter.codelab.club/video/1589296982422368.mp4" controls="controls"></video>

### 物理编程

<video width=80% src="https://adapter.codelab.club/video/1589459621915320.mp4" controls="controls"></video>

<video width=80% src="https://adapter.codelab.club/video/1589459630916864.mp4" controls="controls"></video>

#### 构建一个小型解释器

<video width=80% src="https://adapter.codelab.club/video/1589977785885032.mp4" controls="controls"></video>

### spelling

<video width=80% src="https://adapter.codelab.club/video/1590154622682774.mp4" controls="controls"></video>

### 皮卡与皮卡丘

<video width=80% src="https://adapter.codelab.club/video/1590237395592969.mp4" controls="controls"></video>

### 如何画一只会跑的独角兽 🦄️

<video width=80% src="https://adapter.codelab.club/video/1590237319828796.mp4" controls="controls"></video>

### 42

<video width=80% src="https://adapter.codelab.club/video/42.mp4" controls="controls"></video>

### Teachable Machine

<video width=80% src="https://adapter.codelab.club/video/tm_scratch_dy.mp4" controls="controls"></video>

### 动画原理

<video width=80% src="https://adapter.codelab.club/video/1590665913541756.mp4" controls="controls"></video>

<video width=80% src="https://adapter.codelab.club/video/1590665910081123.mp4" controls="controls"></video>

# 是什么

>  技术使普通的物理材料（纸和泥土，卡片和玩具车）栩栩如生。 -- Dynamicland

看了许多原型 demo，我们来归纳一下 ， DynamicTable 是:

-   集体想象的产物。
-   是一个工具包(toolkit)，而不是一个 APP
    -   鼓励创作者使用剪刀、纸张、玩具等事物进行创作。
-   是一种开放的可编程环境
    -   使用 Scratch 即时构建应用程序。
    -   基于 CodeLab Adapter 连接万物
        -   与 CodeLab 可编程空间拥有一样的设计理念，可以视为它的一个 micro 版本
-   实物与虚拟事物融合在桌面上，可交互
    -   交互的规则由用户自定义
    -   在环境中,洞悉(seeing)事物的内部/运行状态，以便于创作者真正理解复杂事物

接下来，我们来细致地阐述它:

## 集体想象的产物

在上文中已经讨论过了。

## 是一个工具包(toolkit)，而不是一个 APP

> Designed for agency, not apps -- Dynamicland

主要受到 Dynamicland 关于 [agency](<https://en.wikipedia.org/wiki/Agency_(sociology)>) 的思考的影响。

在社会科学中，agency 被定义为个人独立行动和进行自由选择的能力。

约翰·洛克最早在政治学领域讨论了[agency](<https://en.wikipedia.org/wiki/Agency_(sociology)>)的概念， 他拒绝传统的束缚和社会契约概念(卢梭)，导致了 agency 的概念，他认为 agency 是人类塑造其生活环境的能力。洛克把自由的概念建立在其上 ，在这个意义上，我相信 Bret 是计算机世界的 约翰·洛克。

Bret 的目标是构建人性化的动态媒体(Dynamic Medium)，所有人都可以使用其全部功能，以及用于创造新东西。

### APP 模式的问题

APP 模式意味着你能够做的事情的边界早已由 APP 供应商确定，你最好是一个标准"消费者"， 使用开发商已经为你规划好的功能，如果你总有许多新想法，你就不是一个“好用户”，而且将处处碰壁。

APP 模式就像公共汽车。你可以乘坐它抵达许多地方，但无法抵达路线图里未曾规划的地方。除非你已经明确知道要去哪里，乘坐公共汽车才是一种方便快捷的旅行方式。

如果你要做的事情是高度个性化的，与创造有关，你就需要一套更加强大的工具，让你随心所欲去表达。除了想象力，不应该有其他边界。它必须是高度可扩展的、开放的（我们在[CodeLab 可编程空间 背后的理念与设计原则](https://www.codelab.club/blog/design-principles-behind-neverland/)做了讨论）。

Scratch 这样的编程/创作平台，其精神内核是反 APP 模式的，它希望人们成为创作者，去表达自己的愿望和热情，以及基于自己的需要，去构建适合自己的东西(可能是动画、游戏或者 APP)，Scratch 试图拓展用户自己可以做的事情：一个孩子可以自己构建游戏或者动画，而不只是消费它，所以 Scratch 许多年以来一直被禁止在 Apple 应用商店中使用。(参考[Why AR Will Win - And Why it Matters How it Will Win](http://www.croquet.zone/2019/01/why-ar-will-win-and-why-it-matters-how.html))。

### 工具包(toolkit)

> 一些大宗商品，如汽车和电视机，试图以一种相当呆板的方式预测和提供各种应用；那些希望做一些不同的事情的人将不得不付出相当大的努力。其他物品，如纸和粘土，提供了多种可能性和高分辨率；许多人可能会以一种意想不到的方式使用这些工具 --Alan Kay & Adele Goldberg 《Personal Dynamic Media》

![](http://adapter.codelab.club/img/WechatIMG1946.jpeg)

CodeLab DynamicTable 沿袭 Scratch 的精神内核，试图提供一种创作的环境，它将创作环境从屏幕延伸到你的桌面上。

我们希望提供一个工具包，工具包里有纸张、橡皮泥、剪刀、水彩笔... 工具包本身的可扩展的，你可以把任何你喜欢的东西加入进来。使用它们去动手创作和编程。

这正是 CodeLab DynamicTable 与今天所有桌面实物编程产品的区别（大多数是 APP 模式）。 <!--诸如 [Osmo](https://www.playosmo.com/)-->

DynamicTable 不假设你对哪类事物编程，它可能是 Toio、Cozmo，或者桌面的一盏台灯。 可能你想使用**剪刀**把小人书的最喜欢的角色剪了下来，为这些角色编排一个舞台剧；或者让机器人馋你的香蕉味的**彩虹糖**。

<video width=80% src="https://adapter.codelab.club/video/toio_candy.mp4" controls="controls"></video>

可能你在入门 AI 的时候，使用 Teachable Machine 演奏卡片上的乐器

<video width=80% src="https://adapter.codelab.club/video/tm_scratch_dy.mp4" controls="controls"></video>

而在 Teachable Machine 无法支撑你的想象时，准备把深度学习引入其中(就像@在梦里现在在做的)。

CodeLab DynamicTable 不对你使用的工具做限制，而是试图提供一个通用的工具包(toolkit)，这个工具包包含一些真正强大的事物:

-   铅笔
-   剪刀
-   纸张
-   橡皮泥
-   可打印的 Marker
-   摄像头
-   显示设备(短焦投影仪)
-   桌子
-   CodeLab Scratch
-   CodeLab Adapter
-   ...

## 开放的可编程环境

如果只是在桌子上剪纸、画画，这和 CodeLab 有啥关系呢？毕竟 CodeLab 使命是:

> 传递编程的乐趣，帮助孩子成为数字时代的创作者。

DynamicTable 上的纸张、橡皮泥和机器人，全部是可编程的！

可是它们都没电子元件？如何与计算机互动呢？

这便是今天的 AI 技术 派上用场的地方了，我们可以使用机器视觉等技术，让桌面的实物融入计算环境中，进而使其成为 Scratch 可操控的事物。桌面环境是计算机的一部分。具有了动态(Dynamic)/可编程的属性。

我们使用 CodeLab Scratch 和 CodeLab Adapter 构建这个可编程环境。

#### Scratch

> 其次，孩子们喜欢！对话的互动性、他们掌控一切的事实、他们在做真实事情而不是玩玩具或解决“指定”问题的感觉，其结果的形象化和听觉性，所有这些都为他们的经历带来了巨大的成就感。他们的注意力持续时间是用小时而不是分钟来衡量的。 --Alan Kay & Adele Goldberg 《Personal Dynamic Media》

选择 Scratch 的原因是因为，全球有 5000 万+的孩子熟悉 Scratch，孩子们可以使用 Scratch 自行构建个性化的应用程序。

幼儿园老师，以及不同学科的老师，在没有任何编程基础的背景下，可以轻松学会 Scratch(毕竟许多 7 岁的孩子都能熟练使用它)。这样一来，这些老师就可以制作出最适合自己学科的生动教案。

假设我是一个物理学老师，我希望让学生"感受"万有引力常数 G 对宇宙的影响(`F = (G*M*m)/(r^2)`)， 我可以基于 Scratch 构建这样一个程序：

<video width=80% src="https://adapter.codelab.club/video/%E9%87%8D%E5%8A%9B%E6%95%88%E5%BA%94.mp4" controls="controls"></video>

程序采用 Scratch 构建，使用 leap motion 将学生的手投射到虚拟的宇宙中，动"手"去改变 引力常数 G 的大小，观察宇宙的变化，去"感受"它。

如果我是一个数学老师，正准备向学生解释二进制。我可以构建一个探索式的环境，在给出二进制与十进制的转换规则前，让大家在桌子上去探索它:

<video width=80% src="https://adapter.codelab.club/video/二进制.mp4" controls="controls"></video>

由于这些应用程序只是 Scratch，所以人们也可以把它分享到社区，让更多人可以使用自己制作的教学应用，如果参与的人多，则自然形成一个应用市场。

一家商业公司可以构建精致的学科案例或者从社区中挑选优质的案例，去服务特定人群，作为解决方案分发它。

#### 基于 CodeLab Adapter 连接万物

DynamicTable 与 [CodeLab 可编程空间拥有一样的设计理念](https://www.codelab.club/blog/design-principles-behind-neverland/)，可以视为它的一个 micro 版本。

由于 CodeLab Adapter 可以连接一切开放的事物，所有这些东西都可以成为桌面上的创造素材！

![](https://adapter.codelab.club/img/adapter_party.jpeg)

## 实物与虚拟事物融合在桌面上，可交互

这是 AR（增强现实， Augmented Reality） 吗？

AR 是指:

> 透过摄影机影像的位置及角度精算并加上图像分析技术，让屏幕上的虚拟世界能够与现实世界场景进行结合与交互的技术。

在 DynamicTable 上，投影里的数字世界与现实世界场景似乎进行了融合，在这个视角下，它们似乎相似。但 DynamicTable 不是 AR，它只是现实(R，Reality) (参考[DYNAMICLAND AND THE WHIMSICAL DIGITAL OBJECT](http://www.cabinetmagazine.org/kiosk/kan-sperling_olivia_28_august_2019.php))。

DynamicTable 与 AR 的区别不在于技术，在于它们的目标不同。DynamicTable 的目标是构建一种灵活的创造环境，将计算机延伸到一个桌面上。投影仪只是为实现这个目标的临时策略。随着物联网(iot)技术的进展，每个小物体都是一个计算机(Smalltalk 构想了递归的计算机)，不远的未来，现实中将充满计算设备。未来，投影未必是需要的, 呈现信息的方式，可能采用 Dynamic Paper（这是 Bret 构思的一种连接动态媒介）。更多的脑洞参考[这篇文章](https://medium.com/@wittkensis/reflections-on-dynamicland-65158b06196)。 关于这点更清晰的说明来自 Dynamicland 的 FAQ 页面，不过近期这个页面暂时无法访问。

我们在桌面上叠加投影的目标是为了动态呈现信息, 主要受到 Bret[《Seeing Spaces》](http://worrydream.com/SeeingSpaces/)的启发:

> The challenge is not building it but understanding it -- Bret 《Seeing Spaces》

![](http://adapter.codelab.club/img/2d7ce60948c640ce4ece2178165e48e7.png)

如果你有过制作复杂游戏、机器人、或者构建智能体的经验，可能感受过构建这些复杂事物的困难所在: 我们的视野狭窄，所见的信息都是碎片，难以看到智能事物的内部状态(它的行为通常与它的状态有关)，当意外情况发生时，我们甚至难以复现真实场景，机器人本该左转 30 度，为何转了 60 度？你的同伴可能争辩说，不，它转动了 45 度！谁是对的？我们希望时间倒退，重复观察一次。因为错误有时是难以复现的。

是当前的光线变量干扰它了吗？是它的传感器数据的错误吗？是运行时候，策略逻辑设计的有问题吗？

Bret 在这个问题下，发表了[《Seeing Spaces》](http://worrydream.com/SeeingSpaces/)的演讲，极具冲击性。为了理解复杂事物， 我们需要:

-   seeing inside
-   seeing across time
-   seeing across possibilities

如果我们的环境本身就是计算机，环境中的事物与它融为一体，那我们就可以使用这个环境来增强、记录环境中的事物.

由于环境本身可编程，并且可以叠加丰富的信息，我们在这样的环境中将获得新的视野。

Bret 的关注点始终是 计算机增强人类。

这样的桌面环境，它不止可以帮助创作者获得多维视角去理解被造物。

同时允许他们去制作一些交互式的好玩事物, just for fun:

<video width=80% src="https://adapter.codelab.club/video/1590237319828796.mp4" controls="controls"></video>

## 技术视角

我们现在站在技术的视角上看看 DynamicTable 的构成是些什么东西。

前边提到，它的构成包括:

-   铅笔
-   剪刀
-   纸张
-   橡皮泥
-   可打印的 Marker
-   摄像头
-   显示设备(超短焦投影仪)
-   桌子
-   CodeLab Scratch
-   CodeLab Adapter
-   ...

铅笔、剪刀、纸张、橡皮泥这些东西来自日常，无需特别说明。

我们重点说说:

-   可打印的 Marker
-   摄像头
-   短焦投影仪
-   桌子
-   CodeLab Scratch
-   CodeLab Adapter

### 可打印的 Marker

我们目前没有选择 Dynamicland 的 Marker（彩色圆点）:

![](https://adapter.codelab.club/img/1_H3t1twFMu28vOdyMbrfmPw.png)

而选择了 ArUco（在机器人领域用的很广泛，从 amazon 的自动化仓库到 ROS 机器人社区都在使用它） 作为 Marker。ArUco Marker 在 AR 领域用得也很广泛，它是一个开放项目。

![](https://adapter.codelab.club/img/271fd78437972115df19f73162066695.png)

我们通过 ArUco marker 将任何现实事物投射到计算机里。 ArUco marker 有许多优良的特性，@在梦里 前边想要的特性"图像类型，甚至位置"都能实现，而且可以在毫秒级的时间里解析数十个 Marker！

之所以暂未使用 Dynamicland 所使用的 Marker，因其尚未公开更多细节。 虽然有社区实现版，但 Bret 思虑深远，目前社区对他的理解，都只是在各个不同横截面上，我们期待 Dynamicland 公布 Marker 和驱动程序的真实细节。

如果疫情允许，年底计划在他们 2020 年里程碑完成之后，重新过去一趟，那时会考虑切换到 Dynamicland 的 Marker 上。

在 DynamiTable 场景中， ArUco Marker 相比于 Dynamicland 的 Marker，有一些明显缺陷，Dynamicland Marker 是包裹式的，它可以动态选择实物的边界！这个特性十分优越！Dynamicland Marker 的可见度也更好。 不过 ArUco Marker 也已经很不错了。

### 摄像头

普通 USB 摄像头即可（我们选择了罗技的一款摄像头），最好配上活动支架。由于 DynamiTable 是一个灵活的创造环境， 摄像头会服务于多种场景，最好是活动的。 CodeLab 里的活动摄像头组件 ， 由 @David 在实习的时候选配和搭建。目前我们用得很好。

### 超短焦投影仪

![](https://adapter.codelab.club/img/1eec2b121660441c6d5ba7ceceef469c.png)

我们选择了 LG 的一款短焦投影: PH450UG， 33cm 就可以获得 80 英寸的大屏幕。

但其流明不高：450。 所以我们演示时一般只留一盏灯。

### 桌子

目前我们选择的桌子是宜家的电动升降桌，桌面反光率并不理想，我们合作团队 Longan 正在寻找更合适的桌子。 @jackson 觉得 `亚光白色防火板可能OK`，有待实验。

我们希望将信息和虚拟世界叠加在桌面而不是幕布上，因为我们希望“计算机就是桌面环境”，它们应融为一体。 这种一体感允许构建许多有趣的应用，索尼的黑科技: Xperia Touch 展示了这方便的有趣场景。

这样一张桌面也是一个用于实验和展示的舞台区。它可能出现在一个展厅里，作为交互中心。

甚至可能是一个 DJ 台，打碟的工具就是香蕉和苹果！

<video width=80% src="https://adapter.codelab.club/video/1590913857227893.mp4" controls="controls"></video>

### CodeLab Scratch

> 动画、音乐和编程可以被认为是动态过程的不同感官视图。 --Alan Kay & Adele Goldberg 《Personal Dynamic Media》

CodeLab Scratch 是编程创作平台。

未来我们也允许在社区里分发这些应用，它可能是一个老师构建来用于数学/物理教育的应用(如我们前头展示的)，也可能只是孩子们制作的游戏或恶作剧。 又或者是一个交互式博物馆里用于展示新冠疫情的探索式可视化应用。

重要的是，一切都是 Scratch！任何人，包括 8 岁的孩子都可以轻松理解它；基于它再创作；并把自己的新想法融入进去。

### CodeLab Adapter

CodeLab Adapter 负责连接一切，通用的基础设施将作为 Adapter 插件，发布在 Adapter 插件市场里。

诸如前头解析 ArUco Marker 的程序，就是一个 Adapter 插件 （基于 OpenCV 构建），它还不到 100 行代码！这些工具足够通用，所以只要有人完成一次，社区里的所有成员都可以使用它去构建新的事物。值得一提的是，使用这些插件并不需要理解它，因为它们已经被抽象为了 Scratch 积木，积木才是创作者需要的原语。

这样一来我们可以做到: `all in scratch`。 这是提高可理解性的关键。

# 产品化

如果你对 DynamicTable 感兴趣，想将其产品化， [Toio](https://toio.io/)的模式值得参考: 定期推出不同主题的套件包。

<!--
最理解幼儿园的是老师

谁来设计软件

和 Dynamicland 回答同一个问题

# 构成

DynamicCard

## 硬件
树莓派或电脑

扫码打开

## 产品化需要考虑

树莓派按钮
切换游戏

自动联网
wifi connect

运行程序 Scratch

DynamicTable 构想(基于标识码的应用)

龙眼盒+摄像头(硬件设备)

定期推出的应用套件包(学习 toio)
桌面编程套餐包
英文拼写
小组比赛
中文拼写套餐包
动物主题套餐包
恐龙主题(各种不同的恐龙)
化学方程式套餐包
美术主题
神笔马良
四则运算套餐包
函数套餐包(李懿在松下体验馆看到的东西)
…

技术架构
Adapter 插件市场

阐述 蒙台梭利
如果蒙台梭利活在 21 世纪会做什么

建构主义

探索 恐龙 单词

默认主页 adapter，不要关闭
管理页

运行 Scratch 屏幕上也可以

-->

# 参考

-   《Mindstorms》
-   [Dynamicland](https://dynamicland.org/)
    -   [Seeing Space](http://worrydream.com/SeeingSpaces/)
    -   [Agency (sociology)](<https://en.wikipedia.org/wiki/Agency_(sociology)>)
-   [HyperCard](https://en.wikipedia.org/wiki/HyperCard)
-   [End-User Programming](<https://tinlizzie.org/IA/index.php/End-User_Programming_by_Alan_Kay_(1991)>)
-   [A Personal Computer for Children of All Ages](https://mprove.de/visionreality/media/kay72.html)
-   [Toio](https://toio.io/)
-   [CodeLab 可编程空间 背后的理念与设计原则](https://www.codelab.club/blog/design-principles-behind-neverland/)
-   [Personal Dynamic Media](http://www.newmediareader.com/book_samples/nmr-26-kay.pdf)
-   [Why AR Will Win - And Why it Matters How it Will Win](http://www.croquet.zone/2019/01/why-ar-will-win-and-why-it-matters-how.html)

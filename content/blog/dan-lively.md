---
Date: 2020-01-19
title: "Dan Ingalls 与 Lively"
Slug: Dan-Ingalls-and-Lively
tags: ["programming"]
categories: ["编程"]
author: "种瓜"
---

最近的兴趣集中在 `如何构建灵活、实时的编程环境, 为教育、创造和探索提供友好的支持`

正在研究以下几个项目:

*  [Etoys](http://www.squeakland.org/)
*  [Dynamicland](https://dynamicland.org/)
*  [Croquet](https://en.wikipedia.org/wiki/Croquet_Project)
*  [Lively](https://lively-kernel.org/)

本文主要对 Lively 相关资料做一番梳理，做为备忘录。

<!--more-->

# Dan Ingalls
Dan Ingalls是五代Smalltalk环境的主要架构师、设计师和实现者, 也是Alan Kay在施乐(Xerox Palo Alto)的老搭档。

Alan Kay在[《The Early History Of Smalltalk》](http://worrydream.com/EarlyHistoryOfSmalltalk/)里提到:

>  我们所有人都同意，在Smalltalk的大部分开发中，Daniel是核心人物…Daniel不仅仅是一个出色的实现者，随着Smalltalk进入到现实世界，Daniel逐渐承担越来越多设计师的职责，不仅是语言设计师，还包括用户界面设计师。

Dan Ingalls的最新项目是[Lively](https://lively-kernel.org/)。

# Lively

你可以通过[这个PPT](https://lively-next.org/users/robert/welcome.html)获得对Lively的直观感受.

PPT中提到的项目，你也可以亲手体验:

*  [Draggable Code](https://lively-web.org/users/robertkrahn/draggable-code.html)

## 概述
Lively是一种新的Web编程方法，使用MIT开源协议。目前该项目放在[HPI软件构架小组](http://www.hpi.uni-potsdam.de/hirschfeld/)下。它为Web应用程序提供了完整的平台，包括动态图形，网络访问和开发工具。

[维基百科](https://en.wikipedia.org/wiki/Lively_Kernel)将其概括为:

>  Lively Kernel是一个JavaScript环境，该环境允许实时、交互式进行Web编程，或与Web浏览器内部的对象进行实时交互。


>  Lively Kernel是一个图形合成和集成编程环境，它使用标准的浏览器图形（W3C Canvas或SVG）完全以JavaScript编写。因此，兼容任何浏览器，在加载网页后便开始运行。它能够编辑自己的代码和图形，并且通过其内置的[WebDAV](https://en.wikipedia.org/wiki/WebDAV)支持，可以保存结果，甚至可以将其克隆到新的网页上。除了具有应用程序开发功能外，它还可以充当自己的集成开发环境（IDE），使整个系统能够自给自足，除了浏览器外没有其他依赖。

## 称其为Lively的原因
*  只是网页。 无需安装。采用JavaScript编写，一旦浏览器加载了页面，它就会立即激活。
*  它可以改变自己并创建新内容。 Lively Kernel包括一个允许其更改和创建新图形内容的基本图形编辑器，以及一个允许其更改和创建新应用程序的集成开发环境（IDE）。它带有一个图形和计算组件库，这些组件以及内核可以随时更改和扩展。
*  它可以保存新的工件，甚至可以将自身克隆到新的Web页面上。该内核包括WebDAV支持，用于浏览和扩展远程文件系统，因此可以将其对象和"世界"（应用程序）保存为新的Web页面， 并保存到基于云的存储库中。

## 正在进行的项目
*  [lively.next](https://lively-next.org/):一组软件包, 一起构成了功能强大的IDE和构建套件。lively.next软件包可以与其他系统结合使用，以将它们连接并`提升`到Lively宇宙中，从而使Lively成为控制和混搭中心。
*  [Pronto](https://www.youtube.com/watch?v=if72CFsF_SY): Pronto是对Lively用户体验的重新构想，使新用户可以更轻松地访问它。更容易在平板电脑和其他触摸设备上使用，为简单的对象构造提供更多的指导和更少的混乱选择。 它将提供更强大和具体的构造功能，例如复制，简单的物理方法和其他约束。
*  [Lively-4](https://github.com/LivelyKernel/lively4-core): Lively-4是我们在Hasso Plattner Institute的合作者的工作 ，位于德国波茨坦。它具有与网页DOM结构更紧密结合的体系结构。提供了与非Lively网页进行更紧密交互的可能性。

逐一做些记录

# [lively.next](https://lively-next.org/)
lively.next主页的自我介绍是:

>  一个个人编程工具包。它强调生动、直接和互动。

## 目的
一个表达[有力想法](https://www.ted.com/talks/alan_kay_shares_a_powerful_idea_about_ideas#t-1110785)的平台，much in the tradition of [original](http://www.dougengelbart.org/firsts/dougs-1968-demo.html) [systems](http://worrydream.com/EarlyHistoryOfSmalltalk/) [and](https://www.youtube.com/watch?v=QQhVQ1UG6aM&feature=youtu.be&t=9s) [tools](https://en.wikipedia.org/wiki/HyperCard) that defined the meaning of "personal computing" –-这就是Lively项目的目的。

live.next系统构成了一个灵活的个人计算环境和构建工具包。我们希望这将是真正帮助我们思考、学习、做事和创造的媒介的垫脚石。

## 演示
<video width=80% src="https://lively-next.org/users/robert/lively-zine-2017-06/cpu-viz-2017.mp4" controls="controls"></video>

<video width=80% src="https://lively-next.org/webpage/Draggable_Code_Prototype_shorter.mp4" controls="controls"></video>


## [特性](https://lively-next.org/)
*  设计，开发，共享
    *  具有深度编程功能的对象系统， 对象可被直接操纵。lively.next允许人们快速制作原型并分享想法。开发是实时，即时和有趣的。 [调试模式是唯一模式](https://gbracha.blogspot.com/2012/11/debug-mode-is-only-mode.html)。
*  个人编程套件
    *  可以自由地修改，存储和共享工作区和对象。这允许创建针对特定任务的定制环境。临时脚本很容易，可以自动执行重复性任务或创建特定于领域的工具。
*  连接，混搭，提升
    *  是Web服务、JavaScript库、操作系统还是数据库；可以通过将外部系统的流程和数据与Lively丰富的编程功能结合起来，来构建混搭和系统集成。这将动态性较差的系统`提升`到实时编程领域。
*  全栈和模块化
    *  [lively.next的体系结构](https://lively-next.org/architecture.html)包括客户端和服务器，以及形成交互式开发环境所需的各个部分，例如运行时元系统，对象图持久性，存储和资源抽象等。这些组件是模块化和可重用的，请参阅我们的[开源库](https://github.com/LivelyKernel/)
*  起源
    *  Lively的外观可能不同于传统的编程系统，它是基于与40年前推出的Smalltalk系统相同的思想和机制。它的用户界面是Self的[Morphic](http://ftp.squeak.org/docs/Self-4.0-UI-Framework.pdf)的变体。Lively项目的目标是发展那些功能强大的概念，并将它们与新颖的思想相结合，以减少编程的僵化和狭窄。与其他Smalltalk系统类似，Lively是使用它自己来建模和实现的，没有人为的边界限制探索和变更。
*  研究
    *  Lively团队有兴趣探索新的编程抽象和范式。尽管当前的系统主要基于文本编程，但是我们正在积极开发更强大的抽象和工具，以弥合可视化和文本编程之间的鸿沟。可以在[此处](https://lively-next.org/projects.html)找到过去原型的不完整列表。


## 体验lively-next
[点击这儿](https://lively-next.org/worlds/)

# [Lively-4](https://github.com/LivelyKernel/lively4-core)
>  一个基于Web的探索性、自支持的开发环境

## 体验
[点击这儿](https://lively-kernel.org/lively4/lively4-core/start.html)

# 我的兴趣
从Dynamicland 回来，开始着手构建CodeLab Adapter 3.0。其中的一个工作是将Lively用做Adapter 其中的一个前端。Lively提供了远超Scratch的灵活性，又确保了易用性和可教学性，是绝佳的教育平台。

<img src="http://blog.just4fun.site/post/img/WechatIMG1128.jpeg" width=350 />

Scratch当然是极好的创造平台，但在基础架构上，整个领域在此停滞太久了，让我们试着做一些真正有想象力的事情吧，别只满足于换壳和重写Scratch了。

如果你也希望在基础设施上做一些改进，试着去理解Smalltalk和Lively。 不理解Smalltalk，你将永远无法理解Scratch(Scratch的第一个版本来自Smalltalk社区)。否则，对它的修修改改，只会导向糟糕得多的系统: 精致、臃肿、不灵活，最后失去创造性。正如我们在今天看到的大多数少儿编程平台。（[我之前的吐槽](https://blog.just4fun.site/post/%E9%9A%8F%E7%AC%94/lively-but-stupid/)）

我目前正在阅读[lively.next源码库](https://github.com/LivelyKernel/lively.next)和[lively4-core](https://github.com/CodeLabClub/lively4-core), 之后会将阅读时做的笔记和批注提交到仓库里。

# 一些问题和建议
lively4和live-next都在积极推进中，目前存在不少bug，诸如:

*  [lively.next源码库](https://github.com/LivelyKernel/lively.next)无法正常install
*  [todo-list-tutorial](https://lively-next.org/doc/todo-list-tutorial.html) 拖拽checkbox到tex中有问题
*  ...

目前建议从一些简单的项目开始探索，以下项目是非常好的起步方式。

*  [Draggable Code](https://lively-web.org/users/robertkrahn/draggable-code.html)
*  [cpu demo](https://lively-next.org/worlds/cpu%20demo)
*  [magic-card](https://lively-next.org/worlds/magic-card)
*  [how events are dispatched](https://lively-next.org/worlds/how%20events%20are%20dispatched)

另一个建议是，适应类Smalltalk环境的最好方式是: 在那个世界中与事物去交互(talk)，不要太在意文本代码的细节。

# 参考
*  [lively-next robert welcome](https://lively-next.org/users/robert/welcome.html)
    *  [Draggable Code](https://lively-web.org/users/robertkrahn/draggable-code.html)
    *  we can't not do this!
*  [Lively home](https://lively-kernel.org/)
*  [wikipedia Lively Kernel](https://en.wikipedia.org/wiki/Lively_Kernel)
*  [harc Lively](https://harc.ycr.org/project/lively/)
*  [lively next](https://lively-next.org/)
    *  [architecture](https://lively-next.org/architecture.html)
    *  [todo-list-tutorial](https://lively-next.org/doc/todo-list-tutorial.html): 拖拽checkbox到tex中有问题
    *  [projects](https://lively-next.org/projects.html)
*  [Lively github](https://github.com/LivelyKernel)
*  [Smalltalk背后的设计原则](https://blog.just4fun.site/post/%E7%BC%96%E7%A8%8B/design-principles-behind-smalltalk/)
*  [Dan Ingalls](https://en.wikipedia.org/wiki/Dan_Ingalls)
    *  [squeakland ingalls](https://web.archive.org/web/20070920090809/http://www.squeakland.org/community/biography/ingalls.html)
*  [Language Hacking in a Live Programming Environment](https://ohmlang.github.io/pubs/live2016/)
*  [Morphic: The Self User Interface Framework](http://ftp.squeak.org/docs/Self-4.0-UI-Framework.pdf)
*  [Debug Mode is the Only Mode](https://gbracha.blogspot.com/2012/11/debug-mode-is-only-mode.html)
    *  关注时间旅行（time-travel debugging）的概念
*  [Self-supporting, Extensible Programming Languages and Environments for Exploratory, Live Software Development](https://shonan.nii.ac.jp/seminars/147/)
*  [Web Browser as an Application Platform: The Lively Kernel Experience](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.137.2713&rep=rep1&type=pdf)
*  [The Sun Labs Lively Kernel](https://lively-kernel.org/development/media/LivelyKernel-TechnicalOverview.pdf)
*  [Learnable Programming](http://worrydream.com/#!/LearnableProgramming)
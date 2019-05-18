---
title: "两种硬件编程风格的比较"
date: 2018-07-25T13:22:00+08:00
---

<!--转载自 适应bootstrap的-->
<div class="alert alert-success">原文地址：<a href="https://blog.just4fun.site/Hardware-Programming-style.html">两种硬件编程风格的比较</a></div>


<img class="img-responsive" src="http://wwj-fig-bed.just4fun.site/message_a34afc78.png" />


>  人的心智活动透过简单的概念而发挥它的力量，方法主要可分为三种：第一，把数个简单的概念组合成一个复合的概念，于是所有复杂的概念成焉。第二，将两个概念，不论简单或复杂，不将它们结合，而是同时并列在一起观察，如此就能得知何为相互关联。第三，把某些概念，与伴随它们其他真实存在的概念区隔出来，称为这抽象艺术化，所有一般化，概化的概念皆是由此而生  - 约翰·洛克《人类理解论》


在[scratch3.0 + micro:bit](https://blog.just4fun.site/scratch3-microbit.html)中，我们提到

>  在少儿编程/硬件编程教育领域，硬件编程有两种风格，我将这两种风格分别称为`灌入式`和`交互式`

我相信就编程教育而言，`交互式`优于`灌入式`

这篇文章我们将讨论这两种编程风格给学习者的编程体验 以及心理状态所带来的影响。所谈论的很多内容，在编程语言的发展历史中都被反复讨论过。

本文中，我们只讨论图形化硬件编程，但得出的结论并不局限于此

<!--more-->

### 灌入式
`灌入式`阵营有名的图形化项目包括：

*  [makecode](https://www.microsoft.com/en-us/makecode)
*  [PythonEditor](https://github.com/bbcmicrobit/PythonEditor)
*  [mixly](http://mixly.org/)
*  以及国内大多数项目(makeblock、mcookie...)

事实上，几乎所有传统的硬件编程都是灌入式的

##### 编程方式
我们以[makecode microbit](https://pxt.microbit.org/)为例，来展示灌入式编程的编程方式.

<img src="http://wwj-fig-bed.just4fun.site/microbit_gr_de9399e6.png" width=500 />

在[makecode microbit](https://pxt.microbit.org/)中，通过拖拽积木，拼搭出我们的程序，接着将程序下载到本地（程序在线上完成编译），最后将下载的文件拖入micro:bit，即可运行。

将代码/固件灌入硬件中，代码(代码编译出的固件)将在硬件运行。我将这种编程风格称为`灌入式`。

如果你熟悉blockly,你会发现这是一种典型的blockly风格(当然，blockly也可以写出交互式风格的blockly app)


### 交互式

`交互式`阵营的图形化编程项目有:

*  [Cozmo code lab](https://www.anki.com/en-us/cozmo/code-lab)
*  [scratch Picoboard](https://en.scratch-wiki.info/wiki/PicoBoard)
*  [S4A](http://s4a.cat/)
*  [scratch microbit extension](https://llk.github.io/scratch-gui/microbit/)
*  [codelab-adapter](https://blog.just4fun.site/lab/codelab-adapter-docs/)

#####  编程方式
我们以[cozmo code lab](https://www.anki.com/en-us/cozmo/code-lab)为例，来展示`交互式`编程的编程方式.

![](http://wwj-fig-bed.just4fun.site/cozmof70f49bd.png)

在[cozmo code lab](https://www.anki.com/en-us/cozmo/code-lab)中，你同样身处积木化的编程界面里，通过拖拽积木，拼搭出所需的程序，点击运行，cozmo即可按照程序的逻辑运行。

程序运行在ipad/手机上，每个积木在实际执行的时候，将消息发给cozmo，从而控制cozmo，这是我将这种风格程序成为`交互式`的原因

在[cozmo code lab](https://www.anki.com/en-us/cozmo/code-lab)中一个非常惊艳的编程体验是:如果你不知道一个积木有什么作用，你不必去翻说明书，你只需要点击一下这个积木，cozmo立马执行这个积木的逻辑，你可以直观地理解陌生的积木。交互式编程所具有的及时反馈特性，鼓励学习者去探索。这是交互式编程给学习者心理上带来的影响之一。

[建构主义](https://zh.wikipedia.org/wiki/%E5%BB%BA%E6%A7%8B%E4%B8%BB%E7%BE%A9_(%E5%AD%B8%E7%BF%92%E7%90%86%E8%AB%96))者(如皮亚杰、艾伦凯、派普特)应该会喜欢这种风格

如果你熟悉scratch，你会发现这是一种典型的`scratch`风格（对象响应消息，很[Smalltalk](https://zh.wikipedia.org/zh-hans/Smalltalk)）。关于scratch风格和blockly风格的比较可以参考我之前的文章:[Blockly与Scratch3.0的比较分析及选型建议](https://blog.just4fun.site/scratch3-blockly.html)


# 对比分析
>  真理越辩越明

<!--
我很喜欢柏拉图《对话录》里苏格拉底对战普罗塔戈拉那一卷

工程师小普和小苏分别拥护`灌入式`和`交互式`，他们决定cosplay苏格拉底对战普罗塔戈拉来一场辩论

小苏:  好久不见啊小普，近来忙些什么

小普:  
-->

在此我们来对比分析一下`灌入式`和`交互式`各自的优势

灌入式阵营可能列出的优势有:

1.  灌入式可以离线运行，只需要将代码烧入进去，即可脱离编程工具
2.  灌入式将带来优于交互式的实时性
3.  灌入式因为需要generate代码，学生可以查看代码

如果有遗漏，欢迎拥护`灌入式`编程的小伙伴来信(wuwenjie718@gmail.com)补充

由于我拥护`交互式`编程，所以我准备在下文里，反驳`灌入式`的优势，并指出`交互式`所具有的优势。如果你不赞同，欢迎来信反驳，观点合理的话，我会及时更新到本文，如有必要，我们也可以使用[理性辩论的平台 Kialo](https://www.kialo.com/)来进行辩论

### 反驳灌入式的优势
我们针对上边`灌入式`阵营提出的三条优势，逐条反驳

>    灌入式可以离线运行，只需要将代码烧入进去，即可脱离编程工具

这个论述本身并没有需要反驳的地方，它只是陈述了一个事实，在此我想提出的是，对于教育而言，`离线运行`不是很重要的特性，如果是工业级的项目或者解决具体问题的硬件产品，离线运行可能是重要的，但对于教育项目而言，我认为这个特性并不重要，如果你实在不愿意一直开着电脑，你可以把上位机运行在树莓派里，若嫌贵，可以使用荔枝派(只要9块9哦)。但需要提醒的是，为了得到`离线运行`的特性，我们很可能会失去交互性(这个问题不是很好谈论，如果需要,我们之后专门来说说这两个特性在什么情况可能冲突，而不可兼得)。

>    灌入式将带来优于交互式的实时性

和上一条观点一样，我认为`实时性`在编程教育中并不重要。我将`离线运行`和`实时性`视为一种对机器性能的优化，前者节约资源、后者节约时间，但这种节约下来的时间，短得也许人类不能感知。我承认在一些竞技类的比赛中，`实时性`是至关重要的，但在教育中，尤其是低龄化编程教育中，被教育者是这件事的核心，我认为这些特性并不重要，尤其是考虑到这些特性可能和交互性冲突

>    灌入式因为需要generate代码，学生可以查看代码

给用户呈现积木所对应的代码，是个帮助用户从图形化过度到文本编程的好办法. 但generate代码这件事并不限于`灌入式`,`交互式`的编程界面里，虽然你并不需要generate代码，但如果愿意，完全可以为每个积木生成对应的代码，而且可以是`任何语言，任何抽象粒度`。`灌入式`阵营的小伙伴可能会反驳说，你们generate的代码并不是真正用于运行的。我会回答说: 对，我恰恰认为，不该把真正执行的代码generate出来给用户看。积木之所以是个好工具，正是因为它能自如地隐藏复杂度，暴露出合适粒度的概念颗粒，积木并不只是帮助我们省去记忆语法规则，更重要的是，它允许我们根据学生所处的阶段，给予他不同抽象程度的积木。我很喜欢来自lisp社区的忠告:`表达你的意图，而不是操作过程，这样有助于我们能站在更高的抽象层面上`

关于这一点，[code.org](code.org)给了我们很好的示范，一个学习者，在[code.org](code.org)里在拖拽了两个积木之后，他看到页面里愤怒的小鸟往东飞一步，接着又往北飞一步，最后成功击中了小猪。

如果学习者愿意，他可以看看与积木等价的代码：

<img src="http://wwj-fig-bed.just4fun.site/codeorg_9b3de524.png" width=600 />

我们看到，这些代码隐藏了很多实现的细节，你也许要抱怨说code.org在欺骗学习者，这并不是真正运行的代码，`真正的代码`是由js在操控svg的元素，但你确定你要给出这个粒度的东西吗？`真正的代码`也许是一串`001101101...`. 我认为平台给出合适抽象粒度的积木在编程教育里是至关重要的

就这点而言，目前很多灌入式的图形化编程并不适合编程教育，尤其不适合少儿编程，他们直接把驱动硬件代码包装到积木下就了事了，积木颗粒在抽象程度上与硬件文本编程无异。如何设计出合适抽象粒度的积木块，不是个简单的问题，我认为这块的从业者都该多看看cozmo和makecode

### 交互式的优势
反驳完灌入式的优势，接着我们来谈谈`交互式`的优势何在，我先简单列出，之后逐条陈述

1.  及时的反馈
2.  允许单步调试
3.  软件编程和硬件编程，不必区分，虚拟人物与现实硬件能彼此联动
4.  强大的可扩展性

罗列完`交互式`的优势后，我们来逐条陈述它们.

>    及时的反馈

我认为这一条，对编程教育是至关重要的。

我们从`REPL`（Read-Eval-Print-Loop）说起，[LISP](https://zh.wikipedia.org/wiki/LISP)最早为我们带来[REPL](https://zh.wikipedia.org/zh-hans/%E8%AF%BB%E5%8F%96%EF%B9%A3%E6%B1%82%E5%80%BC%EF%B9%A3%E8%BE%93%E5%87%BA%E5%BE%AA%E7%8E%AF)。REPL是个交互式的编程环境，用户输入的表达式及时被求值运行，并输出，这对于学习一门新的编程语言有很大的帮助，因为它能立刻对初学者做出回应，所以这个概念被移植到很多编程语言环境里（Python, Scala , Java(since jdk-9)...）。这种交互式的编程环境使得探索性的编程和调试更加便捷，因为“读取-求值-输出”循环通常会比经典的“编辑-编译-运行-调试”模式要更快，这两者的差异很像`交互式`和`灌入式`的差异。我自己使用REPL的一个强烈感受是，在REPL环境中（如ipython），我更乐于探索，对于不懂的api，我会直接做个实验，看看效果，获得直观感受。REPL鼓励每个人在探索中成为自己知识的构建者。而这点正式是早期致力于推广少儿编程的先驱们(艾伦凯、派普特)所追求的

我将硬件编程里的`交互式`编程方式，视为一种硬件编程的`REPL`。如同我在前头举例说的

>  在[cozmo code lab](https://www.anki.com/en-us/cozmo/code-lab)中一个非常惊艳的编程体验是:如果你不知道一个积木有什么作用，你不必去翻说明书，你只需要点击一下这个积木，cozmo立马执行这个积木的逻辑，你可以直观地理解陌生的积木。交互式编程所具有的及时反馈特性，鼓励学习者去探索系统。这是交互式编程给学习者心理上带来的影响之一。

对教学和平台而言，及时的反馈也能带来诸多好处，有了来自硬件的反馈信息，我们可以在平台中给出更多的提示信息，来指导学生修正错误，或者引导他抵达目标，目前国外社区已经有这块的试水者，我正在关注，之后有机会专门写一篇文章。

>    允许单步调试

如果学习者写了一段较为复杂的代码，运行时没有达到预期效果，人们往往无法通过阅读代码找出问题（错误往往揭示了知识或思维盲区），它需要逐行运行代码，看看效果，然后判断究竟是哪一步出了问题，这就是单步调试之所以如此重要的原因，即便对于专业程序员，也是如此。在`灌入式`中我们无法做到单步调试，因为代码是一股脑灌入硬件的。但`交互式`允许我们这样做，因为每次都是消息通信，所以编程界面可以逐步地给硬件发送控制指令。如果你观察过学生在code.org中通过单步调试找到问题，并顺利前行，你就知道这个特性有多棒

>    软件编程和硬件编程，不必区分，虚拟角色与现实硬件能彼此联动

在图形化编程这块，学习者很可能是先学了软件编程，通过闯关式的学习，利用积木控制虚拟角色来达到目标，在这个过程中掌握编程概念。`交互式`硬件编程允许你把硬件也接入到这些web平台里。如此一来，无论是教学软件还是硬件，平台架构上将毫无差别，学生的编程体验也几乎没有差别。它们学习软件编程所积累的知识完全可以用于硬件部分。

而在创作类平台中(比如scratch)，`交互式`编程允许虚拟角色与物理硬件彼此沟通，你可以自由联通虚拟与现实世界，制作体感游戏和富有表现力的故事。这将为我们带来更高的`高天花板`和更多的趣味性，从而点燃大家的热情

关于这块的有趣例子可以参考:[codelab-adapter-docs gallery](https://codelab-adapter-docs.codelab.club/user_guide/gallery/)

>    强大的可扩展性

`交互式`还将为我们带来强大的可扩展性，[ROS(Robot Operating System)](https://zh.wikipedia.org/zh-hans/ROS)和[scratch3_adapter](https://codelab-adapter-docs.codelab.club/)是很好的两个例子。因为基于消息通信，各个部分彼此解耦，这些系统本质上是分布式的，你可以接入任何东西，在[scratch3_adapter](https://codelab-adapter-docs.codelab.club/)中，硬件方面,我们已经接入了:

*  [micro:bit](http://microbit.org/)
*  [Cozmo](https://www.anki.com/en-us/cozmo)
*  [BB8](https://store.sphero.com/products/bb-8-by-sphero)
*  [树莓派](https://www.raspberrypi.org/)
*  [智能家居](https://blog.just4fun.site/scratch3-smart-home.html)

AI方面，我们接入了:

*  [微软认知服务](https://azure.microsoft.com/zh-cn/services/cognitive-services/)
*  [本地化的机器视觉](https://js.tensorflow.org/)
*  [opencv](https://opencv.org/)
*  [实时物体检测](https://pjreddie.com/darknet/yolo/)
*  一些简单的本地自然语言处理(移植了mit media lab的实验项目)

如果你愿意，你可以将小时候的玩具四驱车接入进来。

# 如何实现
>  everything is message

天色已晚，明天要早起，这部分就不多写了，之后单独讨论

如果你熟悉LISP,为了实现一个 LISP REPL，只需要实现read、eval、print三个函数和一个不停轮询的函数(loop)即可,一个基本的REPL就可以用如下的简单形式表达：(loop (print (eval (read))))

一旦你理解了这个概念，就可以自己动手去硬件上实现了。

事实上，社区里的交互式项目(如S4A、snap4arduino、s4m)思路基本都是一样的

我们自己动手实现了[scratch3_adapter](https://codelab-adapter-docs.codelab.club/)

我把写作[scratch3_adapter](https://codelab-adapter-docs.codelab.club/)的过程都记录在博客里，如果你有兴趣，也可以根据最初的架构，自己实现:

*  [为Scratch3.0设计的插件系统(上篇)](https://blog.just4fun.site/scratch3-plugin-1.html)
*  [为Scratch3.0设计的插件系统(下篇)](https://blog.just4fun.site/scratch3-plugin-2.html)
*  [Scratch3 Lab: 将Scratch3接入开源硬件及AI的实验项目](https://blog.just4fun.site/Scratch3-Lab.html)
*  [codelab-adapter-docs](https://codelab-adapter-docs.codelab.club/)

我私下认为[scratch3_adapter](https://codelab-adapter-docs.codelab.club/)基于zeromq的实现也许是目前扩展性最好的，欢迎入坑 ：）



<!--
### 可扩展性
ROS和adapter是个很好的例子，可以做出任意复杂的东西，

这背后的想法是，硬件只是更大系统的一部分  观察传感器的状态

你可以把利用云端的AI，利用本地的摄像头 来自不同的硬件 当温度30度时  人物说很热


这是一种，ROS的策略，adapter在架构上，很多地方模仿了ROS，关于这点，参考:[]()

在体验式，引导你尝试，而这是少儿编程的开创者们所鼓励的 在实践中去把我概念

当温度25度时 打开空调

# 为何交互式是更好的模式
学习硬件本身 还是利用硬件做出其他应用

我为何要知道串口式什么

就像我们教学python的时候，不会教学它的C实现  操作系统原理

adapter致力于将万物积木化，在adapter你可以让google的AI与小米的智能家居互动，这是scratch的思路

mixly则是一个blockly app，致力于映射，你可以将硬件抽象为积木

# microbit
用键盘控制micro:bit

使用消息  可以控制粒度

使用烧录，必须控制串口

总是能写出server代码的，但设计上 这块应该被抽象

-->


# 补遗
### 通讯补丁
灌入式编程可以在一定程度上，也可以实现`交互`特性，一种策略是采用`通讯变量`的概念, makeblock的mblock很好地利用了这点

利用通讯变量，你可以让上下位机实现彼此沟通

技术实现的话，也不会太难，在硬件里跑一个独立的通信进程就行，之后通过uart或其他通道与上位机沟通就行

你最好将这种方式视为一种补丁，`通讯变量`是一种补充策略，通过这种补丁，你无法做到`交互式`的所有特性，但这依然不失为一种很聪明的做法

# 参考
*  [Protocol](https://en.wikipedia.org/wiki/Protocol)
*  [unprotocols](http://hintjens.com/blog:_unprotocols)
*  [PicoBoard](https://en.scratch-wiki.info/wiki/PicoBoard)
    *  [sparkfun/PicoBoard](https://github.com/sparkfun/PicoBoard)
*  [scratch-2-raspberry-pi](https://www.raspberrypi.org/blog/scratch-2-raspberry-pi/)
*  [S4A](http://s4a.cat/)
*  [Mixly，初学Arduino的最佳图形化编程工具](https://zhuanlan.zhihu.com/p/24770930)
*  [Firmata](https://github.com/firmata/protocol)
*  [snap4arduino](http://snap4arduino.rocks/)
*  [MicroPython with WebUSB!](https://nick.zoic.org/art/micropython-webusb/)
*  [Software development at 1 Hz](https://hackernoon.com/software-development-at-1-hz-5530bb58fc0e)
*  [Access USB Devices on the Web](https://developers.google.com/web/updates/2016/03/access-usb-devices-on-the-web)
*  [WebUSB API](https://wicg.github.io/webusb/)
*  [读取﹣求值﹣输出循环(REPL)](https://zh.wikipedia.org/zh-hans/%E8%AF%BB%E5%8F%96%EF%B9%A3%E6%B1%82%E5%80%BC%EF%B9%A3%E8%BE%93%E5%87%BA%E5%BE%AA%E7%8E%AF)
*  [LISP](https://zh.wikipedia.org/wiki/LISP) 
*  [建构主义 (学习理论)](https://zh.wikipedia.org/wiki/%E5%BB%BA%E6%A7%8B%E4%B8%BB%E7%BE%A9_(%E5%AD%B8%E7%BF%92%E7%90%86%E8%AB%96))
*  [The REPL For Hardware](https://www.feld.com/archives/2018/07/the-repl-for-hardware.html)

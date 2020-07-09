---
title: CodeLab 冒险记（一）
author: David
date: 2020-07-09
tags: ["codelab"]
slug: "david-p1"
---

大家好，我是之前在 CodeLab 工作学习过的实习生 David。

我是一名大学生，目前在澳大利亚的悉尼大学就读，专业是物理和计算机科学。我不算聪明，也没有什么特长，但是喜欢脑洞和想一些有的没的。之前想从事量子计算机相关的研究，但是现在更加偏向对通用人工智能的探索。目前最喜欢的书是 Marvin Minsky 写的 The Society of Mind，对人工智能和人类心智模型有兴趣的朋友我强烈推荐这本书，书的门槛并不高但是每一个章节的每个概念都十分的有冲击性。

<br>

<div style="text-align:center">
<img src="/img/societymind.jpg"/>
</div>

<br>

因为我常年居住海外，而且很久没有用中文来写文章，要是文中的一些表述不够简洁得体，请多多见谅。

**该文为个人观点，仅供参考，欢迎讨论。**

---

<!--more-->

-   [前言](#前言)
-   [在 CodeLab 工作是什么体验？](#在-codelab-工作是什么体验)
-   [理念和初衷](#理念和初衷)
-   [观点和思考工具](#观点和思考工具)
-   [计算机？编程？](#计算机编程)
    -   [计算机可以是什么？](#计算机可以是什么)
    -   [编程是什么东西？](#编程是什么东西)
    -   [其他的编程模型？](#其他的编程模型)
    -   [元编程是什么？](#元编程是什么)
    -   [担忧](#担忧)
-   [计算机历史的重要性？](#计算机历史的重要性)
    -   [什么是科学精神？](#什么是科学精神)
    -   [计算机科学？计算机工程？](#计算机科学计算机工程)
    -   [计算机科学应该是怎么样的？](#计算机科学应该是怎么样的)
    -   [70 年代的编程](#70年代的编程)
        -   [从代码到对于数据的直接操控](#从代码到对于数据的直接操控)
        -   [从指令到使用约束条件以及目标](#从指令到使用约束条件以及目标)
    -   [问题的根源？](#问题的根源)
-   [感想](#感想)
-   [参考资料和资源](#参考资料和资源)

@liuqing 之前问到我在标题后加问号“？”的原因，我在这里说明一下。

我在这篇文章主要写了我通过了解 CodeLab 所关注的一些东西，重新对计算机、编程、和计算机科学建立起新的理解的过程。而这些问题都是在这个过程中，我给自己提的问题，而章节内写的是我对这些问题的回答。使用问号的另外一个原因是，我希望这篇文章主要是以分享以及讨论的形式去存在，而不是我自顾自地去强加和强调我自己的观点。对于这些问题，我不认为它们有正确的答案，因为答案会根据观点的不同而变化。说实话，我目前对这些概念的理解也是在揣摩，所以我想以分享讨论的形式来阐述我个人的观点。

---

## 前言

<br>

<img src="/img/boxsand.jpg" alt="/img/boxsand.jpg" style="zoom: 120%;" />

<br>

@种瓜之前跟我说，让我写一篇关于在 CodeLab 的实习感想，以便让其他对 CodeLab 工作感兴趣的小伙伴参考。于是我便开始寻思应该如何写这篇文章。因为在 CodeLab 的两个月对我影响很大，整个过程与其说是在工作，不如说是在学习。所以我最终决定将我在实习过程中学习到的新的观点，以及对目前计算机的想法给总结出来。由于我想要分享的东西比较多，我打算将我想讲的东西分成两篇。这一篇主要会讲到的是，计算机历史如何改变了我对目前计算机的看法，以及我目前认为计算机教育中存在的问题。希望这篇文章能体现出 CodeLab 的一些理念，同时也希望这篇文章可以给各位带来一些启发。

至于我为什么会给这篇实习笔记命名为冒险记。这是因为我觉得在参与 CodeLab 的两个月在@种瓜和@liuqing 的带领下我去到了一个我完全不知道的世界，在这个世界里很多概念都十分新颖，然而这概念都早在我出生前就有了。这些东西就如同那些被遗失的宝藏一样，而我像是冒险一样去挖掘这些被世人遗忘、不被主流看重的宝物。而这些充满了想象力的东西，被过度的商业化的技术掩盖，并且消失在世人眼中。

<br>

## 在 CodeLab 工作是什么体验？

首先先讲讲在 CodeLab 的工作体验，毕竟要是没有这个部分就不能被算作是实习笔记了。

<br>

<img src="/img/codelab_david.jpg" alt="img" style="zoom:50%;" />

<div style="text-align:center">CodeLab 的办公室Neverland <br>现在已经收拾过了，没有那么乱了</div>

<br>

在我参与实习工作期间，CodeLab 里面总共有四个人。@种瓜和@liuqing 是 CodeLab 的全职员工，而我和@Adam 则是参与这次工作的实习生。除了全职员工和实习生以外，CodeLab 还有一些志愿者，他们大多都有技术背景并且在我们做一些项目的时候也会来帮忙。

<br>
<div style="text-align:center;">
<img src="/img/medialab.jpg" alt="img"/>
</div>

<div style="text-align:center">MIT Media Lab的内部，一眼望去五花八门的项目，充满想象力的空间</div>

<br>

可能是因为 CodeLab 所做的是比较有探索性和基础性的工作，比起可以量化产出的工作，我们的工作更像是不断的探索与讨论。这个过程中也会不断地实施新的想法然后再从该过程中学习。这样子的工作模式下，比起像传统的等待上级安排任务，自主探索与学习能力可能更为重要。@种瓜说过他希望大家能做自己喜欢做的事情，而不是他去主动分配任务给每个人。这样注重想象力的模式，给我感觉会更加接近 MIT Media Lab 还有曾经在 90 年代辉煌过的 General Magic 一样。

<br>

<img src="/img/generalmagic.png" alt="img" style="zoom: 100%;"/>

<div style="text-align:center">General Magic在90年代初时想要设计出的个人通信设备（被称为现代智能设备的原型）的构想图</div>

<br>

这种环境下，每个人都各自埋头捣鼓各自的项目，当发现一些有意义的东西的时候（和我们主要讨论的东西有关联的东西，后文会具体提到一些部分），则会叫上大家开始讨论。比如说我，我个人对 AI 比较感兴趣，在实习的后期阶段我主要捣鼓的就是 IBM 的"Machine Learning For Kids"课程以及这个课程所用的算法如何可以接入@种瓜写的 Adapter。但是不幸的是，由于疫情的原因，我的实习之旅草草结束，这项工作并没有得到完成。

@种瓜和@liuqing 给我的印象是，他们读的书很多，而且涉略很多不同的领域。除此之外，他们也很乐于分享，在实习期间经常跟他们讨论有意思的话题，不亦乐乎。因为大家都很乐于分享，而且讨论的内容我都十分认可（虽然有一些内容一开始不是很理解），随着时间的推移，我发现我的书单上想要读的书越来越多（这算是副作用吧？哈哈）。

<br>

<div style="text-align:center">
<img src="/img/rosrobot.jpg" alt="Image result for ros iss"  />
</div>

<div style="text-align:center">在ISS（国际空间站）上运行ROS的机器宇航员</div>

<br>

我和@aoran 所做的虽然也是探索性工作，但是也有一定技术性，不过技术能力并不是核心。这是因为技术方面的不足永远可以通过学习补充回来，但是一个人对于一些领域的兴趣以及探索的渴望比较难改变（比如这次实习中我做的一个项目涉及到了 ROS，虽然之前没有接触过，但是在 CodeLab 志愿者@楠『雨』的帮助下,成功地在一款搭载着树莓派的机器人上运行了 ROS 并与电脑对接，并且通过局域网可以在其他电脑上使用 Scratch 来操控）。在这样的前提下，比起技术能力，可能一个人的兴趣、独立思考能力和想象力会更为重要。但是我相信，参与这项工作的人在工作学习的过程中各方面的能力都会有所提升。

<br>

## 理念和初衷

好了，该讲的背景都讲了，现在应该进入主题了。接下来我要跟大家分享我这次冒险中所收获的宝藏了。

<br>

<div style="text-align:center">
<img src="/img/engelbart.jpg" />
</div>

<br>

Douglas Engelbart (道格拉斯·恩格尔巴特)，计算机鼠标之父，享年 88 岁。

我现在对这种一句话概括一个人的做法并不是很认同，但是在这个快节奏且信息爆炸的年代，很多人偏向简单干练的形容。这样的情况下，很多人一生的工作以及贡献就被缩减成几个标签。除此之外，这些计算机科学家通过他们的项目所想要传达的核心理念没有被理解或接纳,这样的事情在计算机的发展过程中发生过很多次，难免让我感到伤感。

<br>

<div style="text-align:center">
<img src="/img/engelbart1.gif"/><img src="/img/engelbart3.gif"/><img src="/img/engelbart2.gif"/>
</div>

<div style="text-align:center">1968 NLS DEMO <br>从左到右：视频会议以及屏幕共享，超链接，鼠标 <br> 下图：数据的可视化</div>

<br>

<div style="text-align:center">
<img src="https://media.wired.com/photos/5933018d26780e6c04d2e154/master/pass/NLS.jpg" alt="Tech Time Warp of the Week: The Mother of All Demos, 1968 | WIRED" style="zoom: 67%;" />
</div>

<br>

是的，Engelbart 在他 1968 年发布的[NLS 系统](<https://en.wikipedia.org/wiki/NLS_(computer_system)>)中是有用到他发明的鼠标;在他的[演示中](https://youtu.be/yJDv-zdhzMY)他是有用到超链接,有用到屏幕共享，有用到多窗口界面和视频会议。这些都是在将近 60 年前发生的事情，而他当时想表达的概念只有在最近几年才被慢慢理解。他创造 NLS 的初衷并不是为了去展现这些科技，而是想要通过计算机来增强人们合作的能力（在现在又被称为协同办公）。他相信，通过计算机人类社会的集合智力（collective intelligence）可以被大大增强，更多数据可以被显示而且具有动态性和即时性。

> By "augmenting human intellect" we mean increasing the capability of a man to approach a complex problem situation, to gain comprehension to suit his particular needs, and to derive solutions to problems.
>
> Douglas Engelbart, Augmenting Human Intellect: A Conceptual Framework (1962)

他的理念和初衷在当时并没有被理解，人们看到的只是一种新的,被称之为鼠标的指向工具。大部分人甚至觉得他在浪费宝贵的硬件资源，对他所做的事情表示质疑，然后回去自己独立的铁盒里面，独自工作。在互联网得到成熟发展的今天，人们才再次认识到集合智力的强大,开始兴起了各个协同办公平台。但是，大部分人可能并不知道，这个概念在 60 年前就被提出并且实现过。

当我第一次深入了解 Engelbart 和他所做的项目的时候，令我十分震惊。我很久以前，可能是通过电视上面播的科技节目（节目中把他成为鼠标之父），知道有这么一位计算机科学家。但是当时候只是敬佩他所创造的技术（鼠标），而对他所想传递的理念完全不知。在真正明白他的理念以后，不禁然我觉得只通过技术的视角去评判他所做的事情真的十分荒唐，并且完全剥夺了他所想表达的东西。这种经历，让我原本技术至上的观点开始动摇，开始以理解项目初衷的角度去看待各个项目。

<br>

## 观点和思考工具

<br>

<div style="text-align:center">
<img src="/img/alankay.jpg" style="height:260px;"/><img src="/img/dynabook.jpg" style="height:300px;"/>
</div>
<div style="text-align:center">Alan Kay与他 68 年制作的DynaBook模型</div>

<br>
跟 Engelbart 有类似命运的科学家还有 Alan Kay (艾伦·凯) 。

Alan Kay 是一名杰出的计算机科学家，在现代被称为面向对象之父并且在图形界面方面做出了极大的贡献，他在早期的计算机发展中做了很多工作，很多东西都不能用三言两语来形容。上图的项目就是他在 68 年设计的 Dynabook, 可以算是现代平板电脑的原型。而他对我影响最深的项目则是他和他的团队于 1972 年首次发布的 Smalltalk。Smalltalk 是世界上第一款面向对象编程语言，同时带有集成开发环境和图形界面。（关于我对 Smalltalk 的讨论会在下一篇文章进行，但是我在这里剧透一下。我深入了解了 Smalltalk 以后，对于微软以及苹果的印象完全崩塌了）

<br>

<div style="text-align:center">
<img src="/img/smalltalk.jpg"/>
</div>

<br>

> "point of view is worth 80 IQ points."
>
> \- Alan Kay, The Early History Of Smalltalk (1993)

Alan Kay 认为看问题的角度以及观点十分的重要，在他写的一篇文章中，他认为重要的观点与 80 点的智商等价。他在文中提到了 Allen Newell 来参观他的 PARC 实验室发生的趣事。当时 Newell 跟 Kay 提起了他的 theory of hierarchical thinking（层次结构理论），于是 Kay 便提出了一个编程问题来挑战他的理论。

> One little incident of LISP beauty happened when Allen Newell visited PARC with his theory of hierarchical thinking and was challenged to prove it. He was given a programming problem to solve while the protocol was collected. The problem was: given a list of items, produce a list consisting of all of the odd indexed items followed by all of the even indexed items. Newell's internal programming language resembled IPL-V in which pointers are manipulated explicitly, and he got into quite a struggle to do the program. In 2 seconds I wrote down...
>
> \- Alan Kay, The Early History of Smalltalk (1993)

Kay 只花了几秒钟来解答， Newell 却花了半个小时以上都解不出来。 Alan Kay 自认他没有 Allen Newell 那么聪明，但是他所使用的编程语言 Lisp 更为灵活。相比之下 Allen Newell 所信奉的 theory of hierarchical thinking （层次结构思考模式 ）使用的是 IPL-V (资讯处理语言) ,十分笨重而且不宜于思考（可能对人类的心智模型并不友好）。Alan Kay 描述到 " I wasn't smarter but I had a much better internal thinking tool to amplify my abilities." ，这体现出我们看待问题的方式以及思考工具有多么的重要。同样的，假如我们有不同的 "Point of view" (观点), 在看待同样的事件或者事物时，观点看法的差异可能会直接导致对事件、事物的不同理解，可能会看到截然不同的一面。

我之所以会认为这是我这次实习比较重要的收获之一，是因为我在这次学习过程的讨论中收获了许多以前不曾想到过的看法，特别是对于一些我以为我已经熟知的东西。获取这些新的看法，以及通过新的观点重新思考的过程对我十分震撼。像 Alan Kay 这样的早期计算机探索工作的探讨也会时常出现在我们的工作之中，通过学习和深入了解前人所做的事情，我看到了不一样的计算机而且加深了对该领域的理解。

计算机发展历史相关的讨论还会在后面的章节继续进行。

<br>

## 计算机？编程？

<br>

<div style="text-align:center">
<img src="/img/programming.jpg" alt="Image result for computer programming" style="zoom: 67%;" />
</div>

<br>

现在的我如何看待计算机？什么是编程？

这些问题我在这次实习之前是从来没有仔细思考过的，可能是因为我对于计算机的熟悉带给我自以为是的从容，从而让我失去思考这些基础问题的动机和动力。

这两个问题在现代可能小朋友都可以轻易回答 - 计算机是人类创造的计算工具，编程是人类写给计算机运行的指令。

这个回答都是正确的，想必我在几个月前也会这样回答这些问题。但是正确的答案可能不止一个，我现在也认为我之前的回答只是肤浅的定义。这两个问题是基础性问题，在基础问题上的不同回答可能会带来颠覆式的发现，建立在旧的回答上的所有观念可能都会被推翻。

在分享我的观点之前我想先感谢一下 Alan Kay、Bret Victor、Douglas Engelbart、Ivan Sutherland、John McCarthy 等等启发到我的计算机科学家/先驱者。同时也十分的感谢@种瓜，将这些计算机先驱者和他们所做的项目展现给我，与我一起讨论理解这些项目。

我现在对于计算机的理解主要都是受到我上面提到的人的影响。特别是 Bret Victor 的演讲，他的观点深深地打动了我。分别是，["Inventing on Principle"](https://youtu.be/PUv66718DII) 、 ["The Future of Programming"](https://youtu.be/8pTEmbeENF4) 和 ["Stop Drawing Dead Fish"](https://youtu.be/ZfytHvgHybA)。(可能需要一些技术手段才可以在中国观看)。同时还推荐一下 Bret Victor 的个人网站 - [Worrydream.com](http://worrydream.com/)。

<br>

<div style="text-align:center">
<img src="/img/bretvector.jpeg" alt="Image result for bret victor"  />
</div>
<div style="text-align:center"><b>Bret Victor</b></div>

<br>
<br>

### 计算机可以是什么？

<br>

<div style="text-align:center">
<img src="/img/game.jpg" alt="Image result for half life 2" style="zoom: 57%;" />
</div>

<div style="text-align:center"><b><i>半条命二</i></b> 游戏截图</div>

<br>

我自认为和计算机打了很多年的交道，最早可能可以追溯到我三四岁的时候。那时家里有一台老款的七喜电脑，我姐姐放学回家之后我会搬张小凳子在旁边围观我姐姐玩半条命和盟军敢死队（印象比较深的两款游戏，那时虽然看不懂但是觉得很厉害）。后面我自己也成了游戏迷，电脑游戏深深地吸引着我。后来我变得十分沉迷，即便没有玩游戏的时候也在脑内进行各种想象。我以前一直认为，电脑游戏吸引我的原因是因为我想逃离枯燥乏味的学习。与其去死记硬背各种对我没有明确目的性的知识，电脑游戏的世界反而更加有趣。直到后来有更加基础性的动机之后我才爱上了物理。在这次实习之后对计算机的改观才发现电脑游戏吸引我的另外一个理由。

<br>

<img src="https://images.nintendolife.com/546be0c4a8ab5/super-mario-bros-world-1-1-weve-all-seen-this-opening-far-too-many-times.original.jpg" alt="Image result for super mario first" style="zoom:50%;" />

<div style="text-align:center">超级马里奥 游戏截图</div>

<br>

我们现在使用计算机所进行的大部分创作实际上都是计算机诞生前就有的东西（写文章、制图、动画等等），但是唯独有一种媒体是随着计算机的诞生而诞生的，电脑游戏就是一个很好的例子。比较经典的电脑游戏如吃豆人还有超级马里奥在计算机以外的平台上是无法重现的，更不用提我们现代更加精致的电脑游戏。这些游戏所呈现的世界并不受我们世界的物理定律束缚而且在我们的世界里并不存在，也无法存在。

所以这种仅存在于电脑平台上的媒体到底是什么？我认为这个媒体是模拟。计算机具备搭建和呈现模拟的能力基于它的互动性（输入和输出）和计算能力（根据输入计算输出）。从某种意义上来看这与我们人类的想象非常像，而世界上能进行这样不被现实所束缚的模拟的东西可能只有两个，一个是大脑，另一个是计算机。通过计算机，人们可以把脑内所幻想的世界呈现出来，又或者是通过搭建模拟媒体来表达某个复杂抽象的概念（数学、物理等）。而我小时候会喜欢电脑游戏的另外一个原因可能就是因为模拟媒体所具有的互动性以及庞大的信息量（根据我的输入不断改变输出，通过摸索的过程我无意识地学会了游戏里面的“物理定律”。最后在一个不一样的世界里体验到了这个世界里做不到的事情）。

<br>

<img src="/img/sutherland.JPG" style="zoom: 50%;" />

<div style="text-align:center">Ivan Sutherland于 1963 年发布的在TX-2计算机上使用的构图编程软件Sketchpad</div>

<div style="text-align:center">
<img src="/img/bridge.png" alt="img" style="zoom: 67%;" />
</div>

<div style="text-align:center">通过Sketchpad所制作的桥梁受力模拟模型<br>
当改变桥梁结构，桥的各个部分的受力程度和负载力都会被重新计算<br>
比如顶部的图片在桥梁的左右两端侧多加了两个受力点，从而改变了桥梁中心的受力大小<br>
也可以通过设置一些前置条件来自动寻找合适的桥梁结构</div>

<br>

比起语言、图片和动画，在表达我们的一些想法或者尝试理解其他人的想法时计算机的模拟媒体可能会对我们的心智模型更加友好、更加容易理解。所以我现在认为，计算机可以是一个提高人类心智以及思考能力的工具（如同统计学的发明如何让所有正常心智的人可以分析、理解、解读数据）。通过使用计算机这个媒介，我们学习知识的过程应该会更加简单，能做到的事情可以更多，而且会赋予更多的想象空间。

<br>

<div style="text-align:center">
<!--
<figure class="video_container">
  <iframe src="https://scratch3-files.just4fun.site/%E9%87%8D%E5%8A%9B%E6%95%88%E5%BA%94.mp4" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
-->
<video src="https://scratch3-files.just4fun.site/%E9%87%8D%E5%8A%9B%E6%95%88%E5%BA%94.mp4" controls="controls"></video>

</div>

<div style="text-align:center"> CodeLab 的展示视频 重力效应</div>

<br>

特别是在这个物联网快速发展的时代，当我们可以将现实中的实物与计算机关联，计算机能带给我们的教学能力以及富有的信息量是难以用语言形容的。比如上面的展示视频里面就有涉及到物理的重力常量的概念，通过 Leap motion 来控制模拟的模型。这个展示看起来可能没有什么，但是实际操控起来的体验却不同凡响，仿佛是重量常量的值与手的旋转幅度在现实中产生了关联。同时也体现出一个具有互动性的模拟媒体具有的庞大信息量，和我们人类接收和处理这些信息的能力。具体如何通过计算机来加强学习过程也是 CodeLab 时常会去探讨的话题之一。

<br>

### 编程是什么东西？

我在去 CodeLab 实习之前，完全没有想过编程能以其他的方式存在。那个时候的我认为，编程说白了无非就是去书写一连串让电脑执行的指令从而完成某项任务。从最基础的角度上来看，电脑一直在做的事情无非就是以下两件：

> Computers: 1) calculate and 2) copy memory
> most common operation: copy memory from one memory address to another

这个定义出自我大学的一门计算机课程。但是我认为这样子去定义计算机以及编程就如同把人类定义为：

> 人类以及所有生命体都在以摄取外界能量以供生存和自我复制的目标去存在。
> 从 DNA 的自我复制到每个细胞分裂，再到生命体的繁衍，所在进行的都是不断地自我复制。
> 在这个过程中生命体不断地氧化，衰老。
> 细胞不断地更新换代，生命体也在不断地更新换代。

这样的定义方式并没有错误，因为这的确是事实。但是这样的定义下，所有事物都显得十分空虚，而且事物的意义被剥夺了。至于人生的意义，这个话题可能有点偏了，并且每个人对其的定义都不一样。但是我认为编程是可以有一个基础以及通用的定义的。而我现在比较认同的定义是：

> 编程是将我们的心智或者逻辑施加到计算机上的一个过程。
> 计算机会通过编程成为我们想法或者意识的延申。

更简单来讲，编程就是为了让计算机去做我们想做的事情的一个过程。比如，我想写个程序来算 1+1 又或者是在屏幕上显示 Hello World!又或者是通过对物联网设备编程来达到我的目的如打一个响指就开启家里所有的灯。具体要去实现每个工作的过程可能都不一样，有的可能要某某 API 又或者某某 SDK，而且难度可能都会有所不同。但是我在这里想要强调的是我想，这个我可以是任何人，这个我在大部分场景下都会是程序员。具体是谁并不重要，重要的是在编程的这个过程中离不开一个个体想要延申自我意识（或者逻辑）的想法。

换句话说，我想要表达的是，计算机编程都离不开两个最基本的目的：

> 1.  去运用计算机具有的，强大的运算能力
> 2.  根据我们的想法去操控计算机

我顺着这个思路思考之后，开始自问“实现这些目的的方法只有一种吗？”

抱着这种观点再去看待编程的时候，给我一种退一步海阔天空的感觉。编程不再局限于写的代码，其他对计算机施加自我意识的过程都变成了编程。包括 1962 年 Ivan Sutherland 制作的 Sketchpad 也是编程的其中一种形式。获得了新的观点之后，我仿佛打破了自己对于编程的思维定式，不禁开始思考编程可以是什么？

<br>

### 其他的编程模型？

先让我们回顾过去的编程是怎么样的吧。

<br>

​<img src="/img/binary.png" alt="img"  /><img src="/img/soap.png" alt="img"  />

<div style="text-align:center"> 早期编程语言的演变过程
<br>二进制代码编程 - 汇编语言编程（Symbolic Optimal Assembly Program） - FORTRAN (第一门高级编程语言）</div>

<br>

> "In the beginning we programmed in absolute binary... Finally, a Symbolic Assembly Program was devised -- after more years than you are apt to believe during which most programmers continued their heroic absolute binary programming. At the time [the assembler] first appeared I would guess about 1% of the older programmers were interested in it -- using [assembly] was "sissy stuff", and a real programmer would not stoop to wasting machine capacity to do the assembly.
>
> Yes! Programmers wanted no part of it, though when pressed they had to admit their old methods used more machine time in locating and fixing up errors than the [assembler] ever used. One of the main complaints was when using a symbolic system you do not know where anything was in storage -- though in the early days we supplied a mapping of symbolic to actual storage, and believe it or not they later lovingly pored over such sheets rather than realize they did not need to know that information if they stuck to operating within the system -- no! When correcting errors they preferred to do it in absolute binary.
>
> FORTRAN was proposed by Backus and friends, and again was opposed by almost all programmers. First, it was said it could not be done. Second, if it could be done, it would be too wasteful of machine time and capacity. Third, even if it did work, no respectable programmer would use it -- it was only for sissies!"
>
> \- Bret Victor, The Future of Programming (2013)

这是 Bret Victor 在他的 ["The Future of Programming"](https://youtu.be/8pTEmbeENF4) 演讲开场所讲述的，编程语言在早期发展时候的故事。我对这段被遗失的历史的第一感想是，早期的各位程序员们真的好顽固。使用更加对于人类心智友好的工具变成了一种弱者的行为（"sissy stuff"）。各个流派的程序员们（二进制看不起汇编，汇编看不起 FORTRAN)，像是变成了谁越能像机器一般思考谁就越厉害的比拼。这种行为在早期硬件资源有限的时候还比较合理，但是在硬件资源充足之后这像是自愿尝试克服种种不必要的障碍一样。

随着时间的推移,编程语言也一直在发展，从 FORTRAN 到 C，再从 C 到 JAVA 和 PYTHON。编程语言一直发展前进，但是 Bret Victor 对于这些发展表示担忧。

> “The real tragedy would be if people forgot that you could have new ideas about programming models..”
>
> \- Bret Victor, The Future of Programming (2013)

现在计算机在我们的社会中扮演着不可或缺的角色，这也就造成了目前 IT 界的过度商业化。导致大部分在这个业界的人会更加注重效率和技术，而且在开发时一般只会基于已有通用的结构。Bret Victor 所担心的就是现代程序员对于编程概念的固化使编程一成不变，人们不再像早期计算机领域的探索者那样去思考编程可以是什么。

我十分认同 Bret Victor 的观点，特别是在学习计算机历史的时候， 很多前人所做的事情让我十分震惊。虽然那些项目已经过时而且不一定适合现代的应用，但是那些项目和架构还有设计理念则是十分值得学习的。比如@种瓜所制作的 Adapter 是主要使用 Python 来实现，而架构核心（EIM， Everything is a Message）就有参照 Smalltalk 以及一些元编程（[Metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming)）的概念。

<br>

### 元编程是什么？

我虽然在 CodeLab 实习之前也有了一段时间的编程经验, 但是从来没有想象过指令式编程以外的编程方式，也不知道其他的编程模型的存在。其中我印象比较深的一种基于元编程的语言是[Lisp](https://en.wikipedia.org/wiki/Lisp)。元编程这种编程模型的主要特点就是程序本身可以当作一种数据来解释以及改写，而在 List Processing (Lisp) 中所有东西都是 List，包括程序本身也可以被理解为 List 的某个 Element。基于这种结构，一个程序可以读取其他的程序、生成新的程序、分析其他程序、改变其他程序的架构、甚至可以在运行时通过递归不断改变自身的结构。而这种功能是指令式编程做不到的，在一些情景中, Lisp 的代码可以更加精简并且更加灵活。在了解到有其他的编程存在的时候，对我冲击巨大。

<br>

<div style="text-align:center">
<img src="/img/list1.png" alt="img" style="zoom:120%;" />
</div>

<div style="text-align:center"> 使用短短几行的LISP代码写的图灵完备LISP解释器（有借助pmatch）
<br>出自：<a href = "https://youtu.be/OyfBQmvr2Hc">William Byrd on The Most Beautiful Program Ever Written</a></div>

<br>

<img src="/img/list2.jpg" alt="r/ProgrammerHumor - LISP is ugly and confusing" style="zoom: 40%;" />

<div style="text-align:center"> "Lisp is ugly and confusing"</div>

<br>

λ 演算在 Lisp 上十分适用，早期计算机科学家对于人工智能方面的探索也是使用 Lisp 来进行实验。虽然与 Python 和 Java 相比 Lisp 需要花上更多时间才能上手并且更加复杂，但是 Lisp 是一门十分强大的语言这点是毋庸置疑的。

在了解到这些不被主流重视且充满想象力又强大的编程模型之后，不禁让我产生疑问。为什么这些模型鲜为人知而且不被重视呢？在这个问题上我和@种瓜也有讨论过，最后得出的结论就是过度商业化的领域导致固化的思考方式和工作方式。这也剥夺了那些在现代想要更加深入学习计算机的人选择的权力，让他们不知道其他选项的可能。我觉得我自己就是一个很好的例子，假如没有参与实习的话我可能很长一段时间内不会知道这篇文章所提及的东西。

<br>

<div style="text-align:center">
<img src="/img/list3.png" alt="Lisp Cycles" style="zoom:130%;" />
</div>
<div style="text-align:center"> "Lisp Cycles"</div>

<br>

下面是我在国外的论坛 Quora 上偶然看到的一个通过中世纪战争来解释这个现象的例子（取自 Gerwin Dox 的[发言](https://qr.ae/pNKON0)）。我觉得这个例子十分贴切，在这里引用翻译一下。

在中世纪的欧洲，领地之间时常会有纠纷以及战争。现在让我们来想象一下中世纪的两个领主由于某些纠纷决定开战，而军队的组成大部分是被征召入军没有任何战斗经验的领民，那些领民会使用什么样的武器呢？

**长剑？**

<br>
<div style="text-align:center">
<img src="/img/fight.jfif" alt="Is the boar spear, as opposed to other types of spears ..." style="zoom:140%;" />
</div>
<br>

他们会使用**长矛**

长剑虽然强大，可以斩，可以刺。在会使用剑的人的手中，长剑可以发挥出极强的威力。但是由于长剑的价格昂贵，给军队的全员装备长剑是几乎不可能的。另一方面，长矛会比较便宜而且更加容易量产（只有尖端需要使用金属）。使用长矛的另外一个好处就是长矛更加容易上手，所以领主可以把领地内所有身体健全的领民征召入军。没有任何战斗经验的领民们只需要花不到一天的时间就可学会如何握矛，如何使用长矛突刺，就可以算为战斗力的一部分。短短的时间可以让他们像身经百战的战士一样吗？不能。他们会有像样的长矛使用技巧吗？可能不会。但是对于领地的领主来说，他有了一支还算像样的军队。

Java 就像例子中的长矛一样，能使用 Java 开发者多如牛毛。相比之下，能使用 Lisp 的开发者十分稀有，也就是因为这样, 大型企业开发一款完全基于 Lisp 的软件几乎是不可能的。与 Lisp 相反，从企业的角度上来看使用 Java 开发软件更加现实和经济。Gerwin Dox 还提到，那些会使用 Lisp 的开发者大多都是编程专家，就如中世纪的骑士一样能武善战但是数量不多。从企业的角度上来讲，雇佣编程专家来当码农无非是大材小用，将他们雇佣为技术方面管理层的人员会更加合理。

也就是因为以上原因，绝大多数的企业不会使用精简强大同时又困难的工具。这也解释了为什么 Java 这种极度工业化以及笨重繁琐的语言会这么流行。我虽然可以理解企业的行为，但是这也导致了目前计算机领域模式固化的问题。大学等其他教育机构所传授的内容完全是根据目前业界需求去提供的，毕竟大部分学生是以求职为目的去学习的。结果可想而知，那些无法被利益化的技术以及想法（Smalltalk, Lisp 等等）就会慢慢从主流技术领域的视野中消失，而那些在业界常用的技术就会越来越热门。在这种背景下，很难有新的，具有想象力的而且有深度的想法，这也是一部分计算机先驱者所担心的“Pop Culture” 流行文化([Alan Kay 对于这个问题的看法](https://queue.acm.org/detail.cfm?id=1039523))。

最后再让我们回到中世纪，想象一下有一个战士，他并不是军队的一员。他是一匹独狼，只为自己而战。这个战士会使用什么样的武器呢？

<br>

<div style="text-align:center">
<img src="/img/warrior.jpg" alt="good morning ! おはよう #samurai #musashi #katana #wakizashi ..." style="zoom:45%;" />
</div>

<br>

这个战士会使用**武士刀**

**_难用，昂贵，但是十分锋利_**

虽然像 Lisp 或者 Smalltalk 这样的编程模型在现代应用中十分罕见，但是还是受到一小部分人的追捧。比如之前提到的 William Byrd 和他的几个朋友做的逻辑/关系编程解释器项目[miniKanren](http://minikanren.org/)（在 The Most Beautiful Program Ever Written 演讲的最后有展示）就是使用了 Lisp。在 Rigetti 量子计算机工作的研究者 Robert Smith 也有在[Computerphile 的采访](https://www.youtube.com/watch?v=svmPz5oxMlI)中提到为什么比起其他语言 Lisp 在量子计算机项目中更适用。除了学术研究以外，Lisp 在黑客社区中也十分受欢迎而且经常有人[讨论](https://hn.algolia.com/?q=lisp)。基于 Smalltalk 开发的有意思的项目也有很多，而其中 CodeLab 有在关注 Etoys、 Dynamicland、Corquet、lively，特别是 Bret Victor 在做的 Dynamicland 是关注重点之一。

<br>

### 担忧

> “The most dangerous thought that you can have as a creative person is to think that you know what you’re doing.
> Because once you think you know what you’re doing, you stop looking around for other ways of doing things and you stop being able to see other ways of doing things, you become blind…”
>
> \- Bret Victor, The Future of Programming (2013)

我通过元编程这个例子主要想要说明和表现的的就是，编程可以以其他的方式去存在。编程的问题往往不止是技术方面的问题，反而跟我们人类的心智模型以及认知还有思考方式密切相连。在早期的计算机发展中，抱有不同观点，以不同视角去看待编程的人很多。但在现在这种观念十分少有，大多数人在开始学习编程之前就已经对编程是什么有了一个大致印象。这也就是 Bret Victor 对于目前计算机发展的担忧。我也认为这是目前计算机科学教育方面所存在的问题。

<br>

## 计算机历史的重要性？

在实习的时间里我慢慢地了解了更多关于计算机的历史以及以前早期的先驱者们所做的事情，之后,我发现计算机科学与物理化学等自然科学在教育本质上有所不同。根据我在国外学习物理的经验，如何通过学习科学方法（Scientific Method）来学会科学精神（Scientific Thinking）在课程中扮演着一个至关重要的角色。这些观念可能会跟国内的教育方式有些不同，以下的观点都是根据我个人的经历得出。

<br>

### 什么是科学精神？

<br>

<div style="text-align:center">
<img src="/img/sciencehero.jpg" alt="Teaching Science through the History &amp; Philosophy of Science ..." style="zoom:50%;" />
</div>
<div style="text-align:center"> 印着各个科学学科先驱者的邮票</div>

<br>

关于科学方法的学习可以概括为，如何根据目前已知的模型以及观察到的信息提出有科学意义的假说、如何搭建实验来证明提出的假说、如何通过实验中所收集的数据来得出有意义的结论、最后如何将整个实验包括假说整理成文章供其他人阅读和验证。而学习的方法主要是学习以前各个不同年代的科学家们所做过的实验以及他们如何通过实验得出了他们的模型以及验证了他们的猜想。

<br>

<div style="text-align:center">
<img src="/img/electron.png" alt="J.J. Thomson's cathode ray tube | Download Scientific Diagram" style="zoom: 67%;" />
</div>
<div style="text-align:center"> 约瑟夫·汤姆逊用于实验的阴极射线管</div>

<br>

比如我最初在高三学习原子模型的时候，我首先学习了约瑟夫·汤姆逊（J.J.Thomson 1856-1940）在 1897 年所做的关于阴极射线管从而发现电子的实验（人类首次发现亚原子级粒子，汤姆逊于 1906 年被授予诺贝尔物理学奖）。汤姆逊后来根据他的发现，提出了原子的梅子布丁模型（Plum Pudding Model）, 认为原子是由电子以及像布丁一样的正极云存在。

<br>

<div style="text-align:center">
<img src="/img/electron2.png">
</div>

<div style="text-align:center"> 约瑟夫·汤姆逊于1904年提出的梅子布丁模型</div>

<br>

后来欧内斯特·卢瑟福（Ernest Rutherford 1871-1937 在 1895-1898 年接受过汤姆逊的指导）于 1907 指导他的助手汉斯·盖格（1882-1942 德国物理学家）以及他的学生欧内斯特·马斯登（Ernest Marsden 1889-1970 当时候只是一名本科生，与卢瑟福同名不同姓）做了基于梅子布丁原子模型的阿尔法粒子散射的实验（又被称为卢瑟福散射实验）。让卢瑟福没有想到的是，他所指导的实验得出了与预期完全不同的结果从而否定了梅子布丁模型。因为当他们拿有带正极而且有极大动能的阿尔法粒子轰击金属箔的时候，时常会有阿尔法粒子被反射回来。这使他们确信原子的中心存在某个拥有极大质量的粒子，这个粒子后来被卢瑟福命名为原子核同时提出了卢瑟福模型。

<br>

<img src="https://cdn.kastatic.org/ka-perseus-images/b111a455939c419c172a300ac2def63d56aa573c.svg" alt="img" style="zoom:50%;" />

<div style="text-align:center"> 梅子布丁模型与卢瑟福模型在卢瑟福散射实验结果预期的对比</div>
<div style="text-align:center"> 紫色为带负极电子，浅绿色为带有正极的区域（左边为正极云，右边为原子核），蓝色线代表阿尔法粒子的轨道
直到学习到现代基于量子物理的原子模型（电子所在的位置以概率的方式去形容）之前我还学习了其他“错误的”原子模型。</div>

<br>

<div style="text-align:center">
<img src="/img/electron3.jpg">
</div>

<br>

我所说的科学精神里面包括的想法有很多，但是我想通过这个例子所表现的想法如下。

> 有反例的模型是错误的，没有反例的模型也不一定是对的。
> 没有模型是正确的，只有与其他模型相比之下更好的模型。

我们目前所有的大部分模型都存在局限性，有些即便存在缺陷的模型也被认作为目前最好的模型而被物理学家使用着。比如爱因斯坦的广义相对论取代了牛顿的万有引力定律，但是在黑洞的行为上[不适用](https://en.wikipedia.org/wiki/Criticism_of_the_theory_of_relativity)。而且相对论与爱因斯坦在 20 世纪早期解释以及证明的[量子物理相互冲突](https://researchoutreach.org/articles/unifying-quantum-mechanics-einstein-general-relativity/)，他下半生大部分工作主要都花在相对论以及否决量子物理上。更加有趣的是，他所拿的诺贝尔奖就是基于他在量子物理方面的工作颁发的。这样的模型在科学界真的太多太多了，其他还有有关于流体动力的公式 - [纳维尔·斯托克斯方程](https://en.wikipedia.org/wiki/Navier%E2%80%93Stokes_equations)无法解释湍流而且在一些情况下计算得出流体速度为无限、宇宙中 80%的物质都是[暗物质](https://en.wikipedia.org/wiki/Dark_matter)但是至今只是理论上存在、[超导体理论](https://www.sciencedaily.com/releases/2019/09/190926145001.htm)目前还是玄学, 等等。通过学习这些物理模型的发展过程，了解那些无论是被否决的还是最先进的模型的缺陷以及局限性，我学会了如何去质疑，以及应该怎么样做才能得出更好的模型的科学精神。也就是这种精神，才推进了科学的发展并且促使了科学家们继续研究并且提出新的模型。

这样子去形容现代科学可能会给人一种科学实际上是很不牢靠的一种东西，但是事实也是如此。科学基于事实但并不等于事实（Science is based on fact, but science is not fact)，而且受限于人类的视角，我们可能永远没有办法把握宇宙的真理。由于我是不可知论者，我认为科学是基于信仰之上的。接下来说一下我和@种瓜在这个方面讨论的时候经常会用到的论据。这个论据是基于 Bertand Russell（伯特兰·罗素）所提出的“罗素的火鸡”问题的改编版本。

> 从前有个饲养火鸡的农场，在每年的感恩节的早上所有的火鸡都会被拉去贩卖。同时，火鸡场又会进预计在下一年感恩节出售的火鸡幼崽来养。

在我们的角度上来看，我们知道这些火鸡只会在农场里面生活 365 天。但是假设在火鸡的社会里，有一只火鸡科学家。这只火鸡科学家在它在农场里生活的第 364 天时进行判断，根据它过去 363 天的观察，它推测明天也就是第 365 天，它也会在农场里过着吃饱喝足的日子。因为在过去他所收集的数据里，无论是风吹日晒雨淋，还是春夏秋冬，它的这种生活方式都没有改变过。这时的它完全不知道明天可能会在某个饭桌上。

这个例子所体现出的是，我们的所有模型都是基于经验以及过去发生的事情，我们的科学模型证明的只是过去发生的事情，即便是在现在做的实验，在下一秒也会成为过去，而未来会发生的事情并没有被证明也无法被证明。就比如，“明天的太阳会升起”，在明天到来之前我们是没有办法证明的，但是基于我们的经验以及信念我们会相信明天的太阳会升起。同样的，我们没有办法证明宇宙的定律是永恒不变的，因为那是不可被证的，所以我认为科学实际上只是根据过去发生的事情得出的信仰罢了。

我认为不可知论的论据完全驳倒了科学是事实的说法，假如我相信科学事实的情况下，我的科学观念会完全崩塌。这也就是为什么我所学会的科学精神如此重要，因为我打从一开始就被告知所有的科学模型都不是正确的，当一个模型被证伪的时候，科学家则会继续研究并且提出新的模型来对应把之前模型证伪的案例。假如明天的太阳并没有升起，那科学家们会去调查太阳没有升起或者消失的原因来提出新的星系模型（假如地球还健在的话，哈哈）。在我看来，科学模型本身不是牢固的，但是科学精神是坚不可摧的。这也就是为什么科学精神如此重要，而学习这种精神的方式是通过学习那些在过去被否决的模型以及现有模型的缺陷。同时也体现出了科学史以及科学哲学的重要性。

<br>

### 计算机科学？计算机工程？

<br>

<div style="text-align:center">
<img src="/img/se.jpg"/>
</div>

<br>

与物理学等自然科学学科相比，计算机科学的教学更像是一门工程学科。而科学和工程学最大的差别在于，工程学只在乎一个科学模型的实用性。除了实用性、稳定性、以及效率以外的其他东西并没有太大兴趣。从工程学的角度来看，科学模型就是事实，而且对某个模型的来源以及推导过程并没有特别关注。像物理或者是数学，一个模型的推导过程以及思维方式更加重要，而最后的模型反而是次要的。

<br>

<div style="text-align:center">
<img src="/img/test.jpg"/>
</div>

<div style="text-align:center"> 悉尼大学某门物理科目期末考试试卷里面公式表（总共有3页）</div>

<br>

就比如我们大学的物理期末考试，在试卷前面几页几乎包括了一个学期内学习的所有模型（公式），没有包括的模型也可以用提供的模型推导出来。而试题的内容一般包括，如何从语言描述的问题中提取出物理问题以及对应该问题的模型应用、重现某个模型的推导过程、甚至是给予与现有模型不同的前置因素，基于这些因素推导出一个新的模型来解决问题。根据我个人的学习经历，我发现了科学教育所做的并不是去训练一些能将各个公式和模型倒背如流的机器，而是去培养能理解和处理未知问题的心智。而去培养这种心智最佳的方法，就是去学习以前的科学家是如何思考、如何实验、如何得出结论的。

类似这样的精神或者思考方式，在我学习计算机科学的过程中完全没有体现出来。而学校对于学生的考核往往基于如何应用教授过的模型、算法、结构来处理不同的问题。这种情景下，我们并不会去考虑或者质疑模型本身，更不会了解一个模型或者算法的推导过程和设计理念，因为我们只在乎如何应用他们。比如像是图灵完备这种十分基础和根本的计算机概念，我在大学的计算机科学课程中完全没有接触到。这也就是为什么我觉得我所在读的计算机学科不应该被称之为科学，而应该被称为工程。这也是为什么每年都有数万个新的 JavaScript 框架发布，而我们的编程模型一直还停留在 70 年代。

<br>

### 计算机科学应该是怎么样的？

我个人认为，计算机科学应该与其他科学一样，应从前人所做过的事情以及想法来进行学习，而不是先入为主地灌输当今主流的技术概念。而专注于技术的部分应该分离出来成为计算机工程学科，而计算机科学应该研究探讨的是不同的编程模型以及人类心智和认知的问题。就像是物理学不会过多地去在乎技术上的细节，而更多关注于研究以及改善模型来更好地解释以及理解物理现象那样。在现代为了去推进计算机的发展，我认为最好的起点就是从计算机历史开始。可能也就只有这样计算机编程才能继续发展，才能像早期计算机科学家那样去思考计算机可以是什么。

<br>

### 70 年代的编程

我在跟很多人谈论到这个关于编程或者科技现状相关问题的时候，我都会说我们的编程一直停留在 70 年代停滞不前。当他们第一次听我这样说的时候往往都会认为我在痴人说梦，然后举出互联网、人工智能、现代逼真的 3D 图像渲染、智能设备等例子来向我证明我们现在能做到以前做不到的事情。这时我通常都会问，“你是否同意现在的编程是基于文本的序列指令代码？”。而通常的回答都是，“是啊，你所说的不就是编程吗？除了这个以外还能有其他的编程？”。很不巧的是，这种编程方式与 70 年代的主流编程方式几乎一样。

但是根据以前的计算机科学家所做过的实验性和探索性学术项目，我们可以很轻易地想象出更加先进的编程方式。而这方面的探索在 60 到 70 年代盛行过，但是在 80 年代商业化项目兴起后停止了。更多资源和资金被投入到基于当时相对成熟的架构上以便用于商业目的，而那些实验项目由于硬件资源短缺等原因而不被重视。

**Bret Victor** 在他的 **_["The Future of Programming"](https://youtu.be/8pTEmbeENF4)_** 演讲中根据 70 年代的项目总结出了他对未来编程的期望。其中主要有以下四个方向。他的这个演讲对我影响很大，对这个方向感兴趣的朋友我再次推荐这个演讲。我认为我对第三和第四点的理解还不是十分透彻，我在这里只会说说关于第一和第二点的各个项目以及我个人的一些观点 。

<div style="text-align:center">
<img src="/img/4points.png"/>
</div>

<div style="text-align:center"> Bret Victor 对于未来编程的看法</div>

<br>

#### 从代码到对于数据的直接操控

<br>

<div style="text-align:center">
<img src="/img/matlab.png"/>
</div>
<div style="text-align:center">我之前使用MATLAB所模拟的一个关于中子在不同环境下散射的实验</div>

<br>

“现代的编程就如同闭着眼睛去排列符号一样。”这个定义也是 Bret Victor 提出的，我认为十分恰当并且有过这个经历。这个定义有两个部分，第一个是“闭着眼睛“，另一个是“排列符号”。在我的物理课程中时常会有使用计算机来研究物理模型的实验的部分，学习的主要是如何使用 MATLAB 或者 Jupyter 来处理数据（一般是将数据变得可视化）和模拟实验（将某个物理公式的行为变得可视化）。这样做的好处是当我们构建好一个程序以后可以动态地改变实验数据或者约束条件去得出新的图片，但是构建程序的过程是完全静态的。在编译和运行一个程序之前，我完全看不到程序会输出一个怎样的结果，我需要在脑内想象并且根据我所想象的图像去修改程序。为了得出我想要的输出我需要一直不停地修改、编译和运行, 反反复复。而且有些时候，当我完全不明白程序为什么没有像我所期望的那样去运行的时候，我就要逐行检查, 使用各种 debug 技巧。

<br>

<div style="text-align:center">
<img src="/img/TX2-panorama.jpg"/>
</div>

<div style="text-align:center"> 1958年在MIT竣工的TX-2计算机</div>
<div style="text-align:center">左图中白衣衬衫男子和黑色西装男子之间的是TX-2计算机的内存(320KB)</div>
<div style="text-align:center">左图的黑色西装男子的右边和右图是TX-2计算机的控制端（进行输入和显示输出）</div>

<br>
<div style="text-align:center">
​<img src="/img/tx1.gif" alt="Ivan Sutherland : Sketchpad Demo (2/2) GIF by hyper_text | Gfycat" style="zoom: 50%" /><img src="/img/tx2.gif" style="height:245px;"/><img src="/img/tx3.gif" style="height:245px"/><img src="https://kisd.de/~rbaehren/img/SKETCHPAD2.jpg" alt="skpad" style="zoom:50%;" />
</div>

<br>

在之前提到过的，Ivan Sutherland 和他的团队所制作的 Sketchpad 就是在 TX-2 计算机上制作和运行的。Sketchpad 的核心概念就是对于数据的直接操控，并且可以通过约束条件来改变数据和基于给予的数据和约束条件来计算（[桥梁模拟例子](https://i.imgur.com/JUPYxqQ.png)）。如果我们有像 Sutherland 所想象的那样继续去发展编程，那在将近 60 年后的今天（Sketchpad 在 1963 年发布），科学家以及其他创作者可能不再需要去闭着眼睛排列符号也能动态地将他们想表达的东西可视化。更讽刺的是，我们现在每人口袋里都有一个比 TX-2 强大几万倍的计算机。

关于 Sketchpad 的更多资源：[Sutherland 的演示](https://www.youtube.com/watch?v=6orsmFndx_o) [Alan Kay 解说 Sketchpad](https://youtu.be/495nCzxM9PI)

在更加深入地了解 Ivan Sutherland 所做的事情的时候，我还看到他和 Bob Sproull 在 1966 年对 VR/AR 的[首次尝试](<https://en.wikipedia.org/wiki/The_Sword_of_Damocles_(virtual_reality)>)。再次让我震惊，当时候我的第一想法是：所谓的最新科技缺乏一些原创性啊，不过是把前人提出过的概念用新的硬件去实现罢了。

<br>

<div style="text-align:center">
<img src="/img/3d.gif"/>
</div>
<div style="text-align:center"> 左右两个视频是分开录制的所以并不同步</div>

<br>

#### 从指令到使用约束条件以及目标

在 Sutherland 的 Sketchpad 里面也有体现出这个概念，比如在 Alan Kay 对于 Sketchpad 的解说里所用到的例子就是如何通过在使用者所画的一个图形的的几条边上施加关系（互相平行，互相垂直等），让计算机来生成新的图形。但是在这里我想说明的是一种更加通用的编程模型，这种模型也是通过施加约束条件以及目标来运用计算机庞大的计算能力，这在现代又被称之为逻辑编程。在逻辑编程模型下，使用者不再去编写各种指令来构造程序，而是通过给予编译器各种约束条件以及程序的最终目标，让编译器自行生成一个符合条件的程序。逻辑编程是真正地去从人类的逻辑方式出发的，比如在逻辑编程中，“=”会真正地成为等号，因为这样子才符合人类的逻辑方式。

```python
x = 5
5 = x
```

假如你用 Python 运行上面这段代码，终端会给你报错。

```
File "main.py", line 2
	5 = x
	^
SyntaxError: can't assign to literal
```

熟悉编程的朋友们应该都知道，“=”在这里的意思并不是等于，而是给某一个部分的内存指定数值。但是从我们已有的数学以及逻辑来看这完全不合理，我们并没有让计算机适应我们的思考方式，而是反过来去像计算机一样思考。

<br>

<div style="text-align:center">
<img src="/img/lj1.jpg"/>
</div>

<div style="text-align:center"> 在维基百科上的一个Prolog例子</div>
<div style="text-align:center"> 这里先是定义了一些数据，然后定义了一些逻辑条件</div>
<div style="text-align:center"> 最后根据之前的数据以及定义的逻辑得出了符合逻辑的解答</div>

<br>

这一方面的探索工作早在 60 年代就有进行过, 比如[PLANNER](https://arxiv.org/vc/arxiv/papers/0904/0904.3036v25.pdf)（1969 - Carl Hewitt）还有[Prolog](https://en.wikipedia.org/wiki/Prolog)（1972 - Alain Colmerauer)。逻辑编程其中的一个应用就是在模式匹配上，比如我们熟悉的[Regular Expression](https://en.wikipedia.org/wiki/Regular_expression#History) （Ken Thompson 1967）- 正则表达式就是一个很好的例子。假如没有这方面的工作的话，假如我想在颜色表中找出所有以“灰”开头并且以“色”结尾的颜色名字（比如灰黑色、灰蓝色、灰绿色、灰红色），可能还要写一大串的指令来读取每个字符然后逐个匹配，这绝对会比“CTRL+f”然后输入搜索“灰\*色”要麻烦的多。

最近让我印象比较深刻的逻辑编程的例子还包括我之前提到过的[miniKanren](http://minikanren.org/)。仅仅 400 行 Lisp 代码所搭建的逻辑编程解释器，可以做到的事情令人震惊。在[The Most Beautiful Program Ever Written](https://youtu.be/OyfBQmvr2Hc)里面 William Byrd 展示了几个例子，其中包括：

<br>

1.

<img src="/img/lj2.jpg" style="zoom:100%;" />

```
条件：两个List
目标：append 之后得出（a b c d e)
答案数量：全部符合要求的答案
miniKanren会回答：
() (a b c d e)
(a) (b c d e)
(a b) (c d e)
(a b c) (d e)
(a b c d) (e)
(a b c d e) ()
```

<br>

2.

   <img src="/img/lj3.jpg" style="zoom:55%;" />

```
条件：
	案例1. 两个空的List
	案例2. （a b c） (d e)
目标： 想要一个function，当案例1和2使用了这个function之后会得出一下结果
    答案1. 一个空的List
   	答案2. （a b c d e)
答案数量：1个
miniKanren会回答:append
```

<br>

这样的例子让我相信逻辑编程的可能性，而且也是我理想中的编程方式，这也和我未来想要做的项目相关。这些例子展现出了逻辑编程的强大而且能大大减少使用者的负担以及缩小使用门槛。假如有一天我们有一个完美的逻辑编程系统的话，社会上的大部分人都能更加有效地利用计算机强大的计算能力（现在需要使用者懂得各种算法、框架和库），计算机将会真正成为一个提高人类心智的工具，也会是真正有意义的计算机革新。

根据我所知道的信息，逻辑编程方面研究在现代只有一小部分人在做，并没有得到主流社区的关注。假如以现在的形式继续发展下去，那个完美的逻辑编程系统可能遥遥无期。

<br>

### 问题的根源？

<br>

<img src="/img/moore.png" alt="refer to caption" style="zoom: 40%;" />

<br>

计算机的硬件一直在稳步向前，而我们用这些新的硬件所做的事情在本质上没有任何变化。软件本身只是思想的载体，而硬件也可以被视为一种特殊的软件，只不过实现逻辑的方式是通过现实存在的硅胶二极管。假如我们不去考虑如何提升构建软件的方式本身（编程），无论我们再怎么样去提升硬件计算机也不会有质的改变，而反复在做的只会是拿新的技术去适应旧的系统。基于我们编程方式所构建出来的硬件总是会有同样的缺陷。比如[冯·诺伊曼结构瓶颈](https://en.wikipedia.org/wiki/Von_Neumann_architecture#Von_Neumann_bottleneck) - 在目前计算机架构中扮演着重要地位的内存的大部分区域在使用时都处于空闲状态，因为在目前架构下的 CPU 只能同时操控一定数量的内存区域，这也是序列指令式编程所导致的 - 更好的方案[Actor Model](https://en.wikipedia.org/wiki/Actor_model)。

在 70 年代，计算机科学家们做了很多有意义的探索，但是由于计算机历史在计算机科学教育中的缺失，导致了只有一小部分乐于探索的人乐意去探讨那些“非主流”而且“陈旧”的想法。那时候的科学家由于对计算机和编程没有一个主观的看法，也正是因为大家都不知道计算机编程是什么才敢于去想象。可能也就是在这个过程中各个科学家发现了，编程实际上与我们人类的认知密切相关，才有了想要设计出更加符合人类心智模型的编程模型的想法。Engelbart 的 NLS 显现出了如何通过计算机来达到更加具有互动性的协同办公；Sutherland 提出了 Sketchpad 以及直接操控数据的编程，因为就如画画一样, 我们可以直观即时地看到我们在摆弄什么；Hewitt 提出了 PLANNER，一个更加符合人类逻辑的编程方式；Kay 根据人类如何认知和处理我们所在的现实（现实中所有的事物都是一个对象），提出了 Smalltalk 和 OOP。

> "Where Newton said he saw further by standing on the shoulders of giants, computer computer scientists all too often stand on each others toes. "
> \- Alan Kay, "The Early History of Smalltalk"

我认为，计算机科学与自然科学不一样，没有正确和错误的模型，也没有更好的模型，只有基于不同的思考或者观点的模型。在计算机的模拟世界里，我们可以依据不同的理念去搭建不同的模型。只有了解了各个系统和想法的优缺点，才可以踏出提升的第一步。只有了解了前人所做过的事情以及对于计算机所进行过的探索，我们才能站在巨人的肩膀上而不是在站在互相的脚趾头上。

<br>

## 感想

我非常庆幸能有在 CodeLab 工作的经历，这个经历让我受益匪浅，非常感谢@种瓜, @liuqing 还有@aoran 的分享以及一起做过的讨论，同时也十分感谢@楠『雨』以及其他 Codelab 志愿者在技术方面的指导以及讨论。通过学习 CodeLab 所聚焦关注的东西，我得到了巨大的启发，但是也意识到了很多的问题。这些问题，可能不一定会被全部人所认可，但是对于我个人来说这是一个十分严重而且又无解的问题。毕竟在通过商业推动的领域，人文方面的正义可能在大多数情况下没法得到伸张。说实话，在写到一些部分的时候，会使我感到悲愤，仿佛是切身经历那种理念无法被传达，观念不被理解和认可的感受。

当然，我所说的这些只是基于我个人的观点，假如你持有不同的观点又想对这个方面进行更加深入的讨论的话，我会张开双臂随时欢迎。而那些与我有着同样观念的朋友，我想说的是，在这个技术十分成熟的年代，想要去与其抗衡可能是十分困难的，而我们能做的可能只是尽量地去分享这些东西和讨论这些观点。

过去的几个月，我有和不少人交流过，主要都是我大学的同学和朋友。大部分人会觉得我所说的东西匪夷所思，但是还是有一小部分人对这些注重人性和充满想象力的东西感兴趣的。这些概念都十分复杂，并且很难用三言两语来表达，所以去一起讨论来建立和加深理解十分的重要。比如我正在写的第二篇文章中讨论的 Smalltalk 还有 Dynamicland 里面所包含的概念就十分的多，从不同的角度上去看都会看到不一样的东西 ，而每次再去看这些项目的时候，又会看到不一样的东西。我也会经常与@种瓜讨论这方面的问题，十分的有意思。

<br>

## 参考资料和资源

1. En.wikipedia.org. 2020. _Marvin Minsky_. [online] Available at: <https://en.wikipedia.org/wiki/Marvin_Minsky> [Accessed February 2020].
2. Minksy, M., 2020. _The Society Of Mind_. [image] Available at: <https://i.ebayimg.com/images/g/YKkAAOSwDpJdhTK6/s-l400.jpg> [Accessed February 2020].
3. Logicsource.com,2020. _Tressure Box_. [image] Available at: <https://logicsource.com/wp-content/uploads/2019/01/iStock-969484620-1.jpg"> [Accessed February 2020].
4. Architectualrecord.com,2020. _MIT Media Lab_. [image] Available at: <https://www.architecturalrecord.com/ext/resources/Static_Images/Imports/MIT-Media-Lab_09.jpg> [Accessed February 2020].
5. Zonefestival.com,2020. _General Magic Blue Print (Revised 2018)_. [image] Available at: <http://zonefestival.com/document/edge/4/film/318/photo/General_Magic_1120x635.png> [Accessed February 2020].
6. ROS.org, 2020. _ROS On ISS_. [image] Available at: <https://www.ros.org/news/assets_c/2014/09/R2-stow-pose-thumb-480x318-936.jpg> [Accessed February 2020].
7. History-computer.com, 2020. _Engelbart During Lecture_. [image] Available at: <https://history-computer.com/ModernComputer/Basis/images/Engelbart_during_lecture.jpg> [Accessed July 2020].
8. SRI International's Augmentation Research Center, 2020. _Mother Of All Demos (1968) - GIF and IMAGE_. [video] Available at: <https://www.youtube.com/watch?v=yJDv-zdhzMY> [Accessed July 2020].
9. History-computer.com. 2020. _Dynabook - Complete History Of The Dynabook Computer_. [online] Available at: <https://history-computer.com/ModernComputer/Personal/Dynabook.html> [Accessed July 2020].
10. Guzdia, M., 2003. _Programming Environments For Novices_. [ebook] Georgia, Altanta, US: College of Computing, Georgia Institute of Technology, p.9. Available at: <http://coweb.cc.gatech.edu/mediaComp-plan/uploads/37/novice-envs2.pdf> [Accessed July 2020].
11. Kay, A., 1993. _The Early History Of Smalltalk_. [ebook] MA, USA: Apple Computer, p.Chapter III. Available at: <https://raw.githubusercontent.com/worrydream/EarlyHistoryOfSmalltalk/master/SmalltalkHistoryHOPL-scanned-2015-07-16.pdf> [Accessed January 2020].
12. USF health, 2018. _Programming Code On Computer_. [image] Available at: <https://health.usf.edu/-/media/Blog/HealthIS/Images/2018/04/Programming-code-on-computer.ashx?h=234&w=350&hash=C2B094D3FC563F7699B02C86DF95C77834BDC13B&hash=C2B094D3FC563F7699B02C86DF95C77834BDC13B&la=en> [Accessed February 2020].
13. Amazon - AWS, 2012. _Bret Victor_. [image] Available at: <https://s3.amazonaws.com/strangeloop/static-site/prod/speakers/2012/7a1011a0-665c-11e1-ac66-00505684009c_large.jpeg> [Accessed February 2020].
14. Valve, 2004. _Half-Life 2_. [image] Available at: <https://steamcdn-a.akamaihd.net/steam/apps/220/0000001872.1920x1080.jpg?t=1579629810> [Accessed February 2020].
15. Nintendo, n.d. _Super Mario Bros World 1-1_. [image] Available at: <https://images.nintendolife.com/546be0c4a8ab5/super-mario-bros-world-1-1-weve-all-seen-this-opening-far-too-many-times.original.jpg> [Accessed February 2020].
16. \2020. _Ivan Sutherland_. [image] Available at: <https://3.bp.blogspot.com/-aQj-6aLorzc/W5ANW5WxrbI/AAAAAAADSFw/zf4oATiZDjEmLbJQmIp3C6GtUPguK8UUgCLcBGAs/s1600/ivan-sutherland.JPG> [Accessed 9 July 2020].
17. Victor, B., 2013. _References For "The Future Of Programming"_. [online] Worrydream.com. Available at: <http://worrydream.com/dbx/> [Accessed January 2020].
18. Codelab, 2020. _重力效应_. [video] Available at: <http://scratch3-files.just4fun.site/%E9%87%8D%E5%8A%9B%E6%95%88%E5%BA%94.mp4> [Accessed February 2020].
19. MIT's Lincoln Labs, 1963. _Ivan Sutherland Sketchpad Demo_. [video] Available at: <https://www.youtube.com/watch?v=6orsmFndx_o> [Accessed February 2020].
20. En.wikipedia.org. n.d. _Metaprogramming_. [online] Available at: <https://en.wikipedia.org/wiki/Metaprogramming> [Accessed June 2020].
21. En.wikipedia.org. n.d. _Lisp_. [online] Available at: <https://en.wikipedia.org/wiki/Lisp> [Accessed June 2020].
22. PapersWeLove, 2017. _William Byrd On "The Most Beautiful Program Ever Written" [PWL NYC]_. [video] Available at: <https://www.youtube.com/watch?v=OyfBQmvr2Hc> [Accessed June 2020].
23. esgarth, 2020. _William Byrd On "The Most Beautiful Program Ever Written" [X-Post /R/Programming] : Lisp_. [online] Reddit.com. Available at: <https://www.reddit.com/r/lisp/comments/6p0riq/william_byrd_on_the_most_beautiful_program_ever/> [Accessed June 2020].
24. freetonik, 2019. _Lisp Is Ugly And Confusing_. [image] Available at: <https://www.reddit.com/r/ProgrammerHumor/comments/9ocqiw/lisp_is_ugly_and_confusing/> [Accessed 9 July 2020].
25. xkcd, n.d. _Lisp Cycles_. [image] Available at: <https://imgs.xkcd.com/comics/lisp_cycles.png> [Accessed June 2020].
26. Dox, G., 2016. _Gerwin Dox's Answer To If Lisp Is Such A Great Language Then Why Isn't It Used More In Software Development? - Quora_. [online] Qr.ae. Available at: <https://qr.ae/pNKON0> [Accessed June 2020].
27. Mair, P., 1550. _[24] A Piece On The Rapier Against The Boar-Spear_. [image] Available at: <https://www.wiktenauer.com/wiki/Paulus_Hector_Mair> [Accessed June 2020].
28. Kay, A. and Feldman, S., 2004. _A Conversation With Alan Kay - ACM Queue_. [online] Queue.acm.org. Available at: <https://queue.acm.org/detail.cfm?id=1039523> [Accessed July 2020].
29. japonlia, 2018. _Good Morning ! おはよう_. [image] Available at: <https://www.instagram.com/p/BpUIHv1n0mN/> [Accessed June 2020].
30. Byrd, W., n.d. _Minikanren.Org_. [online] Minikanren.org. Available at: <http://minikanren.org/> [Accessed June 2020].
31. Victor, B., n.d. _Dynamicland_. [online] Dynamicland.org. Available at: <https://dynamicland.org/> [Accessed December 2019].
32. Boston University Interdisciplinary Conferences, 2016. _Teaching Science Through The History And Philosophy Of Science_. [image] Available at: <https://www.bu.edu/hps-scied/files/2016/02/Royal-Stamp-Hue-Shift.jpg> [Accessed June 2020].
33. Gillies, D., 2019. _J.J. Thomson's Cathode Ray Tube_. [image] Available at: <https://www.researchgate.net/figure/JJ-Thomsons-cathode-ray-tube_fig4_332320926> [Accessed June 2020].
34. Zh.wikipedia.org. n.d. _梅子布丁模型_. [online] Available at: <https://zh.wikipedia.org/wiki/%E6%A2%85%E5%AD%90%E5%B8%83%E4%B8%81%E6%A8%A1%E5%9E%8B> [Accessed 9 July 2020].
35. Khan Academy. n.d. _Discovery Of The Electron And Nucleus (Article) | Khan Academy_. [online] Available at: <https://www.khanacademy.org/science/chemistry/electronic-structure-of-atoms/history-of-atomic-structure/a/discovery-of-the-electron-and-nucleus> [Accessed July 2020].
36. WebElements, n.d. _The Orbitron Gallery Of Atomic Orbitals_. [image] Available at: <https://i.stack.imgur.com/8aDOv.jpg> [Accessed July 2020].
37. Broskander, 2014. _Science Vs. Engineering_. [image] Available at: <https://www.reddit.com/r/funny/comments/2a41i2/science_vs_engineering/> [Accessed July 2020].
38. Kay, A., Carroll, D. and Sutherland, I., 2007. _Sketchpad, By Dr. Ivan Sutherland With Comments By Alan Kay (1986)_. [video] Available at: <https://www.youtube.com/watch?v=495nCzxM9PI&feature=youtu.be> [Accessed July 2020].
39. En.wikipedia.org. n.d. _The Sword Of Damocles (Virtual Reality)_. [online] Available at: <https://en.wikipedia.org/wiki/The_Sword_of_Damocles_(virtual_reality)> [Accessed July 2020].
40. Sutherland, I., Sproull, B. and Ultimate History of Video Games, 2018. _Sword Of Damocles (1966) - First Augmented Reality Head-Mounted Display_. [video] Available at: <https://www.youtube.com/watch?v=eVUgfUvP4uk> [Accessed July 2020].
41. En.wikipedia.org. n.d. _Prolog_. [online] Available at: <https://en.wikipedia.org/wiki/Prolog> [Accessed July 2020].
42. En.wikipedia.org. n.d. _Moore's Law_. [image] Available at: <https://en.wikipedia.org/wiki/Moore%27s_law> [Accessed July 2020].
43. En.wikipedia.org. n.d. _Von Neumann Architecture_. [online] Available at: <https://en.wikipedia.org/wiki/Von_Neumann_architecture#Von_Neumann_bottleneck> [Accessed July 2020].
44. En.wikipedia.org. n.d. _Actor Model_. [online] Available at: <https://en.wikipedia.org/wiki/Actor_model> [Accessed July 2020].

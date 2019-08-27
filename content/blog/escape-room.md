---
title: "空间编程、物理计算与密室逃脱"
author: 种瓜
date: 2019-06-25
tags: ["programming"]
---

<img class="img-responsive" src="http://wwj-fig-bed.just4fun.site/room_7d2361f2.png" />

>  就象一个躺在黑房间里但是醒在床上的人，忽然看见窗帘上透进一道光线，心里知道只要拉开窗帘，眼前就会展开一片晨光朗照的原野似的。 -- 毛姆 《刀锋》

# 前言

本文来自今早与@李懿的交流。

交流中，@李懿提到与朋友介绍Neverland，这个朋友喜欢`解谜游戏`，提议说`解谜`的元素是否可能加入到Nevlernad空间里


>  我朋友提到说，既然我们可以联动空间里的任何物体，有可能实现的场景如：① 通过操作机关,将灯的颜色按特定顺序排列后，激活投影仪，在墙壁上投影出提示信息；② 带有四位数字的密码锁，允许通过简单编程来暴力破解 ③ 在空间中寻找 Scratch 的拼图积木来解密（机器视觉识别出拼出的图案，运行对应逻辑）。

<!--more-->

此外，@李懿还补充到

>  “两只老虎”的例子给了我一个启发，用户在场景中演奏特定曲目，识别后解锁。曲目的选取则与故事内容发生关联。

<!--，既然我们可以为空间里如此多的物理实体编程，是否可以通过物体的彼此互动，就像。比方说-->

# 两只老虎、传感器与萨满巫师
@李懿提到的`两只老虎`是我们此前做的一个演示：将三个小伙伴的手掌转化为钢琴的三个按键(`Do-Re-Mi`)。接触手掌时，如同按下钢琴键。

<video width=400 src="http://scratch3-files.just4fun.site/%E4%B8%A4%E5%8F%AA%E8%80%81%E8%99%8E.mp4" controls="controls"></video>

在这个例子中，通过一个传感器，采集到人体的接触信号，经过简单的编程，就可以将人与人的接触转化为音符。

利用同样的传感器，也可以捕捉到人与物体的接触。例如我们将传感器连接到楼梯上，就可以将楼梯变成钢琴阶梯，你踩在不同的阶梯上，房间里随即响起不同的旋律。

值得注意的是，我们在此谈论的不是一个商品，你可以很容易在市面上买到`钢琴阶梯`，这些商品化的专有设备是容易购买的。我们在此谈论的是，基于通用的传感器和CodeLab的创作平台，你可以轻易创作出这些东西，你的很多点子是市面上所没有的，整个宇宙可能都没有，它只存在你的脑子里，我们希望帮你表达出他们。

利用前头提到的传感器，在`解谜游戏`中我们可以做更多有趣的设计。

设想一个萨满巫师被困在岩洞里，岩壁上满是象形文字和古代狩猎图案，眼前有一个巨石堵住了出口。巫师看完墙壁上的文字，低头走到巨石下，他赤脚站在一块印有古代图腾的石板上，左手碰到巨石的瞬间，巨石豁然开启。(这一幕颇似《塞尔达》里主角探索地下神庙的场景)。利用上述的传感器，我们完全可以在技术上实现它，技术层面，当巫师站在那块特殊的石板上时，手掌碰到巨石，他的身体成为一根导线，接通了电路，触发开关。

# Neverland 与 CodeLab Adapter
前头只用到一个传感器，便可实现上述这些有趣的场景。在我们的办公室（Neverland）里，有许许多多类似的有趣而强大的传感器。从捕获目光的眼动仪传感器、捕获手部运动的手势传感器 到 捕获脑电波的传感器应有尽有。

CodeLab构建了[CodeLab Adapter](https://adapter.codelab.club/)这个通用工具，[CodeLab Adapter](https://adapter.codelab.club/)试图连接万物，让它们能彼此沟通，用户可以通过简易图形化编程即可赋予他们新的能力。

目前我们的办公室（Neverland）整个空间都由[CodeLab Adapter](https://adapter.codelab.club/)驱动，办公室里的的门禁、窗帘、电视、彩灯、冰箱插座,以及桌上的纸盒子(Switch Labo)、机器人(BB8/Cozmo/Vector/LejuRobot) 、飞行器(DJI Tello/Parrot)、儿童玩具(toio)...全部都由[CodeLab Adapter](https://adapter.codelab.club/)驱动。

换句话说通过[CodeLab Adapter](https://adapter.codelab.club/)可以为整个空间编程，赋予空间新的交互逻辑。

与@李懿的交流过程中，我们想到`密室逃脱`也许是非常有趣的应用场景，它也是绝佳的教育场景，因为解谜者的好奇心已经被充分激发。

# 密室逃脱
按照维基百科的定义:

>  密室逃脱一般泛指一种特定的游戏类型。在该类游戏中，玩家的视角通常以第一视角为主，并且往往被限定在一个近乎完全封闭或者对自身存在威胁的环境内，需要发现和利用身边的物品（工具），完成指定任务，最终达到逃离该区域的目的。正因如此，该类游戏通常也被认为是属于解谜冒险类游戏的一个特殊分支。

今天的密室系统，在谜题方面可以极尽聪明灵巧，谜题的破解过程运行在解谜者大脑里，密室空间只要提供线索即可，谜题的内容本身不受任何限制。

但密室在机关方面的设计却很薄弱。如果依赖于机械装置，设计一些精巧的交互系统是极为困难的，天才机械师可并不好找。天才机械师要么像鲁班一样忙于在前线输出(《王者荣耀》)，要么像维特根斯坦一样跑去当哲学家了。由此可见，天才机械师不仅人数稀少，而且不太专注于老本行，喜欢跨界工作。 但我们知道，在游戏里制作一个有趣的机关是容易的，不需要天才游戏开发者，虚拟世界里的一切交互都可由程序轻松定义，它们是`软`的，是一种可以任意捏造的橡皮泥。如果我们能将空间软件化，很多问题就变得简单了。

[CodeLab Adapter](https://adapter.codelab.club/)除了用于教育，另一个应用域就是物理计算：驱动无数传感器，为物理世界编程，最终驱动整个空间。

### 技术视角
不妨`密室`看作一个交互式的物理系统，传感器连接了数字世界和物理世界(我们的现实世界)。用户的行为作为系统输入（传感器是采集设备），系统输出则为机关的反馈。

`密室`中可能会有数十数百个传感设备。[CodeLab Adapter](https://adapter.codelab.club/)将其连在一起，密室创建者 可以在我们提供的创作工具(CodeLab Scratch)上定义密室的机关规则。

由[CodeLab Adapter](https://adapter.codelab.club/)驱动的密室是一个live system，一种活的系统，它在白天的行为和晚上可以完全不同，所有这些可以由密室创建者随时定义它。

# 爱迪生密室
目前在旧金山，便存在一个与上述描述相似的密室系统:[爱迪生密室](https://palace-games.com/the-edison-escape-room/)

![](http://wwj-fig-bed.just4fun.site/room_1af9bf0f.png)

它在全球的密室中的排名第六！

<img width=500 src="http://wwj-fig-bed.just4fun.site/room_f0b39422.png" />

这是一个充满灯泡、传感器和沉浸式体验的密室。

密室由Raspberry Pi驱动，包含有数百个传感器和执行器

<img width=500 src="http://wwj-fig-bed.just4fun.site/room_df72885f.png" />

数百个传感器和执行器之间在进行高速通信，他们之间的通信由[Banyan](https://github.com/MrYsLab/python_banyan)驱动，[Banyan](https://github.com/MrYsLab/python_banyan)是一个为物理计算设计的消息系统，我写过一篇关于它的架构设计的文章：[Python Banyan学习笔记之架构设计](https://blog.just4fun.site/Python-Banyan-note-Architecture.html)。 这个项目在架构上和[CodeLab Adapter](https://adapter.codelab.club/)有许多相似之处，都基于ZeroMQ，将消息视为一等公民。此外，我也是这个项目的贡献者之一。

在今天，如果你想设计一个驱动整个空间的系统，高速的消息通信是核心。如果考虑到空间功能会持续调整和升级，那么系统的开放性就是必要的。考虑到开放性，目前大部分的商业项目都可以排除在外。满足以上特质的项目，据我所知，目前至少有四个:

*  [dynamicland](https://dynamicland.org)
*  [Banyan](https://github.com/MrYsLab/python_banyan)
*  [CodeLab Adapter](https://adapter.codelab.club)
*  [Home Assistant](https://www.home-assistant.io)


近期CodeLab将在参与一个生物实验室的建设，在那儿我们将用[CodeLab Adapter](https://adapter.codelab.club/)驱动整个空间，赋予它智能。

也欢迎阅读本文的密室逃脱从业者联系我们：）

<!--
# 一些想象空间
[环球影城
    广告位

消息通信

展示内容

迪斯尼 连接万物

leeyi 展示内容 网红 解密

将参与一个`生物实验室`的共建，提供计算平台和设备 物理计算 dynamicland
-->


# 参考
*  [Physical computing](https://en.wikipedia.org/wiki/Physical_computing)
*  [密室逃脱](https://zh.wikipedia.org/zh-hans/%E5%AF%86%E5%AE%A4%E9%80%83%E8%84%B1)
*  [dynamicland](https://dynamicland.org/)
*  [空间编程](https://blog.just4fun.site/scratch3-smart-home.html#_6)
*  [Objectifier Spatial Programming](https://experiments.withgoogle.com/objectifier-spatial-programming)
*  [空间操作系统](https://blog.just4fun.site/Pharo-IoT.html#_2)
*  [Raspberry Pi vs a Raspberry Pi–powered escape room](https://www.raspberrypi.org/blog/raspberry-pi-escape-room/)
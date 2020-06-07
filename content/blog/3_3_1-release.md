---
title: 发布 CodeLab Adapter 3.3.1
author: CodeLab
date: 2020-06-07
tags: ["codelab"]
---

<img class="img-responsive" src="http://adapter.codelab.club/img/WechatIMG1946.jpeg" />

> 技术使普通的物理材料（纸和泥土，卡片和玩具车）栩栩如生。 – Dynamicland

3.3.1 包含以下重大更新。

<!--more-->

# 重大更新

## DynamicTable

`3.3.1` 支持 DynamicTable。

DynamicTable 的核心是[node_physical_blocks](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/nodes_v3/node_physical_blocks.py) 插件, 该插件已经内置在 `3.3.1` 版本中。

DynamicTable 是:

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

我们先来看几个在 DynamicTable 构建的项目:

<video width=80% src="https://adapter.codelab.club/video/1590154622682774.mp4" controls="controls"></video>

<video width=80% src="https://adapter.codelab.club/video/1589459621915320.mp4" controls="controls"></video>

<video width=80% src="https://adapter.codelab.club/video/1590665913541756.mp4" controls="controls"></video>

关于 DynamicTable 的更多信息参考:

-   [CodeLab DynamicTable: A Seeing World](https://www.codelab.club/blog/codelab-dynamictable-a-seeing-world/)
-   [CodeLab DynamicTable: 一个可实施的技术方案](https://www.codelab.club/blog/codelab-dynamictable-an-instance/)

## 新的 Web UI

> Adapter 缺乏一个体面的 UI.

和许多开源项目一样，CodeLab Adapter 的 UI 有些简陋。

近期我们的合作方 Longan 团队正将 CodeLab Adapter 实施于商业项目，他们为 Adapter 重新设计了 UI:

![](https://adapter.codelab.club/img/15b06590c09a5212db8bb3cb7a0f1620.png)

新的 UI，致力于对用户更加友好和可理解，大家如果有什么更好的建议, 欢迎在 [issue](https://github.com/CodeLabClub/codelab_adapter_extensions/issues) 中反馈，我们会持续迭代它。

## 新增插件

### node_physical_blocks 插件

主要用于构建 DynamicTable。前边已经论述。

当然该插件也可以用于其他用途，诸如周末活动的参与者 @taotao 今天在 Neverland 里编程时发现，在用户未接触 marker 时，它的空间信息仍然会发生细微变化，一开始我们都感到疑惑，以为是代码有问题。经过排查，发现原因是因为摄像机能捕获到肉眼不可见的 marker 位置变化, 而 marker 的位置变化则由桌面的微小震动引起(通过实验获知)，所以它可以用于检测桌子的震动！

这是我们设计 node_physical_blocks 插件时，未曾想到的应用场景，由一个编程入门者的疑惑引起的发现。

如果进一步放大震动，甚至有可能用于检测地震。

### node_eim_monitor 插件

如果你是新手，想使用 Python 增强 Scratch，[EIM Monitor](https://adapter.codelab.club/extension_guide/eim_monitor/) 插件可能是最佳选择。

EIM Monitor 致力于在灵活与简易之间取得一个平衡，让新手能够轻松起步。

此前 EIM Monitor 只有 Extension 版本。如果你想引入 Python 社区的第三方库，它便无法满足。

于是我们构建了 EIM Monitor 的 [Node](https://adapter.codelab.club/dev_guide/Adapter-Node/) 版本, 保持 EIM Monitor 简易性的同时，允许用户使用 Python 社区的任何第三方库。

### Yanshee 插件

![](https://www.ubtechedu.com/Uploads/image/20181119/5bf267e6c6ccc.png)

[Yanshee](https://www.ubtechedu.com/show-59.html) 是一个开源人形机器人教学平台， 面向高中和大学生开发，提供专业开源学习软件。

Yanshee 是一个开放的硬件平台，采用 Raspberry Pi + STM32 开放式硬件平台架构，内嵌陀螺仪，开放 GPIO 接口。

采用基于 Linux 的开源软件架构，支持用户直接调用并集成海量的 Raspberry Pi 的开源软件模块

<video width=50% src="https://adapter.codelab.club/video/1589960907435316.mp4" controls="controls"></video>

## 分离 Adapter client

重构前端 adapter client，使其独立成一个类:[codelab_adapter_client.js](https://github.com/CodeLabClub/scratch3_eim/blob/v3/codelab_adapter_base.js), 方便第三方开发者集成，或用于自定义 UI。

目前 EIM 插件和 Web UI 都在使用它，源码是开放的。

## 增强自省能力

CodeLab Scratch EIM 插件增加了 `is_adapter_running` 积木，从而允许用户动态得获取 Adapter 运行情况。

![](https://adapter.codelab.club/img/206dfb1db7d27c3302b7f4a35796fc06.png)

典型的用例是，当项目被社区用户打开时，可以告知用户是否需要启动 Adapter。

Adapter Version 目前已经添加到 env 中，可供外部应用程序查询，以便于协同合作。

## 提升安全性

-   提升所有用到 `eval` 函数的插件的安全性。
-   除了一些受信任域名，从其他域名连接 Adapter，需要手动输入 token（在 Web UI 中可以获取）。

# 插件增强 && bug 修复

-   修复关闭 node 引起的问题。
-   修复 node_minecraft 和 node_raspberrypi 的 bug。在 Scratch 中填入设备 IP，而不需要手动修改 Adapter 插件。
-   增强 CodeLab Scratch json 插件，并[添加社区文档](https://adapter.codelab.club/extension_guide/json/).
-   [@Hanson 同学](https://rcfclass7.wordpress.com/author/hansonxie/)为我们构建了 Box2D 插件的 [文档](https://adapter.codelab.club/extension_guide/Box2D/)
-   Cozmo/Vector 社区用户提到说 `I’ve been playing with the Codelabs setup for Vector, but I am unable to work out how to return status variables from Vector.`，我们之前只在 Cozmo 中完成这个功能，此次更新，将 Cozmo 的 sensor/event 迁移到了 Vector 插件中。
-   改进 extension_webserver 插件:[文档](https://adapter.codelab.club/extension_guide/webserver/)，用户可以在 Adapter 中轻松构建自己的第一个网站。

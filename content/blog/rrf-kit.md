---
Date: 2019-11-06
title: "Revolution Robotics Challenge Kit: 为STEM教育注入变革的力量"
Slug: rrf-kit
tags: ["robot","pragramming","Python","Kit"]
categories: ["少儿编程"]
---

<img class="img-responsive" src="https://blog.just4fun.site/post/img/rrf_home.png" />


>  ROBOTICS IS FOR EVERYONE!

# 想象一下
设想这样一款STEM编程套件:

1. 类似乐高积木的结构件和控制主机(网口)
2. 使用树莓派作为大脑，运行Linux
3. 新手友好的APP
    *  3D视图的项目搭建引导
    *  图形化编程界面(同时显示Python代码)
    *  内置手柄、摇杆等控制器
4. 使用蓝牙连接，方便在课堂、户外等环境中使用
5. 爱好者们在社区中交流讨论并分享作品
6. 以上这些全部开源！

我想，这是许多STEM教育从业者梦寐以求的开放套件。个中原因容易理解。

<!--more-->

大家之所以偏好开放套件，无非是受够了封闭生态的掣肘；之所以梦寐以求，无非至今的探索都不如人意。

# 详细原因
让我们详细分析一下人们为何喜欢拥有上述特性的STEM套件，逐条陈述。

1. 乐高积木拥有绝佳的可上手性，如果对此抱有怀疑，不妨看看学龄前孩子自己使用乐高动手捣鼓的东西。网口接口降低了连接的复杂性，也避免了操作过程中可能的危险。
2. 树莓派作为控制大脑，提供了无限的可能性，树莓派的开放生态让任何创造的起步门槛都变低，同时，它又比任何精致的围墙花园(大多数的商业封闭生态)都更具想象空间，无论是语音控制、网络编程还是机器视觉，你都可以轻松添加进去。
3. 开放性虽代表了未来的无限可能，但过多的选择，容易让初学者无所适从，开源社区因其强烈的自由主义倾向，对初学者缺乏家长式的关怀，许多初学者或许不乐意过早承担自由的`重负`,他们希望在一开始有更贴心的引导，尽管可能不够自由。一个足够友好的APP是不错的折中。
4. 因为ESP32/ESP8266价廉物美，许多产品都采用它们作为通信模块，并优先支持WIFI模式。WIFI有很多优点。其中最显著的一点是，设备一旦联网，就可以接入云端，之后的大多数的工作都可以在云端/Web界面里完成。无论对学习者还是维护者，都极大方便了。例如: m5stack和webduino都做得很好；使用WIFI的另一个优点是传输的带宽足够大，Cozmo便基于WIFI来传输实时控制流和视频流(Cozmo的大脑是分布式的！)。但基于WIFI有一个麻烦，对网络环境的要求较高，教育场景的网络通常是复杂的(室外环境、负载量低、带宽低、复杂的认证机制...)，在这些场合，蓝牙通常是更好地选择。
5. 社区的意义有目共睹，Imagine, Program, Share。在社区中与同伴一同远行。
6. 只要投入足够的精力，围墙花园(封闭生态)总可以打造得优美精致。这是今天消费级商业电子产品取得成功的重要原因。但如果面向教育，情况却有不同。我们须承认，孩子的兴趣是未知的，未来将面为的问题也是未知的。这便是开放性的必要所在。有趣的是，承认世界充满`未知`，也正是[哈耶克](https://zh.wikipedia.org/zh/%E5%BC%97%E9%87%8C%E5%BE%B7%E9%87%8C%E5%B8%8C%C2%B7%E5%93%88%E8%80%B6%E5%85%8B)认为我们需要`自由`的理由。

# 登场
如果以上论述，道出了你对`开放的STEM编程套件`的期望，那么`Revolution Robotics Challenge Kit`便是为你准备的。

我喜欢Revolution Robotics Challenge Kit在[kickstarter](https://www.kickstarter.com/projects/revorobotics/revolution-robotics-affordable-and-fun-open-source-robot-kit?lang=zh)上亮相时所做的自我介绍:

>  STEM教育中的开源革命；不仅仅是玩具机器人套件...还可以编写代码、设计、建造、驱动机器人并从中学习生活技能。

先来看一段官方的介绍视频:

<video width=80% src="/video/rrf.mp4" controls="controls"></video>

### 套件构成
![](https://blog.just4fun.site/post/img/rrf_kits_blocks.png)

Revolution Robotics Challenge Kit是一套完整的机器人构建套件，提供530多种构件， 包括

*  基于树莓派(Raspberry Pi)的大脑
*  五个强大的马达
*  超声波传感器
*  加速度计
*  陀螺仪传感器
*  开关 
*  齿轮
*  轴承
*  以及其他数百个结构件...

Revolution Robotics Challenge Kit符合玩具制造协会的14项优秀STEM/STEAM玩具资格标准。

### 软件
<img src="https://blog.just4fun.site/post/img/rrf_software1.jpg" width=80%/>

随附的Revolution Robotics应用程序(APP)将为8-13岁的孩子提供了详尽的项目引导(3D图)和易于使用的积木编程界面，方便他们编程和控制机器人。有经验的探索者，可以使用Python来对其进行编程。

<img src="https://blog.just4fun.site/post/img/rrf_mobile_c.png" width=80%/>

<img src="https://blog.just4fun.site/post/img/rrf_spin_motor.png" width=80%/>

# 开源
[Revolution Robotics Foundation](https://revolutionrobotics.org/pages/about-us)是一家成立于2018年的非营利组织，致力于使STEM教育机器人价格合理、开放、具有教育意义、公平和有趣。 

联合创始人Jared Schrieber和Jason Morrella希望让更多的孩子参与到机器人技术中。虽然当前的解决方案在推进STEM教育方面显示出巨大希望，但由于专有平台的内在成本、复杂性和不公平性，阻碍了它们的前进。 

[Revolution Robotics Foundation](https://revolutionrobotics.org/pages/about-us)创始者们希望构建一种革命性的开源平台来解决这些问题。

在开源理念之下，[Revolution Robotics Foundation](https://revolutionrobotics.org/pages/about-us)将其所有工作成果开放在Github:[RevolutionRobotics](https://github.com/RevolutionRobotics)。

无论是机器人大脑的[核心源码](https://github.com/RevolutionRobotics/RevvyFramework),还是结构件的[3D打印图纸](https://github.com/RevolutionRobotics/CAD-Resources)......无一保留，全部开放了出来！

![](https://blog.just4fun.site/post/img/rrf_hw.png)

![](https://blog.just4fun.site/post/img/rrf_3d_brain.png)

这意味着，可以据此构建出真正有想象力的项目和社区。

这种彻底的开放，也意味着生态中的企业，可以基于[Revolution Robotics Foundation](https://revolutionrobotics.org/pages/about-us)开创性的工作，快速去生产出千姿百态的STEM套件，去服务更加细分的市场和更加丰富的产品。这些产品中艰难而核心工作都已经都完成了: 多平台的客户端(APP)、通用的机器人框架、固件升级、硬件设计图、结构件3D图纸...


# 内测
![](https://blog.just4fun.site/post/img/rrf_codelab.jpeg)

`Revolution Robotics Challenge Kit`首批产品计划在本月(2019.11)发布。

CodeLab对`Revolution Robotics Challenge Kit`的理念和产品都深感兴趣。我们上个月与Revolution CEO Rosemary Hua 和技术负责人David Dudas通了个电话会议，谈论`Revolution Robotics Challenge Kit`接入CodeLab Adapter和CodeLab Neverland的可能性。他们2人对我们正在做的事情也感兴趣，于是约定在正式发布之前，先给我们寄来一套。

`Revolution Robotics Challenge Kit`依赖于Google的Firebase，目前一些功能暂时无法在国内使用，我们正在与David 商议可能的解决方案。

测试过程中我们发现，`Revolution Robotics Challenge Kit`目前的蓝牙稳定性还存在一些问题，但这块属于软件问题，可以在版本迭代中完善，暂未发现硬件上的硬伤。

就技术和编程教育而言，`Revolution Robotics Challenge Kit`在灵活性和易用性方面的考虑有不少地方超出我的预期。

# 总结
这可能是迄今为止，在STEM领域，就易用性、开放性和完整性方面综合而言，最佳的产品之一，有可能，没有之一。

因为`Revolution Robotics`坚持的开放性和在产品上所付出的巨大努力，我相信`Revolution Robotics Challenge Kit`有望做到其名字中包含的期望`Revolution`:  

为STEM教育注入变革的力量。

# 参考
*  [kickstarter Revolution Robotics Challenge Kit](https://www.kickstarter.com/projects/revorobotics/revolution-robotics-affordable-and-fun-open-source-robot-kit?lang=zh)
*  [revolutionrobotics.org](https://revolutionrobotics.org/)
    *  [ROBOTICS IS FOR EVERYONE!](https://revolutionrobotics.org/blogs/news/robotics-is-for-everyone)
    *  [THE REVOLUTION ROBOTICS CHALLENGE KIT: A COMPLETE ROBOT-BUILDING PACKAGE](https://revolutionrobotics.org/blogs/news/the-revolution-robotics-challenge-kit-a-complete-robot-building-package)
*  [RevolutionRobotics](https://github.com/RevolutionRobotics)
    *  [RevvyFramework](https://github.com/RevolutionRobotics/RevvyFramework)
    *  [CAD-Resources](https://github.com/RevolutionRobotics/CAD-Resources)
    *  [HW-Resources](https://github.com/RevolutionRobotics/HW-Resources)
    *  [BakeRPi](https://github.com/RevolutionRobotics/BakeRPi)
*  [twitter revorobotics](https://twitter.com/revorobotics)
---
title: "CodeLab近况_03"
author: 种瓜
date: "2019-05-19"
---

>  A computer is an instrument whose music is ideas -- Alan Kay

<img class="img-responsive" src="http://wwj-tmp-video.just4fun.site/codelab.jpg" />

这是[CodeLab](https://blog.just4fun.site/about-codelab-club.html)近况的第3篇，前2篇分别是:

*  [CodeLab近况](https://blog.just4fun.site/codelab-club-recent-situation.html)
*  [CodeLab近况与未来](https://blog.just4fun.site/Codelab-Recent-situation-and-future.html)

我们来梳理一下，这段时间[CodeLab](https://blog.just4fun.site/about-codelab-club.html)发生的事情。

<!--more-->



# CodeLab Neverland
首先提及的，是Neverland开张了。

![](http://wwj-fig-bed.just4fun.site/codelab_87d608c1.png)

![](http://wwj-tmp-video.just4fun.site/codelab.jpg)

### 亮灯仪式
2019.05.17 14:30，Neverland举行亮灯仪式。

![](http://wwj-tmp-video.just4fun.site/codelab_startup.jpg)

仪式由CodeLab的工具链驱动，我们在[Turn the world into your playground](https://blog.just4fun.site/Turn-the-world-into-your-playground.html)曾提到:

>  CodeLab[吃自己的狗粮(Eating your own dog food)](https://zh.wikipedia.org/zh-hans/Eating_your_own_dog_food)。

`Eating your own dog food`是一句英语俚语，常用于描述软件开发者使用自己生产的产品。1988年微软公司的高级主管保罗·马瑞兹曾写过一封题为`Eating our own Dogfood`的邮件。让产品设计者去实际使用他们所设计的产品有助于提高产品的质量和可用性。

CodeLab的演讲PPT、Neverland的亮灯仪式，都由`CodeLab`构建的工具链提供驱动力。

驱动亮灯仪式的源代码如图所示:

![](http://wwj-fig-bed.just4fun.site/codelab_neverland_efa5e665.png)

程序的逻辑由两部分构成: 

*  欢迎程序:  当参与者推门而入，门窗感应器将感应到门被打开，则自动播放机器合成的语音: `欢迎参加 Code Lab 亮灯仪式`。
*  亮灯程序:  当CodeLab四位理事将手掌叠在一起，触发亮灯仪式，Neverland空间里的灯光渐次亮起。在原理上，四人手掌交叠，形成电路通路，首尾两人都接触Makey Makey的导线。


[英荔教育](https://blog.just4fun.site/elite-hiring.html)赞助了亮灯仪式的所有物资: 鲜花、食物和饮料...

### 理事会议
仪式结束后，CodeLab召开了自成立以来的第一次理事会议。目前CodeLab的四位理事为：

---

<div id="random_names"></div>

<script>
var random_names = document.querySelector('#random_names');
var pinyin_names = ['程晨', '曾铮', '罗云', '吴文杰']
random_names.innerHTML = pinyin_names.sort(function() { return 0.5 - Math.random() });
</script>

---

理事的排名`不分先后`，我们用程序实现了随机显示，每次刷新页面，排序都会变化。 

按照章程，CodeLab的理事允许罢免和增补。如果你希望申请成为理事，需要做两件事:

*  阅读《Mindstorms》、《终生幼儿园》
*  在申请信中陈述未来对CodeLab的发展所能作出的贡献

此次会议目标是制定下一阶段的执行计划。

议题包括:

*  关于里程碑
    *  Neverland
    *  线上社区
*  下一阶段的执行计划
    *  开放计划
    *  招募计划
*  外部协作/合作的梳理与讨论
    *  合作伙伴
        *  原则和底线
        *  目标与诉求
    *  开源社区
    *  教育社区
*  如何评估CodeLab的工作成效，以随时校正它的方向

延伸出来的其他重要议题包括:

*  一套完整的VI
*  对外输出内容


### 开放计划
Neverland正式开始运营。

Neverland计划对外开放，我们将在下周发布报名地址，到时欢迎大家预约报名。

如此前在[关于codelab.club](https://blog.just4fun.site/about-codelab-club.html#neverland)中提到的:

Neverland(永无乡)是CodeLab活动空间的名字。作为CodeLab办公室的一部分。CodeLab的办公室是开放的, 我们在其中办公，在其中编程，在其中玩乐，在其中做一些有趣的探索和创作。

Neverland名字来自《小飞侠彼得·潘》,是故事中的一座海岛。在永无乡里，人们永远长不大。

>  后来，他领着我飞到了永无乡，那儿还有仙子，还有海盗，还有印第安人，还有人鱼的礁湖；还有地下的家，还有那间小屋子。 --《小飞侠彼得·潘》

我们将在Neverland里做许多有趣的事，我们准备在其中实现空间编程，亲手编程将它打造为一个智慧空间，我们准备在其中创作情景剧、体感游戏，以及构建令人热血沸腾的[Dynamicland](https://blog.just4fun.site/the-next-big-thing-is-a-room.html)。所有这些你都可以参与进来，他们像搭积木一样地简单。在这个过程中，你将学习人工智能、物联网和虚拟现实。


<!--如果你或身边的朋友有兴趣，欢迎预约报名, 报名地址是: [CodeLab Neverland学员报名表]()

    将学到什么
        入门编程
        realworld
            关于我们
        周末俱乐部


此外，我们计划在六月份开始接受组织和个人的参观，大家可以先预约: [CodeLab Neverland参观预约表]()

如果你

欢迎转给你身边感兴趣的朋友，我们目前接纳8-16岁。之后会放宽条件。微信。

是否有Scratch编程经验，

我们也接受参观。时间限制在1小时。预约
--> 


### 招募计划
同时，Neverland开始对外招募实习生。

Neverland目前的全称是`Neverland v1.0.0-rc1`。

rc是`Release Candidate`的缩写，常用于代表软件的候选版本。我们将Neverland整个空间视为一个软件，这个软件运行在各类物理设备上:

*  脑电波传感器
*  眼动仪
*  智能家居设备
    *  门窗感应器
    *  插座
    *  开关面板
    *  空气净化器
    *  扫地机器人
    *  彩灯、吊灯
    *  窗帘电机
    *  双路控制器
        *  门禁
*  Cozmo/Vector
*  四轴飞行器
*  乐高积木
*  Switch Labo
*  各类芯片和控制板: 
    *  Microbit
    *  Raspberrypi
    *  Arduino
    *  BPI-BIT
    *  OpenMV
    *  Makey Makey
    *  Esp32
    *  Esp8266
    *  ...
*  Laserblock

虽然这个空间运行在各类物理设备上，但物理设备是不重要的，就像操作系统是硬件无关的。所以我们使用了软件版本号。这个空间由[CodeLab Adapter](https://codelab-adapter-docs.codelab.club/)驱动，空间里的一切都可动态调整，从开关电灯、窗帘门锁到飞行器、眼动仪，目之所及，皆可编程和再创造。所以Neverland和软件一样可以迭代和进化。

这儿是绝佳的学习和探索环境。欢迎教育学、计算机科学、人工智能、交互艺术等相关专业的学生前来实习。

当然，我们十分欢迎非科班出身，但对教育学、心理学、计算机、人机交互领域充满热情、不断探索之人。

除了丰富的创作设备，我们还接纳孩子随时到空间中与我们一同创造，空间不做任何分割，没有办公区、学习区，在Neverland中发生的一切都是探索与创造。我们信奉Seymour Papert在《Mindstorms》中表达的理念: 承认孩子和非专业用户的智力与创造力，为他们提供优秀的创作工具，然后在协作中一起前进。

有意愿前来实习的学生，欢迎邮件联系:  `wuwenjie@codelab.club`， 也欢迎转给你周围可能感兴趣的朋友。


# 线上社区
Neverland是CodeLab的第一个里程碑。

CodeLab的第二个里程碑是线上社区。

我们已经完成了线上社区的基本功能:

*  用户的注册、登陆
*  项目的创建、保存、浏览、分享、改编(remix)
*  点赞、收藏、讨论

感谢CodeLab的两位志愿者在这块付出的巨大努力,  感谢他们付出的周末和夜晚时间。

目前我们正在将[Scratch全球社区项目](https://scratch.mit.edu/)整合到CodeLab社区中，Scratch全球社区里的4000多万用户贡献了超过一亿个项目。

CodeLab社区不仅允许国内用户浏览和改编全球社区里海量的项目，我们还将允许用户以这海量的创意为基础，将其延伸到现实世界中。

在CodeLab社区，[CodeLab Adapter](https://codelab-adapter-docs.codelab.club/)可以与全球社区中的任何项目混合使用，这意味着，如果你是Scratch用户，在不损失任何东西的情况下，得到了连接万物的能力！CodeLab Adapter通过引入AI、IoT、开源硬件、网络联机(参考[codelab-adapter的虫洞(wormhole)](https://blog.just4fun.site/codelab-adapter-wormhole.html))，进一步扩大想象力的边界。我们希望以此来回应[约翰·杜威](https://zh.wikipedia.org/zh/%E7%BA%A6%E7%BF%B0%C2%B7%E6%9D%9C%E5%A8%81)提倡的:

>  Education as life

由CodeLab Adapter驱动的一些案例，可以在这儿查看:[演示视频(Gallery)](https://adapter.codelab.club/user_guide/gallery/)


关于线上社区，CodeLab一共分享了10篇文章，讨论我们在这方面的思考和工作，希望我们的工作能成为后来者们改进Scratch的基石:

*  [Scratch3.0技术分析之后端API(第0篇)](https://blog.just4fun.site/Scratch3_api_analysis.html)
*  [Scratch3技术分析之创作平台API(第1篇)](https://blog.just4fun.site/Scratch3_api_analysis_1.html)
*  [Scratch3技术分析之静态资源API(第2篇)](https://blog.just4fun.site/Scratch3_asset_analysis_2.html)
*  [Scratch3技术分析之项目主页API(第3篇)](https://blog.just4fun.site/Scratch3_project_homepage_analysis_3.html)
*  [Scratch3技术分析之User API(第4篇)
](https://blog.just4fun.site/Scratch3_user_api_analysis_4.html)
*  [Scratch3技术分析之社区 API(第5篇)](https://blog.just4fun.site/Scratch3_community_analysis_5.html)
*  [Scratch3技术分析之项目内部数据(第6篇）](https://blog.just4fun.site/Scratch3_project_json_analysis_6.html)
*  [Scratch3技术分析之云变量 API(第7篇)](https://blog.just4fun.site/scratch3-cloud-var.html)
*  [Scratch3技术分析之Studio API(第8篇)](https://blog.just4fun.site/scratch3-studio.html)
*  [Scratch3 技术分析之 backpack(书包) API(第 9 篇)](https://blog.just4fun.site/scratch3-backpack.html)


线上社区虽然完成了基础功能，但并不急于对外开放。相比于扩张，我们更关注社区的文化和讨论氛围，我们希望用户在其中真能有所收获、认真交流、找到同伴(peers)。而不是关注点赞数和彼此争吵。我们将从Neverland的线下社区开始，培育彼此尊重、乐于分享的种子。

从线下社区开始的idea，是学习Scratch官方社区的启动方式（记录在《终生幼儿园》一书中，他们早期将孩子邀请到终身幼儿园实验室中，一起编程）。

Scratch官方社区是迄今为止最成功的编程社区之一。一个社区的灵魂是它的氛围，而不是用户数。所以我们短期内不计划对外开放访问。社区将采用邀请制。

# CodeLab Adapter

### 贡献者

首先感谢近期加入的3位贡献者:

*  [junhuanchen](https://github.com/junhuanchen)
*  [bilikyar](https://github.com/bilikyar)
*  [wangshub](https://github.com/wangshub)

##### [junhuanchen](https://github.com/junhuanchen)
[junhuanchen](https://github.com/junhuanchen)是CodeLab Adapter[extension_mpfshell](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extension_mpfshell.py)插件的贡献者和维护者。该插件可以将基于ESP8266的硬件接入到CodeLab Adapter中。

[junhuanchen](https://github.com/junhuanchen)成功将CodeLab Adapter接入到blockly生态中，而且开源了这部分的工作，也写了细致的文档。

据说程序员最痛恨的两件事分别是:

>  自己写文档；别人不写文档。

最喜欢的两件事分别是：

>  别人写文档；自己不用写文档；

[junhuanchen](https://github.com/junhuanchen)写得一手出色的文档，由此可知他是那类招人喜欢的程序员。他在文档里清晰解释了CodeLab Adapter的设计理念，也做了周到的引导示范。对此有兴趣的朋友，可以看他的Github: [junhuanchen](https://github.com/junhuanchen)

此外，[junhuanchen](https://github.com/junhuanchen)与我一起发起了[万物积木化开发者社区](https://forums.codelab.club/)社区。细节参考[这篇文章](https://blog.just4fun.site/forums-4-developers.html)。

##### [bilikyar](https://github.com/bilikyar)
[bilikyar](https://github.com/bilikyar)是CodeLab Adapter [extension_jupyter.py](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extension_jupyter.py)和[extension_arduino_nano.py](https://github.com/Scratch3Lab/scratch3_arduino/blob/master/extension_arduino_nano.py)插件的贡献者和维护者。

[extension_jupyter.py](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extension_jupyter.py)允许使用CodeLab Adapter GUI启停jupyter，而jupyter安装在一个嵌入式Python环境中。[bilikyar](https://github.com/bilikyar)的工作解决了困扰我们已久的打包问题，有了这个工作，CodeLab Adapter 面前无疑打开了一扇崭新的大门。之后可以做的东西，一下子变得无限宽广。

方案的细节见: [嵌入式Python环境](https://blog.just4fun.site/embeddable-python-zip-file.html)

[bilikyar](https://github.com/bilikyar)目前所在公司将CodeLab Adapter用于教学。使用了内置的[extension_python_kernel.py](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extension_python_kernel.py)插件。之所以选择该插件而不是采用当前主流的做法，[bilikyar](https://github.com/bilikyar)在[Makecode Static Python](https://forums.codelab.club/t/makecode-static-python/144)这个帖子下做了阐述。

在[bilikyar](https://github.com/bilikyar)的安利下，他们公司的产品部负责人[@李恒](https://github.com/LIHENGs)也成为CodeLab的志愿者，为我们重新设计了UI:

<img src="http://wwj-fig-bed.just4fun.site/adapter_45dbf788.png" width=400 />

### [wangshub](https://github.com/wangshub)
[wangshub](https://github.com/wangshub)是CodeLab Adapter [extension_leju_pando.py](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extension_leju_pando.py)插件的贡献者和维护者。该插件可以将[Leju Pando机器人](https://thinkhard.tech/2019/04/17/codelab-pando-tutorial/)接入到CodeLab Adapter中。

[wangshub](https://github.com/wangshub)为CodeLab Adapter编写了通用的ble驱动，通过兼容dongle，CodeLab Adapter将能够在Windows7和其他不支持ble的电脑上连接ble设备。

目前[wangshub](https://github.com/wangshub)正在将CodeLab Adapter的GUI迁往新的设计上（基于pyqt5），已经基本完成界面构建:

<img src="http://wwj-fig-bed.just4fun.site/pyqt_adapter_f9251223.png" width=500 />

在这次大升级中，[wangshub](https://github.com/wangshub)将基于[fbs](https://github.com/mherrmann/fbs)来整体优化软件包的安装、签名和更新等问题。

### 技术工作
接下来梳理下CodeLab近期在增强CodeLab Adapter这块所做的工作.

#### 物联网(IoT)
物联网是我们关注的一块。

近期CodeLab在IoT方面构建了一些工具。和大多数IoT项目相似，我们的工作也围绕MQTT协议展开。

CodeLab之后除了对外提供基础工具，也希望能对外提供基础服务。我们的工具链和服务都基于开源项目构建。

我们近期的工作包括:

*  Scratch IoT Extension
*  codelab-adapter iot extension
*  IoT server: iot.codelab.club

![](http://wwj-fig-bed.just4fun.site/scratch-iot_072d531a.png)

更多细节，参考我们近期的文章:

*  [CodeLab ❤️ IoT](https://blog.just4fun.site/codelab-love-iot.html)
*  [一辆树莓派可编程小车的问题](https://blog.just4fun.site/rpi-car-difficult.html)
*  [基于树莓派的积木化编程解决方案](https://blog.just4fun.site/codelab-rpi-mqtt-solution.html)

#### 虫洞(wormhole)
![](http://wwj-fig-bed.just4fun.site/wormhole_4fcface5.png)

设想这样一种场景，一群用户聚集在一个线下空间里，线下空间可能是一个线下俱乐部(如[coderdojo](https://coderdojo.com/))、一个线下培训机构、一个班级、以及我们的CodeLab Neverland。他们接入同一个局域网中。学习者们身处同样的物理空间，我们是否考虑将他们所处的虚拟空间和创作平台中也连接在一起，支持更多的协作和交互。

我们想到"虫洞"的概念。

>  相隔遥远的两个巫师同时讲一句相同的魔法咒语，这导致了他们之间建立了某种神秘的联系。接着一个巫师把魔法书扔进虫洞，书就从另一个巫师身边的虫洞掉了出来。

这个概念如此简洁。巫师只是说了相同的咒语，连接就自动建立了。虫洞是声明式的！上帝说要有光，于是就有了光，看起来也类似申明式编程。

我们将"虫洞"内置到Codelab Adapter中，Codelab Adapter通过一个"咒语"发现彼此，之后自动建立连接，消息在adapter内置的虫洞中传递，用户只要收取虫洞里的消息即可。

由于scratch和adapter在设计上都深受Smalltalk的影响，采纳`everything is message`的设计原则，所以MIT Scratch社区里4000多万用户创建的超过1亿的项目将直接得到虫洞功能，在局域网内随意连接！延迟在毫秒级。足以构建实时游戏。

详情见:[Codelab Adapter的虫洞(wormhole)](https://blog.just4fun.site/codelab-adapter-wormhole.html)

### 新接入的设备和软件
CodeLab Adapter最近接入了:

*  脑电波传感器
*  眼动仪
*  物理引擎
*  toio
*  Arduino
*  大疆Tello四轴飞行器
*  Jupyter
*  IoT
*  Leju Pando机器人

欢迎浏览[演示视频(Gallery)](https://codelab-adapter-docs.codelab.club/user_guide/gallery/)

# CodeLab Mindstorms
![](http://scratch3-files.just4fun.site/codelab_branch.png)

在[上一篇近况](https://blog.just4fun.site/Codelab-Recent-situation-and-future.html)中提到CodeLab对未来的规划。

CodeLab Mindstorms是规划之一， 我们曾提到:

>  CodeLab Mindstorms将关注编程教育，但不准备发表“编程有助于提高逻辑思维能力”之类的陈词滥调。CodeLab Mindstorms关注认知论、学习者的心理模型、建构主义、面向对象、设计原则，CodeLab Mindstorms将翻译和解读这个领域最优秀的探索者所做的工作，这些工作中的大多数已经被遗忘，有一部分正在被复活(如Dynamicland、Scratch Team和艾伦凯正在做的事情)，但关注者寥寥，CodeLab Mindstorms将解读[约翰·杜威(John Dewey)](https://zh.wikipedia.org/zh/%E7%BA%A6%E7%BF%B0%C2%B7%E6%9D%9C%E5%A8%81) 、[道格拉斯·恩格尔巴特(Douglas Engelbart)](https://en.wikipedia.org/wiki/Douglas_Engelbart)、[皮亚杰(Jean Piaget)](https://zh.wikipedia.org/zh-hans/%E8%AE%93%C2%B7%E7%9A%AE%E4%BA%9E%E5%82%91)、[艾伦·凯(Alan Curtis Kay)](https://zh.wikipedia.org/zh-hans/%E8%89%BE%E4%BC%A6%C2%B7%E5%87%AF)、[派普特(Seymour Papert)](https://en.wikipedia.org/wiki/Seymour_Papert)、[密契尔(Mitchel Resnick)](https://en.wikipedia.org/wiki/Mitchel_Resnick)、[Bret Victor](http://worrydream.com/)等人的工作。

CodeLab Mindstorms已经付诸实践，我们将其放在Github上:  [codelab-mindstorms](https://github.com/Scratch3Lab/codelab-mindstorms)，鼓励大家在开源社区里协同合作。

感谢以下几位志愿者在CodeLab Mindstorms项目上的工作。

### @林锴
在USCD参加Open edX 2019年会时，正巧收到@林锴的邮件，他提到此前曾在UCSD上学，希望成为CodeLab志愿者。

@林锴在邮件里说:

>  了解到了更多codelab的动向之后，真的有点相知恨晚的感觉，于是提笔。

他介绍自己说到:

>  创业之前的身份是硬件工程师，在硅谷和上海工作了几年，再之前是一名UCSD计算机工程专业的学生。

>  算是Scratch的狂热粉丝，《终生幼儿园》的读者。自己现阶段和未来想做的就是希望，力所能及地，创造一些给青少年了解与学习编程乃至计算机科学的机会，给他们编些真正适合他们学习的书籍和课程。

>  不知道codelab的大计划里有没有一些我可以参与帮助的工作或是内容，志愿者活动或者其他的形式都可以...翻译能力和文笔还可以，现在也在为树莓派基金做些翻译志愿者的工作。

@林锴的工作、学习经验和硬件工程师、计算机工程专业背景，加上在开源社区翻译上的经验，十分适合参与CodeLab的翻译工作。

@林锴翻译了[CodeLab Adapter Value](https://codelab-adapter-docs.codelab.club/about/value/#our-values)。

### @杨柳青
@杨柳青在邮件里说:

>  前段时间Seymour的Mindstorms这本书，我完整阅读了两遍，最终写了一篇文章放在了公司的公众号上。在书前的序中，Alan Kay的名字被提到，由此我又发现了一位让我惊叹不已的人。最近这些天，我就一直在看Alan Kay曾经写的文章，Youtube上的演讲视频，搜索他相关或提及的关键词，也由此发现了你们。

>  我发现我很难用语言准确描述自己的情感，下面我就干脆过滤掉情感平铺直叙了。

>  我的背景是心理学，硕士毕业于中科院心理所。

>  我看到你们正在规划CodeLab Mindstorms项目，计划做的事情也是我最近在阅读过程中有想过的，或许可以加入一起做。我平时的英语阅读量还是挺大的，虽然翻译工作确实没做过，但还是想尝试做。

@杨柳青目前正在参与翻译Alan Kay的[Background On How Children Learn](http://www.squeakland.org/resources/articles/article.jsp?id=1003)

### @[郭瑞彪](https://github.com/guoruibiao)
@[郭瑞彪](https://github.com/guoruibiao)的Github签名是

>  create something scarce, not something cheap.

他参与翻译了[为什么Python对于基础编程课程中的初学者来说是一门很棒的语言](https://github.com/Scratch3Lab/codelab-mindstorms/blob/master/%E8%AF%91%E6%96%87/python-teaching.md)

### @王松
@王松正是我们前头提及的[wangshub](https://github.com/wangshub)，他目前参与翻译了Bret Victor的[Kill Math: 让数学不只是符号](https://github.com/Scratch3Lab/codelab-mindstorms/blob/master/%E8%AF%91%E6%96%87/kill-math.md)一文。

### @廖曼江
@廖曼江目前是教育学研究生，她已经读完《Mindstorms》，觉得深受启发。此前她一直在关注`计算思维`,目前在参与翻译[A new definition of Computational Thinking: It’s the Friction that we want to Minimize unless it’s Generative](https://computinged.wordpress.com/2019/04/29/what-is-computational-thinking-its-the-friction-that-we-want-to-minimize/)

---

CodeLab Mindstorms涉及的内容我们将以翻译者的名义(CodeLab志愿者)陆续刊载在[CodeLab Blog](https://www.codelab.club/blog/), 允许转载。授权协议为[自由转载-非商用-非衍生-保持署名](https://creativecommons.org/licenses/by-nc-nd/3.0/deed.zh)。


# 开源项目
我们近期开源了若干项目，放在这个地址下: [Github codelab.club](https://github.com/Scratch3Lab)

已经开源的项目包括:

*  [codelab_adapter_extensions](https://github.com/Scratch3Lab/codelab_adapter_extensions)
    *  [firmware](https://github.com/Scratch3Lab/codelab_adapter_extensions/tree/master/firmware)
*  [codelab-mindstorms](https://github.com/Scratch3Lab/codelab-mindstorms)
*  [codelab-adapter-docs](https://github.com/Scratch3Lab/codelab-adapter-docs)
*  [scratch3_arduino](https://github.com/Scratch3Lab/scratch3_arduino)
*  [scratch3_eim](https://github.com/Scratch3Lab/scratch3_eim)
*  [scratch3_hello_world](https://github.com/Scratch3Lab/https://github.com/Scratch3Lab/scratch3_hello_world)
*  [scratch3_req_rep](https://github.com/Scratch3Lab/scratch3_req_rep)
*  [scratchblocks2svg](https://github.com/Scratch3Lab/scratchblocks2svg)
*  [scratch3_knn](https://github.com/Scratch3Lab/scratch3_knn)


<!--
接受申请 小程序
codelab 启动仪式
-->

# 合作与交流

### MIT Media Lab
![](http://wwj-tmp-video2.just4fun.site/codelab_mit.jpg)

2019.3.25，从北京飞往洛杉矶，参加Open edX 2019年会。去美国之前给Scratch之父[@Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)发了个邮件, 提到我们计划去MIT Media Lab拜访， 在邮件里分享了CodeLab近期做的事情。[@Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)回复说:

>  I’d be happy to try to set up a meeting...I’m also cc-ing Kreg Hanning, a Scratch Team member who does a lot of work with extensions.

之后他将@Kreg拉入了邮件组。@Kreg是上边截图里右边的那位（哈哈，格子T恤）。

由于隐私在国外比较受重视，我们对拍摄的照片全部做了处理（不露脸），避免侵犯隐私。

2019年4月5号，CodeLab核心志愿者@Finn、CodeLab 2位理事@曾铮、@吴文杰一同到MIT Media Lab拜访，见面时，@Kreg十分热情，带着我们逛了一圈Media Lab，介绍了许多有趣的东西。

我们分享了CodeLab Adapter在增强Scratch这方面的思考和探索，@Kreg对我们设计的开放式插件系统很感兴趣，就着[架构图](https://codelab-adapter-docs.codelab.club/dev_guide/Architecture/)聊了很久。@Kreg很快理解了架构背后的设计意图和原则，他要了份PPT，准备就这个话题在[Lifelong Kindergarten小组](https://www.media.mit.edu/groups/lifelong-kindergarten/overview/)内部再做个分享和讨论，可能会将我们的设计用于增强Scratch，@Kreg计划在今年七月份到CodeLab Neverland参观交流。

### [The Clubhouse Network](https://www.media.mit.edu/projects/computer-clubhouse/overview/)

@Kreg在邮件里向我们推荐了The flagship clubhouse。

>  The flagship clubhouse is nearby in Boston. I would definitely recommend visiting them if you can!


Clubhouse提供创造性和安全的校外学习环境。来自贫困街区的年轻人与成年人导师一起探索自己的想法、开发新技能，并通过使用技术来建立自信。 

第一家Clubhouse成立于1993年，是MIT Lifelong Kindergarten小组和计算机博物馆的合作。

The flagship clubhouse的志愿者耐心地回答了我们的所有疑惑。


我们对clubhouse做了必要的了解，从中学到的东西之后可能用于运营Neverland。

![](http://wwj-tmp-video2.just4fun.site/codelab_clubhouse.jpg)

### iWise论坛

![](http://wwj-fig-bed.just4fun.site/iwise_bret_mindstorms_62844c2b.png)


2019年4月20号，参加iWise Forum 第11期活动，CodeLab带来的分享话题是: [Turn the world into your playground](https://blog.just4fun.site/Turn-the-world-into-your-playground.html)

![](http://wwj-fig-bed.just4fun.site/iwise_d7db51a9.png)


活动详情参考[这儿](https://blog.just4fun.site/Turn-the-world-into-your-playground.html)。

PPT采用[codelab-scratch](https://scratch3.codelab.club/)制作。我们[吃自己的狗粮](https://zh.wikipedia.org/zh-hans/Eating_your_own_dog_food), 翻页笔使用了Switch Joy-Con，由[codelab-adapter](https://adapter.codelab.club/)驱动。

我们现场演示了智能家居、眼动仪、脑电波传感器与积木的结合。


### 奇码科技
前头提到的CodeLab的志愿者[bilikyar](https://github.com/bilikyar)和[@李恒](https://github.com/LIHENGs)皆来自奇码科技，目前奇码科技将CodeLab Adapter用于Python教学和硬件教学。

### BPI
CodeLab的志愿者[junhuanchen](https://github.com/junhuanchen)是BPI的硬件工程师，他也是[BPI-STEAM/BPI-BIT-MicroPython](https://github.com/BPI-STEAM/BPI-BIT-MicroPython)教育项目的维护者。

风靡台湾的[webduino](https://webduino.io/)所采用的硬件便出自BPI。[webduino](https://webduino.io/)在硬件编程教育这块走得很远，他们十分开放，开源了几乎所有东西，之前读了不少他们的源码，写得非常出色，在blockly驱动硬件这块，[webduino](https://webduino.io/)和BPI是目前走得最远的团队之一。

感谢BPI赠予的2款开源硬件。[junhuanchen](https://github.com/junhuanchen)已经将BPI-BIT接入到CodeLab创作平台。


### 乐聚机器人
CodeLab的志愿者[wangshub](https://github.com/wangshub)是乐聚机器人的技术总监，他目前已将[Leju Pando机器人](https://thinkhard.tech/2019/04/17/codelab-pando-tutorial/)接入到CodeLab Adapter中。

[wangshub](https://github.com/wangshub)编写了完整的使用文档:[当遇到 Scratch3-Codelab，Pando 觉醒了！](https://thinkhard.tech/2019/04/17/codelab-pando-tutorial/)

### 网易
应网易卡搭编程团队@汤天亮邀请，与网易的诸位同仁在杭州聊了一个下午。很投缘，网易团队在教育上十分走心。

网易团队对CodeLab探索的几个方向都很感兴趣。探讨了一些可能的合作的模式和机会，包括在活动和技术上的合作可能。

Neverland已经建成，当时约定下次在Neverland再细聊，期待与大家在广州的相聚。

### 大疆(DJI)
感谢大疆赠予了我们两台还在研发中的[Tello Edu](https://store.dji.com/cn/product/tello-edu)飞行器。

与大疆的两位同仁@Melody、@Damom聊了很多编程教育相关的思考，@Melody读完《Mindstorms》之后，觉得深受启发，计划在下周的演讲上引用《Mindstorms》和《终生幼儿园》的教育思路。期待之后与大疆(DJI)在教育领域一同探索、前行。

### 绿米
感谢绿米工程师 @毛勇 一直以来的支持。

目前，Neverland空间里的智能设备目前大多数都选择了绿米的产品。

CodeLab希望让空间里的一切皆可编程，让万物积木化，如此一来，我们就能像书写软件一样书写空间。

我们希望目之所及，皆可编程。但目前市面上的门禁系统都没有开放API接口。为了运行我们的微信开门程序，我们需要hack市面上的门禁系统，此前与@毛勇的沟通中了解到绿米办公室已经成功hack了门禁系统。@毛勇捐赠了改装后的双路继电器，协助我们hack了门禁系统，把电路改造图也分享给了我们。

此外，感谢 @邓婷 带领参观绿米的体验馆。期待CodeLab与绿米在体验馆方面的合作。


# 参考
*  [关于codelab.club](https://blog.just4fun.site/about-codelab-club.html)
*  [CodeLab近况](https://blog.just4fun.site/codelab-club-recent-situation.html)
*  [CodeLab近况与未来](https://blog.just4fun.site/Codelab-Recent-situation-and-future.html)
*  [Codelab Adapter演示视频(Gallery)](https://adapter.codelab.club/user_guide/gallery/)
*  [FutureOfCoding](https://forums.codelab.club/)
*  [Etoys学习笔记: 与Scratch互操作](https://blog.just4fun.site/Etoys-learning-note.html)
*  [Scratch3 技术分析之 backpack(书包) API(第 9 篇)](https://blog.just4fun.site/scratch3-backpack.html)
*  [Turn the world into your playground](https://blog.just4fun.site/Turn-the-world-into-your-playground.html)
*  [The future of coding](https://blog.just4fun.site/The-future-of-coding.html)
*  [美国之行](https://blog.just4fun.site/USA-travel.html)
*  [物联网相关开源项目整理](https://blog.just4fun.site/iot-open-source-projects.html)
*  [物联网、开源硬件与开源社区](https://blog.just4fun.site/iot-open-source-hardware-community.html)
*  [万物积木化开发者社区](https://blog.just4fun.site/forums-4-developers.html)
*  [CodeLab ❤️ Blender](https://blog.just4fun.site/codelab-love-blender.html)
*  [codelab-adapter的虫洞(wormhole)](https://blog.just4fun.site/codelab-adapter-wormhole.html)
*  [基于树莓派的积木化编程解决方案](https://blog.just4fun.site/codelab-rpi-mqtt-solution.html)
*  [一辆树莓派可编程小车的问题](https://blog.just4fun.site/rpi-car-difficult.html)
*  [CodeLab ❤️ IoT](https://blog.just4fun.site/codelab-love-iot.html)
*  [webduino-module-eim](https://github.com/junhuanchen/webduino-module-eim)
*  [codelab-adapter的虫洞(wormhole)](https://blog.just4fun.site/codelab-adapter-wormhole.html)
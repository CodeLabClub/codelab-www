---
Date: 2020-03-09
title: "社区版 Neverland"
Slug: Neverland-community
tags: ["CodeLab"]
categories: ["少儿编程"]
author: "种瓜"
---

<img class="img-responsive" src="http://adapter.codelab.club/img/adapter_party.jpeg" />

# 前言
是的，我们将开放Neverland构建方案。

<!--more-->


<video width="80%" src="https://adapter.codelab.club/video/1583729439575050.mp4" controls="controls"></video>

我们于2019年5月份完成CodeLab Neverland。 接受外部访问后，陆续收到许多访问预约，前后也接待了不少教育从业者/IT从业者(`>100`)。

大家对我们正在做的事情感到兴奋，予以鼓励和支持。许多Maker/Geeker/Hakcer希望我们开放整个构建方案，让大家能自行在 家里/学校/创客实验室 构建出Neverland这样高度灵活和可扩展的`可编程空间`。

过去的时间里，CodeLab忙于探索构建线下空间的可能性 忙于完善CodeLab Neverland的基础设施[CodeLab Adapter](http://adapter.codelab.club/)， 同时也忙于探索与商业公司合作的可能性。 

现在我们终于有时间，来分享社区版 Neverland。供社区爱好者基于我们的工作去再创造，以及，去

>  Turn the world into your playground!

### CodeLab Neverland 是什么？
CodeLab Neverland是一个`可编程空间`。

CodeLab Neverland核心由[CodeLab Adapter](http://adapter.codelab.club/)驱动。它致力于连接万物，无论是软件还是硬件，无论是AI、开源硬件、现实世界的物体、还是虚拟世界的动画角色，在CodeLab Adapter的驱动下，皆可彼此互动。

在CodeLab Neverland，你可以与万物沟通，你可以让神经网络识别出你的身体部位，进而制作一个体感游戏, 或是通过算法让整个空间变得智能。你可以在朋友生日那天，在Ta进门的一刻，将手中的魔杖一挥，在空中划一个字母L的轨迹，瞬间，点亮房间里五彩的灯光。在这儿，你将轻松做出这样的魔杖。

"魔法"是编程绝佳隐喻。将咒语写在石头上，使其在现实世界中显灵，这在过去是关于魔法的传说。今天，这块石头是计算机硬件，它的核心部分由石头里的成分构成--硅。其上的咒语则是代码，当它生效的时候，便能送火箭上天，将信息发送到地球另一边的水晶球(手机屏幕)上。在过去，这些都是魔法学徒们梦寐以求的事情。

我们希望将你带入一个魔法世界，一个由编程驱动的世界。

同时， CodeLab Neverland 也致力于去实践约翰·杜威提倡的

> Education as life.

# 架构
[CodeLab Neverland Architecture](https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1#R7Vhdj5s4FP01lnYfWsV8BR4hYdqVZqvRZKW2jw444I6DWeM0yf76vQYTQiCZrjqZjLR9in18r8Hn3A8HZM%2FWuw%2BSlPmfIqUcWZN0h%2Bw5siyMfQ9%2BNLJvEDfADZBJlhqjDliwf6gBJwbdsJRWPUMlBFes7IOJKAqaqB5GpBTbvtlK8P5TS5LRAbBICB%2Bin1mq8gb1rWmHf6Qsy9snYy9oVtakNTYnqXKSiu0RZMfInkkhVDNa72aUa%2FJaXhq%2FuzOrhxeTtFA%2F4vD0uLMmj%2Fan8Cte3EX3q0dnNX9nNbt8J3xjDmxeVu1bBqTYFCnVm0yQHW1zpuiiJIle3YLmgOVqzWGGYWi2o1LR3dn3xIfTQ9hQsaZK7sHEOPhO42ECxjf0bTv2Pc9g%2BRHzjmNAYhTPDjt3pMDA8PJfOMIDTmgKQWKmQqpcZKIgPO7QqM9aZ3MvRGm4%2BkaV2puIJxsl%2BkzSHVNftPt718y%2Bms30eL47nuzbSQHnNU5uO6%2Fd3geHeedaz3q%2BD1QyII1KAzYH16e9LCaQIzYyoRdYtE3yEplRdcEuGA8OSTlR7Hv%2FPV5e6mH4v6LU%2BFjog%2BzPSd3X%2BTmZb6Co85OK1q6hlGR%2FZFAKVqjqaOcHDXRVxHanvTJin1bHZ%2Bwt97K9g51L9jBo3riLxcPRfyI87V%2Fh%2BeLhOb1lwbEH%2FXcGV6h7sgQwTEmpS%2FH5hoxfpSFje9IP9WDYkvF0pCV7V%2BvIkwEpbz4P3l5Hdn4wQfBkPDxeJ0OcQYZ8hJ11elQVqxSpi7J%2BhDX5TJd%2F5azIqpunzKA7WLdOGW9AI7I8Dk%2BNVqKmsGPL%2B3sj2oV3VZ0NIRhgv9x1izDK9G9Xrj5RoIyTIm03hvds9m4sB6IAvarPfKWkeKIzwYUO90IUOm9XjPMTiHCWFTBNQA6dGZEWi8GfttAsrFma1kk%2FJnW%2FELyA2jYOemqP1cdgRGz7WmJPB2LP9wVZs6SRx6TLIyVcEf7U6rWUrVS%2FodhH0R0KIhS7KMIIalXsoMhH4fz3N5dctnvr5AoGfId%2FoNhG8N%2FVx4tEEpXkh%2FnDHjpPMSS9pnqmbWIPRSGCiImnKMQonNXkRyjyxrxqXfy5dgcXf6YHvlt7weBOr8KGoGAQaFl9C0WWXgoBmR7tfNpQOWdlpXOoykmpwYSLTfo6N45J%2F8aBnaHChy9ExwoH11K4fdhx%2FQR1ojkKcD2IUDDT9IYxiuKaXgf503GVtY1nMguUGvF6Q1p4J1qMFTdrRAr%2Fapc%2F92wrW3YsN%2FUr1qHvxzrWu6a0%2FB90JK8vmo2HqjkjollXE%2B38%2FeOXaG2mWSf%2Fs0YujS8kGky7D8%2FN14nu870d%2Fws%3D)

![](/img/5a257b31bb5aecdf42b35cb5eb5f9038.png)

CodeLab Neverland的架构图如上所示。 它由三部分构成:

*  CodeLab Adapter
*  Home Assistant / WebThings
*  Dynamicland / Realtalk

在早期版本中，我们采用CodeLab Adapter驱动一切。后来我们把与家居和网络有关的硬件交给[Home Assistant](https://www.home-assistant.io/)驱动，它是我最喜欢的开源项目之一。截止到目前，全球有1824位开发者为Home Assistant贡献源代码，一共接入了全球范围内1558款家居设备！

采用[Home Assistant](https://www.home-assistant.io/)的理由是，我们直接将其用作CodeLab Adapter的扩展，而不必重复去做[Home Assistant](https://www.home-assistant.io/)社区的巨大工作。Home Assistant目前运行在CodeLab Neverland的树莓派中。基于消息的`连接`始终是CodeLab Adapter的思考方式。

>  The Big Idea is Messaging --Alan Kay

事实上你也可以不用Home Assistant，而使用CodeLab Adapter驱动一切。[lejurobot](http://www.lejurobot.cn/cn/)的CTO[王松同学](http://thinkhard.tech/)(哈哈王松同学还在读博士，称为同学没毛病) 就提交了一个[CodeLab Adapter插件](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v2/extension_yeelight.py)来驱动Yeelight灯泡, 目前依然可用。

第三部分是`Dynamicland / Realtalk`, 这是是目前正在做的工作, 我们年初去奥克兰拜访了Dynamicland，拿到他们今年的一些规划，他们将在今年离开实验室。接入`Dynamicland / Realtalk`的原因是致力于构建下一代maker spaces -- [Seeing Spaces](https://vimeo.com/97903574)。目前`Dynamicland / Realtalk`的源码只在他们奥克兰的工作室里开放。我们按照他们的想法在做一些原型:

以下是受`Dynamicland / Realtalk`启发，构建的一些原型。


### 重力效应
<video width="80%" src="https://adapter.codelab.club/video/%E9%87%8D%E5%8A%9B%E6%95%88%E5%BA%94.mp4" controls="controls"></video>

### 拍案惊球
<video width="40%" src="https://adapter.codelab.club/video/%E6%8B%8D%E6%A1%88%E6%83%8A%E7%90%83.mp4" controls="controls"></video>

### body programming
<video width="80%" src="https://adapter.codelab.club/video/body_programming.mp4" controls="controls"></video>

### 一场烟火
<video width="80%" src="https://adapter.codelab.club/video/一场烟火.mp4" controls="controls"></video>

### 探索二进制
<video width="80%" src="https://adapter.codelab.club/video/二进制.mp4" controls="controls"></video>

### Seeing Spaces
<video width="80%" src="https://adapter.codelab.club/video/1576905372587643.mp4" controls="controls"></video>

### 增强Scratch游戏
<video width="40%" src="https://adapter.codelab.club/video/toio泡泡龙.mp4" controls="controls"></video>

### Teachable Machine
<video width="80%" src="https://adapter.codelab.club/video/tm_scratch_dy.mp4" controls="controls"></video>

# 规划
这些项目引起许多人的兴趣，之前在邮件中，我提到限于精力我们无法短期内构建完备的文档，未来会陆续开放出具体实施细节。现在就是邮件里提到的那个未来。

我们从本周开始，将构建视频和文档，帮助大家去复现前边这些的有趣的项目，让爱好者们能够在家里/学校先玩起来社区版Neverland，一旦起步，它们就很容易进一步组合、改编，编程将变得充满趣味。

如果你是企业负责人，或校方领导，或不懂技术的家长，希望得到完整的服务，而不是爱好者的技术文档，可以看文末的商业版本。

此外， 我们也将在近期(计划是这周)对外发布CodeLab开放社区，它兼容于Scratch官方社区，结合[CodeLab Insight](https://www.codelab.club/blog/codelab-insight-alpha/)数据可视化工具，我们将Scratch全球数千万项目中，为大家精选最有趣又适合入门的。

这个社区同时兼容CodeLab Adapter和Scratch Link，这意味着它有无限连接能力。

我们将在线上分享我们之前做过的这些有趣创作，大家可以轻松基于它们去remix和分享，我们到时在上边交流：）

# 社区版 与 商业版本
提到社区版，对应的自然是`商业版本`。

开源社区似乎对`商业`带着某种抵触情绪。 <!--觉得他们无非是一群自己也不编程的人，做着一些自己都不吃的狗粮，靠铺天盖地的广告贩卖焦虑和意淫，卖给一群缺乏想象力和辨识能力的人。-->

当然，编程教育里，有不少商业做的不走心。但是，我们依然看到[adafruit](https://www.adafruit.com/)、[toio](https://toio.io/)、[cozmo](https://anki.com/en-us/cozmo.html)这些伟大的商业项目。

>  简单的事情应该简单, 困难的事情应该可能 -- Alan kay

Alan kay对Apple产品的吐槽是:

>  这些产品让简单的事情确实简单, 困难的事情变得不再可能

商业软/硬件，似乎都有类似问题，通过封闭体系控制体验，同时也丧失灵活性。Alan Kay说计算机革命并没有到来，而不是已经结束。

完全的自由度和灵活性，肯定是在开放社区中。可问题是，它通常也意味着，简单的事情在不太简单。我当然是开源拥趸，但这些问题我们不能视而不见。关于这个话题，[Hakcer News](https://news.ycombinator.com/)时常有对开源项目很好的吐槽。

我们也与合作机构一起推出了Neverland的商业版本 -- 「创造乐园」解决方案。

我们希望让简单的事情保持简单，让那些非技术发烧友，也能轻松构建起Neverland这样的魔法世界，沉静式地去编程和创造。至于那些真正复杂的问题 -- 灵活的连接能力，强大的扩展能力...我们也力图在商业版本中保留它们，因为这是一个用于创造的工具, 它不只是消费品，我们希望它的使用者成为表达者和创造者。 这是我们认为编程教育的意义。在这点上，并不会妥协。

如果你需要更完善的管理和教学功能，那么商业方案或许会是你的更优的选择，「创造乐园」解决方案将很快面世。由CodeLab与`Elite Longan`团队一同推出。

---

接下来关于社区版Neverland文档的更新，我们会以周为单位，定期发布在CodeLab博客里。

有任何想法和建议，也欢迎[与我们联系](https://www.codelab.club/about/).
---
Date: 2019-11-13
title: "Scratch项目解析器"
Slug: Scratch-sb3-parser
aliases: ["scratch-sb3-parser"]
tags: ["tools","Scratch","Python"]
categories: ["少儿编程"]
---

<img class="img-responsive" src="/img/scratch_sb3_Pong_Starter_python.png" />

# Scratch增强计划
此前在[Scratch增强计划](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/enhance-scratch3/)中提到:

>  由于需要解析sb3文件，所以会顺手打造一些通用的小工具...简单写了一个脚本, 允许用户解压sb3文件，本地编辑之后，再重新生成sb3，之后在scratch3.0编辑器中依然能加载它. 这有什么用呢？还挺有用的，比如说我目前的一个用例: 之前保存的一些sb3项目在新的scratch3.0编辑器中打不开了(可能是新的平台不存在旧的extension)，我通过移除sb3中对应的extension block就可以重新加载项目...脚本源码和使用方法在这里:[sb3_compress.py](https://gist.github.com/wwj718/cd2447e68409a0f36141f4d1d7698fd9)

<!--more-->

# 解析Scratch项目
要实现[Scratch增强计划](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/enhance-scratch3/)提到的计划，对Scratch项目的解析是基础工作，而解析工作的基础又是以理解Scratch项目的结构为基础，我在前文里提到

>  我希望让新的vm(Virtual Machine)能够解释运行sb3文件。sb3文件结构的设计是很优秀的,我在[Scratch3技术分析之项目内部数据(第6篇）](https://blog.just4fun.site/Scratch3_project_json_analysis_6.html)做了阐述。

原本准备使用[Pharo(Smalltalk)](https://pharo.org/)来做实现它，Pharo中有一些工具很适合做此项工作([PetitParser](https://github.com/moosetechnology/PetitParser)、[NeoJSON](https://github.com/svenvc/NeoJSON)、[Moose](https://moosetechnology.org/)、[Glamorous Toolkit](https://gtoolkit.com/))

但近来事情特多，刚参加完Maker Faire，下个月还准备与国家图书馆一起做一个活动。就暂时鸽了这件事。

# 社区同伴
Scratch Team很早就发布了一个项目叫[scratch-parser](https://github.com/LLK/scratch-parser)，目标是也是解析Scratch项目，后来似乎也鸽了。


今天偶然发现[apple502j](https://github.com/apple502j)在这块做了不少工作:[apple502j/sb3](https://github.com/apple502j/sb3), 于是我准备在[apple502j](https://github.com/apple502j)上前进，之后有时间再迁移到Pharo(我看中Pharo在数据分析上的便利性，当然，Python/Jupyter也很不错)，换一门语言是很快的，解析的业务代码却是耗时的，可喜的是，apple502j已经为我们做了很多辛苦的工作。

[apple502j](https://github.com/apple502j)是个Scratcher, Ta在Scratch社区的账号是[apple502j](https://scratch.mit.edu/users/apple502j/), apple502j除了活跃于Scratch社区，在github上也积极帮助scratch团队和社区开发者解决问题。

# 项目一览
我们来简单看看[apple502j/sb3](https://github.com/apple502j/sb3)项目。

## 安装
```bash
pip3 install sb3
```

## 使用

### 彩蛋

sb3如何使用呢?

[apple502j](https://github.com/apple502j)在使用说明里调皮了一下:

>  All people, cats and other cute animals with Python 3.6 or above can use this library. If you are not cute but want to use this, try sb3.cute().

你需要足够可爱才能使用它，如果你不够可爱怎么办呢？好说，试着运行一下`sb3.cute()`

很有scratcher精神！

### 正式使用

我们对[Pong_Starter.sb3](https://adapter.codelab.club/sb3/Pong_Starter.sb3)进行一些测试, 你可以在[CodeLab Scratch打开它](https://scratch3v3.codelab.club/?sb3url=https://adapter.codelab.club/sb3/Pong_Starter.sb3)。

![](/img/scratch_Pong_Starter.png)

让我们在Jupyter中对项目做一些探索:

![](/img/scratch_sb3_Pong_Starter_python.png)

## 分析有插件的项目
接下来让我们来分析一个带有CodeLab自定义插件的项目:

[microbit_乐器.sb3](https://scratch3v3.codelab.club/?sb3url=https://adapter.codelab.club/sb3/microbit_%E4%B9%90%E5%99%A8.sb3)

<img src="/img/sb3_python_extensions.png" width=600 />

# 前进
有了这个基础项目，我们未来的数据可视化工作以及评估用户的计算思维(computational thinking)会容易许多。

>  做新的解释器过程中，我们需要深入到scratch程序的所有细节里，这就逼着我们做出类似静态分析器的东西，我们自然会理解用户用到的所有程序元素，我们可以据此评估他在程序中展现的计算思维(computational thinking)。评估的教育框架会采用Scratch之父(Mitchel Resnick)早年的论文。  -- [Scratch增强计划](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/enhance-scratch3/)

# 参考
*  [apple502j/sb3](https://github.com/apple502j/sb3)
*  [phosphorus](https://phosphorus.github.io/):runs your Scratch projects really fast by compiling them to JavaScript.
*  [htmlifier](https://sheeptester.github.io/words-go-here/htmlifier/):packages your Scratch project into a single HTML file
*  [scratch-parser](https://github.com/LLK/scratch-parser)
*  [scratch-analysis](https://github.com/LLK/scratch-analysis):Analysis tool for summarizing the structure, composition, and complexity of Scratch programs.
*  [apple502j](https://scratch.mit.edu/users/apple502j/)
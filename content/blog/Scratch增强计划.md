---
Date: 2019-11-13
title: "Scratch增强计划"
Slug: Enhance-Scratch3
aliases: ["/Enhance-Scratch3","/Enhance-Scratch3.html"]
tags: ["scratch"]
categories: ["少儿编程"]
author: 种瓜
---

<img class="img-responsive" src="/img/create_2767ae26.png" />


>  There are many ways to live your life. That's may be the most important thing you can realize in your life is that every aspect of your life is a choice...  
You can choose to accept the world as it is but you don't have to.  
If there is something in the world you feel the wrong and you have a vision for what a better world could be, you can find your guiding principle and you can fight for a cause.  
So after the talk I'd like you to take a little time and think about what matters to you？what you believe in？ what you might fight for？ -- Bret Victor《Inventing on Principle》

<!--more-->


# 前言
上周六，我一直在看[Bret Victor](http://worrydream.com/)的博客，他的工作给我极大的震撼，几乎是叹为观止。


看了他的演讲和文章，夜里和朋友聊了很久，他让我们觉得自己生活在原始时代，刀耕火种，难以忍受。周日下午走街串巷，漫无目的的徒步，一直在想[Bret Victor](http://worrydream.com/)说的一些东西，下午的阳光很好，走在广州的老街道，树木盈抱，墙面斑驳，傍晚时候，一切看起来都像90年代，从[Bret Victor](http://worrydream.com/)的演讲回到现实，好像穿越到了过去，周围的一切都显得那么原始。

关于什么是好的编程环境，什么是好的创造工具，我从前对此一无所知，觉得目前手头的工具基本够用。[Bret Victor](http://worrydream.com/)使我相信，我完全不懂编程是什么。

# Smalltalk
一直没有痛下决心将[Smalltalk](https://zh.wikipedia.org/zh-hans/Smalltalk)作为我的主要语言。此前玩了段时间[squeak](https://zh.wikipedia.org/zh-hans/Squeak)(Smalltalk的一个方言)，在上边很轻松写出了scratch的原型，[scratch的第一代](https://github.com/LLK/Scratch_1.4)就是用[squeak](https://zh.wikipedia.org/zh-hans/Squeak)写的，scratch与创造有关的核心设计似乎都来自[squeak](https://zh.wikipedia.org/zh-hans/Squeak)。正如scratch之父所言scratch的主要创造是社区。这是很中肯的描述。

之后又玩了段时间[Etoys](https://en.wikipedia.org/wiki/Etoys_(programming_language))。

最近有一搭没一搭地使用[Pharo](https://pharo.org/) ，[Pharo](https://pharo.org/)是现代Smalltalk方言。

[Bret Victor](http://worrydream.com/)给了我最后一根稻草，让我确信切换到[Smalltalk](https://zh.wikipedia.org/zh-hans/Smalltalk)是极为重要的一件事，它是绝佳的创造工具。

#   New Scratch3.0 Virtual Machine
我准备在[Pharo](https://pharo.org/)中实现Scratch3.0 Virtual Machine，把scratch重新带回Smalltalk。它既作为我驱动自己学习[Pharo](https://pharo.org/)的项目，又作为探索scratch未来可能性的尝试。尽管最终可能实现出JavaScript版本(考虑到对用户友好)，但正如[Bret Victor](http://worrydream.com/)所言，JavaScript和processing都不是好的语言，它并不适合用于探索。今天有许多公司，用JavaScript(Blockly)去重新抄一遍scratch，除了换一个UI，源代码更为草率，扩展性更糟之外，在编程和创造性这件事上，几乎没有任何改进（事实上基本都是倒退）。有那么多有意思的事情值得做，换一个皮肤的事，竟吸引了那么多公司动则千万的投入。

一旦在[Pharo](https://pharo.org/)中实现了Scratch的解释器，我们就可以轻松使用[Bret Victor](http://worrydream.com/)的创造原则去增强它。

我希望让新的vm(Virtual Machine)能够解释运行sb3文件。sb3文件结构的设计是很优秀的,我在[Scratch3技术分析之项目内部数据(第6篇）](https://blog.just4fun.site/Scratch3_project_json_analysis_6.html)做了阐述。

# 副产品
在实现这个目标的途中可能会顺便得到一些有趣的副产品，有些可能是目前Scratch3.0的用户和开发者所关心的，我大致列一些，目前能想到的一些有趣副产品包括:

### 1.将scratch项目导出为本地应用

scratch社区的用户似乎一直有一个需求: 将scratch项目导出为本地应用(exe/app). 要做到这点，按目前scratch3.0的架构也能做到，诸如直接导出一个electron应用，不过这实在有点笨重。

新的解释器接受sb3文件作为输入，然后解释运行它，所以我们可以做得非常精简。

### 2.离线运行scratch3.0项目

Scratch3.0目前运行在浏览器中，总是需要GUI支持，如果导出的程序并不是视觉动画，例如程序用来将家庭自动化(我在[这里展示了很多例子](https://codelab-adapter-docs.codelab.club/user_guide/gallery/))，我们能否让它离线运行，不用总开着浏览器，让它跑在云端，或跑在没有屏幕的树莓派上。


### 3.评估用户的计算思维(computational thinking)

做新的解释器过程中，我们需要深入到scratch程序的所有细节里，这就逼着我们做出类似静态分析器的东西，我们自然会理解用户用到的所有程序元素，我们可以据此评估他在程序中展现的计算思维(computational thinking)。评估的教育框架会采用Scratch之父(Mitchel Resnick)早年的论文。

### 4.一些通用的sb3文件处理工具 

由于需要解析sb3文件，所以会顺手打造一些通用的小工具。

今天就简单写了一个脚本, 允许用户解压sb3文件，本地编辑之后，再重新生成sb3，之后在scratch3.0编辑器中依然能加载它. 这有什么用呢？还挺有用的，比如说我目前的一个用例: 之前保存的一些sb3项目在新的scratch3.0编辑器中打不开了(可能是新的平台不存在旧的extension)，我通过移除sb3中对应的extension block就可以重新加载项目。

脚本源码和使用方法在这里:[sb3_compress.py](https://gist.github.com/wwj718/cd2447e68409a0f36141f4d1d7698fd9)


# 关于[codelab-adapter](https://codelab-adapter-docs.codelab.club/)
新的虚拟机依然能够与[codelab-adapter](https://codelab-adapter-docs.codelab.club/)通信，我目前计划采用ZeroMQ来实现。事实上[codelab-adapter](https://codelab-adapter-docs.codelab.club/)会采用越来越多[Bret Victor](http://worrydream.com/)建议的设计原则。

# 进展与笔记
近期，我刚开始着手做这件事，[对项目数据的分析](https://blog.just4fun.site/Scratch3_project_json_analysis_6.html)已经完成了。将项目保存为本地文件(sb3)由[以下代码](https://github.com/LLK/scratch-vm/blob/98b92be2d74ba868d876feaf00a02ceb11dbf311/src/virtual-machine.js#L356)驱动:

```js
    /**
     * @returns {string} Project in a Scratch 3.0 JSON representation.
     */
    saveProjectSb3 () {
        const soundDescs = serializeSounds(this.runtime);
        const costumeDescs = serializeCostumes(this.runtime);
        const projectJson = this.toJSON();

        // TODO want to eventually move zip creation out of here, and perhaps
        // into scratch-storage
        const zip = new JSZip();

        // Put everything in a zip file
        zip.file('project.json', projectJson);
        this._addFileDescsToZip(soundDescs.concat(costumeDescs), zip);

        return zip.generateAsync({
            type: 'blob',
            compression: 'DEFLATE',
            compressionOptions: {
                level: 6 // Tradeoff between best speed (1) and best compression (9)
            }
        });
    }

    _addFileDescsToZip (fileDescs, zip) {
        for (let i = 0; i < fileDescs.length; i++) {
            const currFileDesc = fileDescs[i];
            zip.file(currFileDesc.fileName, currFileDesc.fileContent);
        }
    }
```

由此可以看出项目的数据是扁平的。这个分析帮助我们构建了小工具:[sb3_compress.py](https://gist.github.com/wwj718/cd2447e68409a0f36141f4d1d7698fd9)。

春节假期将近，在假期里与家人朋友小聚之余，如果能抽出时间，我就到阳台晒晒太阳，熟悉熟悉[Pharo](https://pharo.org/)，并顺手构建早期的原型。

# 参考
*  [Bret Victor](http://worrydream.com/)
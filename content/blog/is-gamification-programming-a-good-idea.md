---
title: "游戏化编程是个好主意吗？"
author: 种瓜
date: 2019-06-25
tags: ["programming"]
---

<img class="img-responsive" src="http://wwj-fig-bed.just4fun.site/game_code_d0e83807.png" />

>  你把一粒石子投入池中，宇宙就不完全是它先前那样子。 -- 毛姆《刀锋》

# 前言
随着`互联网+`、`AI+`、`5G+`这些词汇变得时髦, 加上政策导向, 编程教育变得炙手可热。在这些时髦词汇中，`游戏化编程`常被提及。

前天晚上和@曾老师(CodeLab理事之一)聊到`游戏化编程`这个话题，聊到很多有趣的观点，<!--明早@曾老师有个做游戏的师弟对这个话题感兴趣（国内最大的游戏公司之一），准备来Neverland交流，也计划用于明天的沟通--> 本文对此做一番梳理。

<!--more-->

什么是`游戏化编程`呢？

# 游戏化编程
今天的`游戏化编程`, 大体上指的是一种编程教育风格，它们是一些伪装成游戏的编程练习，随着学习者闯过一个个关卡，Ta将拿到许多小星星作为奖励(就像课堂上的小红花)，学习者如果通过了所有预设的关卡，就认为Ta掌握所需的编程知识。举例说明的话，可以想到[code.org](https://code.org/)、[codecombat](https://codecombat.com/)...

听起来颇像学校教育的线上版本，知识被拆分为课本里的一个个章节（关卡），每个章节设置一些考题，待学生通过这些考核，收集到了足够多的小红花，每次考试后打上了A、B、C等级的标签，我们就可以宣布Ta是不是掌握了相应知识。

# 有问题吗？
听起来没毛病呀。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)偏偏在《终身幼儿园》里站出来说: `我不赞同`。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)从可汗(Sal Khan)(可汗学院的创始人)的在TED上的演说讲起。

在演说上，可汗回答比尔盖茨的提问时说, 

>  可汗学院引入了一连串的游戏机制，学习者可在网站中获得各类徽章，之后还可能有分地区的排行榜。

看架势，哪天出一个国服三角函数第一也是可以期待的.

可汗继续说道:

>  靠徽章和积分这项措施，你可以控制成千上万的学生奔往你所预设的方向。

为了成为头号玩家，兄弟们还不快上。

人们笃信教育游戏化的效果，既然孩童在玩游戏时，受到分数和徽章的激励，同样的方法为何不用在教育上呢？如此一来，他们不是更有学习的动力吗？就像玩游戏时打怪刷积分那样。

什么？你竟然对此表示怀疑？难道你忘了在多少个夜晚，顶着黑眼圈将王昭君(《王者荣耀》游戏里的角色)的级别从青铜刷到黄金吗？

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)继续说到：

>  游戏化作为传统的教育智慧，被广泛采用着。在教室里，孩童们会得到贴纸和星星作为奖励;在每个学期，他们会得到分数和奖状作为奖励；在家庭里，参与今日的家务，将赢得周六的公园野餐作为奖励。行为主义的先驱们已经证明，提供奖赏以鼓励期望的行为具有很大的威力。他们的理论对整个20世纪的学校教室和工作场所的管理策略产生了深远影响。

我们在前头看到游戏化编程与学校教育的相似性便源于行为主义者的上述理论。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)接下来开始了他的`but`部分,他提到, 近期的一些研究，让人们开始质疑行为主义方法的长期价值。特别是在创意活动上。不可否认，奖赏可用来激励人们在短期内改变行为，但长期效果却很不一样。

在《动机:单纯的力量》一书中，品克(Daniel Pink) 这样形容两者的差异:

>  奖赏就像注入咖啡因能让你再工作好几个小时一样，可造成短期的惊人效果。但这样的效果会递减，而且更糟的是，这可能会降低一个人长期持续某个项目的动机。

品克讨论了好几项研究，它们都显示出利用奖赏做为刺激的限制。在德西(Edward Deci)进行的一项研究中 ，受试对象是大学生，他们必须组合积木以解开谜题，德西将学生分成2组，一组学生每完成一个谜题就会拿到钱 ，另一组学生则没有奖金。与大家预期一致，比起没有钱领的学生，有钱领的学生愿意花更多的时间解题。隔天，学生受邀回来继续解题，但这次没有任何学生领到钱。结果呢？比起第一次没有钱领的学生，先前领到钱的学生比较不愿意花时间解题；换句话说，第一天领到钱的学生比完全没有领到钱的学生还不积极。

另一项由乐博( Mark Lepper)和同事所进行的研究，对象是幼儿园儿童而不是大学生，奖赏是证书而不是现金，结果也相近。部分接受测试的儿童在纸上画图后拿到「优秀选手」的证书。两周后，他们邀请儿童画更多的图，但这次不再提供任何证书。结果发现第一次拿到证书的学生，在第二次的测试里显得比较没兴趣，画图的时间也比较短。牵涉到创意活动时，奖赏会更加没有效果。在一些研究人员邀请受试对象解决需要创意思考的问题时，如果他们解决之后可以拿到钱，受试者解题的时间会比较久。似乎奖赏或奖金的诱感会窄化人们的关往焦点。限制他们的创意。同样的，创意研究人员阿玛贝利(Teresa Amabile)分析了艺术家的绘画和雕塑作品，她发现当艺术家可以获得创作酬务时，他们的作品会比较没有创意，即使创作内容没有受限也是如此。

于是[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)下结论说:

>  如果你的目标是要训练某人在特定的时间执行特定的任务，那么游戏化会是有效的策略。把任务转化成游戏，提供积分或其他诱惑做为奖赏，人们学习任务的速度会更快，也更有效率。但如果你的目标是要帮助人们发展成为创意思考者和终身学习者，那么你会需要不同的策略。与其提供外在酬赏，更好的策略是利用人们的内在动机，也就是人们对于自己觉得有趣或满意的问题/项目，努力想解决的那股欲望。

### 游戏招你惹你了？
[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)不是[杨永信](https://zh.wikipedia.org/zh-hans/%E6%9D%A8%E6%B0%B8%E4%BF%A1)，并不认为游戏有原罪，对游戏也没有什么偏见。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)之所以反对教育游戏化，并不是反对游戏本身，他反对的是今天的教育游戏化项目的设计中，奖励机制的滥用(过去的行为主义支持这种做法)。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)并不反对游戏精神，在《终身幼儿园》121页，[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)开始谈论`可贵的游戏精神`。引述了一堆关于游戏的有趣讨论:

*  >  我们不是因为年老而停止游戏，而是因为我们停止了游戏所以变老。 -- 萧伯纳

*  >  游戏就是孩子的工作。  --让.皮亚杰

*  >  和一个人玩一个小时对他的了解胜过和他一年的交谈。 --柏拉图

*  >  玩具和游戏是重要思想到来的前奏。 -- 查尔斯.埃姆斯

*  >  游戏比任何其他活动都更能使孩子掌控外部世界。 --布鲁诺.贝特尔海姆

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)继续说到：

>  游戏是好奇心、想象力和实验的结合。

# 怀疑论者
[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)对教育游戏化(过关给星星/100分给小红花)的批评，愤慨如怀疑论者。

教育游戏化的拥护者会不服道:  “当一个怀疑论者总是容易的，他只要顾着破坏和攻击现有秩序就行，但问题是如何给出更好的方案，如何成为一个建设者”

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)和他的老师[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)在建设性方面远远好于破坏性。

实际上，我一向认为，对现有不合理秩序的攻击，和建设本身一样重要。

在给出[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)和[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)的建设性意见之前，我们先来试着回答以下几个问题:

*  游戏是什么？
*  编程是什么？
*  他们是否可能结合？如果可能，该如何结合？

# 游戏是什么？
要为游戏下个定义可真不容易。

[维特根斯坦](https://zh.wikipedia.org/zh-cn/%E8%B7%AF%E5%BE%B7%E7%BB%B4%E5%B8%8C%C2%B7%E7%BB%B4%E7%89%B9%E6%A0%B9%E6%96%AF%E5%9D%A6)可能是第一个试图为游戏下定义的哲学家（我是他的铁杆粉），他在后半生的主要著作《哲学研究》里写道:

>  看一看……我们叫作游戏的那些活动。我是指下棋、玩牌、球赛、奥林匹克竞技等等。它们共有的东西是什么？——不要说：一定有某种它们共有的东西，否则它们就不会都叫作“游戏”，而是要观察并确认一下是否有某种它们都共有的东西——因为如果你观察它们，你不会看到某种它们共有的东西，而只看到一些相似、一些关系以及整个一系列相似和关系。……这种考察的结果是：我们看到一个由部分重合和交叉的相似性组成的复杂网络……我想不到有比“家族类似”更能刻画这类相似性的表达式了；对于一个家族成员之间的各种不同的类似性来说：体格、面貌、眼睛颜色、步态、脾气等等等等都以同样方式部分重合和交叉着。——我要说，“游戏”构成了一个家族。（《哲学研究》,P66—67）

维特根斯坦一开始提出游戏的几个要素，像是玩耍、规则及竞争，后来发现这些都无法适当定义游戏。

于是在维特根斯坦那儿，`游戏`被他作为例子来论述`语言像游戏一样并没有可用一种整体理论来发现和阐明的单一本质`。

我完全赞同他对游戏一词的阐述，游戏是一族东西，精确的定义是不可能的。

但历史上依然有很多人试图对游戏下定义，许多非常有趣。

比如说。Bernard Suits对游戏的定义是:

>  所谓游戏，即是自愿接受挑战去面对非必要的障碍。

托马斯·霍尔卡对此表示举双手双脚赞成。

在2008年获颁雨果奖最佳互动电玩游戏奖的Kevin Maroney曾说：

>  游戏是一种具有目标和结构的娱乐形式。

在此，也顺便提一下[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)对游戏本质的看法，他认为游戏的本质是`玩儿心`。

相比于游戏, 电子游戏的定义倒很清晰，按维基百科的说法, 电子游戏是:

>  基于计算机的计算能力，按照一定的逻辑模式（计算序列）对人类假想行为的模拟（或抽象）的一种交互程序。

非常精妙的定义！在这个定义中，游戏是一种人机交互程序。图形界面似乎也完全符合游戏的定义，文件和文件夹被假想在`桌面`上，旁边还有`垃圾桶`！

这也符合我们对60年代计算机先驱的印象，他们开创了大多数今天人们使用的人机交互的方式，他们给外界的印象却是一种在玩。Alan Kay现在已经80岁了，看起来还是继续在做各种儿童玩具，乐此不疲。

# 编程是什么？
`编程是什么？`这个问题绝不会比`游戏是什么？`更好回答。鲁莽地回答这个问题的人，就等着在知乎上被黑吧。

关于这个问题，我最喜欢的两个相关回答分别来自[《SICP》(计算机程序的构造和解释)](https://zh.wikipedia.org/zh-cn/%E8%AE%A1%E7%AE%97%E6%9C%BA%E7%A8%8B%E5%BA%8F%E7%9A%84%E6%9E%84%E9%80%A0%E5%92%8C%E8%A7%A3%E9%87%8A)和[《Mindstorms》](https://book.douban.com/subject/30418117/)。

《SICP》在第一版序言里说:

>  我们希望建立起一种看法:一个计算机语言并不仅仅是让计算机去执行操作的一种方式，更重要的，它是一种表述有关方法学的思想的新颖的形式化媒介。因此，程序必须写得能够供人们阅读，偶尔地去供计算机执行。其次，我们相信，在这层次的课程里，最基本的材料并不是特定程序设计语言的语法，不是有效计算某种功能的巧妙算法，也不是算法的数学分析或者计算的本质基础，而是一些能够用于控制大型软件系统的智力复杂性的技术。

《SICP》里又说道:

>  计算机科学并不是一门科学，而且其重要性和计算机也并无太大的关系。计算机革命是有关我们如何去思考的方式以及我们如何去表达自己的思考的一个革命。

[《Mindstorms》](https://book.douban.com/subject/30418117/)对编程的看法是:

>  所谓编程，不就是对计算机讲一种它能够“听得懂”的语言吗？而学习一种语言，不正是孩子们最擅长的事情之一吗？...当孩子对计算机进行编程，通过教计算机怎么思考，孩子们开始探索自己的思考方式。这种体验颇不寻常，甚至很多成年人也很难拥有--思考关于思考的问题，把孩子变成发生认识论的专家。

在《SICP》和[《Mindstorms》](https://book.douban.com/subject/30418117/)对编程和计算机的阐述中，我们看到编程是一种增强人类认知能力的工具。

当然他们所说的编程和通常意义上的编程并没有什么关系。通常意义上的编程教育（以及今天大多数的编程教育）让你专注在记忆语法、记忆算法以及闯关得分。这只是传统学校数学教育的21世纪翻版。你不大可能从中学到多于你从今天的传统科目里学到的东西。

正如[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)在[《Mindstorms》](https://book.douban.com/subject/30418117/)中说的:

>  我所憧憬的不是完善现有秩序；我的想法和现有的制度根本是背道而驰的。

# 游戏和编程是否可能结合
在上边讨论中，我们看到游戏和编程两者的定义和边界都含糊又广阔。看不出它们有任何相克或冲突的地方。

既然没有明显冲突，那么两者该如何结合呢？

# 如何结合
作为建设者和建构主义者的[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)和[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)都给出了精彩的回答, 我相信他们的回答也是迄今为止最为精彩的回答之一。


### 构建新大陆
[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)认为二者的结合是构建`land`--一种真实的学习氛围，就像呆在法国学习法语，而不是在美国学校课堂里接受非自然的外语培训。

>  成功的学习模式是一个孩子学习说话的方式，那我们就应该致力于营造一个没有刻意组织的学习氛围。所谓的课堂，在我看来不过是一个人为而且低效的学习环境;它的存在完全是因为非正式场合不能解决几个基本知识领域的教育问题:写作，语法，或者是学校版数学。我认为，计算机的存在能够改变这个局面，它可以改变课堂外的学习环境；

[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)自己构建了Logo这个Mathland，他的追随者Alan Kay构建了的[etoys](http://www.squeakland.org)(我有为它写过[一篇文章](https://blog.just4fun.site/Etoys-learning-note.html))、Bret构建了[dynamicland](https://dynamicland.org/)(参考我此前的翻译:["下一件大事"是一个房间](https://blog.just4fun.site/the-next-big-thing-is-a-room.html))，CodeLab则构建了[Neverland](https://blog.just4fun.site/about-codelab-club.html#neverland)。

[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)留下的教诲是，在编程教育中放弃课堂这种知识传递模式（100分奖励小红花、记知识点通关打怪），去构建更真实的`land`, 在这片大陆上，与计算机对话应该是一种很自然的事情，就像在法国说法语。相比之下，今天的编程游戏是非常做作和扭捏的，非常接近于约翰.杜威攻击的学校教育。

如果你乐意，可以到[Dynamicland](https://dynamicland.org/)或[Neverland](https://blog.just4fun.site/about-codelab-club.html#neverland)(我们在广州)体验land与课堂的区别。

### 构建游乐场
[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)认为游戏精神和编程结合的产物是`playground`

可以看出[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)深受[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)影响，`playground`可以视为谦虚版的`land`，它强调开放性。

[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)指出编程与游戏精神结合，存在两种模式，其一是`婴儿围栏`，其二是`游乐场`。

婴儿围栏是一个限制性的环境。在真实的婴儿围栏中，孩子的行动空间有限，探索也十分有限。他们能在围栏里玩玩具，但范围有限。婴儿围栏是一种隐喻，比喻孩子缺乏实验的自由，缺乏探索的自主权，缺乏开发创造性冒险的机会。

游乐场则给孩子提供更多的空间去移动、探索、实验和协作。如果你在游乐场里观察孩子，一定会发现他们在玩着自己的游戏。在这个过程中，孩子才会成长为一个创造性思考者。对于游乐场式的游戏来说，重要的是让孩子自己决定制作什么，以及如何制作。

其中Minecraft（《我的世界》）和Scratch都是游乐场的典型代表(当然etoys和game builder也是)。

# 现代版的land和playground
我认同[Seymour Papert](https://zh.wikipedia.org/zh-hans/%E8%A5%BF%E6%91%A9%E7%88%BE%C2%B7%E6%B4%BE%E6%99%AE%E7%89%B9)和[Mitchel Resnick](https://en.wikipedia.org/wiki/Mitchel_Resnick)的所有论点，事实上，关于编程和教育，我的所有观点都从他们那儿生发而来。

但我现在想做进一步的演绎: 随着物联网和AI的崛起（性能的提升、成本的下降），我们可以构建更加激动人心的land和playground，在现实中构建！我们不在计算机屏幕中模拟，而是将计算叠加到现实中来。将现实作为一个`真实`的创造环境。

目前[Dynamicland](https://dynamicland.org)和[CodeLab Neverland](http://adapter.codelab.club)都是这个方向的探索者，[toio](https://www.sony.net/SonyInfo/design/stories/toio/)最近也正在加入这个行列。

对这个话题有更多兴趣的朋友，欢迎阅读: [空间编程、物理计算与密室逃脱](https://blog.just4fun.site/escape-room.html)。

<!--
# 游戏
不诚实 和课堂相似 
real playing

需要我们重新看待游戏 但肯定不知我们今天使用游戏一次所指的东西


流行的和好的没有 对维护现状 这类论调已经太多了 

Dynamicland岌岌可危。

adafruit的崛起，toio的出现，




游戏的戏剧性 注意力
     冲突

不如改造现实
    计算机的可塑性


是一种戏剧性的活动
        人性的很多热情被激发

# 代码大全
第二章 用隐喻来更充分理解软件开发


是一种 "奖品迷" 

# 写作
*  如何恰当复述他们观点
*  如何论点
*  将本文视为复述和表达自己思想的文章
*  如何组织材料
*  结论 
    利用现实作为舞台 游戏
    回归广义游戏
*  编程是什么 游戏是什么 结合是否合适
    *  编程是什么 alan kay
    *  计算思维
    *  sicp
    *  人机交互

我们关注增强人类 ->  mindstorms


我的世界 gamebuild 开放性 
塞尔达 化学系统

推论 现实 作为计算引擎

基于它 制作内容。承载其他学科

现实作为计算引擎

### 现在
目前据我所知

*  dynamicland
*  toio
*  neverland
-->




# 参考
*  [Mindstorms](https://book.douban.com/subject/30418117/)
*  [代码战争](https://codecombat.com/)
*  [终身幼儿园](https://book.douban.com/subject/30285992/)
*  [路德维希·维特根斯坦](https://zh.wikipedia.org/zh-cn/%E8%B7%AF%E5%BE%B7%E7%BB%B4%E5%B8%8C%C2%B7%E7%BB%B4%E7%89%B9%E6%A0%B9%E6%96%AF%E5%9D%A6)
*  [牛津通识读本:维特根斯坦](https://book.douban.com/subject/24529676/)
*  [哲学研究](https://book.douban.com/subject/1315184/)
*  [代码大全](https://book.douban.com/subject/1477390/)
*  [wikipedia 游戏](https://zh.wikipedia.org/zh/%E6%B8%B8%E6%88%8F)
*  [wikipedia 电子游戏](https://zh.wikipedia.org/zh/%E7%94%B5%E5%AD%90%E6%B8%B8%E6%88%8F)
*  [人机交互](https://zh.wikipedia.org/zh-cn/%E4%BA%BA%E6%9C%BA%E4%BA%A4%E4%BA%92)
*  [空间编程、物理计算与密室逃脱](https://blog.just4fun.site/escape-room.html)
*  [教育游戏化](https://mp.weixin.qq.com/s/fE7K92EoowtRA7uqPzoB7Q)
*  [Etoys学习笔记: 与Scratch互操作](https://blog.just4fun.site/Etoys-learning-note.html)
*  [Mathland - Seymour Papert](https://www.youtube.com/watch?v=UgE05-3SToc)
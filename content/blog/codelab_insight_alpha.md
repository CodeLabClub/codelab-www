---
Date: 2020-02-19
title: "CodeLab Insight 发布 Alpha 版"
Slug: "CodeLab-Insight-alpha"
tags: ["codelab"]
categories: ["codelab"]
author: "种瓜"
---

<img class="img-responsive" src="/img/codelab_insight2.png" />


# 介绍
`CodeLab Insight` 是 CodeLab 推出的 `数据分析/可视化探索` 服务。

服务于 `少儿编程/STEM教育` 领域的 教育者、学习者、研究员、运营人员 和 开发者。 当然也服务于我们自己(CodeLab的成员)，以及CodeLab的合作伙伴。

旨在为他们提供从社区大规模数据中提取`洞见(insight)`和`建议`的工具和服务。

<!--more-->

# 先看 Demo
以下是我们目前开放测试的第一个Playground: `Playground 1: Explore scratch popular projects`.
 
![](/img/playground1_go.png)

图中的每一个彩色圆点均表示一个Scratch项目。

这个可视化工具可以帮助我们进行许多有趣的探索, 从几个简单例子出发:

#### 任务1: 从最流行的10,000个项目中找到人们喜欢却复杂度不高的项目用于入门教学

默认情况下，用户点赞数(`loves`)作为x轴，项目包含的积木数量(`all_blocks_count`)作为y轴。

拖动选择条，让`loves > 2000`(超过2000个点赞)。 图中在y轴底下的都是我们的目标项目（越靠近x轴，越简单），所以一眼发现了很多可选目标。

![](/img/playground1_fun_easy.png)

可以看出，我们选择的项目有`3466`人点赞；`39482`人浏览过；有`78`个项目基于它继续创作；项目引发了`1922`条评论。

在复杂度上，它只用到3个精灵，25块积木之少！此外我们可以看出项目非常年轻，上个月才创建！

如果你想试运行这个项目，在小圆点上点击`shift + click`即可打开项目主页。

如果你乐于挑战，也可以找到所有项目中最复杂的（找到y轴最上方的即可）。

![](/img/playground_fun_hard.png)

该项目由多达`25678`块积木构建，包含88个精灵。如此复杂的项目，还是有4个勇士基于它继续创作。

#### 任务2: 探索点赞数(`loves`)与收藏数(`favorites`)之间的关系
点了`favorite`之后的项目，会被收藏起来，方便日后再玩，所以`favorites`通常意味着更大的喜欢。

来看看点赞数和收藏数之间的关系。

将纵轴改选为`favorites`, 可以看到关系十分清晰，肉眼可见，几乎不必做线性拟合。大约是`4:3.2`左右的关系，虽然这和直觉大体契合(正相关)。但我们可以获得对社区成员的行为模式更量化的感觉。

![](/img/playground_favorites_loves.png)

同样的道理，可以探索点赞数(`loves`)与浏览量(`views`)之间的关系，看看人们在浏览和玩耍项目时，有多少人会顺带点个赞呢？

![](/img/playground1_loves_views.png)

不知道这个结果是不是符合你的预期。

粗略目测线性拟合的结果大约在40:1， 意味者每40个浏览者会有1人点赞，这或许和社区有大量匿名玩家有关。

更细致的处理(诸如线性拟合)可以在其他的Playground里做。

#### 任务3: 探索项目复杂度(`all_blocks_count`)与它的拷贝数`remixes`(人们基于它继续工作)之间的关系

![](/img/playground1_remixes_blocks.png)

大量的项目聚集在y轴附近(`x趋近于0`)。而被很多人拷贝的项目，包含的积木数量很少超过5000。 

太过复杂的项目，让人望而却步。这也符合直觉。如果你想创建社区成员喜欢的项目，太过庞大，可能曲高和寡，这和Github社区不大一样，Github的流行项目基本都是大型复杂项目。

我们来进一步分析，将评论数量(`comments`)映射为小圆点的尺寸大小，小圆点越大，说明引起的讨论越多。

![](/img/playground1_remix_blocks_size.png)

可以看出讨论数与复杂性的关系与前头类似，太复杂的项目，引起的讨论也少.

但图中有一个奇异的点(我们用箭头指出了)，这个项目值得点开一看。它既复杂，引起的讨论和remixes数都很多。想来有其好玩的地方。

---

可进行的探索数不胜数。 

目前`Playground 1`已经发布 [Alpha测试版](http://insight.codelab.club:18000/)，需要申请`Access token`才可访问 。

[CodeLab主页页脚](https://www.codelab.club/)也有入口:

<img src="/img/codelab_home_insight.png" width=90% />

希望`Playground 1`能够帮助到 `少儿编程/STEM教育` 领域的 教育者、学习者、研究员、运营人员 和 开发者。

其他的`Playground`暂时未对普通访客开放，我们会陆续纳入开放计划里。

# 分析对象
当前全球最大规模的少儿编程/创作`社区`是 [Scratch](https://scratch.mit.edu/):

*  49,919,098 (4991万) 分享项目
*  52,021,627 (5202万) 注册用户
*  238,671,904 (2.38亿) 条评论
*  25,241,800 (2524万) 工作室

仅是过去的一个月，[Scratch](https://scratch.mit.edu/)社区就有:

*  263,916,040 (2.63亿) 页面浏览量
*  46,152,020 (4615万) 访问
*  20,913,650 (2091万) 独立访客

考虑到这是一个完全自发的社区，这些数字近乎奇迹。

孩子们在社区里追逐热情，分享创作，寻找同伴。 这儿没有考试、奖励等外部诱惑/压力，不像这个赛道上的绝大多数的编程/教育项目。

>  人类的所有胜利，所有进步，都是以内在的力量为基石的。

如果你也认同蒙台梭利的这句话，那么当看到这个社区里产生的动人故事和惊人创造力(《终生幼儿园》一书里记录和许多)，就不会觉得奇怪。

创造当然发生在一片自由人的国度。这正是蒙台梭利的核心论点之一。

考虑到这些，`CodeLab Insight`的第一个目标锚定在[Scratch社区](https://scratch.mit.edu/)。 尽管未来可能会将视野拓宽到其他编程教育社区。但近期内我们选择目前 `最优秀/最开放` 的社区作为第一个分析对象。

由于[Scratch](https://scratch.mit.edu/)是今天整个少儿编程行业的推动者（很多人甚至将Scratch等同于少儿编程本身)，因其[开放性](https://github.com/LLK/scratch-gui)和优秀的架构设计。今天全球范围内，大量的少儿编程平台，都基于[Scratch](https://scratch.mit.edu/)开放的部分来构建。

所以`CodeLab Insight`也适用于与[Scratch](https://scratch.mit.edu/)保持数据格式(`projectJson`)兼容的产品。

# 社区网络
如果你对Scratch社区还不了解，可以参考我们之前的文章: [https://www.codelab.club/blog/scratch-community-analyze/](https://www.codelab.club/blog/scratch-community-analyze/)。


社区是个非常宽泛的概念，在此，我们关注数据视角下的社区。

Scratch社区拥有海量的注册用户(users)、分享项目(projects)、工作室(studios)、讨论(comments), 这些实体(entities)组成错综复杂的网络:

*  用户关系网(`user--follow--user`)
*  项目关系网(`project--remix--project`)
*  用户与项目关系网(`user--create/love/favorite--project`)
*  用户与工作室关系网(`user--create/curate--studio`)
*  项目与工作室关系网(`studio--collect--project`)
*  评论与 用户/项目/工作室 关系网
*  ...

如果你了解[知识图谱(Knowledge Graph)](https://baike.baidu.com/item/%E7%9F%A5%E8%AF%86%E5%9B%BE%E8%B0%B1), 就会发现，利用前边我们列出的这些三元组(Triples)，加上[网络爬虫](https://zh.wikipedia.org/zh-cn/%E7%B6%B2%E8%B7%AF%E7%88%AC%E8%9F%B2)采集的海量数据，可以构建一张巨大的网络, 涵盖了社区发生的一切。

这些数据，以及由此产生的可视化工具和知识图谱等，可以做许多有意思的事情, 它们不是静物, 而是可交互的知识网络。

![](/img/kg.png)


# 典型用例
以下是一些典型用例。

### 教育者
供教育者使用，将其做海量资源库，用于构建教学内容，诸如使用可视化工具轻松找到`孩子们喜欢却不太难的项目`。教育者也可使用Scratch项目结构可视化工具，分析学生项目的构成，从而更好评估`计算思维` (可依据 Mitchel Resnick 2012年发表的论文)

<video width=60% src="http://scratch3-files.just4fun.site/playground5.mp4" controls="controls"></video>

### 学习者
供学习者使用，由此构建的推荐系统和`AI教师`，可以直接辅助学习者，为其提供建议，帮助学习者寻找`Peers`(聚类)、寻找感兴趣的`Projects`(协同过滤),以及`Passion`(`favorite`数据是不错的指标)所在。去实现《终生幼儿园》提到的4P(`Projects,Passion,Peers,Play`)。

### 社区运营者
供社区运营者使用，可视化工具将帮助运营者发现社区里热门事件、趋势。

### 开发者
供开发者使用，我们在提取这些数据时，构建了一些基础工具，诸如提取Scratch项目内部结构的工具(sprite/blocks)、Scratch项目结构可视化图表，之后可能会做成服务，提供出来。

<img src="/img/project_blocks_tool.png" width=80% />


### 领域Chatbot/AI教师
用于构建领域Chatbot。用个营销意味浓一些的词汇叫`AI教师`, 当然今天宣称的编程教育`AI教师`多数都没有知识图谱作为支撑。

### 推荐系统/社区冷启动
推荐系统。推荐系统容易出现稀疏性和冷启动的问题，知识图谱可对其加以改进。 可以更好地服务早期社区，将社区启动起来。

### 行为模式
结合聚类以及针对图的算法做进一步分析，挖掘出数据模式，从而对大规模人群的行为模式作分析和判断。

### 科研人员
供科研人员使用。这是该领域迄今为止目前最大的开放数据集。追随蒙台梭利的研究者会尤其喜欢它，因其是在自发情况下产生的真实数据！


# 技术构成
以下是我们目前所用的一些技术工具。

*  采用[网络爬虫([Scrapy](http://scrapy.org/))](https://zh.wikipedia.org/zh-cn/%E7%B6%B2%E8%B7%AF%E7%88%AC%E8%9F%B2)抓取[Scratch](https://scratch.mit.edu/)海量数据
*  使用[Pandas](https://pandas.pydata.org/)清洗数据、预处理以及归档
*  使用[scikit-learn](https://scikit-learn.org/)作为机器学习库
*  使用[Vega](https://vega.github.io/vega/)作为可视化语言
*  使用[Smalltalk(Pharo)](http://pharo.org/)/[Jupyter](https://jupyter.org/)做数据交互探索
*  使用[neo4j](https://github.com/neo4j/neo4j)作为图数据库
*  使用[streamlit](https://www.streamlit.io/)部署应用
*  ... 



# 未来
未来CodeLab可能会定期发布白皮书。

`Playground 1: Explore scratch popular projects` 是很小的一个例子，但其展示的东西让很多从业者感兴趣。

我们之后也许利用获取的这些巨大数据和经由分析工具得出的结论，定期对外发布。

当然我们欢迎合作伙伴基于我们已有的工作，进行更深入的合作探讨。

# 背景思考
以下列出我们进行数据分析的思考背景和启发读物:

*  《Mindstorms》
*  《终身幼儿园》
*  [Elements of AI](https://www.elementsofai.com/)
*  《蒙台梭利早期教育法》
*  [New Frameworks for Studying and Assessing the Development of Computational Thinking](https://web.media.mit.edu/~kbrennan/files/Brennan_Resnick_AERA2012_CT.pdf)


在这项工作前，我们之前做的一些准备工作和讨论也列出在此:

*  [Scratch 社区数据分析 与 智能系统](https://www.codelab.club/blog/scratch-community-data-analysis-and-graph-server/)
*  [对《Scratch 社区数据分析与智能系统》的回复](https://www.codelab.club/blog/scratch-community-data-analysis-and-graph-server-reply/)
*  [Scratch3.0技术分析之后端API(第0篇)](https://blog.just4fun.site/post/%E5%B0%91%E5%84%BF%E7%BC%96%E7%A8%8B/scratch3_api_analysis/): 共10篇分析文章
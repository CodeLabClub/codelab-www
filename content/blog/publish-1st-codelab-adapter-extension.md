---
title: "构建并发布一个 CodeLab Adapter 插件"
author: 种瓜
date: 2019-09-10
---

<img class="img-responsive" src="/img/toys_party.jpeg" />

> 好的软件作品，往往源自于开发者的个人需要 -- 《大教堂与集市》

# 前言

在[上一篇文章](/blog/about-opensource)里,我们聊到开源项目与开源社区这两个话题。

本文将带着大家一起构建一个开源项目，并发布它。

<!--more-->

我们不希望这个例子只是一个展示技术原理的`hello world`,那样多少有些枯燥，我们希望它跟你的日常生活有关，所以尽可放心往下阅读，它不大无聊，而且一旦你理解之后，可能会乐意对其作些修改，做一些有趣的恶作剧或日常用得到的小工具。

# 关于 CodeLab Adapter

[CodeLab Adapter](https://adapter.codelab.club/) 是什么东西？

[CodeLab Adapter 的文档](https://adapter.codelab.club/) 里对此的回答是:

> CodeLab Adapter 是由 [CodeLab](http://www.codelab.club/) 构建的基础项目(v2 是最新版本)，致力于连接万物，无论是软件还是硬件，无论是 AI、开源硬件、现实世界的物体、还是虚拟世界的动画角色，在 CodeLab Adapter 的驱动下，皆可彼此互动。

[CodeLab Adapter](https://adapter.codelab.club/)适合用来构建 AIoT 相关的项目。

通过前头的例子，想说明的是，在开源社区，项目的文档是一个项目的说明书，阅读文档，通常是不错的起步。

在[CodeLab Adapter 的文档](https://adapter.codelab.club/) 中，[使用文档](https://adapter.codelab.club/user_guide/install/)和[开发者文档](https://adapter.codelab.club/dev_guide/helloworld/)都包含其中。

### Talk is cheap，show me demo

Linux 之父 Linus Torvalds 有句名言:

> Talk is cheap. Show me the code.

翻译为中文是:

> 废话少说，放码过来

可是,当我初次接触一个项目的时候，我是没有耐心直接阅读它的代码的，如果能给我看些视频，看看这个项目都能干些啥就好了。万一它没什么意思，可以尽早离开干点其他的事--止损是现代人的智慧。 不知你是否耐心多些，我对于不感兴趣之事，很难逼着自己在上头花心思，非强迫自己，多半也是做不好的。

我们先来看看[CodeLab Adapter](https://adapter.codelab.club/)都能用来干嘛: [https://adapter.codelab.club/user_guide/gallery/](https://adapter.codelab.club/user_guide/gallery/)

挑两个比较好玩的 demo:

<video width=40% src="http://scratch3-files.just4fun.site/wand.mp4" controls="controls"></video>

<br/>
<video width=80% src="http://scratch3-files.just4fun.site/cube%20symphony.mp4" controls="controls"></video>

### 开始使用

不知道这些例子对你是否有吸引力，如果觉得它无趣极了，你应当寻找自己感兴趣的东西去，没什么比找到令你感兴趣的事更重要的了，何况大家才大二，有的是时间去折腾。

要是觉得它还挺有趣，不妨按照文档里的说明引导[下载](https://adapter.codelab.club/user_guide/install/)下来玩一玩。

# 积木化编程

前头看到的视频里，经常出现一个充满彩色小块的界面，那东西叫[Scratch](https://zh.wikipedia.org/zh/Scratch)。

CodeLab Adapter 最初的名字叫 Scratch Adapter，不知道你用没用过 [Scratch](https://scratch3v2.codelab.club/)，如果你小时候没用过，你的弟弟妹妹们现在很可能正在用，它是这么个东西

<img src="https://adapter.codelab.club/img/v2/scratch_eim_read_value.png" width=600>

Scratch 是个图形化编程工具，那些没有编程经验的孩子可以很快上手，使用它创作故事、游戏、交互艺术...目前全球有超过 4000 万的孩子使用它创作了数以亿计的编程项目。

CodeLab Adapter 的最初的目标之一就是使用 Python 来增强 Scratch 的能力，让[Scratch](https://scratch3v2.codelab.club/)能够方便地构建与 AI、IoT、开源硬件有关的项目，它的最终目标是支持[约翰·杜威](https://zh.wikipedia.org/zh/%E7%BA%A6%E7%BF%B0%C2%B7%E6%9D%9C%E5%A8%81)提倡的:

> Education is life.

# 构建一个微信插件吧

大家日常使用微信比较多，接下来我们将带领大家基于 CodeLab Adapter 构建一个微信插件，一旦你完成这个插件，你的弟弟妹妹们就可以在[Scratch](https://scratch3v2.codelab.club/)使用`微信积木`来创作好玩的项目了。基于你的插件，孩子们只需要在 Scratch 拖拽积木，拼拼搭搭，就能使用微信与他们的程序互动！或者构建一个新的微信聊天界面:

<video width="80%" src="http://scratch3-files.just4fun.site/wechat.mp4" controls="controls"></video>

由于[Scratch](https://scratch3v2.codelab.club/)的易用性，你也可以让你奶奶基于你的插件来为微信编程。

这里头可以做的事情还有很多, 诸如同时使用微信插件和 CodeLab Adapter 社区里的 IoT 插件，你就可以使用微信控制家里的电气设备。

<video width="40%" src="http://scratch3-files.just4fun.site/%E8%A6%81%E6%9C%89%E5%85%89.mp4" controls="controls"></video>

设想你组织了个 party，每次有人按门铃都得去开门，是不是很烦躁？

把参与者拉到一个微信群，他们一到门口，在群里吼一身芝麻开门, 门即刻自动打开。 codelab-adapter 一端连接微信，一端连接智能门锁。要做到这点，只需在 Scratch 中拖几块积木，将它们拼一起即可。

<video width="40%" src="http://scratch3-files.just4fun.site/wechat_iot.mp4" controls="controls"></video>

期待你的奇思妙想。

### 准备工作

为了编写插件程序，首先得搭建编程环境， 你需要独立完成以下工作:

- 安装 [Python 3.7.4](https://www.python.org/downloads/release/python-374/)
- 安装 Chrome 或 Firefox 浏览器，并将其设为默认浏览器。

以上步骤若遇到问题，你应该能通过搜索引擎自行解决。如果你无法使用[Google](https://www.google.com), [bing](https://cn.bing.com/)(Bing Is Not Google)也是不错的选择。

安装完成之后，你应该能在命令行里(Windows 用户打开 CMD)运行`python`.

### Python 入门

如果你是编程新手，推荐阅读[深入浅出程序设计](https://book.douban.com/subject/10518092/)这本书。

如果你已经有过编程经验,[笨办法学 Python 3](https://book.douban.com/subject/30237842/)能让你快速入门。

如果你已经入门了 Python，我们继续前进。

### 安装第三方库

为了在 Python 中和微信通信，我们需要用到这个库:[ItChat](https://github.com/littlecodersh/ItChat)， 我们稍后将使用它来构建我们的 CodeLab Adapter 微信插件。

[ItChat](https://github.com/littlecodersh/ItChat)是个 Python 库，它也是个开源项目，发布在 Github 上，它有清晰的文档，作者在 Github 里乐于解答用户的问题，是个很棒的项目。

我们可以用 pip 安装它（Windows 用户同样在 CMD 里）: `pip install itchat`

安装成功后，就可以来写一个简单的聊天机器人了！

### 简单的聊天机器人

不知大家平时用什么编辑器写代码，如果还在挑选中, [Sublime Text](https://www.sublimetext.com/)和[VS code](https://code.visualstudio.com/)是推荐的选择。

我自己的话，目前使用 [VS code](https://code.visualstudio.com/) 和 vim 居多，但不推荐 vim。

让我们创建一个文件，叫它`my_little_bot.py`吧。

```python
import itchat

@itchat.msg_register(itchat.content.TEXT)
def text_reply(msg):
    reply = "我是机器人, 我收到如下消息: " + msg.text
    msg.user.send(reply)

itchat.auto_login(hotReload=True)
itchat.run()
```

你的第一个简单的微信聊天机器人就做完了，它会回复微信里收到的任何消息， 并在这条消息前头加上: `我是机器人, 我收到如下消息:`

开始运行它吧: `python my_little_bot.py`

给自己的微信号发消息来测试一下:

<img src="/img/WechatIMG966.jpeg" width=300/>

### 将收到的消息传递给 Scratch

下边来正式开始构建 CodeLab Adapter 插件。插件负责将来自微信的消息传递到 Scratch 中。

在前头的程序里(`my_little_bot.py`), 我们已经了学会在 Python 代码中，接受来自微信好友的消息，并自动回复。

为了将微信消息传递到 Scratch，需要做 3 件事:

1. 构建微信插件。
2. 下载并运行[CodeLab Adapter](https://adapter.codelab.club/user_guide/install/)。
3. 打开 Scratch。
4. 运行微信插件。

先来完成第一件事: `构建微信插件`, 先上源码，稍后解释:

```python
import itchat
from codelab_adapter_client import AdapterNode


class MyFirstNode(AdapterNode):
    def __init__(self):
        super().__init__()
        self.EXTENSION_ID = "eim/wechat"

    def send_to_scratch(self, content):
        message = self.message_template()
        message["payload"]["content"] = content
        self.publish(message)


my_first_node = MyFirstNode()


@itchat.msg_register(itchat.content.TEXT)
def text_reply(msg):
    text = msg.text
    my_first_node.send_to_scratch(text)


try:
    itchat.auto_login(hotReload=True)
    itchat.run()
except KeyboardInterrupt:
    my_first_node.teminate()
```

我们将这段代码放入`my_first_node.py`文件里，这儿引入了新的依赖，先安装它:`pip install codelab_adapter_client`。

这段代码的逻辑是:将微信中接收到的信息转发到 Scratch 中，`my_first_node.send_to_scratch(text)`负责转发消息，暂不讨论它是怎么运作的。在此只需知道通过继承`AdapterNode`，能获得与 Scratch 通信的能力即可。

第一步完成了，接下来:

2. 下载并运行[CodeLab Adapter](https://adapter.codelab.club/user_guide/install/)

这步比较简单，只是下载运行软件。我们构建的`my_first_node.py`是一个 CodeLab Adapter 插件，它需要与 CodeLab Adapter 一同运行。

双击打开 Codelab Adapter。

Codelab Adapter 启动之后，将打开默认浏览器(建议将 Chrome 设为默认浏览器)。

<img width="300px" src="https://adapter.codelab.club/img/v2/codelab_adapter_webui.png"/>

3. 打开 Scratch。

点击前头页面里的`scratch3`，或者点击这个链接[CodeLab Scratch](https://scratch3v2.codelab.club)，将打开如下页面:

![](https://adapter.codelab.club/img/v2/codelab-scratch3.png)

点击图中箭头位置，进入 Scratch 插件列表，选择`微信插件`，拖拽积木, 拼出图示图案， 图中紫色的`说`积木，在左侧`外观`菜单里，它的功能是让角色说出内容。

<img src="/img/scratch_wechat2.png"  width=600/>

以上积木的功能是: 让角色说出微信发来的内容。

4. 运行微信插件。

`python my_first_node.py`

现在，可以给你的微信发信息了，这信息也会显示在 Scratch 中，虚拟角色将"说"出它来。

![](/img/wechat_scratch_1_1.png)

### 交响乐

微信的信息既已能够传递到 Scratch 中，我们便可以使用微信来与 Scratch 互动。

我们来构建这样一个应用: 将微信中的消息演奏为音乐。

<video width=80% src="/img/wechat_music.mp4" controls="controls"></video>

图中`演奏音符`的积木来自 Scratch 插件列表里的第一个插件:`音乐`。

# 发布它！

我们已经完成了第一个 CodeLab Adapter 插件！

它可以将微信的的能力积木化，使其变为 Scratch 的编程元素。

现在让我们发布这个插件，让更多的人使用它。（当然你也可以增添更多好玩的功能再发布）

### 发布到 Github

如果你还不熟悉 Github，建议先浏览一下:

- [如何使用 GitHub？](https://www.zhihu.com/question/20070065/answer/79557687)。
- [最简单的 GitHub 入门教程](https://www.bilibili.com/video/av4857819/)

---

读完这两份资料，对 Github 应该就有基本了解了（git 是另一个话题，暂且把它放一边）。

为了发布我们的新插件，需要做以下工作:

- 注册 Github 账号
- 创建新仓库
- 将插件(`my_first_node.py`)放入新仓库中
  - 可以直接在仓库里，点击`Upload files`（推荐）
  - 也可以使用[GitHub Desktop](https://help.github.com/cn/desktop/getting-started-with-github-desktop/installing-github-desktop)
- 添加说明文档: `README.md`

<img src=/img/adapter_wechat_github_f577712e.png width=80% />

目前我已经将完整的范例放在 Github 上了，供大家参考:[codelab_adapter_wechat_node](https://github.com/wwj718/codelab_adapter_wechat_node)

### 解答使用者遇到的问题

使用者在使用你的程序的时候，如果遇到困难，鼓励他们在[Github issues](https://github.com/wwj718/codelab_adapter_wechat_node/issues)里提问；如果用户有改进建议，鼓励他们提交[Pull Requests](https://github.com/wwj718/codelab_adapter_wechat_node/pulls)。

# FAQ

### 我想继续前进，该怎么做呢？

阅读[开发者文档](https://adapter.codelab.club/dev_guide/introduction/)。

### 有更完整的微信插件源码供参考学习吗?

有的, CodeLab Adapter 内置了一个微信插件：[extension_wechat.py](https://github.com/Scratch3Lab/codelab_adapter_extensions/blob/master/extensions_v2/extension_wechat.py)，基于这个插件，可以在 Scratch 中收发微信消息，无论来自朋友还是群聊。

### CodeLab 是个啥?

[CodeLab](https://www.codelab.club/)是个非营利组织,我们的使命是:

> 传递编程的乐趣，帮助孩子成为数字时代的创作者.

欢迎你成为我们的志愿者.

### 你是不是骗子，我怎么没有找到 CodeLab Adapter 的源码?

CodeLab Adapter 的所有插件源码都是公开的:[codelab_adapter_extensions](https://github.com/Scratch3Lab/codelab_adapter_extensions)，核心源码也承诺公开，具体的时间规划参考:[CodeLab Adapter v2](https://www.codelab.club/blog/codelab-adapter-v2/)

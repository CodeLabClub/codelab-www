---
Date: 2020-06-02
title: "CodeLab DynamicTable: 一个可实施的技术方案"
Slug: CodeLab-DynamicTable-an-instance
tags: ["CodeLab"]
author: CodeLab
categories: ["CodeLab"]
---

> 我的命题可以用以下方式解释：了解我作法的人，会用这些命题当做梯子，越过它们，最终会发现这些梯子是荒谬的。他必须超越这些命题，之后才能正确的看待世界。 -- 维特根斯坦 《逻辑哲学论》

<!--more-->

# 前言

[CodeLab DynamicTable: A Seeing World](https://www.codelab.club/blog/codelab-dynamictable-a-seeing-world/) 可以看作 CodeLab DynamicTable 的白皮书。 文章里，我们着重阐述了想法的来源、设计原则以及可能性，尽管也站在技术视角做了一些讨论，却未给出完整的可实施技术方案。

本文则试着给出一个可实施的技术方案， 它包含硬件设备清单和源码细节。

需要强调的是，开放性和可扩展性是 CodeLab DynamicTable 的灵魂，大家可以随意改造它，构建自己想要的东西.我们也鼓励你为用户保留这种灵活性，让 Ta 自己成为创造者。

我们推荐将本文看作实施 DynamicTable 一个脚手架，而不是标准答案。将其视为一个帮助你爬上墙头的梯子，一旦爬上去之后，去做你自己想做的事情吧，不要拘泥于梯子本身。

# 第 0 号 CodeLab DynamicTable

CodeLab 目前有 4 张办公桌，3 个全职人员。我们将第 4 张桌子构建为 DynamicTable。

![](https://adapter.codelab.club/img/WechatIMG1527.jpeg)

可以把这张桌子视为 `第0号 DynamicTable`。

我们在[CodeLab DynamicTable: A Seeing World](https://www.codelab.club/blog/codelab-dynamictable-a-seeing-world/)提到说， DynamicTable 的构成包括

-   铅笔
-   剪刀
-   纸张
-   橡皮泥
-   可打印的 Marker
-   摄像头
-   显示设备(超短焦投影仪)
-   桌子
-   CodeLab Scratch
-   CodeLab Adapter
-   ...

铅笔、剪刀、纸张、橡皮泥 是日常实物，不做讨论。

其中硬件/设备包括:

-   桌子
-   显示设备(超短焦投影仪)
-   可打印的 Marker
-   摄像头

软件包括:

-   CodeLab Adapter
-   CodeLab Scratch

接下来，我们站在实施的视角来讨论它们。

## 硬件/设备

### 桌子

我们采用了宜家的[这款升降桌](https://www.ikea.cn/cn/zh/p/bekant-bei-ken-te-zuo-zhan-liang-yong-shi-ban-gong-zhuo-bai-se-xiang-mu-tie-mian-bai-se-s69386410/)。

我们选择了橡木纹理表面，这个纹理表面在弱光下，挺适合直接作为投影表面。

它的尺寸信息是:

-   长度: 120 厘米
-   宽度: 80 厘米

选择这款升降桌的最初动机是: 来 CodeLab 参加编程活动的孩子身高不同。此外，它也支持我们站立办公。

需要说明的是: DynamicTable 对桌子没有特别要求。可以任意选择。如果它的表面纹理不适合投影，可以考虑铺一层桌布。

### 显示设备(超短焦投影仪)

![](https://adapter.codelab.club/img/1eec2b121660441c6d5ba7ceceef469c.png)

我们选择了 LG 的这款[超短焦投影仪: PH450UG](https://www.lg.com/cn/projectors/lg-PH450UG)，33cm 就可以获得 80 英寸的大屏幕。

它内置电池，续航超过 2.5 小时。

体积小巧(132 x 200 x 80.5 mm)，单手可握。更详细的参数，参看[产品页](https://www.lg.com/cn/projectors/lg-PH450UG)。

投影既可以是桌面，也可以投射到墙上。

### 可打印的 Marker

![](https://adapter.codelab.club/img/e6cc193e54fdda12ae3ada44c2299dfd.png)

我们目前选择 ArUco 作为 Marker 。上图一共有 `5x6 = 30` 个 Marker， 按照从左到右，从上到下的顺序，Marker id 依次从 1 到 30。

你可以将 Marker 视为一种二维码，计算机可以识别它。计算机除了可以理解它的 id (编号)信息, 还可以理解它在什么位置，旋转角是多少，以及中心点和边缘 4 个角点在镜头下的坐标是多少。

它是一个携带空间信息的二维码。

[ArUco Marker](https://docs.opencv.org/trunk/d5/dae/tutorial_aruco_detection.html) 在 AR 和 机器人领域都用得很广泛，是一个开放项目。

我们目前使用 OpenCV(Python)解析它。

CodeLab 已经构建了解析 [ArUco Marker Adapter 插件](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/nodes_v3/node_physical_blocks.py)，你可以在不了解它的情况下, 在 Scratch 中使用它。

如果你愿意深入学习 ArUco Marker，推荐学习[MECARUCO: mechanics & aruco](https://mecaruco2.readthedocs.io/en/latest)。

#### ArUco Marker 的类型

ArUco Marker 有多种类型， 我们选择了 `4X4_50`布局的， 一共有 50 个不同的 Marker。

如果选择`7X7_1000` 则一共有 1000 种不同的 Marker。

你可以在线查看它们之间的区别: [arucogen](https://chev.me/arucogen/)， 也可以从以上页面生成可打印 Marker。

#### 如何生成以及打印 Marker

有多种方式生成 Marker，既可以从 [arucogen](https://chev.me/arucogen/) 每次生成一个 marker 。

也可以使用 Python 代码批量生成 marker:

![](https://adapter.codelab.club/img/e6cc193e54fdda12ae3ada44c2299dfd.png)

生成以上 marker 的代码为:

```python
import numpy as np
import cv2
from cv2 import aruco
import matplotlib.pyplot as plt
import matplotlib as mpl
# %matplotlib inline

aruco_dict = aruco.Dictionary_get(aruco.DICT_4X4_50)
fig = plt.figure()
nx = 6
ny = 5
for i in range(1, nx*ny+1):
    ax = fig.add_subplot(ny,nx, i)
    img = aruco.drawMarker(aruco_dict,i, 700)
    plt.imshow(img, cmap = mpl.cm.gray, interpolation = "nearest")
    ax.axis("off")

# plt.savefig("_data/markers.pdf")
plt.savefig("markers.png")
# plt.show()
```

#### 每个 marker 多大合适呢？

这个可能需要通过做实验来获得。摄像头摆放的高度，以及分辨率， 都可能影响 marker 识别率。

我们目前在 A4 纸上以黑白模式打印 ArUco Marker，大小是这样的:

![](https://adapter.codelab.club/img/WechatIMG1528.jpeg)

在一张 A4 纸上打印 2 份 30 张的 marker。

如果你想让 marker 更小，也是可以的，最好做一些实验，确保识别率。如果你愿意把 marker 打印得更大，请随意。

### 摄像头

我们选择了[logitech C922PRO 摄像头](https://www.logitech.com.cn/zh-cn/product/c922-pro-stream-webcam?crid=34)， 支持分辨率 1080P 视频流。

选择这款摄像头是因为，我们准备在 CodeLab 办公室做直播。

DynamicTable 使用 Scratch 的视频数据(480x360), 这么低的分辨率对摄像头要求很低，所以绝大多数 USB 摄像头都可以。

为了保证灵活性，最好有一个摄像头活动支架:

![](https://adapter.codelab.club/img/WechatIMG1529.jpeg)

---

以上便说完了 DynamicTable 的硬件/设备构成。

## 软件

### CodeLab Adapter

使用 CodeLab Adapter 插件: [node_physical_blocks.py](https://adapter.codelab.club/extension_guide/physical_blocks/), 我们可以解析摄像头所见到的 ArUco Marker ，并按照从左到右、从上到下的顺序依次列出 Marker id。

目前 node_physical_blocks.py 已经在[插件市场](https://adapter.codelab.club/extension_guide/extension_market/)中。

### CodeLab Scratch

以下是一个简单的案例，识别出拼写单词:

[Scratch-spell-demo](https://scratch3v3.codelab.club/?sb3url=https://adapter.codelab.club/sb3/Scratch-spell-demo.sb3)

按绿旗运行程序， 将开启摄像头，并运行 node_physical_blocks.py 插件，如果你是第一次运行 node_physical_blocks.py 插件，将自动安装依赖:`opencv-contrib-python` , 这个依赖比较大(`> 60MB`) ，耐心等待一会儿，依赖安装完成后，屏幕右上角会出现通知信息。

每次按下`空格`的时候，将分析摄像头画面，从中提取出 marker 信息，并在舞台区域显示识别到的 marker id 列表。（从左到右，从上到下）。

整个 Scratch 程序的逻辑是: `获取当前屏幕的 marker 数据(marker id)，存放到 scratch 变量: markers 里；将 marker id 与 marker 的含义绑定到一起(诸如marker 2 表示字母 c)。如果屏幕中的 marker 拼成的字母是 cat，则触发猫叫声`。

marker id 的含义是`自定义`的；拼写的结果要触发什么行为是`自定义`的。

只要将 [Scratch-spell-demo](https://scratch3v3.codelab.club/?sb3url=https://adapter.codelab.club/sb3/Scratch-spell-demo.sb3) 稍加修改，就可以作出以下视频里的案例。

<video width=80% src="https://adapter.codelab.club/video/1590154622682774.mp4" controls="controls"></video>

以上只是一个非常简单的案例，发挥你的想象力，去做好玩的东西 :)

#### 投影呢？

以上例子的输出只使用了声音，并未将交互动画投影到桌面。

将动画投影到桌面的想法是这样的: 最大化 Scratch 舞台，选一个黑色背景，将舞台区域之外的地方变黑（在最大化舞台区模式下，CodeLab Scratch支持切换到`dark模式`）。

![](https://adapter.codelab.club/img/ce2e5834ef315d8d3c1427bded4e9535.png)

之所以要让角色之外的区域都变黑，是因为投影仪将黑色解释为`没有光照`, 如此一来我们就能让 Scratch 角色与桌子(环境)融为一体。

一旦理解这个想法，你就能自己制作各种有趣的沉浸式场景啦。

# 参考

-   [CodeLab DynamicTable: A Seeing World](https://www.codelab.club/blog/codelab-dynamictable-a-seeing-world/)

---
title: "CodeLab Adapter ❤️ Jupyter/Python"
author: 种瓜
date: 2019-07-30
tags: ["programming"]
---


<img class="img-responsive" src="/img/adapter_jupyter_05932c59.png" />

# 前言
上周与@曾老师一起在杭州湾参加为期四天的AI夏令营，做一些技术支持和辅导的工作，体验颇似黑客马拉松。

活动中教育者与学习者们皆十分用心，有些同学为了做好手头项目彻夜未眠。

由于Alan Kay和Seymour Papert的影响，活动过程中，我的视角一直放在编程/软件环境等基础设施上。大家都在使用Python编程(下个十年的编程教育应该都会基于它)，触及的编程环境五花八门，许多工具恶劣而狂野，以至于教育者和学习者所做的努力中起码有一半用于与糟糕的技术环境搏斗。

<!--more-->

# demo
夏令营的几天里一直在与曾老师讨论如何为初学者设计一种舒适的入门环境，既能自由探索又安全可控。


我们想到Jupyter + CodeLab Adapter。活动结束回到酒店洗完澡，做了个原型:

<video width=600px src="http://scratch3-files.just4fun.site/jupyter_scratch.mp4" controls="controls"></video>

对应源码(调整后):

```python
from codelab_adapter_client import SimpleNode
node = SimpleNode()

node.simple_publish("开启音乐")

node.simple_publish("下一个造型")

import time
for i in range(10):
    time.sleep(0.2)
    node.simple_publish("落下礼花")

# 完整演奏
import time
node.simple_publish("开启音乐")
time.sleep(0.2)
for i in range(30):
    time.sleep(0.2)
    node.simple_publish("下一个造型")
    time.sleep(0.2)
    for i in range(5):
        node.simple_publish("落下礼花")
```

在这个例子里，Jupyter中的Python代码可以与Scratch3.0环境自由互动。

技术层面，往Jupyter中引入[codelab_adapter_client](https://github.com/Scratch3Lab/codelab_adapter_client)，使用AdapterNode与CodeLab Adapter 2.0建立连接。由于CodeLab Adapter 2.0已经接入了Scratch3.0. 所以用户可以使用Python代码为Scratch中的角色编程(Everything Is Message)。Python中的任何能力都可以引入到Scratch3.0中，这可不是简单的积木翻译，是两个环境之间的交互和彼此增强！

这也是CodeLab对`如何从Scratch过渡到Python？`这一问题做出的一个回答。

# 更多的想象空间
由于CodeLab Adapter 2.0已经[接入了数十种软硬件](https://adapter.codelab.club/)。

当我们使用[codelab_adapter_client](https://github.com/Scratch3Lab/codelab_adapter_client)将Jupyter接入CodeLab Adapter 2.0时，我们就可以将Jupyter作为这数十种软硬件的编程平台！

Jupyter是目前最理想Python/数据分析/人工智能的编程教育环境。关于Jupyter在教育上的意义可以参考[使用IPython Notebook来学习编程](https://blog.just4fun.site/use-ipython-notebook.html)。

CodeLab Adapter 1.0致力于将万物带入Scratch，实现`education as life`的目标。CodeLab Adapter 2.0则将万物带入到Python教育中。物联网、人工智能、开源硬件，你现在可以使用Python在Jupyter中与这些东西交互。

### 机器人教学
<video width=600px src="http://scratch3-files.just4fun.site/jupyter_vector.mp4" controls="controls"></video>

涉及的代码如下:

```python
from codelab_adapter_client import AdapterNode
from codelab_adapter_client.topic import JUPYTER_TOPIC

class MyRobotNode(AdapterNode):
    def __init__(self):
        super().__init__()
        self.EXTENSION_ID = "eim/vector"
        self.message = {"topic": JUPYTER_TOPIC, "payload": {"content": "robot.behavior.say_text('hello')"}}

    def forward(self,distance,speed):
        self.message["payload"]["content"] = f"robot.behavior.drive_straight(anki_vector.util.distance_mm({distance}), anki_vector.util.speed_mmps({speed}))"
        self.publish(self.message)
    def turn_left(self,degrees,speed):
        self.message["payload"]["content"] = f"robot.behavior.turn_in_place(anki_vector.util.degrees({degrees}), speed=anki_vector.util.degrees({speed}))"
        self.publish(self.message)

    def say(self,content):
        self.message["payload"]["content"] = f"robot.behavior.say_text('{content}')"
        self.publish(self.message)
     
robot = MyRobotNode()
robot.forward(100,100)
robot.turn_left(90,180)
robot.say("hello")

from pypinyin import  lazy_pinyin
pinyin = "".join(lazy_pinyin('肚子 好饿 去吃 午饭啦'))
print(pinyin)
robot.say(pinyin)
```


# CodeLab Adapter 2.0
CodeLab Adapter 2.0近期计划发布，它试图去聚合所有有趣而设计精良的东西，无论是积木化界面、优秀的Python编程环境(Jupyter)、还是整个日常生活空间，目标是为学习者提供完整而舒适的编程环境。

# 线上学习平台
@曾老师近期在参与一个AI线上学习平台的构建，将基于[Open edX](http://github.com/edx) + [Jupyter](https://jupyter.org/)。

[Open edX](http://github.com/edx)提供了绝佳的学习系统，也许是目前全球最强大的学习系统，它拥有绝佳的开放性和丰富的生态。而[Jupyter](https://jupyter.org/)则是目前最理想的Python//数据分析/机器学习/AI编程工具。@曾老师希望结合两者，为学习者提供舒适而高效的学习环境，初学者不必为环境的搭建焦头烂额，目前斯坦福大学和UC伯克利都在使用[Open edX](http://github.com/edx)和[Jupyter](https://jupyter.org/)作为编程教育平台。

CodeLab Adapter 2.0也将该平台的基础实施之一，将平台能力延伸到任何事物上，无论是机器人教学、物联网教学还是开源硬件教学。学习者只需要在[Jupyter](https://jupyter.org/)中编程，就可以控制CodeLab Adapter 2.0接入的任何事物。

在本地运行[Jupyter](https://jupyter.org/)，连接CodeLab Adapter 2.0是容易的，但云端似乎有些不同。  [Open edX](http://github.com/edx)使用[jupyterhub](https://jupyter.org/hub)将[Jupyter](https://jupyter.org/)运行在云端docker容器里，如此一来，线上平台的Python代码如何与本地硬件交互呢？

策略是利用Javascript！浏览器中Javascript既能与云端Jupyter Python Kernel交互，又能与本地的CodeLab Adapter 2.0交互(我们在Scratch3.0中也是这么做的)，具体原理用以下代码演示:

```Python
from IPython.core.display import Javascript, display
for i in range(3):
    display(Javascript(f"console.log('{i}') //websocket send/recv message <-> CodeLab Adapter 2.0")) 
```

![](/img/notebook_js_python_5dd7081e.png)


<!--
# 没有display不刷新，只运行一次
# 注意 流的问题
# 从摄像头取照片
# 硬件相关 adapter js通道 python运行
-->


# 参考
*  [Embracing web standards](https://jupyter-notebook.readthedocs.io/en/stable/examples/Notebook/JavaScript%20Notebook%20Extensions.html)
*  [IPython Notebook: Javascript/Python Bi-directional Communication](https://jakevdp.github.io/blog/2013/06/01/ipython-notebook-javascript-python-communication/)
*  [Reactive Python-Javascript communication in Jupyter Notebook](https://medium.com/@tomgrek/reactive-python-javascript-communication-in-jupyter-notebook-e2a879e25906)
*  [Javascript can not work with `for`](https://github.com/jupyter/notebook/issues/4792)
*  [Run Python code from JavaScript in a Jupyter notebook](https://gist.github.com/craigsdennis/ddfaa99a6291f05fef879329821872ee)
*  [将codelab-adapter用作Python解释器](https://blog.just4fun.site/scratch3-adapter-as-python-interpreter.html)
*  [使用Python拓展Scratch的能力](https://blog.just4fun.site/scratch-adapter-eim-script.html)
*  [Python与Scratch的双向通信](https://blog.just4fun.site/python-scratch-with-adapter.html)
*  [使用IPython Notebook来学习编程](https://blog.just4fun.site/use-ipython-notebook.html)
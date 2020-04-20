---
Date: 2019-12-04
title: "CodeLab Adapter 接入 Teachable Machine"
Slug: adapter-Teachable-Machine
tags: ["编程", "CodeLab", "AI"]
categories: ["CodeLab"]
author: "种瓜"
---

> 通过教计算机怎样思考，孩子们开始探索自己的思考方式。这种体验颇不寻常，甚至很多成年人也很难拥有--思考关于思考的问题。 -- Seymour Papert 《Mindstorms》

CodeLab Adapter 的目标之一是:

> 连接一切，降低建构和创造的门槛。

[Teachable Machine](https://teachablemachine.withgoogle.com/)是全球最酷的 AI 项目之一，所以我们准定接入它。

<!--more-->

# Teachable Machine

Teachable Machine 是什么? 我们引用其主页的介绍:

> 训练计算机以识别自己的图像、声音和身体姿势。

这是一种快速为网站、APP 等应用创建机器学习模型的方法, 无需专业知识或编程！

它基于 Web，任何人可以轻松使用它。

## 展示一下

<video width=40% src="/video/google_tf_prediction.mp4" controls="controls"></video>

更完整的介绍：

<video width=80% src="/video/google_tm_demo.mp4" controls="controls"></video>

## 如何使用？

Teachable Machine 简单易用，只需 3 步，你就可以在浏览器上训练自己的机器学习模型

### 第一步: 采集数据

收集示例数据(声音、图像)并将其分门别类，计算机将学习你的分类方式。

### 第二步: 训练

训练模型，然后对其进行测试，看看是否能正常地在新的例子上工作。

### 第三步: 导出模型

导出训练模型：将其用于网站中。

## 用什么来教它？

Teachable Machine 非常灵活，即可以使用已经准备好的文件，也可实时采集数据(摄像头、麦克风...), 采集和计算工作都在本地完成，没有数据离开你的计算机，不必担心隐私问题，没有云，没有别人的电脑。

![](/img/google_tm_data.png)

## 示例讲解

Teachable Machine 项目给出了 3 个示例（图片、声音、身体姿态），为我们讲解如何使用它:

1. [《图片：香蕉计》](https://medium.com/@warronbebster/4bfffa765866): 了解如何创建一个模型，它可以判断香蕉是否成熟。
2. [《声音：拍手吹口哨》](https://medium.com/@warronbebster/4212fd7f3555)了解如何创建一个模型来检测你发出的声音。
3. [《身体姿态:头部倾斜》](https://medium.com/@warronbebster/f4f6116f491): 了解如何创建一个模型，该模型可以识别你如何倾斜头部。

## 社区创意

社区里大家构建了很多[好玩的东西](https://teachablemachine.withgoogle.com/):

![](/img/tm_demo001.png)

![](/img/tm_demo002.png)

# 接入 CodeLab Adapter！

CodeLab 近期的工作之一是，搜罗全球有想象力的 AI 项目，并将其接入 CodeLab Adapter，[Teachable Machine](https://teachablemachine.withgoogle.com/)是我们最喜欢的 3 个 AI 项目之一。其余两个我们正在本地化部署到国内，下回再介绍它们。

我们目前已经将 Teachable Machine 接入到了 CodeLab Adapter。你可以根据[文档引导](https://adapter.codelab.club/extension_guide/teachable_machine/)使用它。

Teachable Machine 接入到了 CodeLab Adapter 之后，可以与 CodeLab Adapter 开放生态中的任何事物交互！由于 CodeLab Adapter 的开放性，你可以轻松将[Teachable Machine](https://teachablemachine.withgoogle.com/)用在任何地方: 从你的芭比娃娃、四驱车到整个生活空间！以及 Neverland 里的所有这些事物:

![](https://adapter.codelab.club/img/adapter_party.jpeg)

<!--
在CodeLab Adapter的内测版本中，支持[Teachable Machine](https://teachablemachine.withgoogle.com/)导出的model，使其与CodeLab Adapter开放

我们计划将这项实验功能加入到下个版本里。
-->

<!--
之后与CodeLab Adapter一同使用它。(上传)

### 在线使用
也可以使用p5js 在线 editor，分辨率有问题。把模型上传，之后直接使用


### 本地使用
解压下载文件：my-pose-model.zip

```
wget https://gist.githubusercontent.com/wwj718/xxx/raw/xxx/tm-image.html
python3 -m http.server
```

打开: `http://127.0.0.1:8000/tm-image.html`


### 使用别人模版
https://github.com/wwj718/TeachableMachine4adapter

### 自己训练的模型
https://teachablemachine.withgoogle.com/models/Xubn6ODo/

剪刀 布 和 空
-->

# 一个演示

来看一个演示。

下边的例子展示了在 CodeLab Adapter 中加载《身体姿态:头部倾斜》，加载之后我们就可以将 Teachable Machine 的能力带入到 Scratch 里（以及 CodeLab Adapter 支持的另外 34+编程语言！）

<video width=80% src="/video/adapter_google_teachable_machine.mp4" controls="controls"></video>

# 参考

-   [Teachable Machine](https://teachablemachine.withgoogle.com/)
-   [github teachablemachine-community](https://github.com/googlecreativelab/teachablemachine-community)
-   [pose/tensorflowjs/javascript](https://github.com/googlecreativelab/teachablemachine-community/blob/master/snippets/markdown/pose/tensorflowjs/javascript.md)
-   [Teachable Machine Tutorial: Bananameter](https://medium.com/@warronbebster/teachable-machine-tutorial-bananameter-4bfffa765866)
-   [Tiny Sorter](https://experiments.withgoogle.com/tiny-sorter/view)
    -   [code](https://editor.p5js.org/gbose/sketches/2BN5HQYNK)
-   [coral](https://coral.ai/)
    -   [coral usb accelerator](https://coral.ai/products/accelerator)
-   [Teachable Machine Tutorial: Head Tilt](https://medium.com/@warronbebster/teachable-machine-tutorial-head-tilt-f4f6116f491)
    -   [tm-pose-demo.glitch.me](https://tm-pose-demo.glitch.me/)

---
Date: 2020-06-28
title: "CodeLab ❤ Siri"
Slug: codelab-like-siri
tags: ["CodeLab"]
author: CodeLab
categories: ["CodeLab"]
---

我们近期发布了一个新的 Adapter 插件: [extension_Siri.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v3/extension_Siri.py) (可在[插件市场](https://adapter.codelab.club/extension_guide/extension_market/)下载)

使用该插件，可将 Siri 接入到 Scratch，并于 CodeLab 可编程空间里的一切互动。

<!--more-->

## Demo

<video width=80% src="https://adapter.codelab.club/video/1593328552202841.mp4" controls="controls"></video>

## 原理

原理其实很简单:

-   构建一个接受 http 请求的 web server
-   使用 Siri 的输入(语音识别结果)构建 http 请求

来自快接指令的输入经由 http post 到 web server，再自动转化为 EIM 消息进入 Adapter。之后进入 CodeLab Scratch 。

值得注意的是，通过使用[快捷指令](https://apps.apple.com/cn/app/%E5%BF%AB%E6%8D%B7%E6%8C%87%E4%BB%A4/id915249334)里的`列表`，你可以构建多轮对话。

### 构建一个接受 http 请求的 web server

[extension_Siri.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v3/extension_Siri.py) 实际上是一个 web server，fork 自[extension_webserver.py](https://github.com/CodeLabClub/codelab_adapter_extensions/blob/master/extensions_v3/extension_webserver.py)

插件运行之后，会打开一个新页面，显示当前计算机的 IP。

它有两个重要 API:

-   接受来自 `http://<IP>:18081/api/message/siri?message=hi` 的`GET`请求, 并将请求参数 message 的值作为 eim 消息发送到 Scratch。
-   接受来自 `http://<IP>:18081/api/message/siri` 的`POST`请求, 并将请求参数 message 的值作为 eim 消息发送到 Scratch(json)

如果你的请求参数包含中文，建议使用 POST。

熟悉 Adapter 的朋友可能会发现，该插件的功能和 [Adapter REST API](https://adapter.codelab.club/dev_guide/REST-API/)相近，为何要写成独立插件？原因是 Adapter 默认采用 https，但 https 容易遇到各种安全机制问题， http api 则不会遇到这类问题。

## 使用文档

[文档](https://adapter.codelab.club/extension_guide/siri/)

## 进一步

如果你想对文本做进一步的语义处理，又不想使用云端 API，推荐使用[Rasa_NLU_Chi](https://github.com/crownpku/Rasa_NLU_Chi)，我在 Scratch 里写一个简单的 Adapter 语义解析插件。

以下是它的应用案例: [hey siri](https://www.codelab.club/blog/hey-siri-control-lego/)

NLU 的处理结果如何操控实物呢？[ThingTalk](https://almond.stanford.edu/doc/thingtalk-intro.md) 和 [WebThings](https://iot.mozilla.org/) 提供了很好的思路。

# 参考

-   [ThingTalk](https://almond.stanford.edu/doc/thingtalk-intro.md)

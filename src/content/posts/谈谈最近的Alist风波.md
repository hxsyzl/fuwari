---
title: 谈谈最近的Alist风波
published: 2025-06-14
description: '著名网盘聚合工具 Alist 被出售，官网已切换域，但新公司有黑历史很猛…'
image: 'https://q3.itc.cn/q_70/images03/20250611/2d170b7e5fd740ee9c7e175f9bcb252b.jpeg'
tags: [科技新闻]
category: 'github'
draft: false 
lang: ''
---

![](https://oss.wuxinrom.xyz/fuwari/image/712474d8-833a-4ba7-ba79-ccf7aebebf4e.webp)

**[Alist](https://www.appinn.com/alist-file-list-program/)** 是一个开源项目，它可以将 40 多款主流网盘聚合到一个网页上，进行文件管理、视频播放等操作。来自多个方面的消息，大概2025年4月份左右易手。不过原开发者持续更新代码，但对于这件事原开发者[回应](https://t.me/alist_news/85)：@[Appinn](https://www.appinn.com/alist-ownership-change/)

需要注意，虽然 Alist 是开源项目，但其使用了私有的 API，可能会「不更新就不能用」。



> 项目已交由公司运营，之后我会帮忙审查开源版本仓库的代码，以及确保 release 的分发由 ci 自动构建，main 分支已开启分支保护，后续所有的提交都会经过 pr 审核。



今天早上论坛的 @tempUserName 同学发布了新主题https://meta.appinn.net/t/topic/72174



最早，**Alist** 的官网是 `alist.nn.ci`，目前其更换为 `alistgo.com`

![](https://oss.wuxinrom.xyz/fuwari/image/f6bc393d-3dd0-4d6d-861a-412edd4334e6.webp)

![](https://oss.wuxinrom.xyz/fuwari/image/8416e041-6d02-4d01-9c80-fa176e3eed58.webp)

原开发者最近一次更新在5月11日：甚至上面的PR合并了个意义不明的东西

![](https://oss.wuxinrom.xyz/fuwari/image/110590b7-1137-487b-95c5-c2a1cf377652.webp)

从其新官网价格页面的联系方式看到，为**贵州不够科技**：

![](https://oss.wuxinrom.xyz/fuwari/image/2fd0a56e-7a95-413e-84da-9a9d767fcbd0.webp)

而**贵州不够科技**旗下，还[收购](https://v2ex.com/t/1137799)过好几家开源项目….

![](https://oss.wuxinrom.xyz/fuwari/image/d5335863-3c94-4cbf-9d01-90fa131b29fe.webp)

从最早质疑这件事情的 issue #[8649](https://github.com/AlistGo/alist/issues/8649) 来看：

![](https://oss.wuxinrom.xyz/fuwari/image/efb99188-e687-4b3e-8a85-25af1dced8fd.webp)

![](https://oss.wuxinrom.xyz/fuwari/image/ff48bee9-facd-4ae8-bdb1-f1859ea01999.webp)

以及上周添加用户设备统计代码（但被撤销）：

![](https://oss.wuxinrom.xyz/fuwari/image/3e29b754-2eb3-4e7d-9bf6-340dce54bf07.webp)

鉴于目前有些混乱的情况，包括这家公司的黑历史，请各位 Alist 用户不要更新现有部署，新部署就更不推荐了，Alist 的情况有些担忧。该公司的收购的开源产品不太敢碰，而 Alist 的地位有些特殊。目前好多服务基于 Alist（尤其需要绑定网盘管理文件的服务），也就是说...你躲开了 Alist 本体但不一定躲得开子子孙孙

等待社区解决： Openalist/nlist/blist ...

另外，Alist 使用了私有的 API 服务（原开发者提供的 api.nn.ci ），所以未来不更新可能会导致无法使用。（该 API 提供了很多网盘的 token 申请服务，如果不在提供服务，就需要手动申请各网盘 API）

另外，小雅也是基于 Alist，头大一阵子吧



另外，被称为黑奴、贡献量排名第九的 xrgzs 同学进行了 fork

![](https://oss.wuxinrom.xyz/fuwari/image/8093e041-227b-4a64-8f86-89152ddd7817.webp)

什么是黑奴？

有人根据 Alist 的贡献名单，列出了一张图，并将原主要开发者划去，列出了黑奴榜单

这算不给工资的打黑工嘛？

![](https://oss.wuxinrom.xyz/fuwari/image/49ac4afa-ff58-4c86-ba7c-201cb928cd88.webp)

但是，但是但是：(细节BOT第二位)

![](https://oss.wuxinrom.xyz/fuwari/image/99a23afe-d73d-4c96-9018-e85dc6773dec.webp)

从贡献程度来看，这的确还是一个人的项目，原开发者一个人提交了超过九成的代码

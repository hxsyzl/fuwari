---
title: （国内首发）MTK IMEI 修复教程 For Redmi Note 8 Pro
published: 2025-01-21
description: '把你的IMEI修回来！'
image: './assets/images/imei.jpeg'
tags: [修复IMEI]
category: '刷机救砖'
draft: false 
lang: ''
---

前言  

经过漫长的时间等待，IMEI修复教程总算是来了（麻麻再也不用担心丢了IMEI而烦恼），不需要复杂的手段，就可以将你的手机修好IMEI，最后还是感谢这位老外Tim Josten。不墨迹，直接接下来的内容  

一. 准备工作  

1.一部丢了IMEI的n8p（解锁状态）  
2.电脑和数据线（尽量windows 10及以上）  
3.本文所提到的文件都需要  
4.第三方内核/ROM（kernel或ROM）  

二. 开始制作专属修复imei卡刷包

1.下载好这个压缩包。下载链接；[查看链接](https://wwjo.lanzouy.com/iRXqn0w65lhc "https://wwjo.lanzouy.com/iRXqn0w65lhc")  
2.解压后有以下文件（图1）

![3430069_380b9e7a_7678_3751_568@1920x1030.jpeg.m.jpg](assets/images/26f995f504e7fac7bac1574018d5f6714c3c26b2.jpg)



3.打开config.txt（如图2-3）

![3430069_87c9fe26_7678_376_56@1920x1030.jpeg.m.jpg](assets/images/59b4c8277b83c8cb75e9947c1659fd2f03372c9d.jpg)



![3430069_dcfdd3ff_7678_3766_364@1423x740.jpeg.m.jpg](assets/images/764e73fce12b6fc6748be028699e9ceb641a54d9.jpg)



4.解释一下各参数的用途吧  
①cpidid=设备芯片的ID，每个手机的芯片ID都不一样，所以要如实填写（不要老想着用别人的，出问题了就不能怪自己）  
问；如何获取芯片ID？  
第一步，下载并打开termux（酷安或者百度都可以）  
第二步；输入getprop ro.boot.chipid回车  
第三步；出现图片中的结果就表示获取成功

![3430069_0cf6acc8_7678_377_97@1080x2340.jpeg.m.jpg](assets/images/07656050838c3869233a1c7327a15ef2670c77da.jpg)

本次教程就到这里，该说的我已经说了，要是还不会的话，那我没办法（解锁和刷入第三方twrp应该都会了吧）
强制解锁教程可以参考我；查看链接
TWRP资源可以去我站点下载
如果有其他问题，请在评论区底下进行交流，不懂的我看到了一般会回复，教程结束

②第二和第三就不用说了，自己填（可以是自己的原机imei，也可以像我一样随便填MIUI系统  
第一步，打开设置→我的设备→全部参数  
第二步，找到状态信息→就可以查看这两个MAC地址的详细信息，也是把它复制出来，填到这个配置文件就可以  
操作流程如下（图）

![3430069_5ea81a9d_7678_3774_493@1080x2340.jpeg.m.jpg](assets/images/4670f132e39eb8d1233a4892ae241c0f42b431f0.jpg)



![3430069_b29d22ee_7678_378_889@1080x2340.jpeg.m.jpg](assets/images/8f369d0a168352800980f4251a57816d78f76406.jpg)

![3430069_9958aacc_7678_3788_576@1080x2340.jpeg.m.jpg](assets/images/2eac2a466b707524287030be886c25c12f5fe582.jpg)



![3430069_2fc5dba4_7678_3846_922@1080x2340.jpeg.m.jpg](assets/images/ced734ab7293500ff4734931b38d015a2e5386df.jpg)





问；为什么会显示无法获取？  
就是因为没有打开WIFI和蓝牙功能，打开之后就可以正常获取了  
原生系统  
操作流程跟MIUI差不多，我这里就不发图片了  
5.配置文件全部填完之后保存  
6.直接双击打开mtk_imei.cmd，显示图片中的结果就是制作完成（图）

![3430069_f3ebdc62_7681_8186_657@1223x639.jpeg.m.jpg](assets/images/86103f65f81e018ffef7d2500e94e840a43fe8cd.jpg)





7.完成之后关闭窗口，你会得到一个修补好的卡刷包，使用twrp刷入即可

![3430069_028139c7_7681_8193_358@1920x1030.jpeg.m.jpg](assets/images/64a66b3554bba2a074d76166e7286becfe703da8.jpg)



8.最后就会看到你修复好的IMEI

三. 其他重要说明  

1.本修复教程适用所有基于ROSS的ROM（包括MIUI12.5所有版本，基于这个底层的第三方ROM和类原生）  
2.不适用基于QOSS及以下的ROM（包括miui10.miui11.miui12和基于这个底层的第三方ROM以及类原生）  
3.不适用基于cfw底包的原生系统使用  
4.如果你的WINDOWS缺少Visual C++ Redistributable for Visual Studio 2015(x64)，请点击下方链接下载并安装（如果有了请忽略）  
下载链接；X64；[查看链接](https://wwjo.lanzouy.com/ilfES0w6apmb "https://wwjo.lanzouy.com/ilfES0w6apmb")  
X86；[查看链接](https://wwjo.lanzouy.com/i1wMD0w6aq4j "https://wwjo.lanzouy.com/i1wMD0w6aq4j")  
5.切换ROM时，请确保在刷入ROM后立即刷入“imei_repair.zip”文件，然后再进行第一次开机。这是必要的，因为删除系统分区将需要你再次刷入修复包  
6.官方内核可能会不工作，请使用第三方内核（我的内核已经集成了，到时候再编译一遍不带root的供你们使用）  
7.本教程仅适用Redmi Note 8 Pro，其他机型能不能用我不清楚（自己试试就可以了）  

要求就是内核版本必须是4.14的，而且集成了这个模块  
链接；[查看链接](https://github.com/AgentFabulous/begonia/commit/111f687d092b7fd1ccc64710795035ef30520629 "https://github.com/AgentFabulous/begonia/commit/111f687d092b7fd1ccc64710795035ef30520629")

四.目前状态  
小米账号与小米云服务已正常使用（包括查找手机），其他的就留给你们测试了

五.修复成功截图

![3430069_fc59e41f_7681_8201_565@3325x2494.jpeg.m.jpg](assets/images/1df051d269bd4a2b7355289aa60250d98773e98a.jpg)



![3430069_7adbaa43_7681_8203_974@3325x2494.jpeg.m.jpg](assets/images/f50782ad13660be05f193a96c1bf756364fb9061.jpg)



![3430069_bdd41412_7681_8208_944@3325x2494.jpeg.m.jpg](assets/images/fd421820e00334ac4ca954a11b1b03fe771311a2.jpg)



![3430069_e6586423_7681_8216_798@3325x2494.jpeg.m.jpg](assets/images/38c93e10982a8a4b0f2eee4853a5b964f6cbc1e9.jpg)











本次教程就到这里，该说的我已经说了，要是还不会的话，那我没办法（解锁和刷入第三方twrp应该都会了吧）  
强制解锁教程可以参考我；[查看链接](https://www.coolapk.com/feed/31977436?shareKey=MGRkOTUyMmQ5NmExNjQ2MGFkYjM~&shareUid=3430069&shareFrom=com.coolapk.market_13.1.3 "https://www.coolapk.com/feed/31977436?shareKey=MGRkOTUyMmQ5NmExNjQ2MGFkYjM~&shareUid=3430069&shareFrom=com.coolapk.market_13.1.3")  
TWRP资源可以去我站点下载  
如果有其他问题，请在评论区底下进行交流，不懂的我看到了一般会回复，教程结束

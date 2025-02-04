---
title: 几分钟，让Deepseek接入QQ！
published: 2025-02-04
description: '使用Koishi+chatluna带来丰富可玩性'
image: 'https://p.qlogo.cn/gh/282381753/282381753/640'
tags: [chatluna]
category: 'koishi'
draft: false 
lang: ''
---

# 介绍[​](https://chatluna.chat/guide/introduction.html#%E4%BB%8B%E7%BB%8D)

[ChatLuna](https://github.com/ChatLunaLab/chatluna) 是一款强大的语言模型聊天服务插件，基于 [LangChain](https://github.com/langchain-ai/langchainjs) 开发，目前作为 [Koishi](https://koishi.chat/zh-CN/) 上的插件存在。ChatLuna 支持与多种主流大语言模型进行交互，如 OpenAI、Google Gemini 和 Claude 等。

ChatLuna 不仅为用户提供了模型聊天功能，还为其他 Koishi 插件开发者提供了便捷的 [LangChain Model](https://js.langchain.com/docs/concepts/#chat-models) 接口，方便他们与大语言模型进行交互和扩展开发



## 安装插件

在使用 ChatLuna 之前，你需要安装 Koishi。

按照 [Koishi 官方文档](https://koishi.chat/zh-CN/) 来安装 Koishi。

> [!TIP] 提示
> 社区成员为 Windows 和 Linux 提供了一键安装脚本，该脚本可以一键自动安装 Koishi 以及 ChatLuna。
> 项目地址：https://github.com/hxsyzl/chatluna-install-auto
> 
> 

#### 数据库服务

ChatLuna 需要 `database` 服务，用于存储会话信息等持久化数据。

我们推荐使用 `database-sqlite`，它自带在大部分 Koishi 环境里，已被默认安装并启用。

你也可以安装并配置其他在 Koishi 插件市场上的数据库插件，如 MySQL、MongoDB 等。

#### 

#### 可选服务

这些服务是为了 ChatLuna 的某些功能而额外需要的服务。你可以根据需要选择安装。

- `censor` 服务：用于回复内容过滤。注意，有的插件不审核文本信息，请注意识别。
- `vits` 服务：用于渲染模型回复，生成语音。



# DeepSeek[​](https://chatluna.chat/guide/configure-model-platform/deepseek.html#deepseek)

DeepSeek 是一家专注于通用人工智能底层模型与技术研究的公司，成立于2023年，由知名私募巨头幻方量化创立。公司致力于探索人工智能的本质，发布了多个开源大模型，包括 DeepSeek-LLM 通用大语言模型和 DeepSeek-Coder 代码大模型等。

我们可以安装 `openai-deepseek-adapter` 适配器来使用该公司提供的模型。



## 安装

前往插件市场，搜索 `chatluna-deepseek-adapter`，安装即可。

::: tip 提示
如果无法正常搜索到 `chatluna-deepseek-adapter`，则说明官方插件源没有正常更新。
前往 market 插件设置为其他源即可：

![](https://oss.wuxinrom.xyz/fuwari/image/937485e4-24fd-419b-be86-258bec9d328b.webp)

以下是推荐的一些插件源：

- [https://koishi-registry.yumetsuki.moe/index.json](https://koishi-registry.yumetsuki.moe/index.json)
- [https://kp.itzdrli.cc]([https://kp.itzdrli.cc)

:::

## 配置

在配置之前，请先前往 [DeepSeek](https://platform.deepseek.com/api_keys) 获取 API key。

::: tip 提示
未来我们可能会录制官方教程，敬请期待。
:::

获取到 API key 后，转到 `deepseek-adapter` 的配置页面。
。
当然，你也可以更改你喜欢的其他平台名。

完成后在请求设置里填入你的 API key 和 请求地址。请求地址应为 `https://api.deepseek.com/v1`。

![](https://oss.wuxinrom.xyz/fuwari/image/6c4bf5fc-81be-4d53-8ec9-52adc995c069.webp)

记得点击右上角的保存按钮。

## 使用

在适配器的配置页面，点击运行按钮，如无误，你应该看不到任何错误 log，那即可转到 ChatLuna 的主插件页面。

在主插件页面，下划到 模版房间选项，查看 defaultModel 的选项里是否含有 DeepSeek 模型，如果有，则说明你已经成功地接入了 DeepSeek 平台



## 安装NapCat

NapCat有着众多启动方式，每种方式各有优点：

- **Shell 版本**：具有低内存、服务器部署简单的特点。
- **Framework 版本**：具有方便人机交互、便于窥屏的特点
  
  (在这里Framework不做介绍，感兴趣的可以自行搜搜)



### Shell 启动/安装方式

## NapCat.Shell - Win手动启动教程

1. 前往 [NapCatQQ 的 release 页面](https://github.com/NapNeko/NapCatQQ/releases) 下载NapCat.Shell.zip解压
2. 确保QQ版本安装且最新
3. 双击目录下launcher.bat即可启动 如果是win10 则使用launcher-win10.bat

<mark>如果需要快速登录 将 QQ 号传入参数即可</mark>

::: code-group

```bash
launcher.bat 123456
```

```bash
launcher-win10.bat 123456
```

:::

## NapCat.Win.一键版本

特殊说明: 一键版仅适用 `Windows.AMD64` 无需安装QQ和NapCat 已内置

1. 前往 [NapCatQQ 的 release 页面](https://github.com/NapNeko/NapCatQQ/releases) 下载无头绿色版本解压
2. 启动对应BAT即可

<mark>如果需要快速启动 新建Bat文件写入如下例子</mark>

::: code-group

```bash
NapCatWinBootMain.exe 10001
```

:::

## NapCat.Installer - Linux一键使用脚本(支持Ubuntu 20+/Debian 10+/Centos9)

::: code-group

```bash
curl -o napcat.sh https://nclatest.znin.net/NapNeko/NapCat-Installer/main/script/install.sh && sudo bash napcat.sh
```

```bash
curl -o napcat.sh https://nclatest.znin.net/NapNeko/NapCat-Installer/main/script/install.sh && sudo bash napcat.sh --tui
```

```bash
curl -o napcat.sh https://nclatest.znin.net/NapNeko/NapCat-Installer/main/script/install.sh && sudo bash napcat.sh --docker y --qq "123456789" --mode ws --proxy 1 --confirm
```

```bash
curl -o napcat.sh https://nclatest.znin.net/NapNeko/NapCat-Installer/main/script/install.sh && sudo bash napcat.sh --docker n --cli n --proxy 0 --force
```

:::



<details>

  <summary>命令选项(高级用法)</summary>

  0. --tui: 使用tui可视化交互安装

  1. --docker [y/n]: --docker y 为使用docker安装反之为shell安装

  2. --qq \"123456789\": 传入docker安装时的QQ号

  3. --mode [ws|reverse_ws|reverse_http]: 传入docker安装时的运行模式

  4. --confirm: 传入docker安装时的是否确认执行安装

  5. --proxy [0|1|2|3|4|5|6]: 传入代理, 0为不使用代理, 1为使用内置的第一个,不支持自定义, docker安装可选0-7, shell安装可选0-5

  6. --cli [y/n]: shell安装时是否安装cli

  7. --force: 传入则执行shell强制重装

</details>

仓库地址: [NapCat.installer](https://github.com/NapNeko/NapCat-Installer)



## NapCat.Docker - Linux容器化部署

仓库地址: [NapCat.Docker](https://github.com/NapNeko/NapCat-Docker)



## 安装OneBot插件

前往Koishi的插件市场搜搜adapter-onebot下载安装即可

在QQ号那一栏填写QQ号，最后开启即可

![](https://oss.wuxinrom.xyz/fuwari/image/557fbd70-1373-4540-ac78-c0c0e35b6db9.webp)

## 通过 WebUI 配置OneBot服务（NapCat)

如果你已经启动了 NapCat，并且有多于 1 个开放端口，则可以通过 WebUI 进行配置。

默认地址为 `0.0.0.0`，即监听所有地址。当配置了不可用的地址时 WebUI 将被禁用。

默认端口为 `6099`。

当端口被设置为 `0` 时将禁用 WebUI。

当端口被占用时，会自动对端口 +1，直到找到可用端口（最多尝试100次，失败则会禁用 WebUI），端口号会在启动日志中显示。

启动后可在启动日志中看到形如 `[WebUi] WebUi Local Panel Url: http://127.0.0.1:6099/webui?token=xxxx` 的token信息。

也可打开 `webui.json` 文件，在其中找到token

::: code-group

```json5
{

    "host": "0.0.0.0", // WebUI 监听地址

    "port": 6099, // WebUI 端口

    "token": "xxxx", //登录密钥，默认是自动生成的随机登录密码

    "loginRate": 3, //每分钟登录次数限制

}
```

:::

访问 `http://ip:port/webui/`，然后进行以下操作：

1. 进入 QQ 登录，点击 `QRCode` 进行二维码登录。

2. 登录成功后，即可进入网络配置。

3. 配置完成后，点击保存，重启即可生效。





最后你的Koishi右下角会变成这样

![](https://oss.wuxinrom.xyz/fuwari/image/754bb8d4-05f6-4965-8dc9-40a9e69b8170.webp)

去QQ找你的机器人对话就好了

有疑问可以进入282381753

插头露娜（chatluna）的官方交流群

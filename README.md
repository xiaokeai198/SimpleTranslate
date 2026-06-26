# SimpleTranslate 2.0 / 简单翻译 2.0

**SimpleTranslate（简单翻译）** 是一个 Minecraft 客户端文本翻译模组，适合游玩外语地图、RPG 服务器、剧情整合包、任务书、物品 Lore、告示牌和各种游戏 UI 提示。

**2.0 版本支持所有模型/API 支持的语言互转。**  
它不是只能英译中。只要你配置的翻译模型支持，就可以进行英译中、中译英、日译中、韩译中、多语言混合文本翻译，或任意源语言到任意目标语言的转换。

> 当前公开发布的 2.0 版本：**仅提供 Fabric 构建**。

[下载 SimpleTranslate 2.0](https://github.com/xiaokeai198/SimpleTranslate/releases/tag/v2.0)

---

## 2.0 有什么不同

SimpleTranslate 2.0 将翻译架构重构为 Minecraft **Component JSON** 管线。

旧式翻译通常会把游戏文本压平成普通字符串，翻译后再尝试猜测颜色、样式和位置；这很容易让复杂文本出现颜色错位、结构丢失、悬浮提示混乱等问题。

2.0 会尽量把 Minecraft 原生文本组件交给模型翻译，并接收翻译后的 Component JSON，再作为游戏组件显示。这让它更适合保留：

- 颜色与格式；
- 换行与文本层级；
- 物品 Lore 结构；
- 聊天与书本悬浮提示结构；
- 告示牌布局；
- 书本页面顺序；
- 聊天格式；
- HUD、标题、ActionBar 文本；
- 成就名称与描述。

一句话：**让 Minecraft 里的文本变成你能读懂的语言，同时尽量保持它原本就该有的样子。**

---

## 主要功能

### 聊天翻译

翻译服务器消息、RPG 菜单文本、旁白提示、任务提示和带格式的聊天内容。

聊天中的隐藏悬浮提示会走独立的悬浮提示翻译路径，不会在翻译可见聊天时被顺手翻译，从而减少不必要的 Token 消耗和结构污染。

![聊天原文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-chat-before.png)

![聊天译文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-chat-after.png)

### 物品提示翻译

翻译物品名称、属性、Lore、NBT 相关提示和复杂彩色物品描述。

适合 RPG 服务器、自定义装备、冒险地图、剧情整合包和大量英文物品说明的场景。

### 告示牌翻译

支持单个告示牌或连续告示牌组翻译，适合地图说明、剧情墙、服务器规则板、谜题提示和场景介绍。

![告示牌原文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-sign-before.png)

![告示牌译文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-sign-after.png)

### 书本翻译

支持书本页面翻译，适合剧情书、任务书、说明书和服务器百科内容。

![书本原文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-book-before.png)

![书本译文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-book-after.png)

### 成就翻译

翻译成就/进度的名称和描述。

![成就原文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-advancement-before.png)

![成就译文](https://github.com/xiaokeai198/SimpleTranslate/releases/download/v2.0/demo-advancement-after.png)

### 更多游戏文本

SimpleTranslate 还支持翻译：

- Boss 血条；
- 计分板；
- 标题与副标题；
- ActionBar 动作栏文本；
- 实体名称；
- 文字展示实体；
- 物品悬浮提示；
- 聊天/书本悬浮提示；
- 模组支持的其他 Minecraft UI 文本表面。

---

## 所有语言互转

SimpleTranslate 不锁定固定语言对。

你可以在设置中配置目标语言，并使用任意兼容的翻译服务/模型完成翻译。

示例：

- 英文 -> 中文；
- 中文 -> 英文；
- 日文 -> 中文；
- 韩文 -> 中文；
- 多语言混合文本 -> 中文；
- 任意模型支持的源语言 -> 任意模型支持的目标语言。

实际翻译质量取决于你配置的模型/API。

---

## 缓存、Token 统计与显示原文

SimpleTranslate 提供适合长时间游玩的辅助功能：

- 持久化翻译缓存；
- 共享缓存；
- 请求数与 Token 统计；
- 可配置翻译服务/API/模型；
- 按住快捷键临时显示原文。

“按住显示原文”适合校对译文、查看原始文本、截图对比，或者在复杂场景里临时回到原文。

---

## Fabric 支持版本

SimpleTranslate 2.0 当前提供以下 Fabric 版本：

- 1.19.2、1.19.3、1.19.4；
- 1.20、1.20.1、1.20.2、1.20.3、1.20.4、1.20.5、1.20.6；
- 1.21、1.21.1、1.21.2、1.21.3、1.21.4、1.21.5、1.21.6、1.21.7、1.21.8、1.21.9、1.21.10、1.21.11；
- 26.1、26.1.1、26.1.2、26.2。

请从 [2.0 Release 页面](https://github.com/xiaokeai198/SimpleTranslate/releases/tag/v2.0) 下载与你的 Minecraft 版本匹配的 jar。

---

## 安装需求

- Minecraft Java Edition；
- Fabric Loader；
- Fabric API；
- 客户端安装；
- Mod Menu 可选，但推荐安装，方便打开设置界面；
- 一个可用的翻译服务/API/模型。

---

## 注意事项

- SimpleTranslate 是客户端辅助模组，服务器不需要安装。
- 翻译速度、质量和 Token 消耗取决于你配置的服务商、模型和网络环境。
- 如果希望复杂格式文本更稳定，建议使用更擅长遵循 JSON/结构化输出的模型。

---

# English Overview

SimpleTranslate 2.0 is a client-side Minecraft translation mod for foreign-language maps, RPG servers, adventure content, quest books, item lore, signs, and UI prompts.

It can translate between **any languages supported by your configured model/API**, not only English to Chinese.

This public 2.0 release currently provides **Fabric builds only**.

## Key Features

- Component JSON based translation pipeline.
- Chat, item tooltip, sign, book, advancement, HUD/title/actionbar, scoreboard, boss bar, entity name, and hover tooltip translation.
- Better preservation of colors, line breaks, formatting, and Minecraft text structure.
- Persistent cache, shared cache, token statistics, configurable providers, and hold-to-show-original behavior.

Download: [SimpleTranslate 2.0 Release](https://github.com/xiaokeai198/SimpleTranslate/releases/tag/v2.0)

MC百科: [简单翻译](https://www.mcmod.cn/class/23154.html)

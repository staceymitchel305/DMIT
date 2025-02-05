# 使用 Poe API 打造专属 Telegram AI 智能助手

## 前言
一位订阅者分享了他开发的 Telegram Bot，该机器人支持调用 Poe API，并且已在 GitHub 上开源。目前，Poe API 可以无限调用（限于个人使用，禁止滥用或商用），前提是你需要订阅 Poe 会员服务。相比 OpenAI API，调用 Poe API 无需额外费用，这对于开发者来说是一个巨大的优势。

## Poe 简介
Poe 是一个 AI 聊天平台，提供了多种 AI 模型供用户选择。然而，Poe 平台上的积分消耗速度非常快，尤其是在使用高级模型如 Claude 和 GPT-4 时。为了更经济地使用这些 AI 模型，我们可以利用 Poe 会员 API 来制作自己的 Telegram 聊天机器人。

## 🔗 项目地址
作者已经开源了一个简单的 Poe Telegram 聊天机器人项目，项目地址为：[https://github.com/Timmy-web/Poe-Telegram-Chatbot](https://github.com/Timmy-web/Poe-Telegram-Chatbot)。目前，这个机器人仅支持纯文字交互，暂时不支持上传图片文件等功能。内置的 AI 模型包括 Claude-3-Opus 和 GPT-4，但理论上 Poe 平台上的所有模型都可以使用，只需要在代码中进行相应的修改即可。

## ⚡️ 优势
1. **API 无需额外付费**：使用 Poe 会员 API 调用 AI 模型，不会消耗账号积分。这意味着你可以免费使用这些强大的 AI 模型，而不用担心积分被快速消耗完。
2. **避免积分涨价**：Poe 平台上的积分会出现涨价的情况。例如，3 月 7 日时，Claude-3-Opus 的价格为每条 750 积分，Claude-3-Opus-200k 的价格为每条 1875 积分。但到了 3 月 9 日，Claude-3-Opus 的价格涨到了每条 1000 积分，Claude-3-Opus-200k 的价格更是涨到了每条 6000 积分。使用 API 可以避免这种价格波动的影响。
3. **不会消耗对话次数**：Poe 平台是按照对话次数收费，而不是按照字数收费。使用 API 调用 AI 模型，不会消耗对话次数，因此可以尽情与 AI 聊天，而不用担心费用问题。

## 💻 Demo 演示
以下是使用不同模型的演示截图：

### 默认 Claude-3-Opus 模型
![其他模型例子（未做优化）](https://bbtdd.com/img/5373250994529024.webp)

### CafeMaid 模型
![Poe 官方客户端](https://bbtdd.com/img/93933599.webp)
![Telegram Bot 对话窗](https://bbtdd.com/img/20997064627.webp)

### DALL-E-3 模型
![Poe 官方客户端](https://bbtdd.com/img/57012657396217.webp)
![Telegram Bot 对话窗](https://bbtdd.com/img/009552013.webp)

## ⚠️ 注意事项
根据官方文档，API 可能会带来消息限制。不过开发者认为目前个人或者给几个朋友使用应该没什么影响。

![Poe 官网的注意事项](https://bbtdd.com/img/66120800524.webp)

## 🎙️ 开发者对未来的展望
我希望有更多的开发者能够参与到这个项目中来，帮助完善和优化这个聊天机器人。例如，可以添加上传图片文件的功能，优化代码结构和性能等。让我们一起为这个项目贡献自己的力量，创造出一个更加强大和实用的 Telegram 聊天机器人！

如果你对这个项目感兴趣，欢迎访问 GitHub 仓库，给个 Star，并参与到项目的开发中来。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)
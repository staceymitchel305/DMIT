# Cursor 代码生成器中文使用教程：新手入门完全指南

最近，我开始使用 Cursor 编程工具，之前一直依赖 GPT-4 和 Claude 3.5 通过对话获取代码。自从用上 Cursor 代码生成器，完全替代了复制粘贴的繁琐操作，直接通过对话生成代码，极大提高了开发效率。本文将基于我的使用体验和网上整理的功能说明，为大家带来这份新手入门完全指南！

## 什么是 Cursor？

Cursor 是由 Anysphere 实验室开发的代码编辑器，它集成了 GPT-4、Claude 3.5 等先进 LLM（大语言模型），可以理解为在 VSCode 中集成了 AI 辅助编程助手。从界面布局和使用操作来看，Cursor 与 VSCode 基本一致，包括扩展下载、Python 编译器配置、远程服务器连接和设置等。如果你是资深 VSCode 用户，那么恭喜你，可以直接无缝衔接 Cursor。

![Cursor 与 VSCode 对比](https://bbtdd.com/img/469159417768.webp)

Cursor 与 VSCode 的最大不同在于它内置了 AI 进行代码协作。为此，它对 VSCode 进行了诸多优化，使其体验比在 VSCode 上使用 GitHub Copilot 等插件更加舒适。

## Cursor 新手入门指南

### Cursor 安装

Cursor 需要从其官网下载。下载完成后，需注册才能使用，支持 Google 和 GitHub 账号登录。

![Cursor 下载页面](https://bbtdd.com/img/99055586442.webp)

注册完成后，你将拥有一个专属账号，每个账号的模型调用次数有限。其中，GPT-4 和 Claude 3.5 的免费调用次数为 500 次。Cursor 采取订阅制，新用户可以试用两周的 Pro 订阅，后续每月需支付 20 美元。

![Cursor 订阅页面](https://bbtdd.com/img/6534874970.webp)

安装完成后，Cursor 会在首次启动时提示你是否导入 VSCode 配置。导入后，你将拥有一款 AI 增强版的 VSCode。首次使用时，记得设置中文，操作步骤与 VSCode 一致：

> 点击最上面的框，输入 `>language`，可以配置简体中文。

![Cursor 设置中文](https://bbtdd.com/img/08553068510283.webp)

### 配置模型

Cursor 内置了多种 LLM，包括最先进的 GPT-4、Claude 3.5 和 OpenAI 最新发布的推理模型 o1-preview 和 o1-mini。在右上角的设置中即可打开相应模型进行辅助编程。

![Cursor 模型配置](https://bbtdd.com/img/6965522572.webp)

## Cursor 键盘快捷键

通过以下 Cursor 键盘快捷键，你可以显著提高生产力。本速查表涵盖了 Cursor 的 AI 驱动功能的关键命令，包括 Cursor Tab、Cmd K、聊天、Composer 和 @ 符号。注意：Windows/Linux 上使用 Ctrl，macOS 上使用 ⌘（Command）。

### Cursor Tab（AI 代码补全）

- 打开 Cmd K：`Ctrl/⌘ + K`
- 应更改：`Ctrl/⌘ + ↵`
- 取消/删除更改：`Ctrl/⌘ + ⌫`

### 聊天界面

- 打开聊天：`Ctrl/⌘ + L`
- 将代码添加到聊天：`Ctrl/⌘ + L`

### Composer

- 打开 Composer：`Ctrl/⌘ + I`
- 打开全屏 Composer：`Ctrl/⌘ + Shift + I`

### @ 符号

- 通用

## Cursor 常用功能说明

### Command K

让你使用 AI 编辑和编写代码。要编辑，只需选择一些代码，点击「Edit」，并描述代码应如何改变。要生成全新代码，只需在没有选择任何内容的情况下输入 Command K。

![Command K 功能](https://bbtdd.com/img/1600090778491.webp)

### Copilot++

Cursor 的原生自动完成功能。它是 Copilot 的增强版，可以建议中间行的完成和整个差异。它使用了一个定制模型，专门训练来预测代码库中的下一个编辑。

![Copilot++ 功能](https://bbtdd.com/img/3786617488293391.webp)

### Chat

让你可以与一个能看到你代码库的 AI 进行对话。聊天始终能看到你当前的文件和光标，因此你可以问它问题，比如：「这里有错误吗？」。你可以使用 `Command + Shift + L` 或 @ 符号将特定代码块添加到上下文中。你还可以使用 `Command + Enter` 与整个代码库进行聊天。

![Chat 功能](https://bbtdd.com/img/177163654263877.webp)

### @ 符号

让你轻松向 AI 展示代码。尝试在 `Command + K` 或聊天中输入 @，以获取文件夹中所有文件和代码符号的下拉列表。你可以使用它生成具有特定依赖项的代码（如「使用与@ErrorPopup 相同的样式」）或询问文件（如「@inlineDiffService.ts 做什么」）。



### Codebase Answers

让你可以向 AI 询问整个代码库的问题。要使用此功能，请在聊天中输入 `Command + Enter` 或点击输入框中的「with codebase」按钮。你可以问问题，如「撤销重做逻辑在哪里？」或「我们如何在客户端处理身份验证令牌？」。

![Codebase Answers 功能](https://bbtdd.com/img/43182489.webp)

### Docs

该功能能够提高 AI 对第三方库的理解。要使用 Docs，请在聊天或 `Command K` 中输入 `@LibraryName`。要让 Cursor 爬取自定义文档，请在 `Command K` 或聊天中输入 `@Add`，并指定爬取的起点和所有 URL 应遵循的前缀。

![Docs 功能](https://bbtdd.com/img/64634345.webp)

### Auto-Debug

Auto-debug 是一个用于在 Cursor 的终端中修复错误的代理。要使用它，请在终端错误后点击蓝色的「Auto-debug」按钮。点击后，AI 将查看你的文件，并尝试解决问题。

![Auto-Debug 功能](https://bbtdd.com/img/585101883046216.webp)

### Fix Lints

Cursor 帮助你快速修复 lint 错误。只需将鼠标悬停在任何 lint 错误上，然后点击出现的蓝色「Fix」按钮。AI 回应将出现在聊天中，再也不用对着复杂的 TypeScript 或 Rust 错误挠头了！

![Fix Lints 功能](https://bbtdd.com/img/9673229673450.webp)

## @ 符号常见功能

为了更方便地向大语言模型提供上下文信息，Cursor 内置了多种 `@` 注记，使用 `@` 注记能够方便地注入不同类型的上下文信息到对话中。

> 注：事实上 GitHub Copilot 也有类似功能，但没有 Cursor 齐全好用。

### 1. `@Files` 注记，传递指定代码文件的上下文

当你在对话框输入 `@Files` 注记时，Cursor 会自动弹出代码仓库的检索列表，你可以输入文件名，按下确认键后，相应文件的内容将自动注入到上下文中。

![@Files 功能](https://bbtdd.com/img/3969141531.webp)

### 2. `@Code` 注记，传递指定代码块的上下文

`@Code` 注记提供更精确的代码片段，使用方法与 `@Files` 类似，只需在检索框中输入关键词并选择相应的代码块即可。

![@Code 功能](https://bbtdd.com/img/882956751879.webp)

### 3. `@Docs` 注记，从函数或库的官方文档获取上下文

`@Docs` 注记能够从函数或库的官方文档中获取上下文。目前，它只能从在线文档中提取信息，因此你自己的 JSDoc 等文档除非有线上地址，否则无法使用。

![@Docs 功能](https://bbtdd.com/img/251850934744220.webp)

### 4. `@Web` 注记，从搜索引擎的搜索结果获取上下文

`@Web` 注记会默认将你的提问先向搜索引擎进行搜索，然后从搜索结果中提取上下文喂给 LLM。但由于具体实现方式不明，使用效果有时不太稳定。

### 5. `@Folders` 注记，传递文件目录信息的上下文

`@Folders` 注记能够提供文件目录的相关信息，特别适合在遇到路径问题时使用。

![@Folders 功能](https://bbtdd.com/img/8236489281191916.webp)

### 6. `@Chat` 注记，只能在文件内的代码生成窗口中使用

`@Chat` 注记能够在代码生成窗口（`CTRL + K` 打开的窗口）中将右边打开的对话窗口内容作为上下文传递给大模型。

![@Chat 功能](https://bbtdd.com/img/21872740287.webp)

### 7. `@Definitions` 注记，只能在文件内的代码生成窗口中使用

`@Definitions` 注记会将光标停留行中涉及的变量或类型的相关定义传递给大模型，类似于 `@Code` 注记。

![@Definitions 功能](https://bbtdd.com/img/83175416587.webp)

### 8. `@Git` 注记，只能在对话窗口中使用

通过 `@Git` 注记，你可以将当前 Git 仓库的 commit 历史作为上下文传递给大模型，特别适合代码协作时查找问题。

### 9. `@Codebase` 注记，只能在对话窗口中使用，用于在代码仓库中扫描文件

`@Codebase` 注记能够从代码仓库中扫描并传入你想要的文件的上下文，但使用频率较低，因为它需要设置过滤条件。

![@Codebase 功能](https://bbtdd.com/img/68208995.webp)

## 总结

本文详细介绍了 Cursor 的下载和使用，帮助新手快速上手。Cursor 集成了 LLM 的编译器，功能更加强大且易于上手。在使用一段时间后，你会发现它与 GitHub Copilot 相比，能力更全面、更强大。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)
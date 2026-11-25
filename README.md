# AI-Browser

**English** | [中文](#中文)

Official releases for AI Browser — a browser where the web becomes a workspace you can see, arrange, and control through conversation.

---

## Table of contents

- [Overview](#overview)
- [Quick start](#quick-start)
- [Canvas: work with pages together](#canvas-work-with-pages-together)
- [Multiscreen: give the workspace more room](#multiscreen-give-the-workspace-more-room)
- [River: understand the page or act on it](#river-understand-the-page-or-act-on-it)
- [Context: show River what you mean](#context-show-river-what-you-mean)
- [RiverMCP: connect an external assistant](#rivermcp-connect-an-external-assistant)
- [Settings that shape a workflow](#settings-that-shape-a-workflow)
- [Platform notes](#platform-notes)

---

## Overview

Turn the web into a workspace you can see, arrange, and control through conversation.

| Piece | What it does |
| --- | --- |
| **Canvas** | Puts related pages together in a grid of live webpages |
| **Multiscreen** | Gives that workspace more room across displays |
| **River** | Works with the pages you are using |
| **RiverMCP** | Connects the same live browser to an external AI assistant |

The connection is **context**: the active page, your selection, canvas positions, and your next goal. Show River the relevant material and explain the outcome — without copying every passage into a chat or describing every click.

## Quick start

1. **Connect River.** In `Settings > Models`, enter your model name, OpenAI-compatible endpoint, and API key if required, then click **Save model**. Open River on the toolbar and choose the model. Browser control requires a model that supports tool calling.
2. **Build a small workspace.** Choose **New canvas** and a two-page layout. Open a product page in one cell and its delivery or returns page in the other.
3. **Give River a job.** Turn **Agent** on and ask:
   > Read these two pages. Summarize the total cost, delivery time, and return conditions in a comparison table. Read both pages before answering.
4. **Keep working together.** Select an unclear condition and ask what it means. Ask River to open another source in a particular cell, or take over and browse there yourself. Check the context display when changing the page you want to discuss.

## Canvas: work with pages together

A canvas is a grid of **live, interactive webpages**, not a collection of screenshots. Keep sources, comparisons, and the website you are working on visible in one place. Each cell remains a page you can read and interact with.

### Create and shape a workspace

- Choose **New canvas**, then select a grid.
- Click a cell and use the address bar to open its page.
- Use **Canvas layout** to change the arrangement as the task grows.
- Drag the dividers to give a detailed page more room; **double-click a divider** to restore equal proportions.
- **Zoom canvas page** enlarges the focused page, then returns you to the grid when used again.
- The canvas close-page control closes the focused page; **Close canvas** is a separate action in the canvas menu.

### Focus is how you point

Click the page you want to work with. That cell becomes the current page for the address bar and River. "Explain this page" follows the focused cell, not the canvas as a whole.

For work across cells, name the sources or their positions:

> Read the specifications on the left and the warranty on the right. Tell me which advertised features have warranty exclusions.

River receives the canvas membership and cell positions as part of browser context. Ask it to read the relevant pages explicitly — having several pages visible does not mean every page's full contents have already been read.

### Arrange pages through conversation

You can ask River to organize a canvas instead of doing all the setup yourself:

> Create a two-column canvas. Open the documentation link from this page on the left and its getting-started example on the right.

Use positions such as "left", "right", or "top-right" and describe the page you mean. For an existing workspace, say whether you want a page replaced or a new canvas created.

## Multiscreen: give the workspace more room

On Windows, **Span monitors** expands one browser window across selected displays. Combined with Canvas, this lets you spread related pages over a larger working area while keeping one River conversation and one browser context.

### Choose the displays

1. Connect the displays you want to use.
2. Open **Choose monitors**, beside the **Span monitors** button in the window controls.
3. Select **2 screens side by side**, **2 screens stacked**, or **4 screens (2 by 2)**.
4. Assign a different connected monitor to each position, then click **Save and span**.

The monitor choices include their numbers, resolution, and scale. Match the positions to your physical arrangement. AI Browser saves your selection without changing Windows display settings.

Use **Span monitors** again to restore the previous window. If the button is unavailable, check that a second distinct display is connected. Reopen **Choose monitors** if a saved display has been disconnected.

### Pair the screen layout with the canvas

Spanning makes the window larger; Canvas determines how pages divide that space. After spanning, choose a canvas layout and adjust its dividers so the sources you need remain comfortably visible.

You can also describe the combined setup to River:

> Use my saved monitor selection to span the window, then arrange these pages in a two-by-two canvas.

Focus still follows the page you click, regardless of which monitor contains it.

## River: understand the page or act on it

River is connected to the browsing workspace, rather than being a separate chat that needs everything pasted into it.

| What you want | Choose | How to use it |
| --- | --- | --- |
| Understand or question page content | **Agent off** | Ask about the active page, use selected text, and follow supporting citations |
| Navigate, interact, or complete a browsing task | **Agent on** | Describe the outcome; River can read pages and use browser tools |

Change models with the **Model** button. Tool-calling support is configured under **Advanced** in `Settings > Models`.

### Describe the result, not a script of clicks

A useful request identifies the material, the work, and the stopping point:

> Use the delivery information in this canvas to fill the shipping options on the current form. Leave any missing information blank and stop before submitting.

River can read pages, open links, click controls, fill fields, and use connected tools. Website requirements still apply: complete a login or other required manual step yourself, then tell River where to continue.

During a run, follow the tool activity in the conversation. Model-provided thinking appears separately from the answer. Click **Stop** to interrupt; it does not reverse actions already completed.

## Context: show River what you mean

### The active page and open workspace

River receives the active page's identity, selected text when present, and a list of open pages with canvas locations. It can read page content through browser tools as needed.

When several pages have similar titles, identify the site, document, or canvas position. An open-tab list is not the full contents of every tab.

### Pass a passage through selection

Select text on a webpage to bring it into River's context. Use **Explain**, **Translate**, **Verify**, or **Rewrite**, or write your own request about the selection.

> Compare this selected exception with the policy in the right-hand cell. Are they describing the same restriction?

Check the selection card to see exactly which passage your question refers to.

### Include more sources in a page question

- **Agent off:** use **Also read** to select additional available tabs for a question. This is useful when you want a cited explanation spanning several sources without a browser-control workflow.
- **Agent on:** tell River which pages to read and compare. It can use the workspace's tab and cell information to find them. Be explicit when your conclusion depends on more than the active page.

### Inspect or refine the context

Open **View / edit context** to inspect what River receives about the browser. Use it to check the active source, remove an irrelevant detail, or add task-specific background.

Edits affect Agent mode; page-question mode uses the passages it cites. When the page changes, the edit is discarded and context follows the page again. Use `Settings > Instructions` for a preference that should apply to every Agent run, rather than adding it repeatedly to page context.

If information is missing, expand the relevant section or let it finish loading, then ask River to read it again. Content in inaccessible frames or media without transcripts may not be available.

### Combine navigation and conversation

**Auto / Manual** controls how River handles navigation in Agent mode. In **Auto**, River can open pages itself. In **Manual**, it offers links for you to open. Manual is useful when you want to choose the next source while River helps interpret it.

You can alternate between acting yourself and asking River to continue. After navigating or changing a form, state the next goal rather than repeating the entire task:

> I have selected the delivery option. Review the current page against the requirements we discussed, and list anything still missing.

For a new, unrelated task, click **New**. Previous conversations are available in `Settings > Saved chats`. Keep the same conversation when a follow-up depends on the earlier comparison or instructions.

## RiverMCP: connect an external assistant

River is the assistant inside the browser. **RiverMCP** lets an MCP-capable external client, such as a coding assistant, work with the same live browsing session. It can request browser context, read pages, and use browser controls instead of relying only on a pasted URL or screenshot.

### Connect a client

1. Open `Settings > RiverMCP`.
2. Add an HTTP MCP connection in your external client using the displayed local endpoint and token.
3. Use that client's authentication settings for the token; it is **not** your model API key.

For a client on another computer, replace the local address with this computer's IP address and keep the active port shown in Settings. If you change the port or token, click **Apply** and update the client too. Keep AI Browser running while the client is using it.

### Pass the task across applications

Tell the external assistant what browser material to use and what to do with it:

> Read the API documentation open in AI Browser, including the selected example. Use it to implement this request in my project, then open the local preview in the browser.

This connects browser research to work in another application. Be clear about the context to read; do not assume the client has already loaded every page or River's conversation history. Actions from the client affect the live browser workspace.

> **MCP and RiverMCP work in opposite directions.** `Settings > MCP` adds external tools for River to use. `Settings > RiverMCP` gives another assistant access to this browser.

## Settings that shape a workflow

- **Tools** are enabled by default through one switch in `Settings > Tools`.
- In `Settings > General`, under **River**, **Run actions without asking** controls automatic action approval, and **Max tool rounds per run** sets the saved limit for a task. Click **Save** after changing these settings.
- Tool availability, navigation mode, and approval are separate choices: a tool can be available while an action still waits for approval.
- For repeated workflows, `Settings > Skills` can hold a reusable playbook, such as a comparison checklist, so your requests can focus on the material at hand.

## Platform notes

| Feature | Windows | macOS |
| --- | --- | --- |
| Canvas and River | Use the workspace and context workflows above | Use the same workflows |
| Multiscreen window spanning | Use **Choose monitors** and **Span monitors** | The built-in **Span monitors** control is not available |

Find the installed app version in `Settings > About`.

---

# 中文

[English](#ai-browser) | **中文**

AI Browser 官方发布版 —— 一个把网页变成可看、可排布、可用对话控制的工作区的浏览器。

## 目录

- [概览](#概览)
- [快速开始](#快速开始)
- [Canvas：把网页放在一起用](#canvas把网页放在一起用)
- [多屏：给工作区更多空间](#多屏给工作区更多空间)
- [River：理解页面，或直接操作页面](#river理解页面或直接操作页面)
- [上下文：让 River 明白你的意思](#上下文让-river-明白你的意思)
- [RiverMCP：接入外部助手](#rivermcp接入外部助手)
- [影响工作流的设置](#影响工作流的设置)
- [平台说明](#平台说明)

## 概览

把网页变成一个可看、可排布、可用对话控制的工作区。

| 组成 | 作用 |
| --- | --- |
| **Canvas** | 把相关网页放进同一个网格里 |
| **多屏** | 跨显示器给工作区更多空间 |
| **River** | 与你正在使用的页面协同工作 |
| **RiverMCP** | 把同一个实时浏览器接入外部 AI 助手 |

核心是**上下文**：当前页面、你的选中内容、Canvas 位置，以及你的下一个目标。把相关材料展示给 River，说明你想要的结果——不必把每段文字复制进对话，也不必描述每一次点击。

## 快速开始

1. **连接 River。** 在 `设置 > 模型` 中填入模型名称、OpenAI 兼容的接口地址，以及（如需要）API Key，然后点击 **保存模型**。在工具栏打开 River 并选择模型。浏览器控制需要支持 tool calling 的模型。
2. **搭一个小工作区。** 选择 **新建 Canvas** 和一个双页布局。在一个格子里打开商品页，在另一个格子里打开它的配送或退货页。
3. **给 River 一个任务。** 打开 **Agent**，然后提问：
   > 读这两个页面。用对比表格总结总价、配送时间和退货条件。回答前请先读完两个页面。
4. **继续协作。** 选中一段不清楚的条款，问它是什么意思。让 River 在指定格子里打开另一个来源，或者你自己接手在那里浏览。切换要讨论的页面时，检查一下上下文显示。

## Canvas：把网页放在一起用

Canvas 是一个由**实时、可交互网页**组成的网格，不是截图集合。把来源、对比内容和正在操作的网站放在同一处，每个格子都是可以阅读和交互的页面。

### 创建与调整工作区

- 选择 **新建 Canvas**，然后选一个网格。
- 点击某个格子，用地址栏打开它的页面。
- 任务变大时，用 **Canvas 布局** 调整排布。
- 拖动分隔线，给内容详细的页面更多空间；**双击分隔线**恢复等分比例。
- **放大 Canvas 页面** 会放大当前聚焦的页面，再次使用则回到网格。
- Canvas 的关闭页面按钮关闭当前聚焦的页面；**关闭 Canvas** 是 Canvas 菜单里的另一个独立操作。

### 焦点决定你在指向谁

点击你想操作的页面，那个格子就成为地址栏和 River 的当前页面。“解释这个页面”跟随的是聚焦的格子，而不是整个 Canvas。

跨格子工作时，请指明来源或位置：

> 读左边的规格说明和右边的保修条款。告诉我哪些宣传功能不在保修范围内。

River 会收到 Canvas 的成员关系和格子位置作为浏览器上下文的一部分。请明确要求它读取相关页面——多个页面可见，并不代表每个页面的完整内容都已被读取。

### 用对话排布页面

你可以让 River 帮你整理 Canvas，而不必自己一步步设置：

> 创建一个两列 Canvas。把本页的文档链接放在左边，把它的入门示例放在右边。

使用“左边”“右边”“右上角”这类位置词，并说明你指的是哪个页面。对于已有的工作区，请说明是要替换某个页面，还是新建一个 Canvas。

## 多屏：给工作区更多空间

在 Windows 上，**跨屏显示** 可以把一个浏览器窗口扩展到多个选定的显示器。配合 Canvas，就能在更大的工作区域里铺开相关页面，同时保持同一个 River 对话和同一个浏览器上下文。

### 选择显示器

1. 连接你要使用的显示器。
2. 打开窗口控件中 **跨屏显示** 按钮旁的 **选择显示器**。
3. 选择 **2 屏并排**、**2 屏上下** 或 **4 屏（2×2）**。
4. 为每个位置指定一台已连接的显示器，然后点击 **保存并跨屏**。

显示器选项会显示编号、分辨率和缩放比例。请按你的实际摆放来匹配位置。AI Browser 只保存你的选择，不会修改 Windows 的显示设置。

再次点击 **跨屏显示** 可恢复原来的窗口。如果按钮不可用，请检查是否连接了第二台不同的显示器。如果已保存的显示器被断开，请重新打开 **选择显示器**。

### 把屏幕布局和 Canvas 配合起来

跨屏让窗口变大；Canvas 决定页面如何划分这块空间。跨屏之后，选择一个 Canvas 布局并调整分隔线，让需要的来源都保持舒适可见。

你也可以把组合设置直接描述给 River：

> 用我保存的显示器选择跨屏，然后把这些页面排成 2×2 的 Canvas。

无论页面在哪块显示器上，焦点仍然跟随你点击的页面。

## River：理解页面，或直接操作页面

River 与浏览工作区相连，而不是一个需要你把所有内容粘贴进去的独立聊天窗口。

| 你想做什么 | 选择 | 怎么用 |
| --- | --- | --- |
| 理解或询问页面内容 | **Agent 关闭** | 针对当前页面提问、使用选中文本，并跟随引用来源 |
| 导航、交互或完成浏览任务 | **Agent 开启** | 描述想要的结果；River 可以读取页面并使用浏览器工具 |

用 **模型** 按钮切换模型。tool calling 支持在 `设置 > 模型` 的 **高级** 中配置。

### 描述结果，而不是点击脚本

一个好的请求会说明：材料是什么、要做什么、到哪里停。

> 用这个 Canvas 里的配送信息填写当前表单的配送选项。缺失的信息留空，提交前停下。

River 可以读取页面、打开链接、点击控件、填写字段，并使用已连接的工具。网站的要求依然适用：登录或其他必须手动完成的步骤请你自己完成，然后告诉 River 从哪里继续。

运行过程中，可以在对话里查看工具活动。模型提供的思考过程会与答案分开显示。点击 **停止** 可以中断；它不会撤销已经完成的动作。

## 上下文：让 River 明白你的意思

### 当前页面与打开的工作区

River 会收到当前页面的身份信息、

# AI-Browser

**English** | [中文](#中文)

Official releases for AI Browser — a browser where the web becomes a workspace you can see, arrange, and control through conversation.

**Latest release: `{{VERSION}}`** · [Download](https://github.com/honkliu/AI-Browser/releases/latest) · [All releases](https://github.com/honkliu/AI-Browser/releases)

---

## Download and install

**Latest release: v0.1.0** · [All releases](https://github.com/honkliu/AI-Browser/releases)

| Platform | Installer | Requirements |
| --- | --- | --- |
| Windows x64 | [river_browser_0.1.0_x64-setup.exe](https://github.com/honkliu/AI-Browser/releases/download/v0.1.0/river_browser_0.1.0_x64-setup.exe) | Windows 11, x64 |
| Windows on ARM | [river_browser_0.1.0_arm64-setup.exe](https://github.com/honkliu/AI-Browser/releases/download/v0.1.0/river_browser_0.1.0_arm64-setup.exe) | Windows 11 on ARM64 |

1. Download the installer for your platform and run it.
2. Launch AI Browser.
3. Connect a model: `Settings > Models` → enter model name, OpenAI-compatible endpoint, and API key → **Save model**. Browser control requires tool calling.

---

## Overview

| Piece | What it does |
| --- | --- |
| **Canvas** | Puts related pages together in a grid of live webpages |
| **Multiscreen** | Gives that workspace more room across displays |
| **River** | Works with the pages you are using |
| **RiverMCP** | Connects the same live browser to an external AI assistant |

The connection is **context**: the active page, your selection, canvas positions, and your next goal. Show River the material and state the outcome — no pasting passages or describing clicks.

## Quick start

1. **Build a workspace.** Choose **New canvas** and a two-page layout. Open a product page in one cell and its returns page in the other.
2. **Give River a job.** Turn **Agent** on and ask:
   > Read these two pages. Summarize total cost, delivery time, and return conditions in a comparison table. Read both pages before answering.
3. **Keep working together.** Select an unclear clause and ask what it means, or ask River to open another source in a specific cell.

## Canvas: work with pages together

A canvas is a grid of **live, interactive webpages**, not screenshots. Each cell stays a page you can read and interact with.

- **Create:** **New canvas** → pick a grid → click a cell → open its page in the address bar.
- **Reshape:** **Canvas layout** changes the arrangement; drag dividers for more room, **double-click a divider** to restore equal proportions.
- **Zoom:** **Zoom canvas page** enlarges the focused page, then returns you to the grid.
- **Focus:** the cell you click becomes the current page for the address bar and River. "Explain this page" follows the focused cell, not the whole canvas.

For work across cells, name the sources or positions:

> Read the specifications on the left and the warranty on the right. Which advertised features have warranty exclusions?

River receives canvas membership and cell positions as context, but having pages visible does not mean their contents were read — ask explicitly.

You can also have River arrange the workspace:

> Create a two-column canvas. Open the documentation link from this page on the left and its getting-started example on the right.

## Multiscreen: give the workspace more room

On Windows, **Span monitors** expands one window across selected displays, keeping one River conversation and one browser context.

1. Open **Choose monitors** beside **Span monitors**.
2. Select **2 screens side by side**, **2 screens stacked**, or **4 screens (2 by 2)**.
3. Assign a connected monitor to each position → **Save and span**.

Choices show monitor number, resolution, and scale. AI Browser saves the selection without changing Windows display settings. Click **Span monitors** again to restore the previous window.

Spanning enlarges the window; Canvas decides how pages divide it. After spanning, pick a canvas layout and adjust dividers.

## River: understand the page or act on it

| What you want | Choose | How to use it |
| --- | --- | --- |
| Understand or question page content | **Agent off** | Ask about the active page, use selected text, follow citations |
| Navigate, interact, or complete a task | **Agent on** | Describe the outcome; River reads pages and uses browser tools |

Switch models with the **Model** button. Tool-calling support is configured under **Advanced** in `Settings > Models`.

Describe the result, not a script of clicks:

> Use the delivery information in this canvas to fill the shipping options on the current form. Leave missing information blank and stop before submitting.

River can read pages, open links, click controls, fill fields, and use connected tools. Complete logins or required manual steps yourself, then say where to continue. Click **Stop** to interrupt a run; it does not reverse completed actions.

## Context: show River what you mean

- **Active page and workspace:** River receives the active page's identity, selected text, and a list of open pages with canvas locations. It reads content through browser tools as needed.
- **Selection:** select text to bring it into context, then use **Explain**, **Translate**, **Verify**, **Rewrite**, or your own request.
- **More sources:** with **Agent off**, use **Also read** to add tabs to a question; with **Agent on**, tell River which pages to read and compare.
- **Inspect:** **View / edit context** shows what River receives. Edits apply to Agent mode and are discarded when the page changes. Use `Settings > Instructions` for preferences that should apply to every run.
- **Navigation:** **Auto** lets River open pages; **Manual** offers links for you to open.

For a new, unrelated task, click **New**. Past conversations are in `Settings > Saved chats`.

## RiverMCP: connect an external assistant

**RiverMCP** lets an MCP-capable external client work with the same live browsing session.

1. Open `Settings > RiverMCP`.
2. Add an HTTP MCP connection in your client using the displayed local endpoint and token.
3. Use the client's authentication settings for the token — it is **not** your model API key.

For a client on another computer, replace the local address with this computer's IP and keep the active port. Click **Apply** after changing port or token, and keep AI Browser running.

> **MCP and RiverMCP work in opposite directions.** `Settings > MCP` adds external tools for River. `Settings > RiverMCP` gives another assistant access to this browser.

## Settings that shape a workflow

- **Tools** are enabled by default through one switch in `Settings > Tools`.
- In `Settings > General` under **River**, **Run actions without asking** controls automatic approval, and **Max tool rounds per run** sets the saved task limit. Click **Save**.
- Tool availability, navigation mode, and approval are separate choices.
- `Settings > Skills` holds reusable playbooks, such as a comparison checklist.

## Platform notes

| Feature | Windows | macOS |
| --- | --- | --- |
| Canvas and River | Use the workflows above | Use the same workflows |
| Multiscreen spanning | **Choose monitors** + **Span monitors** | Built-in spanning not available |

Find the installed version in `Settings > About`.

---

# 中文

[English](#ai-browser) | **中文**

AI Browser 官方发布版 —— 把网页变成可看、可排布、可用对话控制的工作区。

## 下载与安装

**最新版本：v0.1.0** · [全部版本](https://github.com/honkliu/AI-Browser/releases)

| 平台 | 安装包 | 系统要求 |
| --- | --- | --- |
| Windows x64 | [river_browser_0.1.0_x64-setup.exe](https://github.com/honkliu/AI-Browser/releases/download/v0.1.0/river_browser_0.1.0_x64-setup.exe) | Windows 11 x64 |
| Windows ARM | [river_browser_0.1.0_arm64-setup.exe](https://github.com/honkliu/AI-Browser/releases/download/v0.1.0/river_browser_0.1.0_arm64-setup.exe) | Windows 11 ARM64 |

1. 下载对应平台的安装包并运行。
2. 启动 AI Browser。
3. 连接模型：`设置 > 模型` → 填入模型名称、OpenAI 兼容接口地址和 API Key → **保存模型**。浏览器控制需要支持 tool calling 的模型。

---

## 概览

| 组成 | 作用 |
| --- | --- |
| **Canvas** | 把相关网页放进同一个网格 |
| **多屏** | 跨显示器给工作区更多空间 |
| **River** | 与你正在使用的页面协同工作 |
| **RiverMCP** | 把同一个实时浏览器接入外部 AI 助手 |

核心是**上下文**：当前页面、选中内容、Canvas 位置和你的下一个目标。把材料展示给 River，说明想要的结果——不必复制段落，也不必描述点击。

## 快速开始

1. **搭工作区。** 选择 **新建 Canvas** 和双页布局。一个格子打开商品页，另一个打开退货页。
2. **给 River 任务。** 打开 **Agent**，提问：
   > 读这两个页面。用对比表格总结总价、配送时间和退货条件。回答前先读完两个页面。
3. **继续协作。** 选中不清楚的条款问它含义，或让 River 在指定格子打开另一个来源。

## Canvas：把网页放在一起用

Canvas 是由**实时、可交互网页**组成的网格，不是截图。每个格子都是可阅读、可交互的页面。

- **创建：** **新建 Canvas** → 选网格 → 点击格子 → 用地址栏打开页面。
- **调整：** **Canvas 布局** 改变排布；拖动分隔线获得更多空间，**双击分隔线**恢复等分。
- **放大：** **放大 Canvas 页面** 放大聚焦页面，再次使用回到网格。
- **焦点：** 点击的格子成为地址栏和 River 的当前页面。“解释这个页面”跟随聚焦格子，而非整个 Canvas。

跨格子工作时，指明来源或位置：

> 读左边的规格说明和右边的保修条款。哪些宣传功能不在保修范围内？

River 会收到 Canvas 成员关系和格子位置，但页面可见不代表内容已被读取——请明确要求。

也可以让 River 帮你排布：

> 创建一个两列 Canvas。把本页的文档链接放左边，入门示例放右边。

## 多屏：给工作区更多空间

在 Windows 上，**跨屏显示** 把一个窗口扩展到多个显示器，保持同一个 River 对话和浏览器上下文。

1. 打开 **跨屏显示** 旁的 **选择显示器**。
2. 选择 **2 屏并排**、**2 屏上下** 或 **4 屏（2×2）**。
3. 为每个位置指定显示器 → **保存并跨屏**。

选项会显示显示器编号、分辨率和缩放。AI Browser 只保存选择，不修改 Windows 显示设置。再次点击 **跨屏显示** 恢复原窗口。

跨屏让窗口变大，Canvas 决定页面如何划分。跨屏后选择布局并调整分隔线。

## River：理解页面，或直接操作页面

| 你想做什么 | 选择 | 怎么用 |
| --- | --- | --- |
| 理解或询问页面内容 | **Agent 关闭** | 针对当前页面提问、使用选中文本、跟随引用 |
| 导航、交互或完成任务 | **Agent 开启** | 描述结果；River 读取页面并使用浏览器工具 |

用 **模型** 按钮切换模型。tool calling 支持在 `设置 > 模型` 的 **高级** 中配置。

描述结果，而不是点击脚本：

> 用这个 Canvas 里的配送信息填写当前表单的配送选项。缺失信息留空，提交前停下。

River 可以读取页面、打开链接、点击控件、填写字段并使用已连接工具。登录等必须手动完成的步骤请自己完成，再告诉 River 从哪里继续。点击 **停止** 中断运行，它不会撤销已完成的动作。

## 上下文：让 River 明白你的意思

- **当前页面与工作区：** River 收到当前页面身份、选中文本，以及带 Canvas 位置的打开页面列表，并按需通过浏览器工具读取内容。
- **选中内容：** 选中文字带入上下文，使用 **解释**、**翻译**、**核实**、**改写**，或自己提问。
- **更多来源：** **Agent 关闭** 时用 **同时读取** 为问题添加标签页；**Agent 开启** 时直接告诉 River 读哪些页面并对比。
- **检查：** **查看/编辑上下文** 显示 River 收到的内容。编辑作用于 Agent 模式，页面切换后即丢弃。需要每次运行都生效的偏好，请用 `设置 > 指令`。
- **导航：** **自动** 让 River 自己打开页面；**手动** 则提供链接由你打开。

开始新的无关任务时点击 **新建**。历史对话在 `设置 > 已保存对话`。

## RiverMCP：接入外部助手

**RiverMCP** 让支持 MCP 的外部客户端使用同一个实时浏览会话。

1. 打开 `设置 > RiverMCP`。
2. 在客户端中用显示的本地地址和 token 添加 HTTP MCP 连接。
3. token 填在客户端的认证设置里——它**不是**你的模型 API Key。

客户端在另一台电脑上时，把本地地址换成这台电脑的 IP，并保持设置中显示的端口。修改端口或 token 后点击 **应用**，并保持 AI Browser 运行。

> **MCP 与 RiverMCP 方向相反。** `设置 > MCP` 为 River 添加外部工具；`设置 > RiverMCP` 让其他助手访问这个浏览器。

## 影响工作流的设置

- **工具** 在 `设置 > 工具` 中通过一个开关默认启用。
- `设置 > 通用` 的 **River** 下，**不询问直接执行操作** 控制自动批准，**每次运行最大工具轮数** 设定任务上限。修改后点击 **保存**。
- 工具可用性、导航模式和批准是三个独立选项。
- `设置 > 技能` 可保存可复用的流程，例如对比清单。

## 平台说明

| 功能 | Windows | macOS |
| --- | --- | --- |
| Canvas 与 River | 使用上述流程 | 使用相同流程 |
| 多屏跨屏 | **选择显示器** + **跨屏显示** | 不支持内置跨屏 |

在 `设置 > 关于` 中查看已安装版本。

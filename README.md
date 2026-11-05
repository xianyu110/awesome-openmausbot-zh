# OpenMausBot 小白中文教程

> 开源「多 Bot 聊天工作台」：本机 harness + 你已有的 agent CLI（社区非官方教程）  
> 上游：[`milind-soni/OpenMausBot`](https://github.com/milind-soni/OpenMausBot) · 官网：[openmausbot.com](https://www.openmausbot.com/) · 文档：[docs.openmausbot.com](https://docs.openmausbot.com/)  
> 教程校对：2026-11-05（Asia/Shanghai）· npm **openmausbot@0.1.141** · CLI 要求 **Node.js ≥ 24**

[![GitHub stars](https://img.shields.io/github/stars/xianyu110/awesome-openmausbot-zh?style=social)](https://github.com/xianyu110/awesome-openmausbot-zh)
[![Upstream](https://img.shields.io/badge/upstream-milind--soni%2FOpenMausBot-blue)](https://github.com/milind-soni/OpenMausBot)
[![License](https://img.shields.io/badge/license-MIT%20tutorial-green.svg)](LICENSE)
[![Pages](https://img.shields.io/badge/GitHub%20Pages-online-brightgreen)](https://xianyu110.github.io/awesome-openmausbot-zh/)
[![npm](https://img.shields.io/badge/npm-openmausbot%400.1.141-cb3837)](https://www.npmjs.com/package/openmausbot)

**完整正文在 `docs/` 分章**（结构对齐 [awesome-openclaw-tutorial](https://github.com/xianyu110/awesome-openclaw-tutorial) 的「README 导航 + docs 章节」）。本页只做总览与入口。

---

## 📌 与上游版本差异（先看）

| 项 | 本教程基线 | 阅读建议 |
|------|------------|----------|
| npm | `openmausbot@0.1.141` | 以 `npm view openmausbot version` 为准 |
| Node | **≥ 24**（CLI / 服务） | 桌面发行包通常自带 harness |
| 截图 | CLI 真图 1 张；桌面 2 张为**示意图** | 无头环境未开 GUI |
| 菜单名 | 以上游与 `--help` 为准 | 界面更新时请对照官方 |

> 本文不是官方文档，也不提供安装包镜像。

---

## 🚀 30 秒快速选择

| 你的情况 | 推荐 | 开始 |
|---------|------|------|
| 想像聊天软件一样用 | **桌面安装包** | → [第 2 章](docs/01-basics/02-installation-desktop.md) |
| 终端 / 手机配对 / VPS | **npm CLI**（Node 24+） | → [第 3 章](docs/01-basics/03-installation-cli.md) |
| 只想最快验证通路 | 桌面装好后第一次对话 | → [第 4 章](docs/01-basics/04-quick-start.md) |
| 改源码 / 贡献 | 上游 From source | → [上游 README](https://github.com/milind-soni/OpenMausBot#readme) |

---

## 📊 教程导航（按学习路径）

### 🎯 零基础入门（必读）

- [第 1 章：认识 OpenMausBot + 准备](docs/01-basics/01-introduction.md)
- [第 2 章：桌面安装](docs/01-basics/02-installation-desktop.md)
- [第 3 章：npm CLI 安装与帮助](docs/01-basics/03-installation-cli.md)
- [第 4 章：创建第一个 Bot / 第一次对话](docs/01-basics/04-quick-start.md)

### ⚙️ 核心使用

- [第 5 章：常用命令速查](docs/02-core/05-commands.md)

### 🚀 进阶

- [第 6 章：服务器 / 手机 / 脚本（简）](docs/03-advanced/07-serve-phone-scripts.md)
- [第 7 章：常见问题排查](docs/03-advanced/08-troubleshooting.md)

### 📎 说明

- [第 8 章：许可证与合规](docs/04-notes/09-compliance.md)

📖 **在线阅读（Pages）**：https://xianyu110.github.io/awesome-openmausbot-zh/

---

## 截图说明

| # | 文件 | 类型 | 说明 |
|---|------|------|------|
| 1 | [`images/01-download.png`](images/01-download.png) | **示意图** | Releases 安装包对照 |
| 2 | [`images/02-npm-cli.png`](images/02-npm-cli.png) | **真实** | `npm view` + `npx openmausbot --help` |
| 3 | [`images/03-first-bot.png`](images/03-first-bot.png) | **示意图** | 创建第一个 Bot 步骤提纲 |

---

## 官方链接

| 资源 | 链接 |
|------|------|
| 源码 | https://github.com/milind-soni/OpenMausBot |
| 官网 | https://www.openmausbot.com/ |
| 文档 | https://docs.openmausbot.com/ |
| Releases | https://github.com/milind-soni/OpenMausBot/releases/latest |
| npm | https://www.npmjs.com/package/openmausbot |

---

## 维护与合规（摘要）

- 教程文字 MIT；上游 OpenMausBot Apache-2.0  
- **不硬推**未备案境外模型 / API 中转；优先本机已登录 CLI、本地模型或你已有的合规渠道  
- 可选软链：[TryAllAPI](https://tryallapi.com/?aff=5A6A)（aff=5A6A）；店铺仅 [MaynorAI](https://wzyp.cn/shop/maynorai)  
- 与 milind-soni / 各模型厂商无隶属关系  

详情见 [第 8 章](docs/04-notes/09-compliance.md)。

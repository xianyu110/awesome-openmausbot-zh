## 1. 这是什么？准备工作

**OpenMausBot** 是一个开源的「多 Bot 聊天工作台」：本机跑一个 harness，把你已经安装并登录的 agent CLI（如 Claude Code / Codex / Grok 等）接到类似即时通讯的界面里。每个 bot 可以绑定不同引擎、记忆，以及（可选）本机 / 应用权限。

官方强调三点：

- **自带 agent**：用本机已有的 CLI；也可在 Settings → Engines 指向自定义二进制
- **本地优先**：默认本机回环地址管理进程；数据目录常见为 `~/.openmausbot`
- **开源**：上游 **Apache-2.0**；与任何同名加密货币**无官方关系**（见上游 README 警告）

本仓库只提供**中文小白教程**（MIT），不二次分发上游安装包。菜单名、版本号以官方为准；本文校对时 npm 包为 **openmausbot@0.1.141**。

### 官方链接（请以官方为准）

| 资源 | 链接 |
|------|------|
| 源码 | https://github.com/milind-soni/OpenMausBot |
| 官网 | https://www.openmausbot.com/ |
| 文档 | https://docs.openmausbot.com/ |
| 最新 Release | https://github.com/milind-soni/OpenMausBot/releases/latest |
| VPS / 自托管 | https://docs.openmausbot.com/docs/self-hosting/deploy-vps |
| npm `openmausbot` | https://www.npmjs.com/package/openmausbot |

### 截图说明

| # | 文件 | 类型 | 说明 |
|---|------|------|------|
| 1 | [`images/01-download.png`](images/01-download.png) | **示意图** | Releases 桌面安装包对照 |
| 2 | [`images/02-npm-cli.png`](images/02-npm-cli.png) | **真实** | `npm view` + `npx openmausbot --help` |
| 3 | [`images/03-first-bot.png`](images/03-first-bot.png) | **示意图** | 桌面端创建第一个 Bot 的步骤提纲 |

> CLI 真实输出采集于沙盒；官方引擎要求 **Node ≥ 24**。密钥、邮箱、私人路径不会出现在图中。

### 开始前 checklist

1. 先装好并**登录**你要用的 agent CLI（终端里能正常对话）
2. 个人日常用 → 走 **桌面安装包**（第 2 章）
3. VPS / 配对 / 脚本 → 准备 **Node.js ≥ 24**，走 **npm CLI**（第 3 章）
4. 引擎优先：DeepSeek / Ollama / 国内兼容端，或你**已经**付费登录的官方 CLI（见第 8 章合规）

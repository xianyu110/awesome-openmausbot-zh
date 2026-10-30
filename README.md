# OpenMausBot 小白中文教程

> 开源「多 Bot 聊天工作台」：本机 harness + 你已有的 agent CLI（社区非官方教程）  
> 上游：[`milind-soni/OpenMausBot`](https://github.com/milind-soni/OpenMausBot) · 官网：[openmausbot.com](https://www.openmausbot.com/) · 文档：[docs.openmausbot.com](https://docs.openmausbot.com/)  
> 教程校对：2026-10-30（Asia/Shanghai）· npm 包 **openmausbot@0.1.134**（`npm view` / `npx --help` 实测）；桌面 GUI 为**示意图**（无图形会话）

[![GitHub stars](https://img.shields.io/github/stars/xianyu110/awesome-openmausbot-zh?style=social)](https://github.com/xianyu110/awesome-openmausbot-zh)
[![Upstream](https://img.shields.io/badge/upstream-milind-soni%2FOpenMausBot-blue)](https://github.com/milind-soni/OpenMausBot)
[![License](https://img.shields.io/badge/license-MIT%20tutorial-green.svg)](LICENSE)
[![Pages](https://img.shields.io/badge/GitHub%20Pages-online-brightgreen)](https://xianyu110.github.io/awesome-openmausbot-zh/)

---

## 截图索引

| # | 文件 | 类型 | 说明 |
|---|------|------|------|
| 1 | [`images/01-download.png`](images/01-download.png) | **示意图** | Releases 桌面安装包对照 |
| 2 | [`images/02-npm-cli.png`](images/02-npm-cli.png) | **真实** | `npm view` + `npx openmausbot --help` |
| 3 | [`images/03-first-bot.png`](images/03-first-bot.png) | **示意图** | 桌面端创建第一个 Bot 的步骤提纲 |

> CLI 真实输出采集于 Node 22 沙盒（官方引擎要求 **Node ≥ 24**，help 仍可打印）。密钥、邮箱、私人路径未出现在图中。

---

## 这是什么？

**OpenMausBot** 把多个 AI bot 放进类似即时通讯的界面：每个 bot 可绑定不同引擎、记忆与（可选）电脑/应用权限。官方强调：

- **自带 agent**：使用本机已安装并登录的 `claude` / `codex` / `grok` 等 CLI（可在 Settings → Engines 指向自定义二进制）  
- **本地优先**：本机 harness（默认本机回环地址）管理进程；数据目录常见为 `~/.openmausbot`  
- **开源**：上游 **Apache-2.0**；与任何同名加密货币**无官方关系**（见上游 README 警告）

本仓库只提供**中文小白教程**（MIT），不二次分发上游安装包。

---

## 官方链接（请以官方为准）

| 资源 | 链接 |
|------|------|
| 源码 | https://github.com/milind-soni/OpenMausBot |
| 官网 | https://www.openmausbot.com/ |
| 文档 | https://docs.openmausbot.com/ |
| 最新 Release | https://github.com/milind-soni/OpenMausBot/releases/latest |
| VPS / 自托管 CLI | https://docs.openmausbot.com/docs/self-hosting/deploy-vps |
| npm `openmausbot` | https://www.npmjs.com/package/openmausbot |

---

## 环境要求（摘要）

### 桌面端（多数个人用户）

- **macOS**（Apple silicon / Intel 各有 `.dmg`）、**Windows x64**（`.exe`）、**Ubuntu 24.04 x64**（`.deb` 或 AppImage，以 Release 说明为准）  
- 先装好并**登录**你要用的 agent CLI（官方 README 点名 Claude Code / Codex / Grok 等）  
- 版本以 [Releases](https://github.com/milind-soni/OpenMausBot/releases/latest) 为准（撰写时可见 **v0.1.134**）

### CLI / 服务端（配对设备、VPS）

- **Node.js ≥ 24**（npm 包 `engines` 声明；低于此版本可能仅能看 help）  
- 详见官方 self-hosting 文档

---

## 安装（macOS / Windows / Linux）

### 方式 A：桌面安装包（推荐日常使用）

1. 打开 [Releases · latest](https://github.com/milind-soni/OpenMausBot/releases/latest)  
2. 按系统下载：  
   - Mac Apple silicon → `OpenMausBot.dmg`  
   - Mac Intel → `OpenMausBot-intel.dmg`  
   - Windows → `OpenMausBot-setup.exe`  
   - Ubuntu → `OpenMausBot-amd64.deb`（或 Release 提供的 AppImage）  
3. 按系统常规方式安装并打开应用  

![下载示意](images/01-download.png)

也可使用官方 README 上的直链按钮（同一 Release 资源）。

### 方式 B：npm CLI（服务 / 配对 / VPS）

```bash
# 建议使用 Node >= 24
npm view openmausbot version
npx openmausbot --help
# 常见：npx openmausbot setup
#       npx openmausbot serve --tunnel
# 或：npm i -g openmausbot
```

本机实测 help：

![npm CLI](images/02-npm-cli.png)

完整子命令（`serve` / `pair` / `login` / `fleet` 等）以 `openmausbot --help` 与官方文档为准。

---

## 第一次演示任务（桌面）

![创建 Bot 示意](images/03-first-bot.png)

1. 确认本机 agent CLI 已能交互（例如已登录的 Claude Code / Codex；**合规优先用你已有订阅或国内兼容封装**）  
2. 安装并打开 OpenMausBot  
3. 在模型 / Engines 选择器中确认引擎可用；不可用时按提示补安装或改路径（Settings → Engines）  
4. 按官网 Quick tour /「Create your first bot」新建 bot，发一条简单消息验证通路  
5. 若启用「控制本机 / 云桌面 / 应用连接」等能力：只开你需要的权限，**先在非敏感目录试用**

手机配对、公网 tunnel、多租户 `fleet` 等进阶能力见官方文档，本入门不展开。

---

## 常见报错与解决

| 现象 | 可能原因 | 处理 |
|------|----------|------|
| 引擎列表为空 | 未装或未登录对应 CLI | 先在终端跑通该 CLI；必要时在 Engines 填自定义路径 |
| `npx` 引擎版本警告 | Node &lt; 24 | 升级 Node 后再作服务端用途 |
| 配对 / tunnel 失败 | 网络或未 `login` | 按 `openmausbot login` 与文档排查；**勿把邮箱验证码、密钥贴进仓库** |
| Ubuntu 主机控制异常 | Wayland 等平台限制 | 见上游 README / issue（如 Wayland 相关说明） |
| 误信「同名代币」 | 第三方炒作 | 以上游「无加密货币关联」声明为准 |

---

## 许可证与合规

- **本教程文字与配图**：MIT（见 [LICENSE](LICENSE)）  
- **上游 OpenMausBot**：Apache-2.0  
- **不硬推**未备案境外模型或 API 中转。Bot 引擎优先：DeepSeek / Ollama / 国内兼容端，或你**已经**付费登录的官方 CLI；本教程不诱导注册新的未备案中转  
- 若 bot 涉及**声音克隆 / 真人形象**：须本人授权，勿用于未授权内容  
- 可选软链：[tryallapi.com](https://tryallapi.com/?aff=5A6A)（aff=5A6A）；店铺仅 [MaynorAI](https://wzyp.cn/shop/maynorai)

与 milind-soni / boat.dev / 各模型厂商**无隶属关系**。本教程不编造菜单名与定价。

---

## GitHub Pages

图文镜像页：https://xianyu110.github.io/awesome-openmausbot-zh/

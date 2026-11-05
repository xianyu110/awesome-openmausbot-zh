## 5. 常用命令速查

以下摘自 **openmausbot@0.1.141** 的 `--help`，方便复制；细节以本机 help 为准。

### 工作区运维

```bash
openmausbot setup
openmausbot start
openmausbot serve [--port 8799] [--data-dir DIR] [--tunnel|--tailscale|--domain HOST]
openmausbot status
openmausbot doctor
```

### 账号与配对

```bash
openmausbot login [--email you@example.com]
openmausbot logout
openmausbot pair [--label NAME] [--client] [--phone ios|android]
openmausbot sessions
openmausbot sessions revoke <ID>
openmausbot access list
openmausbot access add EMAIL [--chat-only]
openmausbot access remove EMAIL
```

### 驱动已运行的工作区（脚本 / CI / 其他 agent）

```bash
openmausbot bots | channels | models
openmausbot run BOT "do this"       # 下发任务并等到完成（含队友）
openmausbot send BOT "text"         # 发一条消息后立即返回
openmausbot wait BOT                # 等待已在跑的工作
openmausbot messages BOT            # 最近消息
openmausbot interrupt BOT [--tree]  # 相当于按 Stop
openmausbot export BOT --out DIR    # 导出 transcript / 文件 / 截图
openmausbot events [--job THREAD]   # 服务端事件 JSON Lines
openmausbot team apply FILE         # 用 team 文件对齐工作区
```

### 常驻与浏览器

```bash
openmausbot service install [--tunnel|--domain HOST|--tailscale] [--port N]
openmausbot service uninstall
openmausbot browser install [--with-deps]
openmausbot browser status
openmausbot sentinel [--once] [--json]
```

> 提示：`service` / `fleet` 建议先 `npm i -g openmausbot` 再装系统单元；`fleet` 多在 Linux + root / Caddy 场景，入门可先跳过。

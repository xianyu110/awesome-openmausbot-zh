## 3. npm CLI（服务 / 配对 / VPS）

### 版本与引擎

```bash
# 需要 Node.js >= 24（package engines）
node -v
npm view openmausbot version   # 校对时为 0.1.141
```

低于 Node 24 时，部分功能可能无法跑通；`npx … --help` 往往仍能打印。

### 快速查看帮助（本教程实测）

```bash
npx openmausbot@0.1.141 --help
# 或全局安装后：
# npm i -g openmausbot
# openmausbot --help
```

![npm CLI（真实截图）](images/02-npm-cli.png)

### 顶层命令一览（摘自 `openmausbot --help`）

| 命令 | 作用（摘要） |
|------|----------------|
| `openmausbot` / `setup` | 首次配置：选 AI 访问方式、可选手机访问；保留已有 bot/聊天 |
| `start` | 按已保存设置打开工作区（等同默认入口） |
| `serve` | 启动服务端；可打印配对链接 + QR；支持 `--port` / `--data-dir` / `--tunnel` 等 |
| `pair` | 对运行中的服务签发配对码（`--client` 仅聊天；`--phone ios\|android`） |
| `sessions` | 列出已配对设备；`sessions revoke ID` 登出某设备 |
| `status` | 查看服务端自我描述 |
| `login` / `logout` | 用邮箱验证码登录 OpenMausBot 账号（tunnel 公网地址需先 login） |
| `access` | 管理可用邮箱登录 `/pair` 的名单（`list` / `add` / `remove`，可 `--chat-only`） |
| `service install\|uninstall` | 写入 systemd（Linux）或 launchd（macOS），开机自启 |
| `sentinel` | 只读健康扫描（也可经 `service install --sentinel` 定时） |
| `browser install\|status` | 安装 bot 用浏览器引擎（agent-browser）与 Chrome for Testing |
| `fleet …` | 一台 Linux 上多租户工作区（需 root / Caddy 等，见官方文档） |

### 常用启动示例

```bash
# 交互式首次配置
npx openmausbot@0.1.141 setup

# 本地启动服务（默认端口示例 8799，以 help 为准）
npx openmausbot@0.1.141 serve --port 8799

# Cloudflare tunnel 公网（需先 login）
npx openmausbot@0.1.141 login
npx openmausbot@0.1.141 serve --tunnel

# Tailscale / 自有域名
# openmausbot serve --tailscale
# openmausbot serve --domain your.host.example
```

`--no-open` 不自动开浏览器；`--no-pair` 跳过手机配对打印；`--local` 本次忽略已保存的远程访问设置。

完整子命令与参数以你本机 `openmausbot --help` 与 [官方文档](https://docs.openmausbot.com/) 为准。

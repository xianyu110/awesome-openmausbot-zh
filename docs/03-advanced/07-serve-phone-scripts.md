## 6. 进阶：服务器 / 手机 / 脚本（简）

> 本章只给路线图；逐步操作以 [官方 self-hosting](https://docs.openmausbot.com/docs/self-hosting/deploy-vps) 与本机 `--help` 为准。

### 服务器（VPS）速览

1. 机器安装 **Node ≥ 24**，建议 `npm i -g openmausbot`
2. `openmausbot setup` 选好引擎与数据目录
3. 远程访问三选一（互斥思路，按场景选）：
   - `--tunnel`：Cloudflare 隧道公网地址，需先 `openmausbot login`
   - `--tailscale`：走 Tailscale MagicDNS（需已登录 Tailscale 并开启 HTTPS 证书）
   - `--domain HOST`：自有域名；会拉起 pinned Caddy 申请证书（DNS 指向本机，开放 80/443）
4. 需要开机自启：`openmausbot service install …`（Linux systemd / macOS launchd）
5. 多客户共用一台机：再看 `openmausbot fleet …`（复杂，适合运营场景）

### 手机配对（简）

1. 服务端已在跑（`serve` / `start` / `service`）
2. `openmausbot pair --phone ios` 或 `--phone android`（或桌面 UI 里的配对入口）
3. 手机扫码 / 输入配对码；仅聊天可用 `pair --client`
4. 管理设备：`openmausbot sessions`；踢掉某台：`sessions revoke <ID>`

### 脚本化对话（简）

适合 CI、定时任务、或让另一个 agent 调用：

```bash
openmausbot doctor
openmausbot run  my-bot  "总结今天仓库里的未合并 PR"
openmausbot send my-bot  "继续，只要结论"
openmausbot messages my-bot
openmausbot export my-bot --out ./omb-out
```

生产环境请限制 `access` 白名单，并避免把邮箱验证码、API Key、数据目录打进日志或公开仓。

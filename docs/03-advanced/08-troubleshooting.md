## 7. 排查

| 现象 | 可能原因 | 处理 |
|------|----------|------|
| 引擎列表为空 | 未装或未登录对应 CLI | 先在终端跑通该 CLI；必要时在 Engines 填自定义路径 |
| `npx` / 安装报引擎版本 | Node &lt; 24 | 升级到 Node ≥ 24 再作服务端用途；可用 `nvm` / 官方安装包 |
| `doctor` 失败 | 服务未起或引擎未就绪 | 先 `serve`/`start`，再查 Engines；看 `status` |
| 配对 / tunnel 失败 | 网络或未 `login` | 先 `openmausbot login`；检查防火墙；**勿把邮箱验证码、密钥贴进仓库或群聊** |
| `serve --domain` 证书失败 | DNS / 80·443 未通 | 确认 A/AAAA 指向本机；云厂商安全组放行 |
| Ubuntu「控制本机」异常 | Wayland 等平台限制 | 见上游 README / issue（Wayland 相关说明） |
| `browser` 相关报错 | 未安装测试浏览器 | `openmausbot browser install`（Linux 缺库时可 `--with-deps`，需 root 一次） |
| 误信「同名代币」 | 第三方炒作 | 以上游「无加密货币关联」声明为准 |
| 权限过大导致误操作 | 给了本机/文件系统过大权限 | 收回非必要权限；只在非敏感目录试用 |

仍卡住时：复制**脱敏**后的 `openmausbot status` / `doctor` 输出，对照 [官方文档](https://docs.openmausbot.com/) 或上游 Issues。

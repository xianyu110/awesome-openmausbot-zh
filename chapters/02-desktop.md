## 2. 桌面安装（推荐日常使用）

### 环境要求（摘要）

- **macOS**（Apple silicon / Intel 各有 `.dmg`）、**Windows x64**（`.exe`）、**Ubuntu 24.04 x64**（`.deb` 或 AppImage，以 Release 说明为准）
- 先装好并登录要用的 agent CLI
- 版本以 [Releases · latest](https://github.com/milind-soni/OpenMausBot/releases/latest) 为准（撰写时与 npm **0.1.141** 同系列）

### 安装步骤

1. 打开 [Releases · latest](https://github.com/milind-soni/OpenMausBot/releases/latest)
2. 按系统下载：
   - Mac Apple silicon → `OpenMausBot.dmg`
   - Mac Intel → `OpenMausBot-intel.dmg`
   - Windows → `OpenMausBot-setup.exe`
   - Ubuntu → `OpenMausBot-amd64.deb`（或 Release 提供的 AppImage）
3. 按系统常规方式安装并打开应用
4. 也可使用官方 README 上的直链按钮（同一 Release 资源）

![下载示意（示意图）](images/01-download.png)

### 打开后先看哪里

- 模型 / Engines 选择器：确认本机 CLI 已被识别
- 不可用时：Settings → Engines 补安装或改自定义路径
- 数据目录一般在用户目录下的 `.openmausbot`（勿把含密钥的配置提交到公开仓库）

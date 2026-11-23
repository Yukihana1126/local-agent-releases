# 本地 Agent 发布版

这是 [本地 Agent] 的发布专用仓库，只放安装包和自动更新清单，不含源码。

## 下载安装

- 最新发布页：https://github.com/Yukihana1126/local-agent-releases/releases/latest
- 直接安装（Windows 11 家庭版可用）：
  https://github.com/Yukihana1126/local-agent-releases/releases/download/v0.2.0/LocalAgentRelease_0.2.0_x64-setup.exe
- 国内直连慢/断流时走镜像（同一文件，sha256 已核对）：
  https://gh-proxy.com/https://github.com/Yukihana1126/local-agent-releases/releases/download/v0.2.0/LocalAgentRelease_0.2.0_x64-setup.exe

安装后：

1. 打开「本地 Agent · 发布版」。
2. 左上角点「＋ 添加端点」，填本机端口或 OpenAI 兼容 Base URL；需要时填 API Key。
3. 之后启动应用会自动检查 GitHub 更新；设置 →「软件更新」里也可手动检查/安装。

## 自动更新

- 更新源：`latest.json`（本仓库 Release 资产）。
- 更新包使用 Tauri 签名校验；签名私钥只保存在发布者本机。
- 若启动时检查失败（网络/离线），应用会静默跳过，不影响使用。

## 版本

- v0.2.0：首个发布版；自定义端点/端口/API Key，默认端点留空，独立发布版配置目录，Tauri updater 基线。

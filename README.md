# Video KG Bot Desktop · 发布通道

本仓库只承载桌面应用的发布产物和 Tauri Updater 清单，不包含源码。

## 通道

| 通道 | 清单地址 | 说明 |
|---|---|---|
| stable | `https://github.com/K-XT/videokgbot-desktop/releases/latest/download/latest.json` | 最新正式版 |
| beta | `https://github.com/K-XT/videokgbot-desktop/releases/download/beta/latest.json` | 内测通道（维护一个 `beta` 标签的发布） |

## 每个版本的 Release 资产

- Windows：`Video KG Bot_<version>_x64-setup.exe` 与同名 `.sig`
- 可选：MSI 与 `.sig`
- `latest.json`：Tauri Updater 清单，`platforms` 中的 `url` 指向本 Release 的安装包
- `SHA256SUMS.txt`：安装包与清单校验和

## 安装与校验

1. 下载安装包与 `SHA256SUMS.txt`；
2. 校验 SHA256；
3. 运行安装包（Windows NSIS 按用户安装，无需管理员）。

## 签名轮换

v0.10.0 起使用新的更新签名公钥。v0.9.0 客户端无法验证新密钥签名的更新包，
需要一次手动覆盖安装；从 v0.10.0 起恢复自动更新。

## 隐私

应用不上传业务数据；模型请求只发送到用户自己配置的在线 API。
离线核心功能（浏览、搜索、图谱、复习、设置、备份）不依赖网络。

# Vela-le

Vela 本地桌面小组件个人修改版，作者：**乐**。本仓库用于分发 Windows x64 安装包和应用更新清单。

本应用由开源项目优化修改，用于学习和个人使用。所有小组件与数据均保存在本地。

[下载最新安装包](https://github.com/1vegedog/Vela-le/releases/latest/download/Vela-win-Setup.exe) · [版本说明](https://github.com/1vegedog/Vela-le/releases)

## 安装与更新

首次请退出系统托盘中的 Vela，下载并手动安装**最新版本（1.0.1 及以后）**，选择原安装目录。应用标识保持不变，继续使用原有本地配置和数据。

1.0.1 已接入本仓库。后续发布更高版本后，可在 **设置 → 更新 → 检查更新 → 下载并安装** 完成升级。默认每 24 小时检查一次，也可关闭自动检查。

旧版 1.0.0 使用上游更新公钥，不能直接验证本修改版的新签名，所以本次需要手动安装一次。

## 已包含的修改

- 重写计算器运算解析，兼容安装版的安全策略。
- 优化计算输入与历史记录渲染，减少窗口命中区域重算，修复小尺寸卡片的历史列表布局。
- 修复卡片拖动状态残留与输入冲突；自动更新后启动新版，更新时不新增快捷方式。
- iCloud 日历双向同步、日视图和显示优化。
- 快捷方式卡片的原生 Windows 文件拖放支持。
- 更新源迁移、签名验证和自动检查开关修复。

苹果提醒事项同步按计划暂缓。启用 iCloud 等联网功能后，相关同步数据会发送到用户配置的服务。

## 发布文件

- `Vela-win-Setup.exe`：Windows x64 安装器，需要 WebView2 和 Microsoft Visual C++ x64 运行库。
- `update.json`：内含版本、发布说明、安装器地址、SHA-256 和 Ed25519 签名。
- `SHA256SUMS.txt`：下载文件完整性校验。
- `update-public-key.json`：本修改版的公开验签密钥。

更新清单签名用于验证更新内容；安装器未使用 Windows Authenticode 证书签名。私钥保留在发布者本机，不在本仓库中。

## 来源与授权

基于 [weixinhao929/vela-cleanroom](https://github.com/weixinhao929/vela-cleanroom/tree/4cef56be0de1c5706e290f3c2be9c3e6acfb94a8) 修改，保留上游 MIT 版权和第三方许可。请参阅 [LICENSE](LICENSE) 与 [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)。

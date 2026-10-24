# LionTV

LionTV 电视端安装包与在线更新发布仓库。

**当前稳定版本：0.6.0** · Android 8.0 及以上 · 32位/64位通用 APK

[下载 LionTV 0.6.0](https://github.com/Huarosen/LionTv/releases/download/v0.6.0/LionTV-0.6.0-universal.apk) · [中国内地下载](https://gitee.com/huarosen/lion-tv/releases/download/v0.6.0/LionTV-0.6.0-universal.apk) · [最新版本](https://github.com/Huarosen/LionTv/releases/latest) · [更新日志](CHANGELOG.md)

## 安装与更新

下载 APK 后通过电视系统允许的方式安装。已安装支持在线更新的版本时，可在 **设置 → 检查更新** 中检查、下载并确认安装；应用每次重新启动也会检查新版本。

0.5.9起优先使用Gitee中国内地入口，连接失败时尝试GitHub；旧版先通过原入口或手动覆盖安装本版。安装需系统授权与用户确认。厂商固件如果限制安装第三方应用，应用无法绕过该限制。此应用不会替换电视桌面。

## 文件说明

- GitHub / Gitee Releases：稳定版本 APK、更新清单和 SHA-256 校验文件。
- `update.json`：应用读取的最新稳定版本索引。
- `SHA256SUMS.txt`：当前稳定 APK 的校验值。
- [发布规则](RELEASE_POLICY.md)：版本、标签、附件和索引规则。

本仓库不存放源码、签名密钥或账号凭据。仅保留正式发布版本；不上传测试包或补传早期历史版本 APK。

## 本地错误反馈

设置 → 错误日志与反馈，可用同一局域网的手机扫码下载日志ZIP。打开邮件草稿后，需手动添加附件并发送至liontv_support@163.com；下载不代表邮件已送达。临时链接在返回、应用进入后台或超时后关闭。

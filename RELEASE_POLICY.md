# LionTV 包体发布规则

1. 此仓库公开提供正式安装包和升级信息，不存放应用源码或内部仓库地址。
2. 版本号格式 `major.minor.patch`，末位只能是0–9：`0.5.9 → 0.6.0`。每次发布必须递增 Android `versionCode`；0.5.3 为8，0.5.4 为9，0.5.5 为10。
3. 稳定版本标签为 `v<版本号>`，例如 `v0.5.3`；标题 `LionTV 0.5.3`。稳定版本不得标记为预发布，最新稳定版本设为 Latest。
4. 每个 Release 附件仅包含该版本的 `LionTV-<版本号>-universal.apk`、`update.json`、`SHA256SUMS.txt`。APK 不提交到 Git 历史，不上传未发布的测试包。每次仅上传当次正式版本，不补传早期历史包。
5. APK 必须使用与已有安装相同的签名，支持Android API26及以上。校验应用ID为 `tv.lion`、版本、签名和构建/lint检查。签名密钥、密码或GitHub令牌不得提交。
6. SHA-256 与文件大小必须根据最终签名APK生成，更新清单的下载地址必须对应当前标签和附件名。
7. 先发布含完整附件的稳定Release，再更新main分支根目录的 `update.json` 与 `SHA256SUMS.txt`；禁止先指向尚不存在的APK。
8. 根目录索引只指向最新稳定版本；每次更新README与CHANGELOG。已发布附件不可覆盖成内容不同的同版本APK，修正必须发布递增版本。
9. 内部仓库名称、地址、源码提交SHA及内部发布映射仅记录在私有文档或本地发布记录中，公开文档和发布说明均不展示这些信息。APK校验值和签名证书指纹可以公开；校验文件不包含签名私钥。
10. 下载和安装必须由用户确认；不提供静默安装或绕过电视厂商校验。

## update.json 格式

`schemaVersion`(1)、`packageName`(`tv.lion`)、`versionName`、`versionCode`、`minSdk`、`notes`，以及 `apk.url`、`apk.size`（字节）、`apk.sha256`（64位小写十六进制）。

应用通过公开的 `https://raw.githubusercontent.com/Huarosen/LionTv/main/update.json` 检查更新，无需登录或内置GitHub访问令牌。

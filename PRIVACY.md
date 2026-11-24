# Clippery 隐私说明 / Privacy Notice

**生效日期 / Effective date**　2026-11-24
**适用版本 / Version**　Clippery 1.2.11 及后续本地版本
**适用客户端 / App**　Windows 桌面客户端（`Clippery.Windows.exe`）

## 一、中文说明

### 1. 谁负责处理你的数据

本软件由以下主体开发和提供：

- **名称**：深圳市罗湖区莲塘街道哈吉米科技工作室（个体工商户）
- **统一社会信用代码**：92440300MAKQBHW82F
- **经营者**：刘嘉俊
- **隐私与安全联系**：1120166455@qq.com

当前版本没有 Clippery 运营的账号系统、云同步服务、遥测服务或广告服务。你的剪贴板历史默认只保存在本机。只有在您主动配置并授权可选 AI 功能时，软件才会连接您指定的第三方端点。

### 2. 我们不收集什么

- 没有遥测、使用统计、行为分析或崩溃上报。
- 没有广告 SDK。
- 没有自动更新检查；关于页的“检查更新”只显示本地提示，不发起网络请求。
- 当前版本没有 Clippery 服务器，开发者不会收到你的剪贴板历史、图片、搜索词或 API Key。
- 不下载网页里的远程图片；只保存剪贴板实际提供的文字、HTML、本地图片、`data:` 图片或位图。
- 我们不出售你的个人信息。

### 3. 本地保存哪些数据

默认数据目录：`%LOCALAPPDATA%\Clippery`。可以通过环境变量 `CLIPPERY_DATA_DIR` 指向其他目录（开发和测试用）。

| 路径 | 内容 |
|---|---|
| `history.db` | 文本、HTML、RTF、时间、置顶/敏感标记、图片索引、关键词索引、OCR 文本、AI 图片描述和 AI 向量 |
| `blobs\` | 去重后的图片文件（PNG） |
| `clipboard-cache\` | 写回剪贴板时临时引用的 PNG，成功写回后按机会式清理 |
| `settings.json` | 记录开关、快捷键、开机启动、界面/OCR 语言、AI 端点/模型/授权状态、隐私同意版本；**不包含 API Key** |
| `app.log` | 启动、热键、托盘、粘贴失败等本地诊断信息；不记录剪贴板正文、图片内容、搜索查询词或 API Key |

这些本地文件默认**不加密**，受 Windows 用户账户权限保护。任何能访问该 Windows 账户或数据目录的人或程序都可能读取它们。需要更强保护时，请使用 BitLocker、EFS 或其他磁盘加密，并限制账户权限。

**保留期限**：本地历史、设置和日志保留到你删除数据目录或在设置中清空历史；`app.log` 当前没有自动轮转，删除数据目录前会一直保留。备份文件保留到你自行删除。

### 4. 剪贴板采集

- 首次安装默认开启采集；首次运行会显示隐私摘要并要求确认。你可以随时在设置或托盘菜单暂停。
- 尊重 Windows 剪贴板隐私格式：`ExcludeClipboardContentFromMonitorProcessing`、`Clipboard Viewer Ignore`、`CanIncludeInClipboardHistory=0`、`CanUploadToCloudClipboard=0` 存在时整条跳过。
- “从不记录这些应用”名单按前台进程名做尽力而为的过滤；剪贴板隐私格式仍是主要保证。
- 文本敏感检测由本机规则执行（常见 Key/token 前缀、私钥、JWT、密码字段、高熵字符串等）。命中后标记为敏感，跳过 AI 索引和本机 OCR；你可以在本地手动取消/恢复标记。
- **敏感检测是启发式，且当前主要覆盖文本、HTML、RTF。** 纯图片截图中的密码、银行卡、病历等内容可能不会被自动识别。开启图片 AI 时，软件会要求你对含图片的条目逐条确认，但这不保证识别所有秘密。
- 纯文件复制（只有 `CF_HDROP`、没有真实图片数据）不进入历史；QQ/微信图片同时带文件路径和位图时会按图片采集。
- 采集、存储、关键词搜索和本机 OCR 都在本机完成。

### 5. 可选 AI 功能

AI 功能默认关闭，且新安装不预置任何厂商端点、模型或 Key。只有你填写自己的 OpenAI 兼容端点、模型和 API Key，并勾选远程数据授权后，相关请求才会发生。

可能发送给**你配置的端点**的数据：

- 文本索引：可被 AI 检索且非敏感的文本或 HTML 纯文本；
- 图片理解：你逐条确认允许的含图片条目所对应的压缩图片（data URL）、可选的同条正文上下文，以及生成描述/OCR 的提示词；
- AI 搜索：你按回车执行语义搜索时的查询词。

边界：

- 远程端点必须使用 HTTPS；只有本机回环地址允许 HTTP。
- 文本敏感条目不会发送；每条历史还有独立的“可被 AI 检索”标记。
- 含图片的条目不会自动加入 AI 索引；你需要在历史卡片上逐条允许并确认。图片可能包含密码、银行信息或其他敏感内容，确认前请自行判断。
- 图片上传授权与文本授权分开；取消图片授权后不会上传图片。
- 你可以随时清除 AI 描述/向量；关键词搜索和本地历史不受影响。
- 你配置的 AI 服务提供方可能按其自身条款记录、保留、训练或处理请求数据；这不属于 Clippery 的控制范围，也不代表 Clippery 的立场。请阅读该服务方的隐私政策。
- 如果你配置的端点位于你所在国家/地区之外，数据可能发生跨境传输；该传输由你选择的服务方处理，请自行评估并取得必要授权。
- API Key 只保存在 Windows 凭据管理器：`Clippery/AiEmbeddingApiKey` 和 `Clippery/AiVisionApiKey`。它不会写入 `settings.json`、`app.log` 或错误消息。
- 某些兼容服务可能使用额外的会话头（例如我们为 OpenCode Go 端点附加 `x-opencode-session`）；这是为了兼容该服务，不包含你的剪贴板正文。

### 6. 本机 OCR

- 使用 Windows 自带的 `Windows.Media.Ocr`，默认启用；图片和 OCR 文本都在本机处理，不上传。
- OCR 只处理非敏感图片条目；识别文本保存在 `history.db`，用于关键词搜索和预览。
- OCR 依赖 Windows 语言包。语言包缺失或所选语言不可用时，设置页会显示不可用/错误提示，不会崩溃。
- 自动模式优先 `zh-Hans-CN`，其次其他中文语言，再回退到用户配置语言或系统可用语言。

### 7. 日志

- `app.log` 只包含启动、热键、托盘、粘贴失败等诊断信息，不记录剪贴板正文、图片内容、搜索查询词或 API Key。
- 日志保存在本机，保留到你删除数据目录；当前没有自动轮转或自动过期。
- 向他人提供日志前，请先检查并删除你不希望分享的信息。

### 8. 备份与恢复

- 导出目录包含 `manifest.json` 和 `images/`，是**明文** JSON 和图片文件。
- **备份默认不包含敏感条目。** 你可以在设置中主动勾选“包含敏感条目”；勾选后会再次提示，备份将包含明文敏感内容。
- 备份不包含 API Key、`settings.json` 或 AI 向量；恢复后如需语义搜索，需要重新索引。
- 恢复只合并且校验 SHA-256，不删除现有历史；重复条目会跳过。
- 备份文件由你选择保存位置。请妥善保管，并在不需要时自行删除；卸载 Clippery 不会删除你另存的备份。

### 9. 数据删除与保留

- 设置 → 历史管理 → 清空历史会删除文本、图片、置顶、搜索索引、OCR 文本、AI 描述/向量和写回缓存，无法恢复。
- 删除整个 `%LOCALAPPDATA%\Clippery` 目录会删除本地历史、设置、日志和缓存。
- 卸载程序默认保留 `%LOCALAPPDATA%\Clippery`，以便重装后恢复历史/设置；需要彻底删除时请手动删除该目录。
- 你的备份副本不会被卸载程序删除，需要单独清理。
- 如果你通过邮件联系我们，我们会保留邮件直到问题处理完毕，并在合理期限内删除，除非法律要求保留。

### 10. 你的权利与法律基础

- 你在适用法律范围内有权查阅、复制、更正、删除你的个人信息，撤回同意，注销账号（当前无账号），以及获取数据副本。
- 请通过 1120166455@qq.com 联系我们；我们会在 15 个工作日内答复，法律另有要求的除外。
- 处理本机剪贴板数据的法律基础是你的同意（首次运行确认及设置中的开关）；提供软件功能所必需的处理基于履行合同；安全与故障排查基于我们的合法利益。可选 AI 上传基于你的单独授权。
- 如果你认为我们处理个人信息的方式违反适用法律，你可以向有管辖权的监管机构投诉。

### 11. 安全与泄露通知

- 我们采取合理措施保护软件和数据，包括限制云端收集、使用 Windows 凭据管理器保存 API Key、只允许 HTTPS 远程端点。
- 本地数据默认不加密；Windows 账户权限、磁盘加密和备份管理由你负责。
- 如果发生影响你个人信息的泄露，我们会按适用法律的要求通知你和/或监管机构。

### 12. 未成年人

本软件不面向 14 周岁以下儿童。未满 14 周岁的未成年人应在监护人同意和指导下使用。我们不会有意收集儿童的个人信息。

### 13. 第三方

Clippery 使用 .NET 10 Desktop Runtime、Microsoft.Data.Sqlite/SQLitePCLRaw、Windows OCR/WinRT 等组件。第三方许可证和版权声明见 `THIRD-PARTY-NOTICES.md` 和安装目录中的 `THIRD-PARTY-NOTICES.TXT`。这些组件不会改变上述“默认不上传”的行为；可选的 AI 请求只发往你配置的端点。

**更新检查 / Update check**：手动点击“检查更新”，或启用“自动检查更新”时，Clippery 会请求 GitHub 的公开接口 `https://api.github.com/repos/54Lynnn/clippery-releases/releases/latest`，读取最新版本号、发布说明和安装包信息。请求不包含剪贴板内容、历史记录、API Key 或账号信息；GitHub 可能看到你的 IP 地址和标准 HTTP 请求头。自动检查默认开启、每天最多一次，可在设置中关闭。Clippery 不会在后台静默下载或安装更新。

### 14. 变更与联系

本说明会随版本更新。涉及数据实践的实质性变更会在发布说明中标注；必要时会在首次运行时重新请求确认。对隐私有疑问，请联系 1120166455@qq.com。

---

## Part B: English

### 1. Who is responsible

The Software is developed and provided by:

- **Name**: 深圳市罗湖区莲塘街道哈吉米科技工作室（个体工商户）
- **Unified Social Credit Code**: 92440300MAKQBHW82F
- **Operator**: 刘嘉俊
- **Privacy and security contact**: 1120166455@qq.com

The current version has no Clippery-operated account system, cloud synchronization, telemetry, or advertising service. Your clipboard history is stored locally by default. The app contacts a third-party endpoint only when you configure and authorize optional AI features.

### 2. What we do not collect

- No telemetry, usage statistics, behavioral analytics, or crash reporting.
- No advertising SDK.
- No automatic update check; the “Check for updates” button only shows a local message and makes no network request.
- The current version has no Clippery server. The developer does not receive your clipboard history, images, search queries, or API keys.
- We do not download remote images from web pages; we store only text, HTML, local images, `data:` images, or bitmaps actually provided by the clipboard.
- We do not sell your personal information.

### 3. Data stored locally

Default data directory: `%LOCALAPPDATA%\Clippery`. The `CLIPPERY_DATA_DIR` environment variable can point to another directory for development and testing.

| Path | Content |
|---|---|
| `history.db` | Text, HTML, RTF, timestamps, pinned/sensitive flags, image index, keyword index, OCR text, AI image descriptions, and AI vectors |
| `blobs\` | Deduplicated image files (PNG) |
| `clipboard-cache\` | Temporary PNGs referenced when writing back to the clipboard; cleaned opportunistically after successful writes |
| `settings.json` | Recording toggle, hotkey, startup, UI/OCR language, AI endpoint/model/authorization flags, privacy consent version; **no API keys** |
| `app.log` | Local diagnostics such as startup, hotkey, tray, and paste failures; no clipboard text, image content, search queries, or API keys |

These local files are **not encrypted** by default. They are protected by Windows user-account permissions. Anyone or any program that can access your Windows account or data directory may read them. For stronger protection, use BitLocker, EFS, or another disk-encryption tool and restrict account access.

**Retention**: Local history, settings, and logs remain until you delete the data directory or clear history in Settings. `app.log` currently has no automatic rotation and remains until the data directory is deleted. Backups remain until you delete them.

### 4. Clipboard capture

- Recording is enabled by default after installation; the first run shows a privacy summary and asks for confirmation. You can pause recording at any time in Settings or the tray menu.
- The app respects Windows clipboard privacy formats: `ExcludeClipboardContentFromMonitorProcessing`, `Clipboard Viewer Ignore`, `CanIncludeInClipboardHistory=0`, and `CanUploadToCloudClipboard=0` cause the entire item to be skipped.
- The “never record these apps” list matches foreground process names on a best-effort basis; clipboard privacy formats remain the primary guarantee.
- Sensitive-content detection runs locally using rules for common key/token prefixes, private keys, JWTs, password fields, and high-entropy strings. Matches are marked sensitive and skipped by AI indexing and local OCR; you can manually remove or restore the flag locally.
- **Detection is heuristic and currently covers mainly text, HTML, and RTF.** Passwords, bank cards, or medical information visible only in an image may not be detected automatically. When image AI is enabled, the app asks you to confirm each image-bearing entry individually, but this does not guarantee that every secret is detected.
- Pure file copies (only `CF_HDROP`, with no real image data) are not stored; QQ/WeChat images that include both file paths and bitmap data are captured as images.
- Capture, storage, keyword search, and local OCR all happen on your device.

### 5. Optional AI features

AI features are off by default, and a new installation contains no vendor endpoint, model, or key. Requests occur only after you enter your own OpenAI-compatible endpoint, model, and API key and grant remote-data authorization.

Data that may be sent to **the endpoint you configure**:

- Text indexing: AI-searchable, non-sensitive text or plain text extracted from HTML;
- Image understanding: compressed images (data URLs) for image-bearing entries you individually approve, optional text context from the same entry, and the prompts used to generate descriptions/OCR;
- AI search: the query text you submit by pressing Enter with AI search enabled.

Boundaries:

- Remote endpoints must use HTTPS; HTTP is allowed only for loopback addresses.
- Text entries marked sensitive are not sent; each history entry also has its own “AI-searchable” flag.
- Image-bearing entries are not added to the AI index automatically; you must allow and confirm them individually on the history card. Images may contain passwords, banking information, or other sensitive content; assess them before confirming.
- Image-upload consent is separate from text consent; disabling image consent stops image uploads.
- You can clear AI descriptions/vectors at any time; keyword search and local history are unaffected.
- The AI provider you configure may log, retain, train on, or otherwise process request data under its own terms. That is outside Clippery's control and does not represent Clippery's position. Read the provider's privacy policy.
- If your endpoint is outside your country/region, data may be transferred across borders; that transfer is handled by the provider you choose. Assess it and obtain any required authorization.
- API keys are stored only in Windows Credential Manager: `Clippery/AiEmbeddingApiKey` and `Clippery/AiVisionApiKey`. They are never written to `settings.json`, `app.log`, or error messages.
- Some compatible services use provider-specific session headers (for example, `x-opencode-session` for OpenCode Go endpoints). This is for compatibility and does not contain clipboard text.

### 6. Local OCR

- Uses Windows `Windows.Media.Ocr`, enabled by default. Images and OCR text are processed locally and are not uploaded.
- OCR processes only non-sensitive image entries; recognized text is stored in `history.db` for keyword search and preview.
- OCR depends on Windows language packs. If no pack is available or the selected language is unavailable, Settings shows an unavailable/error message; the app does not crash.
- Auto mode prefers `zh-Hans-CN`, then other Chinese languages, then the configured or system language.

### 7. Logs

- `app.log` contains only diagnostics such as startup, hotkey, tray, and paste failures. It does not log clipboard text, image content, search queries, or API keys.
- Logs stay on your device until you delete the data directory; there is currently no automatic rotation or expiry.
- Review and redact logs before sharing them.

### 8. Backup and restore

- An export contains `manifest.json` and an `images/` folder as **plaintext** JSON and image files.
- **Sensitive entries are excluded from backups by default.** You may opt in via “Include sensitive entries”; the app warns again, and the backup will contain plaintext sensitive content.
- Backups do not include API keys, `settings.json`, or AI vectors. Reindex if you want semantic search after restore.
- Restore only merges and verifies SHA-256; existing history is not deleted. Duplicate entries are skipped.
- You choose the backup location. Store it securely and delete it when no longer needed. Uninstalling Clippery does not delete backups you saved elsewhere.

### 9. Deletion and retention

- Settings → History → Clear history deletes text, images, pins, search indexes, OCR text, AI descriptions/vectors, and the paste cache. This cannot be undone.
- Deleting `%LOCALAPPDATA%\Clippery` deletes local history, settings, logs, and cache.
- Uninstalling preserves `%LOCALAPPDATA%\Clippery` so history/settings can be restored after reinstall. Delete the directory manually for a full removal.
- Backups you saved elsewhere are not deleted by the uninstaller.
- If you contact us by email, we retain the email until the issue is resolved and delete it within a reasonable period unless law requires retention.

### 10. Your rights and legal bases

- Subject to applicable law, you have the right to access, copy, correct, and delete your personal information, withdraw consent, close an account (none currently), and obtain a copy of your data.
- Contact 1120166455@qq.com. We will respond within 15 working days unless law requires otherwise.
- The legal basis for processing local clipboard data is your consent (first-run confirmation and in-app toggles); processing necessary to provide the Software is based on contract; security and troubleshooting are based on our legitimate interests. Optional AI upload is based on your separate authorization.
- If you believe our processing violates applicable law, you may complain to a competent supervisory authority.

### 11. Security and breach notification

- We take reasonable measures to protect the Software and data, including minimizing cloud collection, storing API keys in Windows Credential Manager, and allowing HTTPS-only remote endpoints.
- Local data is not encrypted by default; Windows account permissions, disk encryption, and backup handling are your responsibility.
- If a breach affecting your personal information occurs, we will notify you and/or regulators as required by applicable law.

### 12. Children

The Software is not directed to children under 14. Children under 14 must use it with guardian consent and guidance. We do not knowingly collect personal information from children.

### 13. Third parties

Clippery uses the .NET 10 Desktop Runtime, Microsoft.Data.Sqlite/SQLitePCLRaw, Windows OCR/WinRT, and other components. Third-party licenses and copyright notices are in `THIRD-PARTY-NOTICES.md` and `THIRD-PARTY-NOTICES.TXT` in the installation directory. These components do not change the “no upload by default” behavior; optional AI requests go only to the endpoint you configure.

**Update check:** When you click “Check for updates,” or when “Check for updates automatically” is enabled, Clippery requests GitHub’s public endpoint `https://api.github.com/repos/54Lynnn/clippery-releases/releases/latest` to read the latest version, release notes, and installer metadata. The request does not include clipboard content, history, API keys, or account information; GitHub may see your IP address and standard HTTP headers. Automatic checks are enabled by default, run at most once a day, and can be disabled in Settings. Clippery does not silently download or install updates in the background.

### 14. Changes and contact

This notice is updated with releases. Material changes to data practices will be identified in release notes and, where required, re-confirmed on first run. For privacy questions, contact 1120166455@qq.com.

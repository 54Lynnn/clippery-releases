# Clippery 1.2.17

## 隐私同意闸门修复

- 历史面板现在在用户确认当前隐私说明前保持关闭，包括全局热键、托盘打开历史、双击托盘和第二实例唤起路径。
- 用户完成隐私确认后，原先待处理的打开历史请求会继续执行。
- 文本 AI 索引和图片 AI 托盘开关在未同意时会回弹为关闭状态，避免界面显示与实际状态不一致。

## 验证

- Windows 11 x64 端到端验证通过：全新启动、隐私版本升级、`--settings`、热键拦截、同意后恢复剪贴板采集。
- Release 构建使用 .NET SDK 10.0.404、SQLite 3.54.1 和 Inno Setup 6.7.4。
- SHA-256 将由正式发布脚本写入本文件和 `RELEASE-MANIFEST.json`。

## SHA-256

```text
79C75418069A7C2BB0C73296D462C5DBAF7397E2E60E8F4C7CA83DDA0C61FD94  Clippery-Setup-1.2.17.exe
```

## Detached signature

Use `RELEASE-SIGNING-KEY.asc` to verify `RELEASE-MANIFEST.json.asc` before trusting the manifest.

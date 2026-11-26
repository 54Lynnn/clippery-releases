# Security Policy

## Reporting a vulnerability

请不要在公开 Issue、Release 评论或公开聊天中粘贴剪贴板内容、图片、API Key、日志原文或可利用漏洞细节。请将安全问题发送到：`1120166455@qq.com`。

报告中请尽量包含：受影响版本、Windows 版本、复现步骤、影响范围和最小化的脱敏日志。不要发送真实剪贴板数据库、图片或 API Key；如确实需要样本，请先通过邮件确认安全的传输方式。

我们会在确认收到报告后回复，并在修复或缓解方案确定后更新报告人。当前支持范围是最新公开 Release；旧版本不承诺继续获得安全修复。

## Release integrity

公开安装包发布在 [clippery-releases](https://github.com/54Lynnn/clippery-releases)。下载后请使用同一 Release 中的 `SHA256SUMS.txt` 和 `RELEASE-MANIFEST.json` 校验文件名、版本和 SHA-256。当前安装包未做 Authenticode 签名，Windows SmartScreen 的未知发布者提示是预期行为。

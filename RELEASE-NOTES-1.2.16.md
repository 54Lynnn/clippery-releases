# Clippery 1.2.16

## 隐私同意闸门

- 首次运行、隐私说明升级和 `--settings` 启动在用户确认当前隐私说明前不会启动剪贴板采集。
- 文本 AI 自动索引和图片 AI 自动理解的后台任务也会等待确认；确认后按原有设置恢复。
- 增加隐私闸门回归测试，避免未同意时发生本地采集或远程 AI 后台处理。

## 版权与发布安全

- EULA 增加版本、生效日期和完整英文 Licensor 信息。
- 发布仓库增加漏洞报告入口、发布清单和安装包完整性校验信息。
- 源码仍保存在私有仓库，公开仓库只包含安装包、文档、许可证和第三方声明。

## 验证

- Release 构建：0 warning / 0 error
- 自动化测试：358/358
- SHA-256 将由正式发布脚本写入本文件和 `RELEASE-MANIFEST.json`。

## SHA-256

```text
98F3F766AD0200CF8FDCAE3F6DE7FA41ECB10790E769DBCDE061443A2B23B768  Clippery-Setup-1.2.16.exe
```

## Detached signature

Use `RELEASE-SIGNING-KEY.asc` to verify `RELEASE-MANIFEST.json.asc` before trusting the manifest.

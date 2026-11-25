# Clippery 1.2.12

这是 Clippery 的 Windows 安装包发布页。

## 下载

- `Clippery-Setup-1.2.12.exe`
- `SHA256SUMS.txt`

## 本版变更

- 图片理解与 Embedding 解耦。没有 Embedding 时仍可生成图片标题、描述和 OCR 文本。
- 配置 Embedding 后，为已有图片描述增量补写语义向量，不重复调用视觉模型。
- 图片描述指纹只跟随视觉配置，旧版组合指纹会自动迁移。
- 图片描述保存和清除时区分文本向量与视觉向量，避免破坏混合条目的文本语义索引。
- 图文条目增量回填保留原始文本和 HTML 上下文。
- 设置页区分图片描述数量和语义向量数量。
- 修正共享图片端点留空时的授权确认和实际端点显示。
- 更新隐私说明，明确更新检查访问 GitHub Releases 的行为。
- 构建 0 warning / 0 error；AI 相关测试 75/75；新增回归测试 4/4。

## 安装

1. 下载 `Clippery-Setup-1.2.12.exe`
2. 双击运行
3. 接受许可协议
4. 选择安装目录，默认 `%LOCALAPPDATA%\Programs\Clippery`
5. 安装并启动
6. 按 `Ctrl+Alt+V` 打开历史面板

每用户安装，不需要管理员权限；已包含 .NET 10 Desktop Runtime。

## 已知限制

- 安装包未签名，SmartScreen 可能显示“未知发布者”
- 升级需要手动下载安装包覆盖安装
- Windows 11 x64 已完成实机验收，Windows 10 21H2 仅完成静态兼容性审计
- 当前无账号、云同步或付费会员

## 隐私与许可

- [隐私说明](https://github.com/54Lynnn/clippery-releases/blob/main/PRIVACY.md)
- [最终用户许可协议](https://github.com/54Lynnn/clippery-releases/blob/main/LICENSE)
- [第三方组件与许可证](https://github.com/54Lynnn/clippery-releases/blob/main/THIRD-PARTY-NOTICES.md)

联系：1120166455@qq.com

## SHA-256

```text
118EE8152C137A2CA8945A596A1EBE7DB598792B132D302FB1CE14392B5E2020  Clippery-Setup-1.2.12.exe
```

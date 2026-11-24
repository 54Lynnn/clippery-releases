# Clippery 1.2.8

这是 Clippery 的 Windows 安装包发布页。

## 下载

- `Clippery-Setup-1.2.8.exe`
- `SHA256SUMS.txt`

## SHA-256

```text
5214C134CDF99756FF0F1CE0ED5587D6A08F2D6647F0EE1DD5114C3650E26310  Clippery-Setup-1.2.8.exe
```

## 本版变更

- 输入框、密码框、下拉框和复选框统一为 Fluent 浅色样式，补齐圆角、焦点、hover 和选中状态。
- 设置页新增“本机 OCR”Tab，六区导航与内容顺序一致。
- 历史面板顶部改为“AI 搜索”，与条目的 AI 索引区分；`Ctrl+Alt+V` 改为快捷键 keycap 样式。
- EULA 的版权/许可方信息块移到第一部分第 1 条首段之后；安装包许可页首屏不再展示主体信息，法律条款内容不变。
- 覆盖安装时如果 Clippery 正在运行，交互安装会提示关闭，静默安装会自动结束 Clippery 后继续；历史与设置保留。
- 构建 0 warning / 0 error；自动化测试 324/324 通过。

## 安装

1. 下载 `Clippery-Setup-1.2.8.exe`
2. 双击运行
3. 接受许可协议
4. 选择安装目录（默认 `%LOCALAPPDATA%\Programs\Clippery`）
5. 安装并启动
6. 按 `Ctrl+Alt+V` 打开历史面板

每用户安装，不需要管理员权限；已包含 .NET 10 Desktop Runtime。

## 已知限制

- 安装包未签名；SmartScreen 可能显示“未知发布者”，需 More info → Run anyway
- 无自动更新；升级请手动下载新安装包覆盖安装
- Windows 11 x64 已运行验证；Windows 10 21H2 LTSC/Enterprise 仅静态审计，未实机验收
- 当前无账号、云同步或付费会员

## 隐私与许可

- [隐私说明](https://github.com/54Lynnn/clippery-releases/blob/main/PRIVACY.md)
- [最终用户许可协议](https://github.com/54Lynnn/clippery-releases/blob/main/LICENSE)
- [第三方组件与许可证](https://github.com/54Lynnn/clippery-releases/blob/main/THIRD-PARTY-NOTICES.md)

联系：1120166455@qq.com

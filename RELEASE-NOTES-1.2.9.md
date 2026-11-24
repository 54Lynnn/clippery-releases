# Clippery 1.2.9

这是 Clippery 的 Windows 安装包发布页。

## 下载

- `Clippery-Setup-1.2.9.exe`
- `SHA256SUMS.txt`

## SHA-256

```text
9CCE77C10E8A005C33FC60BF3FA640877C843216256EE29C48D3415E2DB6E771  Clippery-Setup-1.2.9.exe
```

## 本版变更

- 修复历史面板图片缩略图只加载前 40 条的问题。
- 改为列表项进入可视区域时按需加载缩略图；滚动到更早的图片条目也会显示预览。
- 缩略图加载失败时仍保留“图”占位符，不影响复制和粘贴。
- 构建 0 warning / 0 error；自动化测试 324/324 通过。

## 安装

1. 下载 `Clippery-Setup-1.2.9.exe`
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

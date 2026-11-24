# Clippery 1.2.4

这是 Clippery 的 Windows 安装包发布页。

## 下载

- `Clippery-Setup-1.2.4.exe`
- `SHA256SUMS.txt`

## SHA-256

```text
169D600C6F9396C23A4CAE44A60424347C0C4F7BAF2758CBBEED125F697D4E58  Clippery-Setup-1.2.4.exe
```

## 本版变更

- 从 EULA 和隐私说明的中英文版本中移除公开地址
- 新增图片 AI 逐条确认策略和 4 个单元测试；含图片条目不会自动进入 AI 索引
- 备份导出默认排除敏感条目，Core 默认值改为 `includeSensitive: false`
- 自动化测试 324/324，备份/恢复测试 5/5
- 法律主体更正为：深圳市罗湖区莲塘街道哈吉米科技工作室（个体工商户）

## 安装

1. 下载 `Clippery-Setup-1.2.4.exe`
2. 双击运行
3. 接受许可协议
4. 选择安装目录（默认 `%LOCALAPPDATA%\Programs\Clippery`）
5. 安装并启动
6. 按 `Ctrl+Alt+V` 打开历史面板

每用户安装，不需要管理员权限；已包含 .NET 10 Desktop Runtime。

## 已知限制

- 安装包未签名；SmartScreen 可能显示“未知发布者”，需 More info → Run anyway
- 无自动更新；升级请手动下载新安装包覆盖安装
- Windows 11 x64 已实机验收；Windows 10 21H2 LTSC/Enterprise 仅静态审计，未实机验收
- 图片 AI 需要逐条确认；文本敏感检测不能保证识别图片中的秘密
- 当前无账号、云同步或付费会员

## 隐私与许可

- [隐私说明](https://github.com/54Lynnn/clippery-releases/blob/main/PRIVACY.md)
- [最终用户许可协议](https://github.com/54Lynnn/clippery-releases/blob/main/LICENSE)
- [第三方组件与许可证](https://github.com/54Lynnn/clippery-releases/blob/main/THIRD-PARTY-NOTICES.md)

联系：1120166455@qq.com

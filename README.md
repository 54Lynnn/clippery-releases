# Clippery Downloads

Clippery 是一个 Windows 本地剪贴板历史快捷面板：按 `Ctrl+Alt+V` 打开，用中文找回最近的文本、图片和图文记录，并可以写回剪贴板或直接粘贴到刚才的应用。

这个仓库**只用于发布安装包和发布说明**。Clippery 的应用源码是私有的，不在此仓库中。

## 下载

进入 [Releases](https://github.com/54Lynnn/clippery-releases/releases/latest)，下载：

```text
Clippery-Setup-1.2.4.exe
```

可选下载 `SHA256SUMS.txt` 校验安装包。

## 系统要求

- Windows 11 x64（已实机验证）
- Windows 10 21H2 LTSC/Enterprise / Windows 11 x64
- 安装包是 self-contained，已包含 .NET 10 Desktop Runtime，**不需要另装 .NET**
- Windows 10 Home/Pro 已停止微软支持，未验证，不承诺可用

## 安装

1. 下载 `Clippery-Setup-1.2.4.exe`
2. 双击运行
3. 接受许可协议
4. 选择安装目录（默认 `%LOCALAPPDATA%\Programs\Clippery`）
5. 可选创建桌面图标
6. 安装并启动 Clippery
7. 按 `Ctrl+Alt+V` 打开历史面板

安装是每用户的，不需要管理员权限。历史数据默认在 `%LOCALAPPDATA%\Clippery`。

## 校验安装包

PowerShell：

```powershell
Get-FileHash .\Clippery-Setup-1.2.4.exe -Algorithm SHA256
```

与 `SHA256SUMS.txt` 中的值比较。

## 未签名提示

当前安装包**未做代码签名**。从网上下载后，Windows SmartScreen 可能提示“未知发布者”或“Windows protected your PC”。这是未签名安装包的预期行为：

- 点 **More info**
- 点 **Run anyway**

如果你不希望绕过该提示，可以等后续签名版本。

## 卸载

从 Windows 设置 → 应用，或开始菜单的 `Uninstall Clippery` 卸载。

卸载默认**保留** `%LOCALAPPDATA%\Clippery` 的历史和设置；需要彻底删除时手动删除该目录。

## 隐私与许可

- [隐私说明](PRIVACY.md)
- [最终用户许可协议](LICENSE)
- [第三方组件与许可证](THIRD-PARTY-NOTICES.md)

客户端采用专有许可：可免费用于个人、非商业用途；商业使用、云同步、预设模型和 Token 服务需要单独的书面授权或服务条款。

开发者：深圳市罗湖区莲塘街道哈吉米科技工作室（个体工商户）  
联系：1120166455@qq.com

## 更新

当前没有自动更新。新版本会发布在本仓库 Releases，请手动下载新安装包覆盖安装。

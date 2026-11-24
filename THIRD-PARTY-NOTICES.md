# Clippery 第三方组件与许可证

**适用版本**　Clippery 1.2.4
**更新日期**　2026-11-23

Clippery 的 Windows 安装包包含自包含的 .NET 运行时和若干第三方组件。本文件列出随应用分发或用于构建/测试的主要组件及其许可证。各组件的版权归其各自作者所有；本文件不改变这些许可证的条款。

## 1. 随应用分发的主要组件

| 组件 | 版本 | 许可证 | 版权/来源 |
|---|---|---|---|
| .NET 10 Desktop Runtime（`Microsoft.NETCore.App` / `Microsoft.WindowsDesktop.App`） | 10.0.15 | MIT | Copyright (c) .NET Foundation and Contributors；https://github.com/dotnet/runtime |
| WPF / WinForms | .NET 10 | MIT | Copyright (c) .NET Foundation and Contributors；https://github.com/dotnet/wpf |
| Microsoft.Data.Sqlite / Microsoft.Data.Sqlite.Core | 10.0.4 | MIT | Copyright (c) .NET Foundation and Contributors；https://github.com/dotnet/efcore |
| SQLitePCLRaw.core / bundle_e_sqlite3 / provider_e_sqlite3 / lib.e_sqlite3 | 2.1.11 | Apache-2.0 | Copyright (c) Eric Sink and contributors；https://github.com/ericsink/SQLitePCL.raw |
| SQLite（由 SQLitePCLRaw 带入的原生库） | 3.x | Public Domain | https://www.sqlite.org/copyright.html |
| System.Drawing.Common | 10.0.4 | MIT | Copyright (c) .NET Foundation and Contributors；https://github.com/dotnet/winforms |
| Microsoft.Windows.SDK.NET.Ref（C#/WinRT 投影） | 10.0.19041.57 | Microsoft Windows SDK License | https://aka.ms/WinSDKLicenseURL |
| Windows API / WinRT / Windows.Media.Ocr | Windows 10/11 | Microsoft 软件许可条款 | 操作系统组件，随 Windows 提供 |

.NET 运行时还包含其他第三方组件。完整声明随安装包分发为安装目录中的 `THIRD-PARTY-NOTICES.TXT`；也可以查看：
https://github.com/dotnet/runtime/blob/main/THIRD-PARTY-NOTICES.TXT

## 2. 仅用于构建或测试的组件（不随应用分发）

| 组件 | 版本 | 许可证 | 说明 |
|---|---|---|---|
| Inno Setup | 6 | Inno Setup License | 用于生成安装包；生成的安装程序受 Inno Setup 许可证约束。Copyright (C) 1997-2026 Jordan Russell；Portions Copyright (C) 2000-2026 Martijn Laan |
| xUnit | 2.9.3 | Apache-2.0 | 测试框架；Copyright (c) .NET Foundation and Contributors |
| xunit.runner.visualstudio | 3.1.4 | Apache-2.0 | 测试运行器；Copyright (c) .NET Foundation and Contributors |
| Microsoft.NET.Test.Sdk | 17.14.1 | MIT | 测试 SDK；Copyright (c) Microsoft Corporation |
| coverlet.collector | 6.0.4 | MIT | 覆盖率收集器；Copyright (c) 2018 Toni Solarin-Sodara and contributors |

这些组件不会安装到最终用户的 Clippery 安装目录。

## 3. 开发期参考（不包含在发布物中）

Clippery 在开发前期仅将 **Relic v1.0.66** 作为剪贴板行为的参考和隔离验证工具。发布源码和安装包中**没有包含 Relic 的代码、二进制、数据库或运行时依赖**；详细的来源审计记录保存在项目的发布文档中。若未来需要复用任何 AGPL-3.0 代码，必须单独评估并遵守 AGPL 的开源义务。

## 4. 许可证全文

- .NET 运行时第三方声明：安装目录中的 `THIRD-PARTY-NOTICES.TXT`
- MIT 许可证全文：`licenses/MIT.txt`
- Apache License 2.0 全文：`licenses/Apache-2.0.txt`
- Microsoft Windows SDK 许可证：https://aka.ms/WinSDKLicenseURL
- SQLite 版权说明：https://www.sqlite.org/copyright.html
- Inno Setup 许可证：https://jrsoftware.org/isinfo.php

如你需要某一份许可证的纸质/单独副本，请通过获取 Clippery 的渠道联系发布者。

## 5. 商标

Clippery 的名称、图标和标识归其权利人所有。本文件不授予任何商标许可。第三方名称和标识归其各自权利人所有。

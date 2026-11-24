# Clippery 1.2.11

这是 Clippery 的 Windows 安装包发布页。

## 下载

- `Clippery-Setup-1.2.11.exe`
- `SHA256SUMS.txt`

## SHA-256

```text
08D8C242E836BB85BD45F5925E89C6D397451808A466BA6DEAB1D2D3178E0093  Clippery-Setup-1.2.11.exe
```

## 本版变更

- 历史面板支持 Space 切换预览：选中条目按 Space 打开，再按 Space 或 Esc 关闭。
- 预览多图时可用左右方向键切换上一张/下一张。
- 列表获得焦点时输入文字会自动回到搜索框并继续输入。
- 预览布局重做：左栏按原始顺序显示文字和图片缩略图，右栏放大选中图片。
- 预览增加独立原图窗口（默认最大化）：Space 打开，Space 或 Esc 返回预览；原图窗口里 ←/→ 切换图片；鼠标滚轮以指针位置为中心缩放，按住左键拖动平移，双击回到 100% 居中；点击右栏图片也可打开原图窗口，窗口内可用按钮调用默认程序打开。
- 预览中 ↑/↓ 滚动内容栏；切换图片时内容栏自动滚到当前图片。
- 有 HTML 信息的混合条目按 HTML 中文字/图片顺序排列；没有 HTML 的旧条目回退为“文字后图片”。
- 修复搜索框 placeholder 在聚焦时遮挡插入符的问题。
- 历史筛选菜单改为与设置页一致的 Fluent 风格。
- 右下角显示“当前热键 + 键盘操作”提示，修改热键后会跟随更新。
- 设置页 Tab 增加轻量 hover 反馈。
- 设置页整理：数据目录、打开数据目录、打开日志移到“通用”；关于页移除重复按钮，项目主页保留为链接，隐私说明/许可证/第三方声明改为文字链接，检查更新单独一栏。
- 设置页“界面语言”和“本机 OCR 语言”下拉框改为右侧对齐，复选框说明文字与复选框文字对齐；数据目录过长时可悬停查看完整路径。
- 设置页新增“检查更新”：显示已是最新或发现新版本；自动检查默认开启、每日最多一次，可在设置中关闭；托盘右键也可检查更新。本版只检测并打开发布页，不静默下载或安装。
- 构建 0 warning / 0 error；自动化测试 331/331 通过。

## 安装

1. 下载 `Clippery-Setup-1.2.11.exe`
2. 双击运行
3. 接受许可协议
4. 选择安装目录（默认 `%LOCALAPPDATA%\Programs\Clippery`）
5. 安装并启动
6. 按 `Ctrl+Alt+V` 打开历史面板

每用户安装，不需要管理员权限；已包含 .NET 10 Desktop Runtime。

## 已知限制

- 安装包未签名；SmartScreen 可能显示“未知发布者”，需 More info → Run anyway
- 无自动安装更新；本版只检测新版本并打开发布页，升级请手动下载新安装包覆盖安装
- Windows 11 x64 已运行验证；Windows 10 21H2 LTSC/Enterprise 仅静态审计，未实机验收
- 当前无账号、云同步或付费会员

## 隐私与许可

- [隐私说明](https://github.com/54Lynnn/clippery-releases/blob/main/PRIVACY.md)
- [最终用户许可协议](https://github.com/54Lynnn/clippery-releases/blob/main/LICENSE)
- [第三方组件与许可证](https://github.com/54Lynnn/clippery-releases/blob/main/THIRD-PARTY-NOTICES.md)

联系：1120166455@qq.com

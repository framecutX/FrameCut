# 映刻（FrameCut）下载

这里是映刻 Windows 安装包的官方发布仓库。仓库本身只保留这份说明，安装包通过 [GitHub Releases](https://github.com/framecutX/FrameCut/releases) 提供。

映刻是一款桌面视频编辑器，支持素材管理、视频预览、多轨时间线、图片/视频/音频/文字编辑、音频波形和 MP4 导出。

## 下载

- [下载最新版本](https://github.com/framecutX/FrameCut/releases/latest)
- [访问映刻官网](https://framecutx.github.io/)

当前 Windows 版本：`1.0.4+9`

| 项目 | 内容 |
| --- | --- |
| 安装包 | `framecut-1.0.4+9-setup.exe` |
| 系统 | Windows 10 / 11 x64 |
| 大小 | 327.97 MiB |
| SHA256 | `634a4eea2bdf204294cf0c396b977a3adf1d399d8f83450841eae40020db1306` |
| 签名 | 当前版本未进行代码签名 |

本版未通过完整 GUI 回归，嵌套预览仍记录到间歇性绑定循环警告。安装包已完成版本与载荷完整性检查。

可在 PowerShell 中核对安装包：

```powershell
Get-FileHash .\framecut-1.0.4+9-setup.exe -Algorithm SHA256
```

## 发布约定

每个正式版本使用 `v<versionName>+<versionCode>` 标签，例如 `v1.0.4+9`。Release 标题使用“映刻 `<versionName>+<versionCode>`”，安装包名称固定为：

```text
framecut-<versionName>+<versionCode>-setup.exe
```

发布时创建并推送对应标签，然后在 GitHub Release 中上传经过验收的安装包，填写版本变化、系统要求、文件大小和 SHA256。Release 设为正式版后，官网会通过 GitHub Releases API 自动读取最新版本和下载地址。

示例：

```powershell
git tag v1.0.4+9
git push origin v1.0.4+9
gh release create v1.0.4+9 `
  "D:\Qt5.6.3\projects\framecut\dist\1.0.4+9\windows-x64\framecut-1.0.4+9-setup.exe" `
  --title "映刻 1.0.4+9" `
  --notes-file "D:\Qt5.6.3\projects\framecut\docs\release-notes-v1.0.4+9.md"
```

此仓库不存放应用源码、构建产物目录、调试符号或私有发布证据。

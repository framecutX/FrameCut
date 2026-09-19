# 映剪（FrameCut）下载

这里是映剪 Windows 安装包的官方发布仓库。仓库本身只保留这份说明，安装包通过 [GitHub Releases](https://github.com/framecutX/FrameCut/releases) 提供。

映剪是一款桌面视频编辑器，支持素材管理、视频预览、多轨时间线、图片/视频/音频/文字编辑、音频波形和 MP4 导出。

## 下载

- [下载最新版本](https://github.com/framecutX/FrameCut/releases/latest)
- [访问映剪官网](https://framecutx.github.io/)

当前 Windows 版本：`1.0.1+5`

| 项目 | 内容 |
| --- | --- |
| 安装包 | `framecut-1.0.1+5-setup.exe` |
| 系统 | Windows 10 / 11 x64 |
| 大小 | 29.72 MiB |
| SHA256 | `03bc6f151dc93050a980107860b61243d5b556bb4f4595b9c35b72997d1386d4` |
| 签名 | 当前版本未进行代码签名 |

可在 PowerShell 中核对安装包：

```powershell
Get-FileHash .\framecut-1.0.1+5-setup.exe -Algorithm SHA256
```

## 发布约定

每个正式版本使用 `v<versionName>+<versionCode>` 标签，例如 `v1.0.1+5`。Release 标题使用“映剪 `<versionName>+<versionCode>`”，安装包名称固定为：

```text
framecut-<versionName>+<versionCode>-setup.exe
```

发布时创建并推送对应标签，然后在 GitHub Release 中上传经过验收的安装包，填写版本变化、系统要求、文件大小和 SHA256。Release 设为正式版后，官网会通过 GitHub Releases API 自动读取最新版本和下载地址。

示例：

```powershell
git tag v1.0.1+5
git push origin v1.0.1+5
gh release create v1.0.1+5 `
  "D:\Qt5.6.3\projects\framecut\dist\1.0.1+5\windows-x64\framecut-1.0.1+5-setup.exe" `
  --title "映剪 1.0.1+5" `
  --notes-file "D:\Qt5.6.3\projects\framecut\docs\release-notes-v1.0.1+5.md"
```

此仓库不存放应用源码、构建产物目录、调试符号或私有发布证据。

# 常见问题

## 导航

语言：[俄语](README.md) | [英语](README.en.md) | [法语](README.fr.md) | [中文](README.zh.md)

### Delphi

🎫 错误信息：

[错误] RLINK32：文件“uMain.dfm”中存在不支持的 16 位资源

🎫 错误位置：

Ctrl + F9

🎫 解决方案步骤 1：

Get-ChildItem -Path "C:\project_folder", "C:\Delphcomp" -Include *.dcu, *.~*, *.ddp, *.dsk, *.identcache, *.local -Recurse | Remove-Item -Force

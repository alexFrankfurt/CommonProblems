# CommonProblems

## Navigation
Language: [Russian](README.md) | [English](README.en.md) | [Français](README.fr.md) | [中文](README.zh.md)

### Delphi

🎫 Error text:
[Error] RLINK32: Unsupported 16-bit resource in file "uMain.dfm"

🎫 Error location:
Ctrl + F9

🎫 Solution steps 1:
Get-ChildItem -Path "C:\project_folder", "C:\Delphcomp" -Include *.dcu, *.~*, *.ddp, *.dsk, *.identcache, *.local -Recurse | Remove-Item -Force

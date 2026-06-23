# CommonProblems


## Navigation
Language: [Russian](README.md) | [English](README.en.md) | [Français](README.fr.md) | [中文](README.zh.md)



### Delphi


🎫 Текст ошибки:  
[Error] RLINK32: Unsupported 16bit resource in file "uMain.dfm"

🎫 Место обнаружения ошибки:  
Ctrl + F9

🎫 Шаги решения 1:  
Get-ChildItem -Path "C:\project_folder", "C:\Delphcomp" -Include *.dcu, *.~*, *.ddp, *.dsk, *.identcache, *.local -Recurse | Remove-Item -Force

# Problèmes courants

## Navigation
Langue : [Русский](README.md) | [English](README.en.md) | [Français](README.fr.md) | [中文](README.zh.md)

### Delphi

🎫 Texte de l'erreur :  
[Erreur] RLINK32 : Ressource 16 bits non prise en charge dans le fichier « uMain.dfm »

🎫 Emplacement de l'erreur :  
Ctrl + F9

🎫 Étapes de la solution 1 :  
Get-ChildItem -Path « C:\project_folder », « C:\Delphcomp » -Include *.dcu, *.~*, *.ddp, *.dsk, *.identcache, *.local -Recurse | Remove-Item -Force

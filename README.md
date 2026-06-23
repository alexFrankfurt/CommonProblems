# CommonProblems


## Navigation
Язык: [Русский](README.md) | [English](README.en.md) | [Français](README.fr.md) | [中文](README.zh.md)



### Delphi


🎫 Текст ошибки:  
[Error] RLINK32: Unsupported 16bit resource in file "uMain.dfm"

🎫 Место обнаружения ошибки:  
Ctrl + F9

🎫 Шаги решения 1:  
Get-ChildItem -Path "C:\project_folder", "C:\Delphcomp" -Include *.dcu, *.~*, *.ddp, *.dsk, *.identcache, *.local -Recurse | Remove-Item -Force





### Linux
🎫 Текст ошибки:
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), is another process using it?
❌ ❌ Failed to install curl, nodejs, or npm.

🎫 Место обнаружения ошибки:
sudo apt update

🎫 Шаги решения 1:
# 1. Find what's holding the lock
sudo fuser -v /var/lib/dpkg/lock-frontend 2>/dev/null || echo "No process holding lock"

# 2. Safely stop background updaters
sudo systemctl stop unattended-upgrades
sudo systemctl stop apt-daily.service apt-daily-upgrade.service

# 3. Clear locks & fix interrupted state
sudo rm -f /var/lib/dpkg/lock-frontend /var/lib/dpkg/lock /var/cache/apt/archives/lock
sudo dpkg --configure -a


Шаги решения 2:
# уменьшить с 1500 до 1350:
sudo ip link set dev ens33 mtu 1350

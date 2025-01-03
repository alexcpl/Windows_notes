## Enable WSL
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
## Enable Virtual Machine Platform
```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```
## Set WSL 2 as Default Version
```powershell
wsl --set-default-version 2
```
## Install Kali Linux
```powershell
wsl --install -d kali-linux
```
## Launch Kali Linux
```powershell
wsl -d kali-linux
```

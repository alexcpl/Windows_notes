# Backup to network drive

```cmd
@echo off
echo Backing up Desktop
xcopy %userprofile%\Desktop\*.* \\nas01\home\Desktop /Y /E /C /I /F
echo Backing up Documents
xcopy %userprofile%\Documents\*.* \\nas01\home\Documents /Y /E /C /I /F
echo Backing up Downloads
xcopy %userprofile%\Downloads\*.* \\nas01\home\Downloads /Y /E /C /I /F
pause
```

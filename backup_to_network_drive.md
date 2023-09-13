# Backup to network drive using xcopy

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
# using robocopy
Create a folder under c:\log to store the log files

```cmd
robocopy %userprofile%\Desktop \\nas\Backups\Desktop-01\Desktop /MIR /XA:H /W:0 /R:1 /REG /FFT >> C:\log\externalbackup.log
robocopy %userprofile%\Documents \\nas\Backups\Desktop-01\Documents /MIR /XA:H /W:0 /R:1 /REG /FFT >> C:\log\externalbackup.log
robocopy %userprofile%\Downloads \\nas\Backups\Desktop-01\Downloads /MIR /XA:H /W:0 /R:1 /REG /FFT >> C:\log\externalbackup.log
```

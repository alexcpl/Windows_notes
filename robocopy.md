### Robocopy example

```
robocopy %userprofile%\Documents \\nas\Backups\Desktop-01\Documents /MIR /XA:H /W:0 /R:1 /REG /FFT >> C:\log\externalbackup.log
robocopy %userprofile%\Desktop \\nas\Backups\Desktop-01\Desktop /MIR /XA:H /W:0 /R:1 /REG /FFT >> C:\log\externalbackup.log
```

Windows Environment Variables -- <https://ss64.com/nt/syntax-variables.html>

Create a backup.bat file under C:\Scripts\ (or any folder of your choice) using the commands provided. Then, you can set up a scheduled task to instruct Windows to perform daily backups to your destination.

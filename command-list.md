### Create user and add it to admin group

```
net user username [password] /add [/domain]

net local group administrators username /add

net group "Domain Admins"  username /add /domain
```

#### Auto time stamp in notepad

Simply put ".LOG" in the first line, then every time when saving the file,
notepad will put a timestamp at the end of the file.

#### Mount network drive

```
net use * \\server\share [password] /user:[domain\]username

example:
net use * \\192.168.1.5\backup veryStrongPassword /user:alex /persistent:yes
```

#### Time sync Windows Server command

```
@echo off
w32tm /config /manualpeerlist:64.147.116.229 /syncfromflags:MANUAL
w32tm /config /update
w32tm /resync
pause

@echo off
w32tm /config /syncfromflags:manual /manualpeerlist:0.pool.ntp.org,1.pool.ntp.org,2.pool.ntp.org,3.pool.ntp.org
w32tm /config /update
w32tm /resync
pause
```

[Time Server peer list](http://www.pool.ntp.org/en/use.html)

#### Enable Remote Desktop

Run cmd as Administrators

```
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 0 /f
```

Disable Remote Desktop

```
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Terminal Server" /v fDenyTSConnections /t REG_DWORD /d 1 /f
```

Enable Windows Firewall Remote Desktop rules

```
netsh advfirewall firewall set rule group="remote desktop" new enable=Yes
```

Disable firewall rules

```
netsh advfirewall firewall set rule group="remote desktop" new enable=No
```

#### Windows Control Panel commands

```
# WIN + R
control userpassword2

# Windows Default application
computerdefaults

# Fonts Clear Type Tune
cttune

# DirectX diagnostic tool
dxdiag

# Disk utilities management
diskmgmt.msc

# Microsoft config
msconfig

# Information panel
msinfo32

# Power panel
powercfg.cpl

# Steps Recorder
psr

# Windows version
winver

# Network connection center
ncpa.cpl

# Time and Time zone control panel
timedate.cpl

# Application control panel (add and remove programs)
appwiz.cpl

# Task Manager
taskmgr
```

#### Boot into BIOS/UEFI

```
# make a shortcut on Windows
cmd.exe /k shutdown /r /fw /t 1
```

#### Restart IIS

```
iisreset -noforce
```

Usage: iisreset [computername]

```
/RESTART -- Stop and then restart all Internet services.
/START -- Start all Internet services.
/STOP -- Stop all Internet services.
/REBOOT -- Reboot the computer.
/REBOOTONERROR -- Reboot the computer if an error occurs when starting, stopping, or restarting Internet services.
/NOFORCE -- Do not forcefully terminate Internet services if attempting to stop them gracefully fails.
/TIMEOUT:val -- Specify the timeout value ( in seconds ) to wait for a successful stop of Internet services. On expiration of this timeout the computer can be rebooted if the /REBOOTONERROR parameter is specified. The default value is 20s for restart, 60s for stop, and 0s for reboot.
/STATUS -- Display the status of all Internet services.
/ENABLE -- Enable restarting of Internet Services on the local system.
/DISABLE -- Disable restarting of Internet Services on the local system.
```

### Windows tweaks 
[CHrisTitus](https://christitus.com)<br>
[GitHub](https://github.com/ChrisTitusTech/winutil)<br>

__Stable Branch__
```
irm "https://christitus.com/win" | iex
```

# CreateNewWinAdmin

```cmd
cd %windir%\system32
net user tempadmin /add
net user tempadmin /active:yes
net user tempadmin 12345
net localgroup administrators tempadmin /add
```

# Chris Titus Tech's Windows Utility
-   Press the Windows key.
-   Type "PowerShell" or "Terminal" (for Windows 11).
-   Press `Ctrl + Shift + Enter` or Right-click and choose "Run as administrator" to launch it with administrator privileges.

```
irm "https://christitus.com/win" | iex
```
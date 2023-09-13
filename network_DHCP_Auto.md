# Set network interface to get IP from DHCP server
```cmd
@ECHO OFF
netsh int ip set address "Ethernet" source=dhcp
netsh int ip set dns "Ethernet" source=dhcp
ipconfig /renew
netsh int ip show config
pause
```

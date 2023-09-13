# Set network interface to get IP from DHCP server
```cmd
@ECHO OFF
netsh int ip set address "Ethernet" source=dhcp
netsh int ip set dns "Ethernet" source=dhcp
ipconfig /renew
netsh int ip show config
pause
```

# Set network interface to static IP
* change it to your own IP network
```cmd
@echo off
netsh interface ip set address "Ethernet" static 10.0.38.16 255.255.255.0 10.0.38.254
netsh interface ipv4 add dnsserver "Ethernet" 10.0.38.254 index=1
netsh interface ipv4 add dnsserver "Ethernet" 8.8.8.8 index=2
netsh int ip show config
pause
```

### example
```cmd
netsh interface ipv4 set address "Local Area Connection" static 10.0.38.16 255.255.255.0 10.0.38.254
netsh interface ipv4 add dnsserver "Local Area Connection" 8.8.8.8 index=1
netsh interface ipv4 add dnsserver "Local Area Connection" 8.8.4.4 index=2

::netsh interface ipv4 set address "Local Area Connection" source=dhcp
::netsh interface ipv4 set dnsserver "Local Area Connection" source=dhcp
pause
```

# List wifi profile

```cmd
@echo off
netsh wlan show profile
```
get the ssid
```cmd
netsh wlan show profile <<SSID>> key=clear
```

# Create user add to administrator group

```cmd
cd %windir%\system32
net user tempadmin /add
net user tempadmin /active:yes
net user tempadmin 12345
net localgroup administrators tempadmin /add
```

1. Create Folder
2. share it

net share
net user

# access the share_folder
\\your-ip\share_folder

# open firewall port
TCP 139
TCP 445

# find what is running on port 80
netstat -an | findstr "80"

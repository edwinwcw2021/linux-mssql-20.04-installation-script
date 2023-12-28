# Install Microsoft SQL Server 2022 in ubuntu linux in 3 minutes
---
## Prerequisites:
Steps to install and access Ubuntu Linux using a virtual machine and PuTTY:  

Choose a virtual machine software or Run Ubuntu Linux for free, indefinitely on [Oracle Cloud's Free Tier](https://www.oracle.com/uk/cloud/free/).  

#### Virtual machine software
1. Download and install either [VMware Workstation Player](https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html) or [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads). Both are free for personal use.  
2. Download Ubuntu Linux: Visit the official [Ubuntu website]([https://ubuntu.com/download/desktop](https://ubuntu.com/download/server)) and download the latest version of Ubuntu Server.  
3. On your client machine download [PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html).

Open PuTTY.
Enter the IP address of the Ubuntu virtual machine(usually displayed within the virtual machine software).

Click "Open."
Log in using the username and password you created during Ubuntu installation.
Now you can access and interact with the Ubuntu Linux environment from your client machine using PuTTY.

#### Steps to install MSSQL
```
curl https://packages.microsoft.com/keys/microsoft.asc | sudo tee /etc/apt/trusted.gpg.d/microsoft.asc  
```
  
```  
add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2022.list)"
```
  
```
apt-get update
apt-get install -y mssql-server
```
  
```
/opt/mssql/bin/mssql-conf setup
```
  
```
systemctl status mssql-server
```
  
```
apt install net-tools -y
```
  
```
netstat -tulpn
```
  
Drop by my [youtube channel for details](https://youtu.be/W5hO_xuZ8JI)  
Drop by my [rumble channel for details](https://rumble.com/v3xn46a-mssql-installation-on-linux-in-3-minutes.html)  


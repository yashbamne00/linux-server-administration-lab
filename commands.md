# Linux Commands Reference

This document contains the Linux commands used throughout this project along with a brief explanation of each command.

---

# System Information

Check the current user:

```bash
whoami
```

Display the hostname:

```bash
hostname
```

Show Linux version:

```bash
lsb_release -a
```

Display system uptime:

```bash
uptime
```

---

# Package Management

Update package list:

```bash
sudo apt update
```

Upgrade installed packages:

```bash
sudo apt upgrade -y
```

Remove unused packages:

```bash
sudo apt autoremove -y
```

Install a package:

```bash
sudo apt install <package-name>
```

Remove a package:

```bash
sudo apt remove <package-name>
```

Search for a package:

```bash
apt search <package-name>
```

---

# User Management

Create a user:

```bash
sudo adduser username
```

Delete a user:

```bash
sudo deluser username
```

View all users:

```bash
cat /etc/passwd
```

Switch user:

```bash
su username
```

Check current groups:

```bash
groups
```

---

# Group Management

Create a group:

```bash
sudo groupadd groupname
```

Add a user to a group:

```bash
sudo usermod -aG groupname username
```

View user groups:

```bash
groups username
```

---

# File & Directory Commands

Display current directory:

```bash
pwd
```

List files:

```bash
ls
```

Detailed list:

```bash
ls -l
```

Create a directory:

```bash
mkdir directory_name
```

Remove a directory:

```bash
rmdir directory_name
```

Copy files:

```bash
cp source destination
```

Move or rename files:

```bash
mv source destination
```

Delete files:

```bash
rm filename
```

Display directory tree:

```bash
tree
```

---

# File Permissions

Change permissions:

```bash
chmod 755 filename
```

Change owner:

```bash
sudo chown user:group filename
```

Change group:

```bash
sudo chgrp groupname filename
```

View file permissions:

```bash
ls -l
```

Check default permissions:

```bash
umask
```

---

# Networking

Display IP address:

```bash
ip a
```

Show network interfaces:

```bash
ip link
```

Display routing table:

```bash
ip route
```

Check network connections:

```bash
netstat -tuln
```

Test connectivity:

```bash
ping google.com
```

---

# SSH

Start SSH service:

```bash
sudo systemctl start ssh
```

Enable SSH at boot:

```bash
sudo systemctl enable ssh
```

Check SSH status:

```bash
sudo systemctl status ssh
```

Connect to a remote server:

```bash
ssh username@server_ip
```

Generate SSH key:

```bash
ssh-keygen
```

---

# Apache

Install Apache:

```bash
sudo apt install apache2
```

Start Apache:

```bash
sudo systemctl start apache2
```

Restart Apache:

```bash
sudo systemctl restart apache2
```

Check Apache status:

```bash
sudo systemctl status apache2
```

---

# Nginx

Install Nginx:

```bash
sudo apt install nginx
```

Start Nginx:

```bash
sudo systemctl start nginx
```

Restart Nginx:

```bash
sudo systemctl restart nginx
```

Check Nginx status:

```bash
sudo systemctl status nginx
```

---

# MariaDB

Install MariaDB:

```bash
sudo apt install mariadb-server
```

Secure installation:

```bash
sudo mysql_secure_installation
```

Open MariaDB:

```bash
sudo mysql
```

---

# Firewall (UFW)

Allow SSH:

```bash
sudo ufw allow ssh
```

Allow HTTP:

```bash
sudo ufw allow http
```

Allow HTTPS:

```bash
sudo ufw allow https
```

Enable firewall:

```bash
sudo ufw enable
```

Check firewall status:

```bash
sudo ufw status
```

---

# Cron Jobs

Edit cron jobs:

```bash
crontab -e
```

View cron jobs:

```bash
crontab -l
```

---

# Service Management

Check service status:

```bash
sudo systemctl status service_name
```

Start a service:

```bash
sudo systemctl start service_name
```

Stop a service:

```bash
sudo systemctl stop service_name
```

Restart a service:

```bash
sudo systemctl restart service_name
```

Enable service at boot:

```bash
sudo systemctl enable service_name
```

---

# Log Analysis

View system logs:

```bash
journalctl
```

Monitor logs in real time:

```bash
tail -f /var/log/syslog
```

View authentication logs:

```bash
less /var/log/auth.log
```

---

# Disk & Memory

Disk usage:

```bash
df -h
```

Directory size:

```bash
du -sh *
```

Memory usage:

```bash
free -h
```

Running processes:

```bash
htop
```

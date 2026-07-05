# Network Configuration

This document provides an overview of the networking setup used in the Linux Server Administration Lab.

---

# Virtual Machine Network

The Ubuntu Server virtual machine runs inside Oracle VirtualBox.

Network Mode:

* **Bridged Adapter**

Using a Bridged Adapter allows the virtual machine to appear as a separate device on the local network. This makes it possible to connect to the server from the host computer using SSH and access hosted web services through a web browser.

---

# Network Architecture

```text
Windows Laptop
      │
      ▼
VirtualBox
      │
      ▼
Ubuntu Server
      │
      ├── SSH (Port 22)
      ├── Apache (Port 80)
      ├── Nginx (Port 80)
      └── MariaDB (Local Database)
```

---

# Check IP Address

Display the assigned IP address:

```bash
ip a
```

or

```bash
hostname -I
```

Example:

```text
192.168.1.120
```

---

# Test Network Connectivity

Ping another device or website:

```bash
ping google.com
```

---

# View Network Interfaces

```bash
ip link
```

---

# View Routing Information

```bash
ip route
```

---

# Open Ports

The following ports are used in this project:

| Service | Port | Protocol | Purpose              |
| ------- | ---: | -------- | -------------------- |
| SSH     |   22 | TCP      | Remote server access |
| HTTP    |   80 | TCP      | Web server           |
| HTTPS   |  443 | TCP      | Secure web server    |

---

# Firewall Rules

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

Verify firewall status:

```bash
sudo ufw status
```

---

# SSH Connection

Connect to the server from another computer:

```bash
ssh username@server_ip
```

Example:

```bash
ssh developer@192.168.1.120
```

---

# Verify Running Services

Check if SSH is listening:

```bash
sudo systemctl status ssh
```

Check Apache:

```bash
sudo systemctl status apache2
```

Check Nginx:

```bash
sudo systemctl status nginx
```

---

# Useful Network Commands

Display IP address:

```bash
ip a
```

Show listening ports:

```bash
netstat -tuln
```

Display active network connections:

```bash
ss -tuln
```

Check DNS resolution:

```bash
nslookup google.com
```

Display hostname:

```bash
hostname
```

---

# Summary

This project uses a simple bridged network configuration to simulate a real Linux server connected to a local network. The server can be managed remotely using SSH, serves web pages through Apache or Nginx, and is protected by UFW firewall rules. This setup provides a practical environment for learning Linux networking and server administration.

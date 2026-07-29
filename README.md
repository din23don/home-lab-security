# home-lab-security

## Project Overview

This project is a personal Linux home laboratory created for learning Linux administration, networking, SSH, security basics and system documentation.

The laboratory contains two virtual machines:

- Ubuntu Server — main server
- Kali Linux — testing and security analysis machine

Virtualization platform:

- VirtualBox

---

# Lab Architecture

```
Host Machine

|
VirtualBox Network

----------------------------

Ubuntu Server Kali Linux

Server VM Testing VM

NAT NAT
10.0.2.15 Internet

Host-only Host-only
192.168.56.101 <-------> Kali
```

---

# Technologies Used

- Ubuntu Server
- Kali Linux
- VirtualBox
- SSH
- Netplan
- UFW Firewall
- Nmap
- Wireshark
- GitHub Documentation

---

# Completed Tasks

## Virtual Machine Setup

Completed:

- Created Ubuntu Server VM
- Created Kali Linux VM
- Configured VirtualBox networking
- Configured Host-only communication

Ubuntu network:

```
enp0s3:
10.0.2.15

enp0s8:
192.168.56.101
```

---

# SSH Configuration

Configured remote administration using SSH.

Connection test from Kali:

```bash
ssh labuser@192.168.56.101
```

Result:

- SSH connection successful

Documentation:

```
ubuntu-server/ssh.md
```

---

# Linux Users and Permissions

Performed Linux administration tasks:

Checked groups:

```bash
groups
```

Checked sudo permissions:

```bash
sudo -l
```

Studied:

- users
- groups
- file permissions
- ownership

Documentation:

```
ubuntu-server/users.md
ubuntu-server/permissions.md
```

---

# System Logs

Analyzed Linux logs:

Commands used:

```bash
journalctl -n 20
```

```bash
sudo journalctl -u ssh
```

```bash
last
```

Documentation:

```
ubuntu-server/logs.md
```

---

# Network Testing

## Nmap

Performed network scanning from Kali Linux:

```bash
nmap 192.168.56.101
```

Detected:

```
22/tcp open ssh
```

---

# Wireshark

Captured network traffic between Kali Linux and Ubuntu Server.

Tests performed:

ICMP:

```bash
ping 192.168.56.101
```

SSH traffic:

```bash
ssh labuser@192.168.56.101
```

Documentation:

```
ubuntu-server/wireshark.md
```

---

# Firewall Configuration

Configured Ubuntu firewall using UFW.

Installed:

```bash
sudo apt install ufw -y
```

Allowed SSH:

```bash
sudo ufw allow ssh
```

Enabled firewall:

```bash
sudo ufw enable
```

Added HTTP access for Apache testing:

```bash
sudo ufw allow http
```

Verified using:

```bash
nmap 192.168.56.101
```

Allowed services:

```
22/tcp SSH
80/tcp HTTP
```

Documentation:

```
ubuntu-server/firewall.md
```

---

# Repository Structure

```
HomeLab/

├── README.md

├── ubuntu-server/

│ ├── setup.md
│ ├── ssh.md
│ ├── users.md
│ ├── permissions.md
│ ├── logs.md
│ ├── wireshark.md
│ └── firewall.md

└── screenshots/

├── ssh.png
├── nmap.png
├── permissions.png
├── logs.png
├── wireshark.png
├── ufw-status.png
├── apache-status.png
├── ufw-nmap.png
└── firewall-http-test.png
```

---

# Skills Practiced

During this project I practiced:

- Linux server installation
- Virtual networking
- SSH administration
- User and permission management
- Log analysis
- Network scanning
- Packet analysis
- Firewall configuration
- Technical documentation

---

# Future Improvements

Planned next steps:

- Fail2ban installation
- Docker deployment
- Web server configuration
- Bash automation scripts
- System monitoring
- Additional security testing


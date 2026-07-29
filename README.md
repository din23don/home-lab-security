# home-lab-security

## Project Overview

This project is a personal Linux home laboratory created for learning Linux administration, networking, SSH, security basics and system documentation.

## Environment

- Ubuntu Server
- Kali Linux
- VirtualBox
- NAT + Host-only Network
- SSH

# Lab Architecture

```
Host Machine
VirtualBox Network
Ubuntu Server Kali Linux
Server VM Testing VM

NAT NAT
10.0.2.15 Internet

Host-only Host-only
192.168.56.101 <-------> Kali
```


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

## Completed Tasks

### Linux Administration

- User management
- File permissions
- System logs

### Networking

- SSH
- Ping
- Nmap
- Wireshark

### Security

- UFW Firewall configuration
- Fail2ban installation
- SSH brute-force attack testing from Kali Linux
- Automatic IP blocking and unbanning

### Containers

- Docker installation
- Running an Nginx container
- Verifying web access from Kali Linux

### Automation

- Bash backup script
- Automatic backups using Cron

## Repository Structure

```text
HomeLab/
│
├── README.md
├── ubuntu-server/
└── screenshots/
```

---

## Documentation

- setup.md
- ssh.md
- users-permissions.md
- permissions.md
- logs.md
- wireshark.md
- firewall.md
- fail2ban.md
- docker.md
- bash-automation.md
- cron.md

## Skills Practiced

- Linux Administration
- Networking
- SSH
- Firewall Management
- Fail2ban
- Docker
- Bash Scripting
- Cron Automation

## Author

This Home Lab was created as a personal learning project to develop practical Linux system administration skills.

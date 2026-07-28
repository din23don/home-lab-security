# SSH Configuration

## Overview

SSH (Secure Shell) is used for remote administration of Linux Servers.

In this lab, SSH is used to practice remote server managment.

## Installation

OpenSSH server was installed on Ubuntu Server:

```bash
sudo apt install openssh-server -y
```
## SSH Service Status Check

The SSH service status was checked using:

```bash
sudo systemctl status ssh
```

Expected resault:

```text
Active: active (running)
```
## Enable SSH Service

SSH was configured to start automaticaly after system reboot:

```bash
sudo system enable ssh
```

## Network Configuration

Server IP address was checked:

```bash
ip a
```

## Skill Practicing

- Installing OpenSSH server
- Managing Linux services
- Checking service status
- Preparing server for remote administration

## Screenshots 

Screenshoots  showing SSH configuration will be added to this section.


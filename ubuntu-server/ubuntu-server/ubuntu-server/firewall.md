# Linux Firewall (UFW)

## Objective 

Configure Ubuntu Server firewall and control network access using UFW.

## Environment

- Ubuntu Server
- Kali Linux
- VirtualBox Host-Only Network

Ubuntu IP:

```text
192.168.56.101
```

## Check firewall status

```bash
sudo ufw status
```
## Allow SSH access

Before enabling the firewall, SSH access was allowd:

```bash
sudo ufw allow ssh
```
SSH uses:

```text
TCP port 22
```

## Enable firewall

Firewall was enabled:

```bash
sudo ufw enable
```
Check configuration:

```bash
sudo ufw status verbose
```
Result:

```text
Status: active
22/tcp allow
```
## Testing with Nmap

From Kali Linux:

```bash
nmap 192.168.56.101
```
Result:

```text
22/tcp open ssh
```
SSh remined available after enabling the firewall.

# Testing HTTP access

## Installing apache

Apache web server was installed:

```bash
sudo apt install apache2 -y
```
Service check:

```bash
sudo systemctl status apache2
```
Apache listens on:

```text
TCP port 80
```
## Allow HTTP traffic

HTTP sccess was allowd:

```bash
sudo ufw allow http
```
Firewall rules:

```bash
sudo ufw status verbose
```
Result:

```text
22/tcp ALLOW
80/tcp ALLOW
```

## Final Nmap test

From Kali Linux:

```bash
nmap 192.168.56.101
```
Result:

```text
22/tcp open ssh
80/tcp open http
```
## Conclusion

The Ubuntu Server firewall was successfully configured.

Only required services were allowd:
- SSH for remote administration
- HTTP for web access

Network exposure was controlled using UFW and verified using Nmap.

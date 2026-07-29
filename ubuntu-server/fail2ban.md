# Fail2ban SSH Protection

## Objective

Configure Fail2ban on Ubuntu Server to protect SSH from brute-force login attempts.

## Environment

- Ubuntu Server
- Kali Linux
- VirtualBox Host-only Network

Ubuntu IP:

```
192.168.56.101
```

---

## Installing Fail2ban

Fail2ban was installed on Ubuntu Server:

```bash
sudo apt install fail2ban -y
```

Check service status:

```bash
sudo systemctl status fail2ban
```

Result:

```
active (running)
```

---

## SSH Protection Configuration

A custom configuration file was created:

```
/etc/fail2ban/jail.local
```

Configuration:

```ini
[sshd]

enabled = true
port = ssh
filter = sshd
logpath = /var/log/auth.log
maxretry = 3
bantime = 10m
```

Explanation:

- `enabled = true` — enables SSH protection
- `port = ssh` — monitors SSH service
- `logpath` — location of authentication logs
- `maxretry = 3` — maximum failed login attempts
- `bantime = 10m` — IP block duration

---

## Restarting Fail2ban

After configuration changes:

```bash
sudo systemctl restart fail2ban
```

---

## Checking Fail2ban Status

General status:

```bash
sudo fail2ban-client status
```

SSH jail status:

```bash
sudo fail2ban-client status sshd
```

Expected result:

```
Status for the jail: sshd

Currently failed: 0
Currently banned: 0
Total banned: 0
```

---

## Security Result

Fail2ban successfully protects the SSH service.

Protection features:

- monitors SSH authentication logs
- detects failed login attempts
- automatically blocks suspicious IP addresses

---


## Conclusion

Fail2ban adds an additional security layer to Ubuntu Server.

Together with UFW firewall, it provides protection against unauthorized SSH login attempts.


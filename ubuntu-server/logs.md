# Linux Logs Analysis

## Overview

Monitoring and analyzing system logs is an essential task for Linux administration and cybersecurity.

## Commands Used

Display recent system events:

```bash
journalctl -xe
```

View authentication logs:

```bash
sudo cat /var/log/auth.log
```

Show login history:

```bash
last
```

Searching for failed login attemps:

```bash
sudo grep "Failed" /var/log/auth.log
```

## Skills Practiced 

- Reading Linux system logs
- Reviewing authentication events
- Investigating login history
- Searching for failed login attempts
- Understanding basic log analysis

## Screenshots
Screenshots demonstrating log analysis will be added here.

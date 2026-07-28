# Users and Permissions Management 

## Overview

Linux user management and file permissions are fundamental skills for server administration and security.

## User Creation

A new user was created:

```bash
sudo adduser analyst
```
User verification:

```bash
cat /etc/passwd | grep analyst
```
Groups check:

```bash
groups analyst
```
## File permition

A test file was created:

```bash
touch security_test.txt
```
Permission were checked:

```bash
ls -l security_test.txt
```

## Changing permission:

File permission were modified using chmod:

```bash
chmod 600 security_test.txt
```
Result:

- Owner: read and write permissions
- Group: no permissions
- Others: no permissions

## Changing ownership 

File ownership was changed using:

```bash
sudo chown analyst security_test.txt
```

## Skills practiced

- Creating Linux users
- Checking user information
- Understanding file permissions
- Using chmod
- Using chown


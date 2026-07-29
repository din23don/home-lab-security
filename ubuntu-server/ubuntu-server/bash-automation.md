# Bash Automation - Backup Script

## Objective

Create a simple Bash script to automate backup creation on Ubuntu Server.

## Script Location

The backup script was created in the user's home directory:

```text
/home/labuser/scripts/backup.sh
```

## Script


```bash
#!/bin/bash
DATE=$(date +%Y-%m-%d)
BACKUP_DIR="/home/labuser/backups"
mkdir -p $BACKUP_DIR
tar -czf $BACKUP_DIR/backup-$DATE.tar.gz /home/labuser
echo "Backup completed: $DATE" >> $BACKUP_DIR/backup.log
```

## Make the Script Executable

The script was given execute permissions:

```bash
chmod +x ~/scripts/backup.sh
```

Permissions were verified:

```bash
ls -la ~/scripts
```

Result:

```text
-rwxr-xr-x 1 labuser labuser backup.sh
```

## Running the Script

The script was executed manually:

```bash
~/scripts/backup.sh
```

## Backup Verification

The backup directory was checked:

```bash
ls -la ~/backups
```

The following files were created:

- backup-YYYY-MM-DD.tar.gz
- backup.log

The log file was verified:


```bash
cat ~/backups/backup.log
```

Result:

```text
Backup completed: YYYY-MM-DD
```

## Conclusion

A Bash script was successfully created to automate backup creation.

The script creates a compressed archive of the user's home directory and records each execution in a log file.

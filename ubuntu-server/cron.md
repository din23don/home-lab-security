# Cron Job Automation

## Objective

Configure Cron to automatically run the backup script on Ubuntu Server.

## Verify Cron Service

The Cron service was checked:

```bash
sudo systemctl status cron
```

Result:

```text
active (running)
```

## Edit User Crontab

The user's crontab was opened:

```bash
crontab -e
```

## Testing the Cron Job

To verify that Cron was working correctly, the backup script was scheduled to run every minute:

```text
* * * * * /home/labuser/scripts/backup.sh
```

This configuration was used only for testing purposes.

## Verify Automatic Execution

After waiting a few minutes, the backup directory and log file were checked:

```bash
ls -la ~/backups
```

```bash
cat ~/backups/backup.log
```

The log confirmed that the script was executed automatically by Cron.

## Final Configuration

After successful testing, the Cron schedule was changed to run once per day at 02:00:

```text
0 2 * * * /home/labuser/scripts/backup.sh
```

## Verify Scheduled Jobs

The configured Cron jobs were displayed using:

```bash
crontab -l
```

## Conclusion

Cron was successfully configured to automate the execution of the backup script.

This allows backups to be performed automatically without manual intervention.

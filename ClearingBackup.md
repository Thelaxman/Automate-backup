** Clearing the backup files that are no longer needed
If we were to let this cronjob run indefinitely, after a while we would end up with a lot of backups in /var/backups. Over time this will cause the disk space being used to grow and could fill our disk. It’s probably best that
we don’t let that happen. To mitigate this risk, we’ll setup another cronjob that runs everyday and cleans up old backups that we don’t need to store

** "FIND" command
Find command is used to find files based on all kinds of criteria and listing them or doing other things to them, such as deleting them. 

```bash
vagrant@ubuntu2204:~$ sudo find /var/backups -name "home.*.tar.gz"
/var/backups/home.2024-05-26.tar.gz
...
```
What this command is doing is looking for all of the files in /var/backups that start with home. and end with .tar.gz. The * is a wildcard character that matches any string.

*** create a scheduled task that will find all of the files older than 7 days in /var/backups and delete them. Run sudo crontab -e and install the following cronjob.

```bash
30 5 * * * find /var/backups -name "home.*.tar.gz" -mtime +7 -delete
```

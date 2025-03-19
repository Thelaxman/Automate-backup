# Automate-backup

Documnetation on Automating a backup in a linux environmnet on a virtual server running on AWS. The backup would be scheduled to run once every week based on a Cronjob script.

## Crontab

Crontab is a configuration that specifies commands to be run periodically at fixed times, dates, or intervals.

### Basic Crontab Commands:

- crontab -l - Lists the current cron jobs.
- crontab -e - Edits the crontab file.
- crontab -r - Removes the current crontab file.

## Cronjob

A cronjob is a specific task or command that is scheduled to run at regular intervals. Cronjobs are defined inside the crontab file using a specific syntax.


## Prerequisite

- Running Server locally or remotely.
- Ubuntu(preferred) or any other linux distro OS.
- SSH access to the remote server(if server is hosted remotely).

## Tasks
- Schedule daily backups of user’s home directories.
- Schedule a task that looks for any backups that are more than 7 days old and deletes them

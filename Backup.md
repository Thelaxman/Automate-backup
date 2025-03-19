# Automating Backups

## Task: Create a backup of user's home directory.

### Script that creates a compressed archive of all of the user's home directory using the "tar(tape archive)" utility.

```bash
vagrant@ubuntu2204:~$ sudo tar -czvf /var/backups/home.tar.gz /home/
tar: Removing leading `/' from member names
/home/
/home/ubuntu/
/home/ubuntu/.profile
/home/ubuntu/.bash_logout
/home/ubuntu/.bashrc
/home/ubuntu/.ssh/
/home/ubuntu/.ssh/authorized_keys
...
```
### Creating a Cronjob with the test-script created above that will be executed everyday at 05:00

```bash
sudo crontab -e

0 5 * * * tar -zcf /var/backups/home.$(date -I).tar.gz /home/

```

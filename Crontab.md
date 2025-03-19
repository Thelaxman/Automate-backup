In Linux we use the crontab command to interact with tasks scheduled with the cron daemon. Each user, including the root user, can schedule jobs that run as their user.
Display your user’s crontab with crontab -l.

```bash
vagrant@ubuntu2204:~$ crontab -l
no crontab for vagrant
```
No crontab will showup since we haven't created one yet. 

## Create one using the command: crontab -e

```bash
vagrant@ubuntu2204:~$ crontab -e
no crontab for vagrant - using an empty one

Select an editor.  To change later, run 'select-editor'.
  1. /bin/nano        <---- easiest
  2. /usr/bin/vim.basic
  3. /usr/bin/vim.tiny
  4. /bin/ed

Choose 1-4 [1]: 2
```
At the bottom of the file add the following cronjob and then save and quit the file.

```bash
* * * * * echo "Hello world!" > /dev/pts/0
```
Now, enter the command "crontab -l" and it will display the following output:

```bash
* * * * * echo "Hello world!" > /dev/pts/0
```
```bash
vagrant@ubuntu2204:~$ Hello world!
Hello world!
Hello world!
...
```


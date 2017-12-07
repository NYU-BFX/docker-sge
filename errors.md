# Docker
keep getting errors when trying to build the image with `docker build -t stevekm/docker-sge .`

```

Processing triggers for libc-bin (2.19-0ubuntu6.13) ...
Processing triggers for initramfs-tools (0.103ubuntu4.10) ...
Processing triggers for ca-certificates (20170717~14.04.1) ...
Updating certificates in /etc/ssl/certs... 46 added, 62 removed; done.
Running hooks in /etc/ca-certificates/update.d....done.
Errors were encountered while processing:
 sudo
E: Sub-process /usr/bin/dpkg returned an error code (1)
The command '/bin/sh -c apt-get upgrade -y' returned a non-zero code: 100

```

# SGE Container

```
sgeadmin@2c2eac15dd6d:~$ echo "echo Running test from $HOSTNAME" | qsub
Unable to run job: warning: sgeadmin's job is not allowed to run in any queue
Your job 2 ("STDIN") has been submitted
Exiting.
```

Check the available users

```
sgeadmin@2c2eac15dd6d:~$ cut -d: -f1 /etc/passwd
root
daemon
bin
sys
sync
games
man
lp
mail
news
uucp
proxy
www-data
backup
list
irc
gnats
nobody
libuuid
syslog
sshd
messagebus
postfix
munge
colord
hdfs
mapred
sgeadmin
```

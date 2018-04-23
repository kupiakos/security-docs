---
title: Gathering Info on Linux
category: linux
layout: post
---

Here are the commands I use to gather general information on Linux:

System information
```
$ (uname -a && cat /etc/issue && date && who)
```

Show network info
```
$ route -n
$ cat /etc/resolv.conf
$ netstat -panut
```

Get a list of all services and their PIDs
```
$ (service --status-all 2>&1 | grep + | cut -c9-; initctl list | grep 'start/' | cut -d' ' -f1,4 | tr ' ' /) | sort | uniq
```

Show scheduled jobs
```
$ (for i in /etc/crontab /etc/cron*/* /var/spool/cron/at*/*; do echo $i; cat $i; done)
```

Show running processes
```
$ ps uxeaf
```

List installed kernel modules
```
$ lsmod
```

List environment variables
```
env
```

List block devices
```
lsblk -f
```

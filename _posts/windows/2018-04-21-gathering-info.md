---
title: Gathering info on Windows
category: windows
layout: post
---

Here are the commands I use to gather general information on Windows:
```
net start - list services
netstat -ano - lists open network connections
tasklist /svc - shows the list of running services and their applications
ver - version info
ipconfig /all - network info
date /t && time /t - current date & time
at && schtacks - both AT and Schtasks scheduled tasks
route print - print active routes
psloggedon - display who's logged on, even on XP
openfiles - display currently open files
for /f "skip=4 tokens=2" %i in ('tasklist') do procdump %i.0 - dump all process memory
```
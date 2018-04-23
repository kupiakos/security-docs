---
title: Leave No Trace
category: generic
tags: forensics
layout: post
---

When performing computer forensics, it is important to leave as little of a trace as physically possible.
It may also be important to trust as little as possible.
In the case of live forensics, this means minimaly affecting the volatile components of the running system.
For example, one should almost always avoid installing drivers or writing to disk if possible.
For offline forensics, taking a disk image should use a write blocker.

## Don't trust the target
Overall, the live target could be doing nasty things to prevent analysis.
It could have a 
Worst, it could have a kernel rootkit installed.
It's considered best practice to get tools that you trust onto the system.
This can even include built-in tools, as they may be compromised.

Compiling a toolset can be done a few ways:
 - Download an existing toolset
 - Extracting tools from a trusted system
 - Compiling the tools yourself with static builds enabled
 - Using a tool such as [`static-get`](https://github.com/minos-org/minos-static)

There's a few problems with extracting from a trusted system.
Many tools depend on libraries (DLL, .so) on the system, and those are just as likely to be compromised.
Using statically-built tools or copying libraries and setting `LD_LIBRARY_PATH` for Linux systems may work.
Of course, this doesn't get around a rootkit affecting the kernel itself.

Lastly, _always take checksums_!

## Third-Party Tools
Sometimes what's built-in is not always what's best!
See the [Useful Tools]({% post_url generic/2018-04-20-useful-tools %}) document for more.

## Getting your tools onto the system
Generally speaking, one should avoid installing drivers, add filesystems, etc.
So, this is generally the order you should prefer to get items on your system.

1. CD-ROM
2. Floppy Disk (good luck finding tools fitting on 1.44M)
3. Memory Card (with built-in reader, SD Card, etc.)
4. Network Drive (SMB, NFS, FTP)
5. USB Key

USB Keys will likely require installing drivers, unless it is known that the system has used a key of the same model before.
On Windows systems, holding down the left shift key should disable autoplay if that's a possible effect.

## Building an ISO
Once you've compiled the tools you want.

### Linux

### Windows
Windows loves to make things hard.
If you can't install anything, modifying [this](https://gist.github.com/marnix/3944688) PowerShell script can work, or using the [`New-ISOFile` cmdlet](https://gallery.technet.microsoft.com/scriptcenter/New-ISOFile-function-a8deeffd).
You could a variety of tools, such as [IsoCreator](https://sourceforge.net/projects/iso-creator-cs/).
Using Bash on Ubuntu on Windows allows you to use the same tools as in the Linux section.
